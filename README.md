# BoostKit Milvus

## 项目品牌名称

Milvus

### 最新消息

* [2025.06.30] 发布 `Milvus-KBest优化` V1.1.0 版本，鲲鹏自研图索引算法，新增 6 个优化参数，QPS 性能提升 30% 以上。
* [2025.06.30] 发布 `Milvus-KScaNN优化` 特性，针对鲲鹏架构深度优化的向量检索算法，QPS 性能提升 30% 以上。
* [2025.03.30] 发布 `Milvus向量指令优化` 特性，支持 SVE 向量指令和 PF 预取优化，HNSW 算法 QPS 提升 20%，ScaNN 算法 QPS 提升 20%。

### 项目介绍

BoostKit Milvus 是面向鲲鹏平台的 Milvus 向量数据库优化补丁仓库，提供：

- **向量指令优化补丁**：使用 SVE（可伸缩向量扩展）和 PF（预取）技术优化向量计算性能。
- **KBest 算法补丁**：鲲鹏自研高效图索引算法，通过量化和向量指令优化最近邻搜索性能。
- **KScaNN 算法补丁**：针对鲲鹏芯片架构深度优化的向量检索算法，基于倒排索引实现。

所有优化特性以补丁文件（patch）形式提供，需要对开源 Milvus 源码进行编译集成。

仓库文档导航如下：

| 文档名称 | 内容说明 | 链接 |
| --- | --- | --- |
| milvus_vector_instruction_optimization_release_notes | 版本发布及配套信息 | [版本说明书](docs/zh/milvus_vector_instruction_optimization_release_notes.md) |
| milvus_vector_instruction_optimization_feature_guide | SVE+PF 优化原理、安装配置方法 | [特性指南](docs/zh/milvus_vector_instruction_optimization_feature_guide.md) |
| milvus_kbest_optimization_release_note | KBest 版本说明及配套信息 | [版本说明书](docs/zh/milvus_kbest_optimization_release_note.md) |
| milvus_kbest_optimization_feature_guide | KBest 算法原理、安装使用方法 | [特性指南](docs/zh/milvus_kbest_optimization_feature_guide.md) |
| milvus_kscann_optimization_release_notes | KScaNN 版本说明及配套信息 | [版本说明书](docs/zh/milvus_kscann_optimization_release_notes.md) |
| milvus_kscann_optimization_feature_guide | KScaNN 算法原理、安装使用方法 | [特性指南](docs/zh/milvus_kscann_optimization_feature_guide.md) |

### 目录结构

```text
milvus/
├── README.md                                                             # 仓库总览入口，说明分支与特性导航
├── docs/zh/
│   ├── milvus_vector_instruction_optimization_release_notes.md           # 向量指令优化版本发布说明
│   ├── milvus_vector_instruction_optimization_feature_guide.md           # 向量指令优化原理与使能指导
│   ├── milvus_kbest_optimization_release_note.md                         # KBest 优化版本发布说明
│   ├── milvus_kbest_optimization_feature_guide.md                        # KBest 算法原理与使能指导
│   ├── milvus_kscann_optimization_release_notes.md                       # KScaNN 优化版本发布说明
│   ├── milvus_kscann_optimization_feature_guide.md                       # KScaNN 算法原理与使能指导
│   └── figures/                                                          # 文档配图目录
│       ├── Milvus整体查询架构.png                                         # Milvus 查询架构图
│       ├── Milvus整体查询架构-0.png                                       # Milvus 查询架构图（KScaNN）
│       ├── 优化特性使能前后性能对比.png                                    # KBest 性能对比图
│       ├── 优化特性使能前后性能对比-1.png                                  # KScaNN 性能对比图
│       └── 优化特性使能前后性能对比-2.png                                  # 向量指令优化性能对比图
└── (branch) milvus-v2.4.5/
    ├── README.md                                                         # milvus-v2.4.5 分支总览与补丁说明
    ├── knowhere-2.3.5-hnsw-scann-pf-sve.patch                            # 向量指令优化补丁（SVE+PF）
    ├── knowhere-2.3.5-kbest-kscann.patch                                 # KBest 和 KScaNN 算法补丁（Knowhere）
    └── milvus-2.4.5-kbest-kscann.patch                                   # KBest 和 KScaNN 算法补丁（Milvus）
```

### 特性简介

