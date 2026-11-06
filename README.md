# Repolex Knowledge Graph of carsongee/pytest-pylint

RDF knowledge graph data for [carsongee/pytest-pylint](https://github.com/carsongee/pytest-pylint), parsed by [repolex](https://repolex.ai).

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
rlex download carsongee/pytest-pylint
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 35ffa7124a8775285336d01cd9a6880a094bf66e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 35ffa7124a8775285336d01cd9a6880a094bf66e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0fc0662a61342f649b73020edfe422a95acff599.nq.gz
│   ├── 119d5ff52a5a9ba294f6285c91bdcac1c305b702.nq.gz
│   ├── 1e1c9264cddc970f9fe4a037552716ee9d3c3d8f.nq.gz
│   ├── 1e3dec2dac44bc4784aeb1351450004b0f0d2538.nq.gz
│   ├── 2379f6fa6a8a8f339627c03c1c4f6d90526a2885.nq.gz
│   ├── 2f67e209fbfdeb58dd4ff795fce0ace6c9a436a7.nq.gz
│   ├── 3a2da875fee978b974ace4a10a3f8f24b78186bc.nq.gz
│   ├── 4c87ac336690defb2f2d472b389945c91fae5d31.nq.gz
│   ├── 618d6e8c214347238f21e5216b719b7e992830ff.nq.gz
│   ├── 7bf571d29d9af1c90feff1f78c02479bc592b233.nq.gz
│   ├── 954acda072604656e88386d3cf9852054cee2691.nq.gz
│   ├── 9d0ef656b7d312f1cf4148e338328755f9a20ddb.nq.gz
│   ├── b79016598da43b1e5f0438ecd5eb6d714ff45374.nq.gz
│   ├── c3aff1aed78ca6cd1c565a1813d99c8bb6da0602.nq.gz
│   ├── cdb60f52866862fa35faa9d7b7acc058999b3a71.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f966a5eb3bbff3ed8c8006e753b3b3acbfd3a40e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 35ffa7124a8775285336d01cd9a6880a094bf66e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 25 files
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

[carsongee/pytest-pylint](https://github.com/carsongee/pytest-pylint)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
