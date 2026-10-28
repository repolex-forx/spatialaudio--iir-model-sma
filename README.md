# Repolex Knowledge Graph of spatialaudio/iir-model-sma

RDF knowledge graph data for [spatialaudio/iir-model-sma](https://github.com/spatialaudio/iir-model-sma), parsed by [repolex](https://repolex.ai).

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
rlex download spatialaudio/iir-model-sma
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fa67a2c35561cfb8ed50eddca6e484ad75ab13db
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fa67a2c35561cfb8ed50eddca6e484ad75ab13db
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e9821298962d834a758b3a636887dfea0e82364.nq.gz
│   ├── 76a79efdcdb4117ac23526378ffc481f51c83659.nq.gz
│   ├── 8f61f2a729122dcdcaec119d7ea86182dce44d97.nq.gz
│   ├── 9e02fe8c9f6714ebffb59b0c084e45911123af75.nq.gz
│   ├── b75c7d2c951d3e34fc54a00dd0d6c101a596452f.nq.gz
│   └── f4c03f28d71b04caad3e2d5d383892485c91d172.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fa67a2c35561cfb8ed50eddca6e484ad75ab13db.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 12 files
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

[spatialaudio/iir-model-sma](https://github.com/spatialaudio/iir-model-sma)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
