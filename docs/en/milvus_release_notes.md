# Release Notes

## 2025-06-30

### Change History

| Version| Date      | Description                                                                                                                                |
| ---- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| 02   | 2025-06-30 |- Optimized the KBest algorithm and added the <code>build_index_type</code>, <code>graph_opt_iter</code>, <code>reorder</code>, <code>adding_pref</code>, <code>patience</code>, and <code>level</code> parameters.<br>- Released the Milvus KScaNN optimization feature.|

### Version Mapping

#### Product Version Information

| Product Name     | Version    |
| --------- | -------- |
| BoostDB | 25.1.RC1 |

#### Software Version Mapping

|Feature Name|Software|Version|
|--|--|--|
|Milvus KBest optimization and Milvus KScaNN optimization|OS|openEuler 22.03 LTS SP3 or openEuler 22.03 LTS SP4|
|Milvus KBest optimization and Milvus KScaNN optimization|Milvus|2.4.5|
|Milvus KBest optimization|GCC|10.3.1|
|Milvus KScaNN optimization|KSL|2.4.0|
|Milvus KScaNN optimization|KScaNN|1.2.0|

#### Hardware Version Mapping

| Feature         | Item         | Requirement                                     |
| ------------- | ------------- | ----------------------------------------- |
| Milvus KBest optimization and Milvus KScaNN optimization     | Processor          | New Kunpeng 920 processor model                 |

#### Virus Scan Results

Virus scanning is not involved because no software package is released.

### Important Notes

None

### Release Notes

#### Change Description

##### Milvus KBest Optimization

The KBest algorithm is continuously optimized and the `build_index_type`, `graph_opt_iter`, `reorder`, `adding_pref`, `patience`, and `level` parameters are added.

##### Milvus KScaNN Optimization

The Milvus KScaNN optimization feature is released for the first time.

Due to the architectural differences of Kunpeng processors, the advantages in hardware-software collaboration of the ScaNN algorithm cannot be fully realized on Kunpeng servers. To address this, the Kunpeng Scalable Nearest Neighbors (KScaNN) optimization feature is introduced to enhance the performance of the ScaNN algorithm on these servers.

#### Resolved Issues

None

#### Known Issues

None

### Related Documentation

|Document|Description|Delivery Method|
|--|--|--|
|*Milvus KBest Optimization Feature Guide*|Describes the environment requirements and provides guidance on enabling the KBest algorithm in Milvus.|Open-source repository|
|*Milvus KScaNN Optimization Feature Guide*|Describes the environment requirements and provides guidance on enabling the KScaNN algorithm in Milvus.|Open-source repository|

### Obtaining Documentation<a name="EN-US_TOPIC_0000002544372643"></a>

Visit the [open-source repository](https://gitcode.com/boostkit/milvus/tree/master/docs/en) to view or download required documents.

## 2025-03-30

### Change History

| Version| Date      | Description                                                                                                                                |
| ---- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| 01   | 2025-03-30 |- Released the Milvus KBest optimization feature.<br>- Released the Milvus vector instruction optimization feature.|

### Version Mapping

#### Product Version Information

| Product Name     | Version    |
| --------- | -------- |
| BoostDB | 25.0.RC1 |

#### Software Version Mapping

|Feature Name|Software|Version|
|--|--|--|
|Milvus KBest optimization and Milvus vector instruction optimization|OS|openEuler 22.03 LTS SP3 or openEuler 22.03 LTS SP4|
|Milvus KBest optimization and Milvus vector instruction optimization|Milvus|2.4.5|
|Milvus KBest optimization and Milvus vector instruction optimization|GCC|10.3.1|

#### Hardware Version Mapping

| Feature         | Item         | Requirement                                     |
| ------------- | ------------- | ----------------------------------------- |
| Milvus KBest optimization and Milvus vector instruction optimization     | Processor          | New Kunpeng 920 processor model                 |

#### Virus Scan Results

Virus scanning is not involved because no software package is released.

### Important Notes

None

### Release Notes

#### Change Description

##### Milvus KBest Optimization

The Milvus KBest optimization feature is released for the first time.

The Kunpeng Blazing-fast embedding similarity search thruster (KBest) is an efficient, Kunpeng-developed graph search algorithm. It optimizes the performance and precision of the nearest neighbor search by using methods such as quantization and vector instructions, delivering search capabilities equivalent to the open-source Faiss HNSW algorithm. Through the integration of KBest into the Milvus vector database, a more efficient search algorithm is ready for use on Kunpeng servers.

##### Milvus Vector Instruction Optimization

The Milvus vector instruction optimization feature is released for the first time.

Scalable Vector Extension (SVE) is an instruction extension developed by Arm to improve the performance of computing-intensive applications using vectorization. Prefetch (PF) is a technology used to enhance the computer system performance by reducing the idle time of a processor when it waits for memory data.

Milvus is an industry-leading vector database with high performance and scalability. It provides powerful data modeling functions. When the Hierarchical Navigable Small World (HNSW) or Scalable Nearest Neighbors (ScaNN) algorithm is used to test the GIST dataset on Milvus, it is found that the hotspot function for calculating the similarity between two vectors accounts for a large proportion of CPU usage, and the hotspot function involves a large quantity of loops and simple mathematical operations. Using SVE instructions and PF can effectively improve the function execution efficiency.

#### Resolved Issues

None

#### Known Issues

None

### Related Documentation

|Document|Description|Delivery Method|
|--|--|--|
|*Milvus KBest Optimization Feature Guide*|Describes the environment requirements and provides guidance on enabling the KBest algorithm in Milvus.|Open-source repository|
|*Milvus Vector Instruction Optimization Feature Guide*|Describes the environment requirements and provides guidance on enabling the Milvus vector instruction optimization feature.|Open-source repository|

### Obtaining Documentation<a name="EN-US_TOPIC_0000002544372643"></a>

Visit the [open-source repository](https://gitcode.com/boostkit/milvus/tree/master/docs/en) to view or download required documents.
