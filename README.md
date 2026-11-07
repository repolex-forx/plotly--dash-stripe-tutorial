# Repolex Knowledge Graph of plotly/dash-stripe-tutorial

RDF knowledge graph data for [plotly/dash-stripe-tutorial](https://github.com/plotly/dash-stripe-tutorial), parsed by [repolex](https://repolex.ai).

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
rlex download plotly/dash-stripe-tutorial
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 172277bbd6095fe2057f62eef40b4d139887bb0b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 172277bbd6095fe2057f62eef40b4d139887bb0b
│           └── chunk-001.nq.gz
├── blob
│   ├── 1005cb305aabfaea98277e107a92a67181d179fb.nq.gz
│   ├── 153f6607ae2e740ca5af63d11b29de2ffbf8f70e.nq.gz
│   ├── 346fb8b951fb7b10f64b825201a8d8ef981562dd.nq.gz
│   ├── 4e2ff3b9e7f26a1bef412dba5b6d3cee8b52325b.nq.gz
│   ├── 83171935e52e623ad398518e2e3a8e9a42fee545.nq.gz
│   ├── b001eb8b53994c03b825bbb760bd5ae70c32107f.nq.gz
│   ├── b15e2344986c44f8a6b75da3d34b8124e6950798.nq.gz
│   ├── b46016672d7df4ca28d97c53e21f4df5bb56851d.nq.gz
│   ├── b4fd97d6d0805c1bc54f566b4d6c4e13ab5e09a0.nq.gz
│   ├── c6779337178ccad80cc6e05b437876bb87e73c68.nq.gz
│   ├── c9a500347a1ffe677bbf4d9f90d10aef2f36900d.nq.gz
│   └── d75af7b066c635c99e150f39fc5b14ecfacd8551.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 172277bbd6095fe2057f62eef40b4d139887bb0b.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 18 files
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

[plotly/dash-stripe-tutorial](https://github.com/plotly/dash-stripe-tutorial)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
