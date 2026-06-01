# Milvus Vector Instruction Optimization Release Notes



### Version Mapping<a name="EN-US_TOPIC_0000002516126574"></a>

#### Product Version Information<a name="EN-US_TOPIC_0000002547526485"></a>

<a name="table826974415312"></a>
<table><tbody><tr id="row726916447319"><th class="firstcol" valign="top" width="27.79%" id="mcps1.1.3.1.1"><p id="p426912446314"><a name="p426912446314"></a><a name="p426912446314"></a>Product Name</p>
</th>
<td class="cellrowborder" valign="top" width="72.21%" headers="mcps1.1.3.1.1 "><p id="p433219386215"><a name="p433219386215"></a><a name="p433219386215"></a>Kunpeng BoostKit</p>
</td>
</tr>
<tr id="row102692044123111"><th class="firstcol" valign="top" width="27.79%" id="mcps1.1.3.2.1"><p id="p1526912441319"><a name="p1526912441319"></a><a name="p1526912441319"></a>Product Version</p>
</th>
<td class="cellrowborder" valign="top" width="72.21%" headers="mcps1.1.3.2.1 "><p id="p1864713360227"><a name="p1864713360227"></a><a name="p1864713360227"></a><span id="ph1224011917236"><a name="ph1224011917236"></a><a name="ph1224011917236"></a>25.0.RC1</span></p>
</td>
</tr>
<tr id="row14269844183118"><th class="firstcol" valign="top" width="27.79%" id="mcps1.1.3.3.1"><p id="p1027044483111"><a name="p1027044483111"></a><a name="p1027044483111"></a>Software Name</p>
</th>
<td class="cellrowborder" valign="top" width="72.21%" headers="mcps1.1.3.3.1 "><p id="p2270194443117"><a name="p2270194443117"></a><a name="p2270194443117"></a>Milvus vector instruction optimization</p>
</td>
</tr>
</tbody>
</table>


#### Software Version Mapping<a name="EN-US_TOPIC_0000002515966648"></a>

|Type|Version|
|--|--|
|OS|openEuler 22.03 LTS SP3 or openEuler 22.03 LTS SP4|
|Milvus|2.4.5|
|GCC|10.3.1|



#### Hardware Version Mapping<a name="EN-US_TOPIC_0000002515966654"></a>

|Item|Requirement|
|--|--|
|Processor|New Kunpeng 920 processor model|



#### Virus Scan Results<a name="EN-US_TOPIC_0000002515966650"></a>

Virus scanning is not involved because no software package is released.


#### Version Description<a name="EN-US_TOPIC_0000002516126576"></a>

##### Change Description<a name="EN-US_TOPIC_0000002516126572"></a>

Scalable Vector Extension (SVE) is an instruction extension developed by Arm to improve the performance of computing-intensive applications using vectorization. Prefetch (PF) is a technology used to enhance the computer system performance by reducing the idle time of a processor when it waits for memory data.

Milvus is an industry-leading vector database with high performance and scalability. It provides powerful data modeling functions. When the Hierarchical Navigable Small World (HNSW) or Scalable Nearest Neighbors (ScaNN) algorithm is used to test the GIST dataset on Milvus, it is found that the hotspot function for calculating the similarity between two vectors accounts for a large proportion of CPU usage, and the hotspot function involves a large quantity of loops and simple mathematical operations. Using SVE instructions and PF can effectively improve the function execution efficiency.


##### Resolved Issues<a name="EN-US_TOPIC_0000002547606475"></a>

None


##### Known Issues<a name="EN-US_TOPIC_0000002547526487"></a>

None




### Related Documentation<a name="EN-US_TOPIC_0000002515966652"></a>

#### Documentation<a name="EN-US_TOPIC_0000002547606479"></a>

|Document|Description|Delivery Method|
|--|--|--|
|*Kunpeng BoostKit 25.0.RC1 Milvus Vector Instruction Optimization Release Notes*|Describes the version release and mapping information of the Milvus vector instruction optimization feature.|Open-source repository|
|*Kunpeng BoostKit 25.0.RC1 Milvus Vector Instruction Optimization Feature Guide*|Describes the environment requirements and provides guidance on enabling the Milvus vector instruction optimization feature.|Open-source repository|



#### Obtaining Documentation<a name="EN-US_TOPIC_0000002547526489"></a>

Visit the [open-source repository](https://gitcode.com/boostkit/milvus/tree/master/docs/en) to view or download required documents.




## Acronyms and Abbreviations<a name="EN-US_TOPIC_0000002516126578"></a>

|Acronym/Abbreviation|Full Spelling|
|--|--|
|SVE|Scalable Vector Extension|
|NEON|Advanced SIMD (Single Instruction Multiple Data)|
|PF|Prefetch|
|QPS|queries per second|
