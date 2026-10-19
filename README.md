# Repolex Knowledge Graph of sanic-org/sanic-routing

RDF knowledge graph data for [sanic-org/sanic-routing](https://github.com/sanic-org/sanic-routing), parsed by [repolex](https://repolex.ai).

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
rlex download sanic-org/sanic-routing
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7863561c8670a1e990ce2295982e47b93fd3cab1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7863561c8670a1e990ce2295982e47b93fd3cab1
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a2eaebd9ab179ba875a397e1097ab7f3d466e0f.nq.gz
│   ├── 0ba913f24e44fe55a45717946295236867c866a3.nq.gz
│   ├── 17d3e88c949b4df5bf6ba4b85633dcf4ac1b889a.nq.gz
│   ├── 18beeb08ca5d571536583183c700c19201810ba7.nq.gz
│   ├── 2374e0986861739e77d138440f7834729b8a15b9.nq.gz
│   ├── 2e9d6f9e8499892a373f7e49a0bdf0774c6b2972.nq.gz
│   ├── 3baabded116d7489081208c28fdf825c7e23cc79.nq.gz
│   ├── 4eedddb7e6775ff81fb60cb56bff37aa25109abb.nq.gz
│   ├── 60b38728a13d9df9d4b7097bb73096d89acfe8c6.nq.gz
│   ├── 62e9f140d031d464d1bdbbfbbf320a1d03064364.nq.gz
│   ├── 6575a32137a3b4955b62331cabc9b9dcb7941ec3.nq.gz
│   ├── 66c5e034aa2190d44a6346980ced61dd2d31207f.nq.gz
│   ├── 6b3e4e2202606aa3be72192f56a07e4b458da3c4.nq.gz
│   ├── 706de3e20c743f7372336ec51cd185b18eec59fa.nq.gz
│   ├── 7bb576f58ff689c2a88f3c359af57c2421cda4fb.nq.gz
│   ├── 90e73f6989b4a26fc2994f763bc49ff0dbf7aeba.nq.gz
│   ├── 91cac37094c8c27e4c2477db142e961d0f1024bd.nq.gz
│   ├── 95db12d3fc6379a7a5bcd349cc5c7aa914c13b10.nq.gz
│   ├── 9b53acc27973d97ac6f21e25f11b018b0ceb25aa.nq.gz
│   ├── a2cbf971946804e0a1b4b0f99c439e2a0035e764.nq.gz
│   ├── b37d3068bda0bdaf5acb3dc6338e47ba192a4335.nq.gz
│   ├── c1507e7f23f44d0de7beb0d77413f0313339624b.nq.gz
│   ├── c3acb863780134da32a892399b7f24e9feb64a43.nq.gz
│   ├── d00f92ffebdc159aab45649cacc15a5186afbd0a.nq.gz
│   ├── d739e90413bdd3ff5e67ebbaa66ad12110351da9.nq.gz
│   ├── dc04b2b44e0fad093d068722bac8914e2af3778b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eee17d166f0303153d180d90fe0dc99e9675e75f.nq.gz
│   └── f912e2a4808f381979844885e3b981047c437997.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7863561c8670a1e990ce2295982e47b93fd3cab1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[sanic-org/sanic-routing](https://github.com/sanic-org/sanic-routing)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
