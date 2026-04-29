# Milvus向量指令优化 版本说明书



### 版本配套说明<a name="ZH-CN_TOPIC_0000002516126574"></a>

#### 产品版本信息<a name="ZH-CN_TOPIC_0000002547526485"></a>

<a name="table826974415312"></a>
<table><tbody><tr id="row726916447319"><th class="firstcol" valign="top" width="27.79%" id="mcps1.1.3.1.1"><p id="p426912446314"><a name="p426912446314"></a><a name="p426912446314"></a>产品名称</p>
</th>
<td class="cellrowborder" valign="top" width="72.21%" headers="mcps1.1.3.1.1 "><p id="p433219386215"><a name="p433219386215"></a><a name="p433219386215"></a>Kunpeng BoostKit</p>
</td>
</tr>
<tr id="row102692044123111"><th class="firstcol" valign="top" width="27.79%" id="mcps1.1.3.2.1"><p id="p1526912441319"><a name="p1526912441319"></a><a name="p1526912441319"></a>产品版本</p>
</th>
<td class="cellrowborder" valign="top" width="72.21%" headers="mcps1.1.3.2.1 "><p id="p1864713360227"><a name="p1864713360227"></a><a name="p1864713360227"></a><span id="ph1224011917236"><a name="ph1224011917236"></a><a name="ph1224011917236"></a>25.0.RC1</span></p>
</td>
</tr>
<tr id="row14269844183118"><th class="firstcol" valign="top" width="27.79%" id="mcps1.1.3.3.1"><p id="p1027044483111"><a name="p1027044483111"></a><a name="p1027044483111"></a>软件名称</p>
</th>
<td class="cellrowborder" valign="top" width="72.21%" headers="mcps1.1.3.3.1 "><p id="p2270194443117"><a name="p2270194443117"></a><a name="p2270194443117"></a>Milvus向量指令优化</p>
</td>
</tr>
</tbody>
</table>


#### 软件版本配套说明<a name="ZH-CN_TOPIC_0000002515966648"></a>

|软件类型|版本|
|--|--|
|OS|openEuler 22.03 LTS SP3、openEuler 22.03 LTS SP4|
|Milvus|2.4.5|
|GCC|10.3.1|



#### 硬件版本配套说明<a name="ZH-CN_TOPIC_0000002515966654"></a>

|项目|要求|
|--|--|
|处理器|鲲鹏920新型号处理器|



#### 病毒扫描结果<a name="ZH-CN_TOPIC_0000002515966650"></a>

不涉及软件包发布，不涉及病毒扫描。


#### 版本说明<a name="ZH-CN_TOPIC_0000002516126576"></a>

##### 更新说明<a name="ZH-CN_TOPIC_0000002516126572"></a>

SVE（Scalable Vector Extension，可伸缩向量扩展）是由ARM公司开发的一种指令集扩展，旨在通过向量化技术提升计算密集型应用的性能。PF（Prefetch，预取）是一种用于优化计算机系统性能的技术，主要用于减少处理器在等待内存数据时的空闲时间。

Milvus是业界领先的一种高性能、高扩展性的向量数据库，它提供强大的数据建模功能。在Milvus上使用HNSW算法或者ScaNN算法对数据集GIST进行测试时发现，两个向量之间求相似度的热点函数占比很高，而该热点函数存在大量循环和简单数学运算的操作，使用SVE指令和PF可以有效地提高函数执行效率。


##### 已解决的问题<a name="ZH-CN_TOPIC_0000002547606475"></a>

无。


##### 遗留问题<a name="ZH-CN_TOPIC_0000002547526487"></a>

无。




### 版本配套文档<a name="ZH-CN_TOPIC_0000002515966652"></a>

#### 版本配套文档<a name="ZH-CN_TOPIC_0000002547606479"></a>

|文档名称|内容简介|交付形式|
|--|--|--|
|《Kunpeng BoostKit 25.0.RC1 Milvus向量指令优化 版本说明书》|本文档提供Milvus向量指令优化的版本发布及其配套信息。|开源仓|
|《Kunpeng BoostKit 25.0.RC1 Milvus向量指令优化 特性指南》|本文档提供Milvus向量指令优化的环境要求、特性使能指导。|开源仓|



#### 获取文档的方法<a name="ZH-CN_TOPIC_0000002547526489"></a>

您可以通过访问[开源仓](https://gitcode.com/boostkit/milvus/tree/master/docs/zh)浏览和获取相关文档。




## 缩略语<a name="ZH-CN_TOPIC_0000002516126578"></a>

|缩略语|英文全称|中文全称|
|--|--|--|
|SVE|Scalable Vector Extension|可扩展向量扩展|
|NEON|Advanced SIMD (Single Instruction Multiple Data)|高级单指令多数据流|
|PF|Prefetching|预取|
|QPS|Queries Per Second|每秒查询率|



