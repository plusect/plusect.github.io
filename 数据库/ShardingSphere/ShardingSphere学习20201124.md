# ShardingProxy

## Netty

### EventLoopGroup
支持NIO和Epoll两种，通过org.apache.shardingsphere.shardingproxy.frontend.bootstrap.ShardingProxy#createEventLoopGroup的Epoll.isAvailable()判断
#### NioEventLoopGroup
不支持netty-transport-native-epoll的平台
#### EpollEventLoopGroup
支持netty-transport-native-epoll的平台
* Linux (since 4.0.16)
* MacOS/BSD (since 4.1.11)

### Channel
#### NioServerSocketChannel
NioEventLoopGroup下的Channel为NioServerSocketChannel
#### EpollServerSocketChannel
EpollEventLoopGroup下的Channel为EpollServerSocketChannel，为ET模式  
Epoll分为LT和ET模式，ET比LT效率高

### Handler
#### ServerHandlerInitializer
该类负责向ChannelPipeline添加Proxy自定义的Handler，实现了支持DB协议。  
根据schema.xml里的DatabaseType创建对应的DatabaseProtocolFrontendEngine，自定义了Handler的编码/解码器用于支持DB的Packet编、解码，自定义了Handler的InboundHandler用于后续整个Proxy处理流程。