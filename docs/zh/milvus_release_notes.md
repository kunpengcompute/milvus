# Milvus 版本说明书<a name="ZH-CN_TOPIC_0000002552895601"></a>

本文档整合了Milvus KBest优化、KScaNN优化和向量指令优化三个特性的版本说明。

## 版本配套说明<a name="ZH-CN_TOPIC_0000002549826111"></a>

### 产品版本信息<a name="ZH-CN_TOPIC_0000002518186340"></a>

<a name="table229mcpsimp"></a>
<table><tbody><tr id="row234mcpsimp"><th class="firstcol" valign="top" width="14.000000000000002%" id="mcps1.1.3.1.1"><p id="p236mcpsimp"><a name="p236mcpsimp"></a><a name="p236mcpsimp"></a>产品名称</p>
</th>
<td class="cellrowborder" valign="top" width="86%" headers="mcps1.1.3.1.1 "><p id="p6308719427"><a name="p6308719427"></a><a name="p6308719427"></a>Kunpeng BoostKit</p>
</td>
</tr>
<tr id="row239mcpsimp"><th class="firstcol" valign="top" width="14.000000000000002%" id="mcps1.1.3.2.1"><p id="p241mcpsimp"><a name="p241mcpsimp"></a><a name="p241mcpsimp"></a>产品版本</p>
</th>
<td class="cellrowborder" valign="top" width="86%" headers="mcps1.1.3.2.1 "><p id="p243mcpsimp"><a name="p243mcpsimp"></a><a name="p243mcpsimp"></a><span id="text10612828441"><a name="text10612828441"></a><a name="text10612828441"></a>25.1.RC1</span></p>
</td>
</tr>
<tr id="row244mcpsimp"><th class="firstcol" valign="top" width="14.000000000000002%" id="mcps1.1.3.3.1"><p id="p246mcpsimp"><a name="p246mcpsimp"></a><a name="p246mcpsimp"></a>特性名称</p>
</th>
<td class="cellrowborder" valign="top" width="86%" headers="mcps1.1.3.3.1 "><p id="p248mcpsimp"><a name="p248mcpsimp"></a><a name="p248mcpsimp"></a>Milvus优化特性</p>
</td>
</tr>
</tbody>
</table>

### 软件版本配套说明<a name="ZH-CN_TOPIC_0000002549826109"></a>

|软件类型|版本|备注|
|--|--|--|
|OS|openEuler 22.03 LTS SP3、openEuler 22.03 LTS SP4|-|
|Milvus|Milvus 2.4.5|-|
|GCC|GCC 10.3.1|-|
|KSL|2.4.0|KScaNN优化特性配套|
|KScaNN|1.2.0|KScaNN优化特性配套|

### 硬件版本配套说明<a name="ZH-CN_TOPIC_0000002549826113"></a>

|服务器类型|处理器型号|
|--|--|
|鲲鹏服务器|鲲鹏920新型号处理器|

### 病毒扫描结果<a name="ZH-CN_TOPIC_0000002549706115"></a>

不涉及软件包发布，不涉及病毒扫描。

## 2 版本使用注意事项<a name="ZH-CN_TOPIC_0000002518346260"></a>

版本使用注意事项详见各特性指南。



### 4 Milvus KBest优化<a name="ZH-CN_TOPIC_0000002518186342"></a>

## 4.1 更新说明<a name="ZH-CN_TOPIC_0000002549706113"></a>

**新增特性<a name="section402mcpsimp"></a>**

KBest（Kunpeng Blazing-fast embedding similarity search thruster）是鲲鹏自研的高效的图索引算法，通过量化、向量指令等方法优化了最近邻搜索的性能和精度，提供了对标开源Faiss HNSW算法的检索能力。通过在Milvus向量数据库中集成KBest索引算法，可以让用户在鲲鹏服务器上使用更高效的索引算法。

**修改特性<a name="section451mcpsimp"></a>**

V1.1.0版本持续优化KBest算法，新增build_index_type、graph_opt_iter、reorder、adding_pref、patience和level参数。

**删除特性<a name="section454mcpsimp"></a>**

无

### 4.2 已解决的问题<a name="ZH-CN_TOPIC_0000002549706111"></a>

无

