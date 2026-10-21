# Repolex Knowledge Graph of twisted/twisted-iocpsupport

RDF knowledge graph data for [twisted/twisted-iocpsupport](https://github.com/twisted/twisted-iocpsupport), parsed by [repolex](https://repolex.ai).

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
rlex download twisted/twisted-iocpsupport
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e4d81ed027e64edf8d591be7966152c9bcfc9005
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e4d81ed027e64edf8d591be7966152c9bcfc9005
│           └── chunk-001.nq.gz
├── blob
│   ├── 07bbfab0d0b53ecbf36e2d66a07b0c9d90c4694f.nq.gz
│   ├── 0ddc13b425e8d968ebafff286c6a5d35113ea53e.nq.gz
│   ├── 0fd21ca3782b6ef5a89283f311940064893b64b4.nq.gz
│   ├── 260cdfd43aab94f7651a7831a5b076d5aa22c058.nq.gz
│   ├── 2fe1b489d9c162ec87ba375a3eb3e277ca60bfeb.nq.gz
│   ├── 31284e7e808dd73940021ae822d9f4d7d57aaff1.nq.gz
│   ├── 3f544bf7f039edf28a0e86b3cff6405584af6b23.nq.gz
│   ├── 4379c5bf0c555ed33c439c44b5cad1ea4a8a9e84.nq.gz
│   ├── 5b334ad617ab7f79735b942fc85a230e1f014551.nq.gz
│   ├── 6761c5b04c536fa2a4becaf98b7b5899fa11a93e.nq.gz
│   ├── 7301756ce7bb14991357cded481db028eea730e4.nq.gz
│   ├── 77d5b176461226bd4f8d540ab4ab3a9417c3cea5.nq.gz
│   ├── 900b11aca75c6c8a81d51440b9a1ec9f0bdf0c2b.nq.gz
│   ├── 93557709fccda214d4250e464be3b521ba5dc2ea.nq.gz
│   ├── 99f9418cb9bf1eb926e652f21ca08de8c71f5ff9.nq.gz
│   ├── b668bd8f5cb165689501178ae83fb69c0e356079.nq.gz
│   ├── cc9601c7a739fbdc0d48e285049e6d9fcc31ae89.nq.gz
│   ├── da74d4e0998eed47edca832131d193ee9fa4d66a.nq.gz
│   ├── dc45aed2f07134423d5863cf5c23f7c7d5d2a6e3.nq.gz
│   ├── e5acea1546c50368db157bd1c25182e42e7f3916.nq.gz
│   └── f3811313cd5272db2e1eb74d1d735005c6032d26.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e4d81ed027e64edf8d591be7966152c9bcfc9005.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 28 files
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

[twisted/twisted-iocpsupport](https://github.com/twisted/twisted-iocpsupport)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
