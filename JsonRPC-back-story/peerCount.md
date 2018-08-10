# peerCount

接口peerCount语意是获取当前节点连接数。先看接口使用的例子：
- 调用

```
curl -X POST --data '{"jsonrpc":"2.0","method":"peerCount","params":[],"id":74}'
```

- 返回

```
{
    "id": 74,
    "jsonrpc": "2.0",
    "result": "0x3"
}
```

CITA使用全连接的网络结构，不知你是否还记得在启动CITA时，需要生成几个节点的配置文件（如果不记得，请参考[这里](https://docs.nervos.org/cita/#/chain/config_tool)），然后用这些配置文件启动区块链。可以在一个节点的network配置中发现如下信息：

`node/0/network.toml`
```
id_card = 0
port = 4000
[[peers]]
id_card = 1
ip = "127.0.0.1"
port = 4001

[[peers]]
id_card = 2
ip = "127.0.0.1"
port = 4002

[[peers]]
id_card = 3
ip = "127.0.0.1"
port = 4003
```

看到这里，我想你应该已经能猜到调用peerCount接口的时返回的结果是从哪里来的了！！

的确，在CITA中有一个微服务叫NETWORK，负责管理与其它节点的连接关系，当JSONRPC接收到peerCount命令时，会转成CITA内部命令，传递给NETWORK，NETWORK根据当前实际连接数返回给JSONRPC，再由JSONRPC将数据返回给你。就是前面看到的结果了...

一开始使用这个接口时，常常会有一个困惑：

我明明在系统中有4个节点，为什么返回给我的结果是3?!

别忘了，接口是peerCount，还没有包括正在执行JSONRPC命令这个节点，上图可以很好说明这个问题。
