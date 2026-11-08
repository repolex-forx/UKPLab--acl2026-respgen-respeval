# Repolex Knowledge Graph of UKPLab/acl2026-respgen-respeval

RDF knowledge graph data for [UKPLab/acl2026-respgen-respeval](https://github.com/UKPLab/acl2026-respgen-respeval), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download UKPLab/acl2026-respgen-respeval
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0e1a3cbc290939e4f6a2a12bd9bda3fa7806cb22
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0e1a3cbc290939e4f6a2a12bd9bda3fa7806cb22
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b5bc48d8208206e4d31738ba47dd6e42d76e55e.nq.gz
│   ├── 0c4e423eb2f025c92b94c7c6284bc3806d49aec3.nq.gz
│   ├── 11d9b7047b177eada389713d81be493bc1e0c000.nq.gz
│   ├── 129771a2f4a5928c6c8ba7fce4216a197f36c146.nq.gz
│   ├── 20a73d623be5cb8c0ca6b42fd9428ba14fd69e95.nq.gz
│   ├── 232343f704c35f555306569d90c5ead96cb877e0.nq.gz
│   ├── 24cc3594592a02d1248561af22681bf7affd9e0f.nq.gz
│   ├── 2b00dde176dee270e9359e490c618fa072be4106.nq.gz
│   ├── 2b9b40a366a00ec4c7bf1a8cf701564a401d3c56.nq.gz
│   ├── 36ea1098a1145b29709424c58e395d68e6f02cf5.nq.gz
│   ├── 5a0733f95f7649a5c233356f295c789675ebfe08.nq.gz
│   ├── 5b46217742d7742fc78d010580615169bba8fd87.nq.gz
│   ├── 5b961e97f9bf551a86f13d5945e8875243fedc5c.nq.gz
│   ├── 5dcef726f671e400c7a0873dc8e9d9f061889630.nq.gz
│   ├── 6036069e0299f816e03c191a47cddafb580415d0.nq.gz
│   ├── 6670e65b5bc66f893f92bf77c44c5605372b14c1.nq.gz
│   ├── 6f25f37ac2de28e132acd19cb2412c5e856d6fa1.nq.gz
│   ├── 6f87c92cad11fef7e80b1d5afa293bdc02c75eea.nq.gz
│   ├── 74626da220adf7ca427f1c5c965ec48273416c32.nq.gz
│   ├── 88e5d038040c13907795e61580b3d27db05d1df1.nq.gz
│   ├── 8cd91c703e15485cab6b30fe94f61b26329e6160.nq.gz
│   ├── 946177cfd7d8637d851089ca200e0dcedc87a68e.nq.gz
│   ├── 9508b7a58edd2ba49bb37ba4e86450769ec2cd04.nq.gz
│   ├── 995e49ceb875769cec226b0bd307987103b85629.nq.gz
│   ├── 9abc65af31836e09c4e3f91bb27b05073b67c40e.nq.gz
│   ├── a10e306a46a3fa3596f66574df29d7fba6b28e8f.nq.gz
│   ├── a7526d241fdd7a0934a198791f9328d7e5c7735b.nq.gz
│   ├── b198a0754fe42d5bd3b20867fe9e29d15566826f.nq.gz
│   ├── cd565149d4b5fcca3cb088e4ace9f760e12df06f.nq.gz
│   ├── cd6a089c57dff5cf2a284a2540ad90e686564c5f.nq.gz
│   ├── d138be33003f5fa1910e61c9de37305bd8633269.nq.gz
│   ├── d23e5bbb9c1681774be4d8e998741a549981551a.nq.gz
│   ├── d81bbe06b67fe3a164037c18dc1493e30d3e9408.nq.gz
│   ├── d86d6ff86f83387f71f2605266d88a8097cf3af5.nq.gz
│   ├── d9eeb91bbff1e83f3d189c70bd702193c0ceb335.nq.gz
│   ├── dae29471184e2150d719ee0abbbd97b21bd58e5d.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e85256d777462adaecdff0cfd2e8564f4722bdf5.nq.gz
│   └── f556dfba3974a7a41229b1e0e0c58d87c056eca2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0e1a3cbc290939e4f6a2a12bd9bda3fa7806cb22.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[UKPLab/acl2026-respgen-respeval](https://github.com/UKPLab/acl2026-respgen-respeval)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
