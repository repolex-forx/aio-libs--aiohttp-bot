# Repolex Knowledge Graph of aio-libs/aiohttp-bot

RDF knowledge graph data for [aio-libs/aiohttp-bot](https://github.com/aio-libs/aiohttp-bot), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aiohttp-bot
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e5585fcd4f054ab72997b489915e5a56cd43514d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e5585fcd4f054ab72997b489915e5a56cd43514d
│           └── chunk-001.nq.gz
├── blob
│   ├── 5872e2179224d4883bddf5754ba51af513b79284.nq.gz
│   ├── 5a87b784b7e84882cec53acabf279a72f50af1db.nq.gz
│   ├── 7fecee062ef3fa8982b8ece5b8a5ee4865a0f696.nq.gz
│   ├── 8067a60420a93dbb144b7b9069faeedcb64d2f52.nq.gz
│   ├── 8644ef13f11ec3429007cd08b05d736c48476917.nq.gz
│   ├── 8a99520386a597009af2faa0932d7031a74f1f89.nq.gz
│   ├── 8ca9c252446a17594cb0fa1b7135756da7277baf.nq.gz
│   ├── ae6e6e67dd551ec15c96a1972ca0859df2392df7.nq.gz
│   ├── c6af553e2d5bc444eea608e60f68286ccb696a56.nq.gz
│   ├── d0966b45b0fcc87a7953d9758e180c3b5c2a4cc3.nq.gz
│   ├── d6a79cd1af42460950ef08545fd6bcfe05ade54c.nq.gz
│   ├── ef1ebad07f5aad5bb135c6a814234be96546e72a.nq.gz
│   └── f4ace83c8bf235f61ed91900d760f6391673fd5f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e5585fcd4f054ab72997b489915e5a56cd43514d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[aio-libs/aiohttp-bot](https://github.com/aio-libs/aiohttp-bot)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
