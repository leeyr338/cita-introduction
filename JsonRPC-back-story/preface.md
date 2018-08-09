# 前言

JsonRPC接口是CITA区块链网络与用户交互的唯一接口；将CITA看作一个黑盒，理解了JsonRPC的所有接口，就可以对CITA提供的能力理解个大概。JsonRPC功能和用法的描述，在CITA的[帮助文档](https://docs.nervos.org/cita/#/rpc_guide/rpc)里有比较详细的描述。这里的小文章，并不打算再重复帮助文档里的内容，而是想把CITA这个黑盒稍微打开一下，让你看到在这些JsonRPC命令背后，CITA这个系统为你做了什么事。
首先，在CITA系统里，的确存在JsonRPC这个微服务，专门负责：

![image1](https://github.com/leeyr338/cita-introduction/blob/master/JsonRPC-back-story/imgs/1.png?raw=true)

1. 处理用户输入的JsonRPC命令，然后将这些命令转化成CITA系统可认识的消息，然后转发给相应的微服务；

2. 接收到相应微服务回复结果后，将CITA系统内的数据转化成JsonRPC数据格式，返回给用户。

其次，再解释一下这里的“用户”,其实在大家与CITA交互时，很少直接使用CITA提供的JsonRPC接口，所以这里所讲的CITA“用户”,准确来说应用是CITA的各个SDK或工具 (如web3.j, web3.js, cita-cli，Remix, truffle等)。

![image2](https://github.com/leeyr338/cita-introduction/blob/master/JsonRPC-back-story/imgs/2.png?raw=true)

所以最后，你与CITA系统的关系图会是：

![image3](https://github.com/leeyr338/cita-introduction/blob/master/JsonRPC-back-story/imgs/3.png?raw=true)
