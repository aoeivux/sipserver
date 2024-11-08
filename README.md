# SipServer

## 介绍
1. 一个基于C++开发的国标GB28181流媒体信令服务器。
2. 采用SipServer+ZLMediaKit。可以搭建一个接收摄像头国标协议推流的国标流媒体服务，然后实现RTSP/RTMP/HTTP-FVL/HLS/WS/SRT等协议分发视频流。
3. SipServer负责信令模块，ZLMediaKit负责流媒体模块。
4. SipServer作为国标流媒体服务器的信令模块。用于接收摄像头的信令注册，注册完成后，
  主动向摄像头发送Invite请求，摄像头收到Invite请求后， 返回Invite的确认。 服务端收到确认后，发送ACK请求，
  摄像头收到ACK请求后，开始通过RTP传输ps流推流至ZLMediaKit的国标RTP Server。 ZLMediaKit作为国标流媒体服务器的流媒体模块，主要用于接收摄像头国标推流和其他协议的分发。

### linxu系统编译运行
1. 常见报错 error while loading shared libraries: libXXX.so.X: cannot open shared object file: No such file [解决方法](https://blog.csdn.net/deeplan_1994/article/details/83927832)





