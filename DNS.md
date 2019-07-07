# DNS
域名系统（DNS）是一种用于TCP/IP应用程序的分布式数据库，它提供主机名字和IP地址之间的转换及有关电子邮件的选路信息
## DNS基础
![DNS层次组织](http://docs.52im.net/extend/docs/book/tcpip/vol1/14/images2/52im_net_1.png)  
一个独立管理的DNS子树称为一个区域(zone)。一个常见的区域是一个二级域，如noao.edu。许多二级域将它们的区域划分成更小的区域  
## DNS报文格式
![DNS报文格式](http://docs.52im.net/extend/docs/book/tcpip/vol1/14/images2/52im_net_3.png) 
## 反向查询
正向查询指的是通过域名得到 IP 的查询,而反向查询就是通过 IP 得到域名。例如用 host 命令,host ip 就可以得到服务器的域名, host domainName 就得到 IP。  
稍微知道一点数据结构的人都能意识到,在正向查询的域里面做反向查询,其做法只有遍历整个数据集合----对于 DNS 来说,那 就是遍历整个数据库, 这将带来巨大的负担,所以 DNS 采取了另一种方法,使用另一棵子树来维护 IP-〉域名的对应表。这个子树的根节点是 in-addr.arpa,而一个 IP 例如192.168.11.2)所具有的 DNS 地址就是 2.11.168.192.in-addr.arpa(ip 倒置)。在 DNS 系统里面,一个 反向地址对应一个 PTR 纪录(对应 A 纪录),所以反向查询又叫 做指针(PTR)查询。

