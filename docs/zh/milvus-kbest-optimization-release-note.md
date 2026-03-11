# Milvus KBest优化 版本说明书<a name="ZH-CN_TOPIC_0000002521016466"></a>



### 版本配套说明<a name="ZH-CN_TOPIC_0000002516121244"></a>

#### 产品版本信息<a name="ZH-CN_TOPIC_0000002547521153"></a>

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
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.1.3.3.1 "><p id="p253mcpsimp"><a name="p253mcpsimp"></a><a name="p253mcpsimp"></a>Milvus KBest优化</p>
</td>
</tr>
</tbody>
</table>


#### 软件版本配套说明<a name="ZH-CN_TOPIC_0000002547601149"></a>

|软件类型|版本|
|--|--|
|OS|openEuler 22.03 LTS SP3、openEuler 22.03 LTS SP4|
|Milvus|Milvus 2.4.5|
|GCC|GCC 10.3.1|



#### 硬件版本配套说明<a name="ZH-CN_TOPIC_0000002515961324"></a>

|项目|要求|
|--|--|
|处理器|鲲鹏920新型号处理器|



#### 病毒扫描结果<a name="ZH-CN_TOPIC_0000002516121246"></a>

不涉及软件包发布，不涉及病毒扫描。



### V1.1.0<a name="ZH-CN_TOPIC_0000002547521147"></a>

#### 更新说明<a name="ZH-CN_TOPIC_0000002547601153"></a>

KBest（Kunpeng Blazing-fast embedding similarity search thruster）是鲲鹏自研的高效的图索引算法，通过量化、向量指令等方法优化了最近邻搜索的性能和精度，提供了对标开源Faiss HNSW算法的检索能力。通过在Milvus向量数据库中集成KBest索引算法，可以让用户在鲲鹏服务器上使用更高效的索引算法。

V1.1.0版本持续优化KBest算法，新增build\_index\_type、graph\_opt\_iter、reorder、adding\_pref、patience和level参数。


#### 已解决的问题<a name="ZH-CN_TOPIC_0000002547521149"></a>

无。


#### 遗留问题<a name="ZH-CN_TOPIC_0000002547601151"></a>

无。



### V1.0.0<a name="ZH-CN_TOPIC_0000002515961322"></a>

#### 更新说明<a name="ZH-CN_TOPIC_0000002515961328"></a>

KBest（Kunpeng Blazing-fast embedding similarity search thruster）是鲲鹏自研的高效的图索引算法，通过量化、向量指令等方法优化了最近邻搜索的性能和精度，提供了对标开源Faiss HNSW算法的检索能力。通过在Milvus向量数据库中集成KBest索引算法，可以让用户在鲲鹏服务器上使用更高效的索引算法。


#### 已解决的问题<a name="ZH-CN_TOPIC_0000002547601145"></a>

无。


#### 遗留问题<a name="ZH-CN_TOPIC_0000002547521151"></a>

无。



### 版本配套文档<a name="ZH-CN_TOPIC_0000002516121240"></a>

#### 版本配套文档<a name="ZH-CN_TOPIC_0000002515961326"></a>

|文档名称|内容简介|交付形式|
|--|--|--|
|《Kunpeng BoostKit 25.1.RC1 Milvus KBest优化 版本说明书》|本文档提供Milvus数据库KBest优化的版本发布及其配套信息。|开源仓|
|《Kunpeng BoostKit 25.1.RC1 Milvus KBest优化 特性指南》|本文档提供Milvus使能KBest算法的环境要求、特性使能指导。|开源仓|



#### 获取文档的方法<a name="ZH-CN_TOPIC_0000002547601147"></a>

您可以通过访问[开源仓](https://gitcode.com/boostkit/milvus/tree/master/docs/zh)浏览和获取相关文档。




