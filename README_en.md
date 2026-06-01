# BoostKit Milvus

## Project Brand Name

Milvus

### Latest Updates

* [2025-06-30] Released `Milvus KBest optimization` V1.1.0, which is a Kunpeng-developed graph index algorithm. Six new parameters are added, improving the QPS performance by more than 30%.
* [2025-06-30] Released the `Milvus KScaNN optimization` feature, which is a vector search algorithm optimized for the Kunpeng architecture. This feature improves the QPS performance by more than 30%.
* [2025-03-30] Released the `Milvus vector instruction optimization` feature, which supports Scalable Vector Extension (SVE) vector instructions and prefetch (PF). This feature improves the QPS performance of the HNSW and ScaNN algorithms by 20%.

### Project Introduction

BoostKit Milvus is a Milvus optimization patch repository based on the Kunpeng platform. It provides:

- **Vector instruction optimization patch**: SVE and PF are used to optimize vector computing performance.
- **KBest algorithm patches**: The KBest algorithm is a Kunpeng-developed efficient graph index algorithm, which optimizes the nearest neighbor search performance through quantization and vector instructions.
- **KScaNN algorithm patches**: The KScaNN algorithm is a vector search algorithm optimized for the Kunpeng chip architecture and implemented based on inverted indexing.

All optimization features are provided in patch files. You need to apply the patches and compile the open-source Milvus source code.

The repository documents are as follows:

| Document| Description| Link|
| --- | --- | --- |
| _milvus_vector_instruction_optimization_release_notes_| Version release and mapping information| [Release Notes](docs/en/milvus_vector_instruction_optimization_release_notes.md)|
| _milvus_vector_instruction_optimization_feature_guide_| SVE+PF optimization principles and installation and configuration methods| [Feature Guide](docs/en/milvus_vector_instruction_optimization_feature_guide.md)|
| _milvus_kbest_optimization_release_note_| KBest version release and mapping information| [Release Notes](docs/en/milvus_kbest_optimization_release_note.md)|
| _milvus_kbest_optimization_feature_guide_| Principles, installation, and usage of the KBest algorithm| [Feature Guide](docs/en/milvus_kbest_optimization_feature_guide.md)|
| _milvus_kscann_optimization_release_notes_| KScaNN version release and mapping information| [Release Notes](docs/en/milvus_kscann_optimization_release_notes.md)|
| _milvus_kscann_optimization_feature_guide_| Principles, installation, and usage of the KScaNN algorithm| [Feature Guide](docs/en/milvus_kscann_optimization_feature_guide.md)|

### Directory Structure

```text
milvus/
├── README.md                                                             # Entry to the repository overview, providing branch details and feature navigation
├── docs/en/
│   ├── milvus_vector_instruction_optimization_release_notes.md           # Release notes of the vector instruction optimization feature
│   ├── milvus_vector_instruction_optimization_feature_guide.md           # Principles and enabling guide of the vector instruction optimization feature
│   ├── milvus_kbest_optimization_release_note.md                         # Release notes of the KBest optimization feature
│   ├── milvus_kbest_optimization_feature_guide.md                        # Principles and enabling guide of the KBest algorithm
│   ├── milvus_kscann_optimization_release_notes.md                       # Release notes of the KScaNN optimization feature
│   ├── milvus_kscann_optimization_feature_guide.md                       # Principles and enabling guide of the KScaNN algorithm
│   └── figures/                                                          # Directory for document figures
│       ├── milvus_query_architecture_kbest.png                      # Milvus query architecture
│       ├── milvus_query_architecture_kscann.png                     # Milvus query architecture (KScaNN)
│       ├── performance_comparison_kbest.png                            # Performance comparison (KBest)
│       ├── performance_comparison_kscann.png                           # Performance comparison (KScaNN)
│       └── performance_comparison_vec_instr.png                         # Performance comparison (vector instruction optimization)
└── (branch) milvus-v2.4.5/
    ├── README.md                                                         # milvus-v2.4.5 branch overview and patch description
    ├── knowhere-2.3.5-hnsw-scann-pf-sve.patch                            # Vector instruction optimization patch (SVE+PF)
    ├── knowhere-2.3.5-kbest-kscann.patch                                 # KBest and KScaNN algorithm patch (Knowhere)
    └── milvus-2.4.5-kbest-kscann.patch                                   # KBest and KScaNN algorithm patch (Milvus)
```

### Feature Introduction

