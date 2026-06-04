# Milvus KScaNN Optimization Release Notes


### Version Mapping<a name="EN-US_TOPIC_0000002516136620"></a>

#### Product Version Information<a name="EN-US_TOPIC_0000002547536527"></a>

<a name="table234mcpsimp"></a>
<table><tbody><tr id="row239mcpsimp"><th class="firstcol" valign="top" width="28.000000000000004%" id="mcps1.1.3.1.1"><p id="p241mcpsimp"><a name="p241mcpsimp"></a><a name="p241mcpsimp"></a>Product Name</p>
</th>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.1.3.1.1 "><p id="p243mcpsimp"><a name="p243mcpsimp"></a><a name="p243mcpsimp"></a>Kunpeng BoostKit</p>
</td>
</tr>
<tr id="row244mcpsimp"><th class="firstcol" valign="top" width="28.000000000000004%" id="mcps1.1.3.2.1"><p id="p246mcpsimp"><a name="p246mcpsimp"></a><a name="p246mcpsimp"></a>Product Version</p>
</th>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.1.3.2.1 "><p id="p248mcpsimp"><a name="p248mcpsimp"></a><a name="p248mcpsimp"></a><span id="ph19215191985117"><a name="ph19215191985117"></a><a name="ph19215191985117"></a>25.1.RC1</span></p>
</td>
</tr>
<tr id="row249mcpsimp"><th class="firstcol" valign="top" width="28.000000000000004%" id="mcps1.1.3.3.1"><p id="p251mcpsimp"><a name="p251mcpsimp"></a><a name="p251mcpsimp"></a>Feature Name</p>
</th>
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.1.3.3.1 "><p id="p253mcpsimp"><a name="p253mcpsimp"></a><a name="p253mcpsimp"></a>Milvus KScaNN optimization</p>
</td>
</tr>
</tbody>
</table>


#### Software Version Mapping<a name="EN-US_TOPIC_0000002547536529"></a>

|Type|Version|
|--|--|
|OS|openEuler 22.03 LTS SP3|
|OS|openEuler 22.03 LTS SP4|
|Milvus|Milvus 2.4.5|
|KSL|2.4.0|
|KScaNN|1.2.0|



#### Hardware Version Mapping<a name="EN-US_TOPIC_0000002515976712"></a>

|Item|Requirement|
|--|--|
|Processor|New Kunpeng 920 processor model|



#### Virus Scan Results<a name="EN-US_TOPIC_0000002547616519"></a>

Virus scanning is not involved because no software package is released.



### Version Description<a name="EN-US_TOPIC_0000002547536533"></a>

#### Change Description<a name="EN-US_TOPIC_0000002516136616"></a>

Due to the architectural differences of Kunpeng processors, the advantages in hardware-software collaboration of the ScaNN algorithm cannot be fully realized on Kunpeng servers. To address this, the Kunpeng Scalable Nearest Neighbors (KScaNN) optimization feature is introduced to enhance the performance of the ScaNN algorithm on these servers. KScaNN is a vector retrieval algorithm that utilizes inverted indexing and is deeply optimized for the Kunpeng processor architecture in terms of index layout, algorithm flow, and computation flow, with the goal of fully exploiting the processor capabilities. The KScaNN interfaces extend and modify the open-source ScaNN interfaces, offering comprehensive retrieval capabilities comparable to those of open-source ScaNN.


#### Resolved Issues<a name="EN-US_TOPIC_0000002516136618"></a>

None


#### Known Issues<a name="EN-US_TOPIC_0000002547616521"></a>

None



### Related Documentation<a name="EN-US_TOPIC_0000002547536531"></a>

#### Documentation<a name="EN-US_TOPIC_0000002515976710"></a>

|Document|Description|Delivery Method|
|--|--|--|
|*Kunpeng BoostKit 25.1.RC1 Milvus KScaNN Optimization Release Notes*|Describes the version release and mapping information of the Milvus KScaNN optimization feature.|Open-source repository|
|*Kunpeng BoostKit 25.1.RC1 Milvus KScaNN Optimization Feature Guide*|Describes the environment requirements and provides guidance on enabling the KScaNN algorithm in Milvus.|Open-source repository|



#### Obtaining Documentation<a name="EN-US_TOPIC_0000002515976708"></a>

Visit the [open-source repository](https://gitcode.com/boostkit/milvus/tree/master/docs/en) to view or download required documents.
