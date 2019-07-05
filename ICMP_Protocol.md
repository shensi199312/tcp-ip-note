# ICMP协议
ICMP经常被认为是IP层的一个组成部分。它传递差错报文以及其他需要注意的信息。ICMP报文通常被IP层或更高层协议（TCP或UDP）使用。一些ICMP报文把差错报文返回给用户进程
## ICMP协议格式
![ICMP报文格式](http://docs.52im.net/extend/docs/book/tcpip/vol1/6/images2/52im_net_1.png)  
ICMP报文是在IP数据报内部被传输的  
## ICMP差错报文的类型
![ICMP报文类型](http://docs.52im.net/extend/docs/book/tcpip/vol1/6/images2/52im_net_3.png)  
下面各种情况都不会导致产生ICMP差错报文(避免广播风暴):  
(1)ICMP差错报文  
(2)目的地址是广播地址或多播地址的IP数据报。  
(3)作为链路层广播的数据报。  
(4)不是IP分片的第一片  
(5)源地址不是单个主机的数据报。这就是说，源地址不能为零地址、环回地址、广播地址或多播地址。  
## ICMP时间戳请求与应答
ICMP时间戳请求允许系统向另一个系统查询当前的时间。返回的建议值是自午夜开始计算的毫秒数，协调的统一时间（Coordinated Universal Time,UTC）
## ICMP端口不可达差错
