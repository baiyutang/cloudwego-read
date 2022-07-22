# CloudWeGo 源码解读

[CloudWeGo](https://github.com/cloudwego) 是字节跳动基础架构团队开源出来的项目，它是一套可快速构建企业级云原生架构的中间件集合，它专注于微服务通信与治理，具备高性能、可扩展、高可靠的特点，且关注易用性。

主要项目：
- Kitex：高性能、强可扩展的 Golang RPC 框架
- Netpoll：高性能、I/O 非阻塞、专注于 RPC 场景的网络框架
- Thriftgo：Golang 实现的 Thrift 编译器，支持插件机制和语义检查
- Netpoll-http2：基于 Netpoll 的 HTTP/2 实现
- Hertz：[həːts] Golang 微服务 HTTP 框架

## Kitex

### 学习资料
- [【仓库】github/cloudwego/kitex](https://github.com/cloudwego/kitex)
- [【官网】cloudwego.io/kitex](https://www.cloudwego.io/zh/docs/kitex/)
- [【文章】字节跳动微服务架构体系演进](https://mp.weixin.qq.com/s/1dgCQXpeufgMTMq_32YKuQ)
- [【掘金小册】Go 组件设计与实现](https://juejin.cn/video/7046282096435789835)
- [【文件】字节杨芮：微服务框架 Kitex 的设计、实践及开源](https://github.com/baiyutang/cloudwego-read/files/9157661/Kitex.pdf)
- [【视频】Go 微服务框架 Kitex 扩展性设计和实践 | JTalk Meetup 11期](https://www.bilibili.com/video/BV1qa4y1H7i2)
- [【PDF集合】CloudWeGo 社区对外 Meetup](https://github.com/cloudwego/community/tree/main/meetup)

### 整体性设计
- [从 CloudWeGo 谈云原生时代的微服务与开源](https://mp.weixin.qq.com/s/xWxb84WkYtWTBoVV3mzs6g)
- Kitex 模块划分及调用链路
- [Kitex 扩展性设计思路](https://xie.infoq.cn/article/50c36c2a3daa25a68da3d7a89)

### 服务治理
- [服务注册](https://xie.infoq.cn/article/3b71488fc9b07f89f8950f8df) / 服务发现
- 熔断
- [限流](https://xie.infoq.cn/article/408cd95d469ee2cdc72c1cd10)
- 请求重试
- 负载均衡

### 公共模块
- rpcinfo
- endpoint
- middleware
- 元信息

### remote

remote 模块是 Kitex 实现的 RPC 核心，是与远端交互的重要模块。

- transport pipeline
- trans handler
- codec
- payloadCodec


## Hertz

### 学习资料
- [github/cloudwego/hertz](https://github.com/cloudwego/hertz)
- [cloudwego.io/hertz](https://www.cloudwego.io/zh/docs/hertz/)
- [[CSG第二期]分享01. 从精通烤肉到精通http](https://meetings.feishu.cn/s/1i38ftnck0f18?src_type=3)
- [[CSG第二期]分享02. 如何利用命令行工具HZ快速开发Hertz服务](https://meetings.feishu.cn/s/1i3fsqit6jchu?src_type=3)
