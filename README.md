# 基于c语言实现tcp/ip协议栈

**你将学习到的知识：**

- 自己从零实现tcp/ip网络协议栈的2/3层
- 从零开始构建网络拓扑
- 100%的编码课程，理论很少
- 定时器、GLthreads、库集成、makefile、项目模块化技术
- 编写自定义的CLI命令来配置网络拓扑
- 实现路由和交换算法
- 使用版本控制系统 git 从头开始管理和开发大型源代码



**要求：**

基本的2层和3层路由知识非常重要

擅长C或者任何一种主流语言的编码

知道如何使用git

擅长C语言的指针和内存管理技能



**说明：**

这是一门 100% 基于 C 语言编码的课程，我们将从头开始开发 TCP/IP 堆栈，其中包含数据链路层、网络层和应用程序层。

它是一个大项目，分为6个小项目。

在本课程中，我们将通过 6 个网络项目实现 TCP/IP 网络协议栈演示。所有以下项目应按所列顺序进行。

**项目1：构建路由器和交换机的多节点拓扑仿真**

**项目2：实现数据链路层（2层路由），包括ARP**

**项目3：实现L2层交换（基于MAC地址的学习和转发）**

**项目4：实现基于VLAN的mac学习和转发**

**项目5：实现网络层（L3路由）**

**项目6：案例研究：实现ip隧道（可选）**

在这些迷你项目中，我们将通过 TCP/IP 网络协议栈（= OSI 模型）层来实现数据包的上行和下行。

我们将实现tcp/ip协议栈，在此过程中，我们将讨论和解决在解决问题过程中遇到的新挑战。

完成这些项目后，您将能够：

1、告诉你什么需要数据链路层和网络层

2、如何在TCP/IP协议栈上设计新的应用程序协议（像ICMP，HTTP等）

3、使用工业级的网络编程让你沾沾自喜

4、学习制作、解析、读取数据包缓冲区

5、了解网络应用程序和 TCP/IP 协议栈的端到端架构和设计

6、搞定网络开发工程师的面试

7、装饰你的github，添加一个强大的项目，本课程的预期代码行数将超过10k行！

该项目将填补理论知识与其实现版本之间的空白。你已亲手编写代码解决ARP，数据包转发等问题。用这个项目来装饰你的简历和github。



本课程分为两部分：

**Part A** - 在这部分课程中，我们将构建由路由器、交换机和连接它们的链路组成的网络拓扑基础设施。节点还可以与其邻居节点交换数据包。我们想在这部分课程中模拟一个完全可编程和可配置的网络拓扑。

**Part B** - 课程 A 部分中构建的可配置网络拓扑将用于实现上面列出的剩余五个项目 [2-6]。

我们将建立所有必需的基础设施来模拟网络拓扑——这本身就是一个迷你项目。我们将创建节点、连接节点、在节点上配置网络参数、发送和接收流量——所有这些都在一个项目中。



这个项目最好的是-在此过程中，您将学习许多其他内容，包括设置定时器、网络拓扑构建，Glthreads - 双向链表的粘合方式，使用Makefile构建工程。附加材料已添加到课程的附录部分。我们将采用模块化，每个文件夹中包含实现特定OSI层功能的代码，我们将从头开始做这一切。

**目录**

********

PART A

********

**[ PROJECT 1]**

**第1节. 了解你的课程**              

**第2节. 开发通用图拓扑**

- 图数据结构
- 图相关 APIs
- 创建我们的第一个静态图

**第3节. 构建网络拓扑图**

- 向图中添加网络拓扑详细信息
- 配置网络拓扑的APIs
- Get ready without first Hello World Network Topology               

**第4节. 命令行集成**

- 将CLI接口集成到项目中
- 编写自定义命令以显示网络拓扑详细信息

**第5节. 通讯设置**

-  在出口上向邻居节点发送数据包
- 监听和监控多个套接字
- 在接口上接收数据包



********

   PART B

  ********

**Section 6. Agenda of Part B**

**[ PROJECT 2]**

**第7节. TCP/IP协议栈开发入门**

- 接口模式
- 以太网报文格式
- 以太网报文操作的分配
- 数据包处理标准
- 数据包缓冲区管理

**第8节. Implement Layer 2 (DataLink Layer) - ARP**             

- 开始ARP实现

- ARP报文格式及示例

- 常见ARP表

- 针对ARP表的增删改查的APIs

- 使用ARP的CLI                       

- ARP 周期 and ARP APIs

- 准备和发送ARP广播请求消息

- 处理ARP广播请求消息

- 发送ARP应答消息

- API to Start Ingress Journey of the Frame

- 处理ARP应答消息和 创建ARP项在ARP表

- ARP 实战

  

**[ PROJECT 3]**

**第9节. Implement Layer 2 (数据链路层) - L2 Switching**         

- 将节点配置为 L2 交换机的 API

- 使用 L2 交换机和主机设置新拓扑

- 实现MAC 学习和转发算法

- L2交换机的MAC表管理

- 使用 ARP 测试 L2 交换行为

  

**[ PROJECT 4]**

**第10节. Layer 2 - Implementing Vlan Based Forwarding**

- 目标和先决条件

- 802.1Q Vlan 头格式

- Vlan标记的以太网报文数据结构

- 用于确定标记帧与未标记帧的 API

- 标记 <--> 未标记帧的转换            

- 基于VLAN的MAC转发 - Further Roadmap

- 帧入口条件表

- 帧入口完成

- 帧出口条件表

- 帧出口完成

- 测试基于Vlan的转发

  

**[ PROJECT 5]**

**第11节. Setting Up Layer 3 Routing Infrastructure (Network Layer)**                 

- 目标和先决条件
- L3路由表设置
- 用于路由表管理的 CRUD API
- L3路由安装
- 定义IP头格式
- 添加Ping CLI
- 网络层和应用层交互
- 重新审视L3路由概念
  - Forwarding Case
  - Direct Host Delivery Case
  - Local Delivery Case
  - Self-Ping Case
- L3 Routing Flowcharts

**第12节. 3 层路由流程图实现**          

- 有效负载数据从L2传输到L3
- 3层流程图实现 - Step by Step
- 3层操作流程图实现
- 2层操作流程图实现
- 测试项目的Beta版本

**第13节. 按需解析ARP**

- 问题描述
- 解决方案策略
- Data Structure Enhancements
- ARP Sane Entry Creation
- ARP Pending List Processing
- Final Demo of our Complete Project



**[Project 6]**

**第14节. Implement IP-IN-IP Encapsulation (Tunneling)**

- Implement IP-IN-IP Encapsulation (Tunneling)



**Future Extension of the Project. Students are supposed to take this forward on their own.**

**第15节. Routing between two Vlans (Inter Vlan Routing)**
