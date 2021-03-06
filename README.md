

# 项目名称：

实时通讯协议中间件（X2Server）

# 项目描述：

工业现场的操作系统需要与各种异构设备通讯，支持不同的协议转换和传输，并通过数据模型来支撑相应业务。

1. 本项目要求开发一个兼容各种通讯协议的中间件，实现数据的收发。通讯协议请从以下设备协议中任选*两种*实现，要求保障通讯的实时性和安全性。

* ModBus

* MTConnect

* 西门子PCL（S1200\S1500\S200\S300\S400）

* OPC UA Client

* ROS

* 欧姆龙PLC

2. 建立数据模型，并将采集到的实时数据存入任意开源数据库中，例如Influxdb、Mysql、Mongodb等。数据模型是对数据的抽象，数据建模会定义该数据的类型、名称、含义、来源以及数据与数据之间的关系，形成一个关联的树状/网状结构。数据模型不仅仅是为了规范数据传输，也是为了在实际生产应用中更好的利用数据。

# 所属赛道

2021全国大学生操作系统比赛的“OS功能设计”赛道

# 参赛要求

* 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生（2021年春季学期或之后本科毕业的大一~大四的学生）
* 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
* 请遵循“2021全国大学生操作系统比赛”的章程和技术方案要求

# 项目导师

付鑫

* email fuxin@jihualab.com

# 难度

中等

# 特征

* 对操作系统网络通讯协议栈有一定理解

* 对不同硬件设备有一定理解

* 了解数据模型，能实现基本的数据建模或者信息模型

# 文档

[西门子PLC](https://new.siemens.com/cn/zh/products/automation/topic-areas/sce/learning-training-documents/basics-of-plc-programming.html)
[ROS](https://www.ros.org/)
[OPC统一架构信息模型](https://opcfoundation.cn/developer-tools/specifications-opc-ua-information-models)

# License

GPL-v3

# 预期目标

1. 拥有一个简单的页面，可以是桌面应用、WEB应用或命令行界面，界面部分的编程不限制语言。

2. 在界面上填写协议名称，设备描述等配置信息后，可以订阅工业设备上的数据测点或者数据节点，建议基于C++或C#来实现协议的解析。
* PLC等设备，可以不用实现所有型号。
* ROS设备和OPC UA Client设备都拥有两种通讯模式，即同步的、实时的订阅/发布模式，以及异步的请求/响应模式。
* 接收到数据后，可以在界面中修改某一测点/节点，修改的值会传递到设备端，也会存储到数据库中

3. 将解析得到的数据实时地存入数据库中，可以使用Websocket、HTTP或者数据库自带的存储方法。若有建立数据模型，则需要将数据模型也保存在数据库中。