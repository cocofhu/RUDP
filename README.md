# RUDP
## a reliable UDP protocol

### 基本原理:
#### 1 首先客户机向服务请求建立连接,发送自己监听的端口号给服务器
#### 2 服务器接收到客户端的消息后,生成一个随机而且不重复的CID(UUID or GUID)给客户端 等待客户端的回复(等待一定时间取消此次连接)
#### 3 客户端收到服务器的消息后将CID保存,以后将用此CID与服务端通信 此时连接建立完成 

#### ---------------------------------------------------
#### note: 如果第一步的包丢失,客户机在一定时间后重新发送连接请求(16次),
