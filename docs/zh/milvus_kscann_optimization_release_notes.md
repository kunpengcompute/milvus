# Milvus KScaNN优化 版本说明书<a name="ZH-CN_TOPIC_0000002521149494"></a>


### 版本配套说明<a name="ZH-CN_TOPIC_0000002516136620"></a>

#### 产品版本信息<a name="ZH-CN_TOPIC_0000002547536527"></a>

<a name="table234mcpsimp"></a>
<table><tbody><tr id="row239mcpsimp"><th class="firstcol" valign="top" width="28.000000000000004%" id="mcps1.1.3.1.1"><p id="p241mcpsimp"><a name="p241mcpsimp"></a><a name="p241mcpsimp"></a>产品名称</p>
</th>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.1.3.1.1 "><p id="p243mcpsimp"><a name="p243mcpsimp"></a><a name="p243mcpsimp"></a>Kunpeng BoostKit</p>
</td>
</tr>
<tr id="row244mcpsimp"><th class="firstcol" valign="top" width="28.000000000000004%" id="mcps1.1.3.2.1"><p id="p246mcpsimp"><a name="p246mcpsimp"></a><a name="p246mcpsimp"></a>产品版本</p>
</th>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.1.3.2.1 "><p id="p248mcpsimp"><a name="p248mcpsimp"></a><a name="p248mcpsimp"></a><span id="ph19215191985117"><a name="ph19215191985117"></a><a name="ph19215191985117"></a>25.1.RC1</span></p>
</td>
</tr>
<tr id="row249mcpsimp"><th class="firstcol" valign="top" width="28.000000000000004%" id="mcps1.1.3.3.1"><p id="p251mcpsimp"><a name="p251mcpsimp"></a><a name="p251mcpsimp"></a>特性名称</p>
</th>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.1.3.3.1 "><p id="p253mcpsimp"><a name="p253mcpsimp"></a><a name="p253mcpsimp"></a>Milvus KScaNN优化</p>
</td>
</tr>
</tbody>
</table>


#### 软件版本配套说明<a name="ZH-CN_TOPIC_0000002547536529"></a>

|软件类型|版本|
|--|--|
|操作系统|openEuler 22.03 LTS SP3|
|操作系统|openEuler 22.03 LTS SP4|
|Milvus|Milvus 2.4.5|
|KSL|2.4.0|
|KScaNN|1.2.0|



#### 硬件版本配套说明<a name="ZH-CN_TOPIC_0000002515976712"></a>

|项目|要求|
|--|--|
|处理器|鲲鹏920新型号处理器|



#### 病毒扫描结果<a name="ZH-CN_TOPIC_0000002547616519"></a>

不涉及软件包发布，不涉及病毒扫描。



### 版本说明<a name="ZH-CN_TOPIC_0000002547536533"></a>

#### 更新说明<a name="ZH-CN_TOPIC_0000002516136616"></a>

由于鲲鹏芯片的架构差异，ScaNN算法的软硬件协同优势在鲲鹏服务器上无法完全发挥，因此推出KScaNN优化特性，用于优化ScaNN类算法在鲲鹏服务器上的性能表现。KScaNN（Kunpeng Scalable Nearest Neighbors）是一种基于倒排索引，并针对鲲鹏芯片架构进行了深度优化索引布局、算法流程和计算流程的向量检索算法，旨在充分利用芯片潜力。KScaNN接口基于ScaNN开源接口进行了扩展及修改，提供了与开源ScaNN相当的完整检索能力。


#### 已解决的问题<a name="ZH-CN_TOPIC_0000002516136618"></a>

无。


#### 遗留问题<a name="ZH-CN_TOPIC_0000002547616521"></a>

无。



### 版本配套文档<a name="ZH-CN_TOPIC_0000002547536531"></a>

#### 版本配套文档<a name="ZH-CN_TOPIC_0000002515976710"></a>

|文档名称|内容简介|交付形式|
|--|--|--|
|《Kunpeng BoostKit 25.1.RC1 Milvus KScaNN优化 版本说明书》|本文档提供Milvus数据库KScaNN优化的版本发布及其配套信息。|开源仓|
|《Kunpeng BoostKit 25.1.RC1 Milvus KScaNN优化 特性指南》|本文档提供Milvus使能KScaNN算法的环境要求、特性使能指导。|开源仓|



#### 获取文档的方法<a name="ZH-CN_TOPIC_0000002515976708"></a>

您可以通过访问[开源仓](https://gitcode.com/boostkit/milvus/tree/master/docs/zh)浏览和获取相关文档。




