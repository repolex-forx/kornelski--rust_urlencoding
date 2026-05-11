# Repolex Knowledge Graph of kornelski/rust_urlencoding

RDF knowledge graph data for [kornelski/rust_urlencoding](https://github.com/kornelski/rust_urlencoding), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download kornelski/rust_urlencoding
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b987b1a1e98e2d4190b6e2a07262a680120c422c
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── b987b1a1e98e2d4190b6e2a07262a680120c422c.nq.gz
│   └── repolex
│       └── b987b1a1e98e2d4190b6e2a07262a680120c422c
│           └── chunk-001.nq.gz
├── blob
│   ├── 1f2e560fdef54460894129c89382da7b61ee5481.nq.gz
│   ├── 291937fb0de795fada6f513a74fd622ed6ed0b85.nq.gz
│   ├── 3134060f6dce881a79133213c358758ab722ebd5.nq.gz
│   ├── 52dd055263f9c6d3a1d812df3db118cecec8ef1f.nq.gz
│   ├── a9d37c560c6ab8d4afbf47eda643e8c42e857716.nq.gz
│   ├── aa44542e3b3dd1ec07314f2becb386716f713ae1.nq.gz
│   ├── b6dc18c4b17e1dc6f7f7cf5b95ef9d89958992e8.nq.gz
│   └── ccf95bbad7454fc2f42cc47d5af92ceac7bc8d9d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b987b1a1e98e2d4190b6e2a07262a680120c422c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 17 files
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

## Source repository

[kornelski/rust_urlencoding](https://github.com/kornelski/rust_urlencoding)

---
*Parsed on 2026-05-11 by [repolex](https://repolex.ai)*
