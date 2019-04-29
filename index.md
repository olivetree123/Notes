

## 随笔
### Golang
1. [HTTP参数解析](./Notes/Golang/HTTP参数解析.md)
2. [类型转换](./Notes/Golang/类型转换.md)
3. [理解mutex](./Notes/Golang/理解mutex.md)
4. [Slice & Array](./Notes/Golang/SliceArray.md)

### Python

### Other
1. [字符编码](./Notes/Other/字符编码.md)

## Protocol
1. 概述
2. 物理层
物理层负责传输0/1电信号，没有协议。
3. 链路层  
物理层传输的0/1电信号应该如何解读？多少个电信号算一组？每个信号为有什么意义？
链路层就是解决这些问题的，它确定了0/1电信号的分组方式，以及每个信号位的意义。   
3.1 [Ethernet(以太网) 协议](./Protocol/以太网协议.md)  
4. 网络层  
4.1 IP 协议  
4.2 ARP 协议  
5. 传输层  
5.1 TCP 协议  
5.2 UDP 协议  
6. 应用层  
6.1 HTTP 协议  
6.2 DNS 协议  
6.3 SOCKS5 协议  

> 参考：[互联网协议入门](http://www.ruanyifeng.com/blog/2012/05/internet_protocol_suite_part_i.html)

### A & Q
1. [Gunicorn 一直重启](./Notes/Questions/Gunicorn一直重启.md)


## 产品手记
#### [官网首页](./ProductNotes/notes/官网首页.md)  
#### [注册和登陆](./ProductNotes/notes/注册和登陆.md)  
#### 导航菜单  
- [横版菜单](./ProductNotes/notes/导航菜单-横版.md)  
- [竖版菜单](./ProductNotes/notes/导航菜单-竖版.md)  

#### 详情页  
- [商品详情页](./ProductNotes/notes/详情页之商品.md)  
- [文章详情页](./ProductNotes/notes/详情页之文章.md)  
- [APP详情页](./ProductNotes/notes/详情页之APP.md)  

#### [翻页导航](./ProductNotes/notes/翻页导航.md)  