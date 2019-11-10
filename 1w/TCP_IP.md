## TCP/IP协议 ##

TCP/IP协议族是一个四层协议系统，自底而上分别是数据链路层，网络层，传输层和应用层。


- **RFC**(Request For Comments) ： 评论请求
- **ARP**协议(Address Resolve Protocol) ： 地址解析协议
- **RARP**协议(Reverse Address Resolve Protocol) ： 逆地址解析协议
- **WAN**(Wide Area Network) ： 广域网
- **LAN**(Local Area Network) ： 局域网
- **IP**协议(Internet Protocol) ： 因特网协议
- **ICMP**协议(Internet Control Message Protocol) ： 因特网控制报文协议
- **UDP**协议(User Datagram Protocol) ： 用户数据报协议
- **SCTP**协议(Stream Control Transmission Protocol) ： 流控制传输协议
- **DNS**(Domain Name Service) ： 域名服务
- **OSPF**(Open Shorttest Path First) ： 开放最短路径优先
- **TCP**协议(Transmission Control Protocol) ： 传输控制协议
- **NIS**(Network Information Service) ： 网络信息服务
- **BGP**(Border Gateway Protocol) ： 边际网关协议
- **RIP**(Routing Information Protocol) ： 路由信息协议

### TCP 协议 ###

- TCP 头部信息。 TCP头部信息出现在每个TCP报文段中，用于指定通信的源端端口号，目的端口号，管理TCP链接，控制两个方向的数据流。
- TCP 状态转义过程。 TCP连接的任意一端都是一个状态机。在TCP连接建立到断开的整个过程中，连接两端的状态机将经历不同的状态变迁。理解TCP 状态转移对于调试网络应用程序将有很大的帮助。
- TCP 数据流。 通过分析 TCP 数据流，我们就可以从网络应用程序外部来了解应用层协议和通信双方交换的应用程序数据。这一部分将讨论两种类型的TCP数据流： 交互数据流和块数据流。TCP 数据流中有一种特殊的数据，称为紧急数据。
- TCP数据流的控制。 为了保证可靠传输和提高网络通信质量，内核需要对TCP数据流进行控制。这一部分讨论TCP数据流控制的两个方面： 超时重传和拥塞控制。

#### Nagle算法 ####

Nagle算法要求一个TCP连接的通信双方在任意时刻都最多只能发送一个未被确认的TCP报文段，在该TCP报文段的确认到达之前不能发送其他TCP报文段。另一方面，发送方在等待确认的同时收集本端需要发送的微量数据，并在确认到来时以一个TCP报文段将它们全部发送出去，这样就极大的减少了在网络上的微小TCP报文段的数量。该算法的另一个优点在于其自适应性：确认到达的越快，数据也就发送得越快。










 





