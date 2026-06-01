# Milvus KBest Optimization Release Notes



### Version Mapping<a name="EN-US_TOPIC_0000002516121244"></a>

#### Product Version Information<a name="EN-US_TOPIC_0000002547521153"></a>

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
<td class="cellrowborder" valign="top" width="72%" headers="mcps1.1.3.3.1 "><p id="p253mcpsimp"><a name="p253mcpsimp"></a><a name="p253mcpsimp"></a>Milvus KBest optimization</p>
</td>
</tr>
</tbody>
</table>


#### Software Version Mapping<a name="EN-US_TOPIC_0000002547601149"></a>

|Type|Version|
|--|--|
|OS|openEuler 22.03 LTS SP3 or openEuler 22.03 LTS SP4|
|Milvus|Milvus 2.4.5|
|GCC|GCC 10.3.1|



#### Hardware Version Mapping<a name="EN-US_TOPIC_0000002515961324"></a>

|Item|Requirement|
|--|--|
|Processor|New Kunpeng 920 processor model|



#### Virus Scan Results<a name="EN-US_TOPIC_0000002516121246"></a>

Virus scanning is not involved because no software package is released.



### V1.1.0<a name="EN-US_TOPIC_0000002547521147"></a>

#### Change Description<a name="EN-US_TOPIC_0000002547601153"></a>

The Kunpeng Blazing-fast embedding similarity search thruster (KBest) is an efficient, Kunpeng-developed graph search algorithm. It optimizes the performance and precision of the nearest neighbor search by using methods such as quantization and vector instructions, delivering search capabilities equivalent to the open-source Faiss HNSW algorithm. Through the integration of KBest into the Milvus vector database, a more efficient search algorithm is ready for use on Kunpeng servers.

V1.1.0 further optimizes the KBest algorithm and adds the `build_index_type`, `graph_opt_iter`, `reorder`, `adding_pref`, `patience`, and `level` parameters.


#### Resolved Issues<a name="EN-US_TOPIC_0000002547521149"></a>

None


#### Known Issues<a name="EN-US_TOPIC_0000002547601151"></a>

None



### V1.0.0<a name="EN-US_TOPIC_0000002515961322"></a>

#### Change Description<a name="EN-US_TOPIC_0000002515961328"></a>

The Kunpeng Blazing-fast embedding similarity search thruster (KBest) is an efficient, Kunpeng-developed graph search algorithm. It optimizes the performance and precision of the nearest neighbor search by using methods such as quantization and vector instructions, delivering search capabilities equivalent to the open-source Faiss HNSW algorithm. Through the integration of KBest into the Milvus vector database, a more efficient search algorithm is ready for use on Kunpeng servers.


#### Resolved Issues<a name="EN-US_TOPIC_0000002547601145"></a>

None


#### Known Issues<a name="EN-US_TOPIC_0000002547521151"></a>

None



### Related Documentation<a name="EN-US_TOPIC_0000002516121240"></a>

#### Documentation<a name="EN-US_TOPIC_0000002515961326"></a>

|Document|Description|Delivery Method|
|--|--|--|
|*Kunpeng BoostKit 25.1.RC1 Milvus KBest Optimization Release Notes*|Describes the version release and mapping information of the Milvus KBest optimization feature.|Open-source repository|
|*Kunpeng BoostKit 25.1.RC1 Milvus KBest Optimization Feature Guide*|Describes the environment requirements and provides guidance on enabling the KBest algorithm in Milvus.|Open-source repository|



#### Obtaining Documentation<a name="EN-US_TOPIC_0000002547601147"></a>

Visit the [open-source repository](https://gitcode.com/boostkit/milvus/tree/master/docs/en) to view or download required documents.
