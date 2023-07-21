# pcdn

## 技术点
 - stun 打洞/网络NAT类型
 - kcp udp可靠传输
 - udp server 信令转发(防止网络变化导致重连问题)
 - httpclient 获取源站数据(目前要求content-length必须可以获取到数据长度)
 - cityhash url->hashid

## 服务器

- udpsrv服务器
  1. 存储peerid信息
  2. 返回peerlist
  3. 转发peer之间的消息
     
- sdk
  1. 穿透打洞
  2. 从对端peer获取数据包
  3. 本地http服务，组数据包返回客户端
  4. 从edge获取数据包
     
- stun服务器
  1. 辅助NAT穿透
  2. 辅助获取NAT类型
 
- edge服务器
  1. 接收sdk获取数据包请求，返回数据包
  2. httpclient获取源站数据

 - 辅助穿透服务器
   1. 辅助预测端口
  