<table>
<thead>
<tr>
<th>Category</th>
<th>Feature Name</th>
<th>Feature Document</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="2">Vector computing acceleration</td>
<td>SVE vector instruction optimization</td>
<td><a href="docs/en/milvus_vector_instruction_optimization_feature_guide.md">milvus_vector_instruction_optimization_feature_guide.md</a></td>
<td>The Arm SVE instruction set is used to optimize vector computing. The length of vector registers can be extended, and vector predicate operations are supported.</td>
</tr>
<tr>
<td>PF optimization</td>
<td><a href="docs/en/milvus_vector_instruction_optimization_feature_guide.md">milvus_vector_instruction_optimization_feature_guide.md</a></td>
<td>The PF technology is used to reduce the memory access latency, and the PRFM instruction is used to load data to the cache in advance.</td>
</tr>
<tr>
<td>Graph index algorithm</td>
<td>KBest optimization</td>
<td><a href="docs/en/milvus_kbest_optimization_feature_guide.md">milvus_kbest_optimization_feature_guide.md</a></td>
<td>The efficient graph index algorithm developed by Kunpeng optimizes the nearest neighbor search through quantization and vector instructions, improving the QPS by more than 30%.</td>
</tr>
<tr>
<td>Vector search optimization</td>
<td>KScaNN optimization</td>
<td><a href="docs/en/milvus_kscann_optimization_feature_guide.md">milvus_kscann_optimization_feature_guide.md</a></td>
<td>This feature is a vector search algorithm optimized for the Kunpeng architecture and implemented based on inverted indexing. It optimizes the index layout and computing process, improving the QPS by more than 30%.</td>
</tr>
</tbody>
</table>

### Milvus Compatibility Information

| Feature Version| Upstream Version| CPU | OS| GCC/Toolchain|
| --- | --- | --- | --- | --- |
| Milvus vector instruction optimization 25.0.RC1| Milvus 2.4.5 | New Kunpeng 920 processor model| openEuler 22.03 LTS SP3/SP4 | GCC 10.3.1 |
| Milvus KBest optimization V1.1.0| Milvus 2.4.5 | New Kunpeng 920 processor model| openEuler 22.03 LTS SP3/SP4 | GCC 10.3.1 |
| Milvus KScaNN optimization 25.1.RC1| Milvus 2.4.5 | New Kunpeng 920 processor model| openEuler 22.03 LTS SP3/SP4 | GCC 10.3.1 |

### Constraints and Precautions

- The optimization features are provided in patch files, which need to be integrated and compiled from the source code and cannot be directly installed using the RPM packages.
- The open-source Milvus source code does not include the index-related component Knowhere. You need to pull the Knowhere source code during Milvus compilation and integrate it into the database.
- Milvus needs to be compiled twice: The first compilation is to obtain the Knowhere source code, and the second compilation is performed after applying the patch files.
- KBest optimization requires the installation of Kunpeng Recall Algorithm Library (`BoostKit-SRA_Recall-1.2.0.zip`).
- KScaNN optimization requires the installation of Kunpeng Recall Algorithm Library and Kunpeng System Library (`BoostKit-ksl_2.4.0.zip`).
- KScaNN optimization requires the additional compilation of the OpenScann dynamic library `libscann_cc.so`.
- You are advised to enable the BIOS prefetch function in advance, which can be used together with software prefetch to obtain better performance.
- The KBest and KScaNN index types are case-sensitive (`KBEST`/`KSCANN`).
- The dimension range supported by KBest is [1, 2999].

### Feature Version Maintenance Strategy

| Feature| Current Version| Maintenance Status| Description|
| --- | --- | --- | --- |
| Milvus vector instruction optimization| 25.0.RC1 | Continuous maintenance| Provides the SVE+PF optimization patch.|
| Milvus KBest optimization| V1.1.0 | Continuous maintenance| Adds six new optimization parameters.|
| Milvus KScaNN optimization| 25.1.RC1 | Continuous maintenance| Provides the KScaNN algorithm patches.|

### Version Maintenance Strategy

| Version| Maintenance Strategy| Current Status| Next Status| EOL Date|
| --- | --- | --- | --- | --- |
| Milvus 2.4.5 | Regular version| Maintenance| - | - |

### Performance Improvement

| Feature| Test Scenario| Dataset| Recall | QPS Improvement|
| --- | --- | --- | --- | --- |
| Milvus vector instruction optimization| Milvus-HNSW algorithm| ANN-Benchmarks GIST| > 0.99| 20% |
| Milvus vector instruction optimization| Milvus-ScaNN algorithm| ANN-Benchmarks GIST| > 0.95| 20% |
| Milvus KBest optimization| Comparison with the Milvus-HNSW algorithm| ANN-Benchmarks GIST| > 0.99| > 30%|
| Milvus KScaNN optimization| Comparison with the Milvus-ScaNN algorithm| ANN-Benchmarks GIST| > 0.95| > 30%|

### Contribution Statement

You are welcome to contribute to the community. If you have any questions, suggestions, feature requirements, or bug reports, please submit:

- [Issues](https://gitcode.com/boostkit/milvus/issues)

For details about the contribution process, see:

- [BoostKit Community Contribution Guide](https://gitcode.com/boostkit/community/blob/master/docs/contributor/contributing.md)

You are also welcome to share insights in:

- [BoostKit Discussions](https://gitcode.com/boostkit/community/discussions)

### License

The documents of this project are licensed under CC-BY 4.0. For details, see [LICENSE](https://gitcode.com/boostkit/milvus/tree/master/docs/LICENSE).