### 4.3 遗留问题<a name="ZH-CN_TOPIC_0000002518186338"></a>

无

## 5 Milvus KScaNN优化<a name="ZH-CN_TOPIC_0000002518186342"></a>

### 5.1 更新说明<a name="ZH-CN_TOPIC_0000002549706113"></a>

**新增特性<a name="section402mcpsimp"></a>**

由于鲲鹏芯片的架构差异，ScaNN算法的软硬件协同优势在鲲鹏服务器上无法完全发挥，因此推出KScaNN优化特性，用于优化ScaNN类算法在鲲鹏服务器上的性能表现。KScaNN（Kunpeng Scalable Nearest Neighbors）是一种基于倒排索引，并针对鲲鹏芯片架构进行了深度优化索引布局、算法流程和计算流程的向量检索算法，旨在充分利用芯片潜力。KScaNN接口基于ScaNN开源接口进行了扩展及修改，提供了与开源ScaNN相当的完整检索能力。

**修改特性<a name="section451mcpsimp"></a>**

无

**删除特性<a name="section454mcpsimp"></a>**

无

### 5.2 已解决的问题<a name="ZH-CN_TOPIC_0000002549706111"></a>

无

### 5.3 遗留问题<a name="ZH-CN_TOPIC_0000002518186338"></a>

无

## 6 Milvus向量指令优化<a name="ZH-CN_TOPIC_0000002518186342"></a>

### 6.1 更新说明<a name="ZH-CN_TOPIC_0000002549706113"></a>

**新增特性<a name="section402mcpsimp"></a>**

SVE（Scalable Vector Extension，可伸缩向量扩展）是由ARM公司开发的一种指令集扩展，旨在通过向量化技术提升计算密集型应用的性能。PF（Prefetch，预取）是一种用于优化计算机系统性能的技术，主要用于减少处理器在等待内存数据时的空闲时间。

Milvus是业界领先的一种高性能、高扩展性的向量数据库，它提供强大的数据建模功能。在Milvus上使用HNSW算法或者ScaNN算法对数据集GIST进行测试时发现，两个向量之间求相似度的热点函数占比很高，而该热点函数存在大量循环和简单数学运算的操作，使用SVE指令和PF可以有效地提高函数执行效率。

**修改特性<a name="section451mcpsimp"></a>**

无

**删除特性<a name="section454mcpsimp"></a>**

无

### 6.2 已解决的问题<a name="ZH-CN_TOPIC_0000002549706111"></a>

无

### 6.3 遗留问题<a name="ZH-CN_TOPIC_0000002518186338"></a>

无

## 7 版本配套文档<a name="ZH-CN_TOPIC_0000002518346256"></a>

### 7.1 配套文档列表<a name="ZH-CN_TOPIC_0000002549706109"></a>

|序号|文档名称|内容简介|获取方法|
|--|--|--|--|
|1|《Kunpeng BoostKit 25.1.RC1 Milvus KBest优化 版本说明书》|本文档提供Milvus数据库KBest优化的版本发布及其配套信息。|开源仓|
|2|《Kunpeng BoostKit 25.1.RC1 Milvus KBest优化 特性指南》|本文档提供Milvus使能KBest算法的环境要求、特性使能指导。|开源仓|
|3|《Kunpeng BoostKit 25.1.RC1 Milvus KScaNN优化 版本说明书》|本文档提供Milvus数据库KScaNN优化的版本发布及其配套信息。|开源仓|
|4|《Kunpeng BoostKit 25.1.RC1 Milvus KScaNN优化 特性指南》|本文档提供Milvus使能KScaNN算法的环境要求、特性使能指导。|开源仓|
|5|《Kunpeng BoostKit 25.0.RC1 Milvus向量指令优化 版本说明书》|本文档提供Milvus向量指令优化的版本发布及其配套信息。|开源仓|
|6|《Kunpeng BoostKit 25.0.RC1 Milvus向量指令优化 特性指南》|本文档提供Milvus向量指令优化的环境要求、特性使能指导。|开源仓|

### 7.2 获取文档方式<a name="ZH-CN_TOPIC_0000002549826107"></a>

您可以通过访问[开源仓](https://gitcode.com/boostkit/milvus/tree/master/docs/zh)浏览和获取相关文档。
