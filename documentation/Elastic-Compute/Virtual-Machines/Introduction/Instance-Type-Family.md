# 实例规格类型

实例是京东智联云为您业务提供计算服务的最小单位，不同实例通过其规格类型及具体规格来标识相应的计算、内存、存储及网络能力。同时，您创建实例时指定的实例类型决定了实例的硬件配置，您可基于需要部署运行的应用类型及规模选择适当的实例规格类型及具体规格。

以下为当前京东智联云在售的实例规格类型信息，不同地域可售卖实例类型及规格不完全相同，请以实例创建页面所显示为准。具体在售实例规格类型根据不同应用场景可以分为：

* 通用型：[通用共享型](instance-type-family#user-content-1)、[通用标准型](instance-type-family#user-content-2)
* 计算优化型：[计算优化共享型](instance-type-family#user-content-9)、[计算优化密集型](instance-type-family#user-content-11)、[计算优化标准型](instance-type-family#user-content-3)
* 内存优化型：[内存优化标准型](instance-type-family#user-content-4)
* 高频计算型：[高频计算通用型](instance-type-family#user-content-5)
* 存储优化型：[存储优化IO型](instance-type-family#user-content-7)、[存储优化大数据型](instance-type-family#user-content-8)、
* GPU型：[GPU标准型](instance-type-family#user-content-6)、[GPU虚拟化型](instance-type-family#user-content-10)

## 通用型
通用型当前提供通用共享型及通用标准型，为您提供均衡的计算及内存资源，可满足大部分业务场景下的需求。其中通用标准型中每一个vCPU都对应一个Intel Xeon处理器的超线程核，其vCPU与内存比为1:4。

### 通用共享型
<div id="user-content-1"></div>
通用共享型实例采用非绑定CPU调度模式，每个vCPU会被分配到任何空闲的超线程核上，不同实例的vCPU可以互相争抢物理CPU资源。通用共享型实例拥有高性价比的优点，但由于需要对资源进行争抢，在性能上可能会受到不同程度的影响。


**规格类型特点：**

* vCPU与内存比为1:1、1:2或1:4，提供多种处理器内存配比。
* 处理器： 
	* 第二代：2.4 GHz主频的Intel Xeon Gold 6148（Skylake）处理器
	* 第一代：2.1 GHz主频的Intel Xeon E5-2683 v4（Broadwell）处理器
* 支持以下类型云硬盘：
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* 访问量较小的个人网站初级阶段
	* 微服务
	* 测试环境

**实例规格**

第二代

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|g.s2.micro|1|1|1
|g.s2.small|1|2|1
|g.s2.medium|1|4|1
|g.s2.large|2|8|2
|g.s2.xlarge|4|16|4
|g.s2.2xlarge|8|32|4

第一代

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|g.s1.micro|1|1|1
|g.s1.small|1|2|1

### 通用标准型
<div id="user-content-2"></div>

**规格类型特点:**

* vCPU与内存比为1:4（g.n1.xlarge_m规格除外）
* 处理器：
	* 第三代：2.6 GHz主频的Intel Xeon Gold 6267（Cascade Lake）处理器  
	* 第二代：2.4 GHz主频的Intel Xeon Gold 6148（Skylake）处理器 或 2.6 GHz主频的Intel Xeon Gold 6267（Cascade Lake）处理器  
	* 第一代：2.1 GHz主频的Intel Xeon E5-2683 v4（Broadwell）处理器
* 支持以下类型云硬盘：
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* 各种类型和规模的企业级应用
	* 中小型数据系统、缓存、搜索集群
	* 数据分析和计算
	* 计算集群、依赖内存的数据处理

**实例规格**

第三代

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|g.n3.medium|1|4|1
|g.n3.large|2|8|2
|g.n3.xlarge|4|16|4
|g.n3.2xlarge|8|32|4
|g.n3.3xlarge|12|48|4
|g.n3.4xlarge|16|64|4
|g.n3.6xlarge|24|96|4
|g.n3.8xlarge|32|128|4
|g.n3.12xlarge|48|192|4
|g.n3.16xlarge|64|256|4
|g.n3.18xlarge|72|288|4

第二代

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|g.n2.medium|1|4|1
|g.n2.large|2|8|2
|g.n2.xlarge|4|16|4
|g.n2.2xlarge|8|32|4
|g.n2.4xlarge|16|64|4
|g.n2.8xlarge|32|128|4
|g.n2.16xlarge|64|256|4
|g.n2.18xlarge|72|288|4
|g.n2.metal|80|384|60

**关于裸金属云主机g.n2.metal更详细说明请查阅[裸金属云主机概述](../Operation-Guide/Instance/Bare-Metal/Bare-Metal-Overview.md)**

第一代

实例规格|vCPU（核）|内存（GB）|网卡多队列|备注
:---|:---|:---|:---|:---
g.n1.medium|1|4|1 | |
g.n1.large|2|8|2 | |
g.n1.xlarge_m	|4|12|4|*
g.n1.xlarge|4|16|4 | |	
g.n1.2xlarge|8|32|4 | |	
g.n1.4xlarge|16|64|4 |	|
g.n1.8xlarge|32|128|4 |	 |

标*表示不支持以该规格新建云主机，且不支持您将当前云主机调整至该规格，但不影响您现有该规格云主机的使用。

## 计算优化型
计算优化型当前提供计算优化共享型及计算优化标准型，其中计算优化标准型可满足每一个vCPU都对应一个Intel Xeon处理器的超线程核，为您提供高性能的计算资源。
### 计算优化共享型
<div id="user-content-9"></div>
计算优化共享型实例采用非绑定CPU调度模式，每个vCPU会被分配到任何空闲的超线程核上，不同实例的可以vCPU互相争抢物理CPU资源。计算优化共享型实例拥有高性价比的优点，但由于需要对资源进行争抢，在性能上可能会受到不同程度的影响。

**规格类型特点：**

* vCPU与内存比约为1:2
* 处理器：2.4 GHz主频的Intel Xeon Gold 6148 （Skylake）处理器
* 支持以下类型云硬盘：
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* 小规模机器学习、数据分析
	* 小规模爬虫
	* 小规模批量计算

**实例规格**

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|c.s2.large|2|4|2
|c.s2.xlarge|4|8|4
|c.s2.2xlarge|8|16|4

### 计算优化密集型
<div id="user-content-11"></div>

**规格类型特点：**

* vCPU与内存比约为1:1
* 处理器：
	* 第三代：2.6 GHz主频的Intel Xeon Gold 6267（Cascade Lake）处理器
	* 第二代：2.4 GHz主频的Intel Xeon Gold 6148 （Skylake）处理器 或 2.6 GHz主频的Intel Xeon Gold 6267（Cascade Lake）处理器  
	* 第一代：2.1 GHz主频的Intel Xeon E5-2683 v4（Broadwell）处理器
* 支持以下类型云硬盘：
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* 批处理工作负载
	* Web前端服务器
	* 大型多人在线游戏（MMO）前端
	* 数据分析、批量计算、视频编码
	* 高性能科学和工程应用

**实例规格**

第二代

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|c.c2.large|2|2|2
|c.c2.xlarge|4|4|4
|c.c2.2xlarge|8|8|4
|c.c2.3xlarge|12|12|4
|c.c2.4xlarge|16|16|4

### 计算优化标准型
<div id="user-content-3"></div>

**规格类型特点：**

* vCPU与内存比约为1:2
* 处理器：
	* 第三代：2.6 GHz主频的Intel Xeon Gold 6267（Cascade Lake）处理器
	* 第二代：2.4 GHz主频的Intel Xeon Gold 6148 （Skylake）处理器 或 2.6 GHz主频的Intel Xeon Gold 6267（Cascade Lake）处理器  
	* 第一代：2.1 GHz主频的Intel Xeon E5-2683 v4（Broadwell）处理器
* 支持以下类型云硬盘：
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* 批处理工作负载
	* Web前端服务器
	* 大型多人在线游戏（MMO）前端
	* 数据分析、批量计算、视频编码
	* 高性能科学和工程应用

**实例规格**

第三代

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|c.n3.large|2|4|2
|c.n3.xlarge|4|8|4
|c.n3.2xlarge|8|16|4
|c.n3.3xlarge|12|24|4
|c.n3.4xlarge|16|32|4
|c.n3.6xlarge|24|48|4
|c.n3.8xlarge|32|64|4
|c.n3.12xlarge|48|96|4
|c.n3.16xlarge|64|128|4
|c.n3.22xlarge|88|176|4

第二代

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|c.n2.large|2|4|2
|c.n2.xlarge|4|8|4
|c.n2.2xlarge|8|16|4
|c.n2.4xlarge|16|32|4
|c.n2.8xlarge|32|64|4
|c.n2.16xlarge|64|128|4
|c.n2.18xlarge	|72|144|4

第一代

实例规格|vCPU（核）|内存（GB）|网卡多队列|备注
:---|:---|:---|:---|:---
|c.n1.large|2|4|2 | |	
|c.n1.xlarge_m	|4|4|4|	*
|c.n1.xlarge|4|8|	4| |
|c.n1.2xlarge_s|8|8|4|*
|c.n1.2xlarge_m|8|12|4|*
|c.n1.2xlarge|8|16|4 |	|
|c.n1.4xlarge_m|16|16|4|*
|c.n1.4xlarge|16|32|4 |	|
|c.n1.8xlarge|32|64|4 | |

标*表示不支持以该规格新建云主机，且不支持您将当前云主机调整至该规格，但不影响您现有该规格云主机的使用。

## 内存优化型
内存优化型当前提供内存优化标准型，适用于存在大量内存操作、查找和计算的应用。每一个vCPU都对应一个Intel Xeon处理器的超线程核。

<div id="user-content-4"></div>

### 内存优化标准型

**规格类型特点：**

* vCPU与内存比约为1:8
* 处理器：
	* 第三代：2.6 GHz主频的Intel Xeon Gold 6267（Cascade Lake）处理器 
	* 第二代：2.4 GHz主频的Intel Xeon Gold 6148 （Skylake）处理器  或 2.6 GHz主频的Intel Xeon Gold 6267（Cascade Lake）处理器  
	* 第一代：2.1 GHz主频的Intel Xeon E5-2683 v4（Broadwell）处理器
* 支持以下类型云硬盘：
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* 高性能数据库、内存数据库
	* 数据分析与挖掘、分布式内存缓存
	* Hadoop、Spark群集以及其他企业大内存需求应用

**实例规格**

第三代

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|m.n3.large|2|16|2
|m.n3.xlarge|4|32|4
|m.n3.2xlarge|8|64|4
|m.n3.3xlarge|12|96|4
|m.n3.4xlarge|16|128|4
|m.n3.6xlarge|24|192|4
|m.n3.8xlarge|32|256|4

第二代

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|m.n2.large|2|16|2
|m.n2.xlarge|4|32|4
|m.n2.2xlarge|8|64|4
|m.n2.4xlarge|16|128|4
|m.n2.8xlarge|32|256|4
|m.n2.16xlarge|64|512|4
|m.n2.18xlarge|72|576|4

第一代

实例规格|vCPU（核）|内存（GB）|网卡多队列|备注
:---|:---|:---|:---	|:---
|m.n1.small| 1 | 8 | 1 | *
|m.n1.medium|2	|12|2|*
|m.n1.large|2|16|2 | |
|m.n1.xlarge|4|32	|4 | |
|m.n1.2xlarge|8|64|4  | |
|m.n1.4xlarge|16|128|4 | |

标*表示不支持以该规格新建云主机，且不支持您将当前云主机调整至该规格，但不影响您现有该规格云主机的使用。

## 高频计算型

高频计算型当前提供高频计算通用型，为您提供高性能的计算资源。每一个vCPU都对应一个Intel Xeon处理器的超线程核。

<div id="user-content-5"></div>

### 高频计算通用型

**规格类型特点：**

* vCPU与内存比为1:4
* 计算性能稳定，处理器主频高
* 处理器：
	* 第二代：3.2 GHz主频的Intel Xeon Gold 6146（Skylake）处理器
	* 第一代：3.2 GHz主频的Intel Xeon E5-2667 v4（Broadwell）处理器
* 支持以下类型云硬盘：
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* 高性能Web前端服务器
	* 高性能科学和工程应用
	* MMO游戏、视频编码

**实例规格**

第二代：

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|h.g2.large|2|8|2
|h.g2.xlarge|4|16|4
|h.g2.2xlarge|8|32|4
|h.g2.4xlarge|16|64|4
|h.g2.8xlarge|32|128|4

第一代：

实例规格|vCPU（核）|内存（GB）|网卡多队列
:---|:---|:---|:---
|h.g1.large|2|8|2
|h.g1.xlarge|4|16|4
|h.g1.2xlarge|8|32|4
|h.g1.4xlarge|16|64|4
|h.g1.6xlarge|24|96|4

## 存储优化型

存储优化型当前提供存储优化IO型及存储优化大数据型，为您提供高性能的本地存储资源。每一个vCPU都对应一个Intel Xeon处理器的超线程核。

<div id="user-content-7"></div>

### 存储优化IO型

**规格类型特点：**

* vCPU与内存比为1:4
* 提供低时延高IO的本地存储
* 处理器：
	* 第三代：2.6 GHz主频的Intel Xeon Gold 6267（Cascade Lake）处理器  
	* 第二代：2.4 GHz主频的Intel Xeon Gold 6148（Skylake）处理器
	* 第一代：2.1 GHz主频的Intel Xeon E5-2683 v4（Broadwell）处理器
* 支持本地数据盘（临时存储），并支持以下类型云硬盘。请注意 **本地数据盘为临时存储盘，有丢失数据的风险（比如发生迁移或宿主机宕机等情况），不适用于应用层没有数据冗余架构的使用场景， 建议您使用云硬盘存储重要数据。** 
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* 高性能关系数据库
	* NoSQL数据库
	* ElasticSearch等场景

**实例规格**


第三代：

实例规格|vCPU（核）|内存（GB）|本地数据盘（临时存储|网卡多队列
:---|:---|:---|:---|:---
|s.i3.2xlarge|8|32|1 x 1862 NVMe SSD|4
|s.i3.4xlarge|16|64|2 x 1862 NVMe SSD|4
|s.i3.6xlarge|24|96|3 x 1862 NVMe SSD|4
|s.i3.8xlarge|32|128|4 x 1862 NVMe SSD|4
|s.i3.12xlarge|48|192|6 x 1862 NVMe SSD|4
|s.i3.16xlarge|64|256|8 x 1862 NVMe SSD|4
|s.i3.22xlarge|88|352|8 x 1862 NVMe SSD|4

第二代：

实例规格|vCPU（核）|内存（GB）|本地数据盘（临时存储|网卡多队列
:---|:---|:---|:---|:---
|s.i2.metal|80|384|1 x 1862 NVMe SSD|60

第一代：

实例规格|vCPU（核）|内存（GB）|本地数据盘（临时存储|网卡多队列
:---|:---|:---|:---|:---
|s.i1.xlarge|4|16|1 x 894GB SSD|4
|s.i1.2xlarge|8|32|2 x 894GB SSD|4
|s.i1.4xlarge|16|64|4 x 894GB SSD|4
|s.i1.8xlarge|32|128|8 x 894GB SSD|4
|s.i1.14xlarge|56|224|14 x 894GB SSD|4

<div id="user-content-8"></div>

### 存储优化大数据型

**规格类型特点：**

* vCPU与内存比约为1:4
* 提供低时延高容量及高吞吐的本地存储
* 处理器：
	* 第二代：2.1 GHz主频的Intel Xeon Silver 4116（Skylake）处理器
	* 第一代：2.2 GHz主频的Intel Xeon E5-2650 v4（Broadwell）处理器
* 支持本地数据盘（临时存储），并支持以下类型云硬盘。请注意 **本地数据盘为临时存储盘，有丢失数据的风险（比如发生迁移或宿主机宕机等情况），不适用于应用层没有数据冗余架构的使用场景， 建议您使用云硬盘存储重要数据。** 
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* Hadoop MapReduce、HDFS、Hive、HBase
	* 其他海量数据存储区及计算的业务场景

**实例规格**

第二代：

实例规格|vCPU（核）|内存（GB）|本地数据盘（临时存储，GB）|网卡多队列
:---|:---|:---|:---|:---
|s.d2.xlarge|4|22|1 x 9313 HDD|4
|s.d2.2xlarge|8|44|2 x 9313 HDD|4
|s.d2.4xlarge|16|88|4 x 9313 HDD|4
|s.d2.8xlarge|32|176|8 x 9313 HDD|4
|s.d2.10xlarge|40|220|12 x 9313 HDD|4

第一代：

实例规格|vCPU（核）|内存（GB）|本地数据盘（临时存储，GB）|网卡多队列
:---|:---|:---|:---|:---
|s.d1.xlarge|4|22|1 x 5587 HDD|4
|s.d1.2xlarge|8|44|2 x 5587 HDD|4
|s.d1.4xlarge|16|88|4 x 5587 HDD|4
|s.d1.8xlarge|32|176|8 x 5587 HDD|4
|s.d1.10xlarge|40|220|12 x 5587 HDD|4

## GPU型

GPU型当前提供GPU标准型和GPU虚拟化型。GPU虚拟化型规格目前在华北部分可用区邀测中，如有购买需求请提交工单。

<div id="user-content-6"></div>

### GPU标准型

**规格类型特点：**

* vCPU与内存比接近1:4
* 异构计算
* GPU：
	* Nvidia Tesla P40 
	* Nvidia Tesla V100
* 处理器：
	* 2.1 GHz主频的Intel Xeon E5-2683 v4（Broadwell）处理器（P40）
	* 2.2 GHz主频的Intel Xeon E5-2650 v4（Broadwell）处理器（V100）
* 支持本地数据盘（临时存储），并支持以下类型云硬盘。请注意 **本地数据盘为临时存储盘，有丢失数据的风险（比如发生迁移或宿主机宕机等情况），不适用于应用层没有数据冗余架构的使用场景， 建议您使用云硬盘存储重要数据。** 
	* 通用型SSD云盘
	* 性能型SSD云盘
	* 容量型HDD云盘
* 适用场景：
	* 科学计算
	* 机器学习
	* 图形渲染 

**实例规格**

第一代：

实例规格|vCPU（核）|内存（GB）|GPU|本地数据盘（临时存储，GB）|网卡多队列
:---|:---|:---|:---|:---|:---|
|p.n1p40.3xlarge|12|48|1 x Nvidia Tesla P40|1 x 894 SSD|4
|p.n1p40.7xlarge|28|110|2 x Nvidia Tesla P40|2 x 894 SSD|4
|p.n1p40.14xlarge|56|220|4 x Nvidia Tesla P40|4 x 894 SSD|4
|p.n1p40h.3xlarge|12|48|1 x Nvidia Tesla P40|1 x 1117 HDD|4
|p.n1p40h.7xlarge|28|110|2 x Nvidia Tesla P40|2 x 1117 HDD|4
|p.n1p40h.14xlarge|56|220|4 x Nvidia Tesla P40|4 x 1117 HDD|4
|p.n1v100.2xlarge|8|44|1 x Nvidia Tesla V100|1 x 5587 HDD|4
|p.n1v100.5xlarge|20|110|2 x Nvidia Tesla V100|2 x 5587 HDD|4
|p.n1v100.10xlarge|40|220|4 x Nvidia Tesla V100|4 x 5587 HDD|4

<div id="user-content-10"></div>

### GPU虚拟化型

**规格类型特点：**

* 异构计算
* GPU类型及规格：
	* 1* 1/6 Nvidia Tesla P40 （显存4GB）
	* 1* 1/4 Nvidia Tesla P40 （显存6GB）
	* 1* 1/2 Nvidia Tesla P40 （显存12GB）
* 处理器：
	* 2.1 GHz主频的Intel Xeon E5-2683 v4（Broadwell）处理器
	* 2.2 GHz主频的Intel Xeon E5-2650 v4（Broadwell）处理器
	* 2.4 GHz主频的Intel Xeon E5-2680 v4（Broadwell）处理器
* 虚拟化类型：
	* C模式
	* Q模式
* 适用场景：
	* 科学计算、机器学习（C模式）
	* 图形渲染、游戏（Q模式） 

**实例规格**

第一代-C模式：

实例规格|vCPU（核）|内存（GB）|GPU|显存（GB）|网卡多队列
:---|:---|:---|:---|:---|:---|
|p.c1p40g.large|2|8|1 x 1/6 Nvidia Tesla P40|4|2
|p.c1p40m.large|2|14|1 x 1/4 Nvidia Tesla P40|6|2
|p.c1p40g.xlarge|4|14|1 x 1/4 Nvidia Tesla P40|6|4
|p.c1p40g.3large|6|28|1 x 1/2 Nvidia Tesla P40|12|4

第一代-Q模式：

实例规格|vCPU（核）|内存（GB）|GPU|显存（GB）|网卡多队列
:---|:---|:---|:---|:---|:---|
|p.q1p40g.large|2|8|1 x 1/6 Nvidia Tesla P40|4|2
|p.q1p40m.large|2|14|1 x 1/4 Nvidia Tesla P40|6|2
|p.q1p40g.xlarge|4|14|1 x 1/4 Nvidia Tesla P40|6|4
|p.q1p40g.3large|6|28|1 x 1/2 Nvidia Tesla P40|12|4


请注意：

* 标 * 规格表示不支持以该规格新建云主机，且不支持您将当前云主机调整至该规格，但不影响您现有该规格云主机的使用；
* 计算优化密集型当前仅在华北-北京、华东-上海地域提供；
* 高频计算型当前仅在华北-北京、华南-广州及华东-上海提供；
* GPU虚拟化型当前在华北-北京、华东-上海部分可用区邀测中；
* 第一代通用型、计算优化型及内存优化型云主机还可能在2.3 GHz主频的Intel Xeon E5-2698 v3（Haswell）处理器上运行；
* 在购买实例后，您可根据业务规模变更情况对实例进行配置修改，详细请参见[调整配置](../Operation-Guide/Instance/Resize-Instance.md)。

## 相关参考

[调整配置](../Operation-Guide/Instance/Resize-Instance.md)
