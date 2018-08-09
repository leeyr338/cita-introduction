# cita-introduction

## 前言
#### 帮助世界，世界帮你
 CITA是[秘猿科技](https://www.cryptape.com/#/)的作品。大家都知道，这些年在区块链领域不乏浮燥之气，见面聊区块链时，总想着一夜暴富，也确实有些人通过它致富了。但能在这样一个浮燥的环境下，能抵住诱惑，坚持走“技术为王”的路线，扛起”建立信任”的使命，持续思考，为社区、世界贡献自己的力量，实属不易。更为难得的是，秘猿一直手握利剑（非常强的技术实力），没有用来割xx，而是用来扛未来（建立信任）。

 “知易行难、行之惟艰”，喊口号都很容易，但要真正做到“知行合一”就很难了，更何况还要坚持。秘猿一直行开源开放之路，[CITA](https://github.com/cryptape/cita)就是一个证明。

 帮助世界，世界帮你；秘猿虽然选择了一路不一样的路，走一条Hard的路，但是它心怀世界，世界也会帮助它，从最近的融资情况就可见一斑。

#### 帮助别人，别人帮人
刚进公司时，我一直想要一份CITA的说明书，能够让我由浅入深地了解CITA，但是没有找到。于是就与我老板对话：

```
我：我想找一份由浅入深介绍CITA的材料，同时能指导我看懂code；

老板：还没有这样一份系统的材料；

我：那我写一份吧；

老板：好。
```
当时我只想要是有这样一份材料，应该可以帮助其它想了解CITA的朋友缩短他们理解CITA的时间；同时写这样一份材料也让我能更好的理解CITA，而我也是一直觉得我比较擅长将一个复杂的系统用形象化的语言表达出来。但我没有想到，这个工作比我想象要难得多。

其一，区块链平台本身就有一定的复杂度；

其二，CITA将系统模块折成了微服务，大量异步操作增加了系统的理解难度；

其三，Rust对我而言是一门陌生的语言，要看懂CITA也需要我先补不少课。

所以直到今天才开始履行我的这个小使命，但在理解过程中得到了很多公司的小伙伴帮助，非常感谢他们。

## 目录

###### CITA模块介绍
 - JsonRPC
 - Auth
 - Executor
 - bft
 - chain
 - network
 - forever


###### CITA源码分析
 - 源码目录介绍
 - Jsonrpc
 - Auth
 - Executor
 - bft
 - chain
 - network
 - forever

###### JsonRPC命令背后的故事
 - [前言](JsonRPC-back-story/preface.md)
 - peerCount
 - blockNumber
 - sendRawTransaction
 - getBlockByHash
 - getBlockByNumber
 - getTransactionReceipt
 - getLogs
 - call
 - getTransaction
 - getTransactionCount
 - getCode
 - getAbi
 - getBalance
 - newFilter
 - newBlockFilter
 - uninstallFilter
 - getFilterChanges
 - getFilterLogs
 - getTransactionProof
 - getMetaData

###### CITA 2.0设计考虑
 - 设计场景
 - 扩展性
 - 可靠性
 - 部署
 - 开发
 - 运维

## 联系我
Email : leeyr@cryptape.com

WeChat: liyaorong3401