<table>
<thead>
<tr>
<th>分类</th>
<th>特性名称</th>
<th>特性文档</th>
<th>特性介绍</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="2">向量计算加速</td>
<td>SVE 向量指令优化</td>
<td><a href="docs/zh/milvus_vector_instruction_optimization_feature_guide.md">milvus_vector_instruction_optimization_feature_guide.md</a></td>
<td>使用 ARM SVE（可伸缩向量扩展）指令集优化向量计算，向量寄存器长度可扩展，支持矢量谓词操作。</td>
</tr>
<tr>
<td>PF 预取优化</td>
<td><a href="docs/zh/milvus_vector_instruction_optimization_feature_guide.md">milvus_vector_instruction_optimization_feature_guide.md</a></td>
<td>使用 Prefetch 预取技术减少内存访问延迟，通过 PRFM 指令提前加载数据到缓存。</td>
</tr>
<tr>
<td>图索引算法</td>
<td>KBest 优化</td>
<td><a href="docs/zh/milvus_kbest_optimization_feature_guide.md">milvus_kbest_optimization_feature_guide.md</a></td>
<td>鲲鹏自研高效图索引算法，通过量化、向量指令等方法优化最近邻搜索，QPS 提升 30% 以上。</td>
</tr>
<tr>
<td>向量检索优化</td>
<td>KScaNN 优化</td>
<td><a href="docs/zh/milvus_kscann_optimization_feature_guide.md">milvus_kscann_optimization_feature_guide.md</a></td>
<td>针对鲲鹏架构深度优化的向量检索算法，基于倒排索引，优化索引布局和计算流程，QPS 提升 30% 以上。</td>
</tr>
</tbody>
</table>

### Milvus 兼容性信息

| 特性版本 | 上游版本 | CPU | 操作系统 | GCC/工具链 |
| --- | --- | --- | --- | --- |
| Milvus 向量指令优化 25.0.RC1 | Milvus 2.4.5 | 鲲鹏920新型号处理器 | openEuler 22.03 LTS SP3/SP4 | GCC 10.3.1 |
| Milvus KBest 优化 V1.1.0 | Milvus 2.4.5 | 鲲鹏920新型号处理器 | openEuler 22.03 LTS SP3/SP4 | GCC 10.3.1 |
| Milvus KScaNN 优化 25.1.RC1 | Milvus 2.4.5 | 鲲鹏920新型号处理器 | openEuler 22.03 LTS SP3/SP4 | GCC 10.3.1 |

### 工具限制与注意事项

- 优化特性以补丁文件（patch）形式提供，需要从源码编译集成，不支持直接 RPM 安装。
- 开源 Milvus 源码不包含索引相关组件 Knowhere，需要在编译过程中拉取 Knowhere 源码并对接。
- 整体使用过程需要编译 Milvus 两次：第一次编译拉取 Knowhere 源码，第二次编译在应用补丁后进行。
- KBest 优化需要安装鲲鹏召回算法库 `BoostKit-SRA_Recall-1.2.0.zip`。
- KScaNN 优化需要安装鲲鹏召回算法库和鲲鹏系统库 `BoostKit-ksl_2.4.0.zip`。
- KScaNN 优化需要额外编译 OpenScann 动态库 `libscann_cc.so`。
- 建议预先开启 BIOS 预取功能，可结合软件预取获得更好性能。
- KBest 和 KScaNN 索引类型需要严格区分大小写（KBEST/KSCANN）。
- KBest 支持的维度范围为[1,2999]。

### 特性版本维护策略

| 特性名称 | 当前版本 | 维护状态 | 说明 |
| --- | --- | --- | --- |
| Milvus 向量指令优化 | 25.0.RC1 | 持续维护 | 提供 SVE+PF 优化补丁 |
| Milvus KBest 优化 | V1.1.0 | 持续维护 | 新增 6 个优化参数 |
| Milvus KScaNN 优化 | 25.1.RC1 | 持续维护 | 提供 KScaNN 算法补丁 |

### 版本维护策略

| 版本 | 维护策略 | 当前状态 | 后续状态 | EOL日期 |
| --- | --- | --- | --- | --- |
| Milvus 2.4.5 | 常规版本 | 维护 | - | - |

### 性能提升效果

| 特性名称 | 测试场景 | 数据集 | Recall | QPS提升 |
| --- | --- | --- | --- | --- |
| Milvus 向量指令优化 | Milvus-HNSW 算法 | ann-benchmarks Gist | 0.99 以上 | 20% |
| Milvus 向量指令优化 | Milvus-ScaNN 算法 | ann-benchmarks Gist | 0.95 以上 | 20% |
| Milvus KBest 优化 | 对比 Milvus-HNSW 算法 | ann-benchmarks Gist | 0.99 以上 | 30%以上 |
| Milvus KScaNN 优化 | 对比 Milvus-ScaNN 算法 | ann-benchmarks Gist | 0.95 以上 | 30%以上 |

### 贡献声明

欢迎大家为社区做贡献。如果使用过程中有任何问题、建议、特性需求或 bug 报告，请提交：

- [Issues](https://gitcode.com/boostkit/milvus/issues)

贡献流程可参考：

- [BoostKit 社区贡献指南](https://gitcode.com/boostkit/community/blob/master/docs/contributor/contributing.md)

也欢迎在讨论区交流：

- [BoostKit Discussions](https://gitcode.com/boostkit/community/discussions)

### License

本项目的文档适用CC-BY 4.0许可证，具体请参见[LICENSE](https://gitcode.com/boostkit/milvus/tree/master/docs/LICENSE)文件。
