# Repolex Knowledge Graph of graphql-python/graphene-pydantic

RDF knowledge graph data for [graphql-python/graphene-pydantic](https://github.com/graphql-python/graphene-pydantic), parsed by [repolex](https://repolex.ai).

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
rlex download graphql-python/graphene-pydantic
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2bc1b037db9dfc95b5140add14de6033ec60ca1a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2bc1b037db9dfc95b5140add14de6033ec60ca1a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0021c05992d5823bc1ec3bdbd96c71fe984279b0.nq.gz
│   ├── 078e16e66a39a694b430bf28bb9ef33698ed5d4a.nq.gz
│   ├── 17d0561f5674549f2f1d2bd5046733de6be4fdf2.nq.gz
│   ├── 1e3297c6f8ea13e9b0a5d5b321385c14416754c7.nq.gz
│   ├── 2738ad3779a94c78a21ea2b932c09fd2bb9d157b.nq.gz
│   ├── 2d696ab3d95afb976ced0c3ae0361a61f46679cb.nq.gz
│   ├── 362f2a28f1d881a1aa7685a0e0b9fba7652bc314.nq.gz
│   ├── 3c9e3226bc571cc61a5fd6a5893982696fd5fee5.nq.gz
│   ├── 47effbee70d55f9adb6fc446c84c7b65b8fffce5.nq.gz
│   ├── 4b5fd2938981fcde760ae848258752e1ff152b96.nq.gz
│   ├── 535106d8dd3af7d3f226202a40050e4045c91fcf.nq.gz
│   ├── 6c18450e0cbff4a832f1f6caf4bd8af9d1df6705.nq.gz
│   ├── 72269d4b2cf3f54d3f8511ce9a21225c4fb8f616.nq.gz
│   ├── 740af088d93bae33958f0891c174ea00f029327f.nq.gz
│   ├── 8021922ffae5fd8da532c601d3202b1c93dabe35.nq.gz
│   ├── 8b94a83b8c383a2a689b0726ac3dea1324067d29.nq.gz
│   ├── 8dfa3824c01c0ef782723ef8c50e3507416bb57b.nq.gz
│   ├── 8ef56510f491e1f7b3441cbc2087a7057a376675.nq.gz
│   ├── 91f6bbd513847e968ef38092204d235bfe27f073.nq.gz
│   ├── 95f444de8354cb5010f944f063c15c085aa1e895.nq.gz
│   ├── abb1b006b606a26d5500d4c29c1dc7fe1afc4cda.nq.gz
│   ├── ae45efdd9f165a2cefb68712670cc4f43cce18f6.nq.gz
│   ├── b8c875f2a95b7e7803a57560d5c7280ec1f71be9.nq.gz
│   ├── c9f278d1a0f52c110a1336ca94267fd29bdb7b2e.nq.gz
│   ├── d1123e8e335317d8768344b190f7a3b3f3a0bbc6.nq.gz
│   ├── d5c499e930117f4d19ff0df1f9ec4d1f78466764.nq.gz
│   ├── de78be1608917a167923a2c79e766a867b245a2b.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2bc1b037db9dfc95b5140add14de6033ec60ca1a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[graphql-python/graphene-pydantic](https://github.com/graphql-python/graphene-pydantic)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
