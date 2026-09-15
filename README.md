# Repolex Knowledge Graph of eslint/doctrine

RDF knowledge graph data for [eslint/doctrine](https://github.com/eslint/doctrine), parsed by [repolex](https://repolex.ai).

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
lexq download eslint/doctrine
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   ├── 42434ca1f85b264a88afcfd317487a7417e6004b
│   │   │   └── chunk-001.nq.gz
│   │   └── aaa37294df8b6d85c39acdae12f2a4a974d50459
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   ├── 42434ca1f85b264a88afcfd317487a7417e6004b.nq.gz
│   │   └── aaa37294df8b6d85c39acdae12f2a4a974d50459.nq.gz
│   └── repolex
│       └── aaa37294df8b6d85c39acdae12f2a4a974d50459
│           └── chunk-001.nq.gz
├── blob
│   ├── 01e7414b58d916c442437be525fdf156c32665e2.nq.gz
│   ├── 0882624b301e7cf689c7588e251ca577c1dc72a3.nq.gz
│   ├── 0a4316f19bc0a1d3f348015ecf01756264850b9b.nq.gz
│   ├── 1ddfbcb28e99fa2a63cddc969a27b3d2c216d59c.nq.gz
│   ├── 224efd6281f3770ca1479072559d132ed31b7ec8.nq.gz
│   ├── 26fad18b90d5c8b39864af4e7fd7e54958cd51fe.nq.gz
│   ├── 2e62126f25a14e25a49d8e9aba2fb4100638d3f5.nq.gz
│   ├── 381580ebe2534af83524e88d64e1536fddfd38df.nq.gz
│   ├── 3e580c355a96e5ab8c4fb2ea4ada2d62287de41f.nq.gz
│   ├── 3e8ba72f69be5744b50a6347ec62253112c066b8.nq.gz
│   ├── 3ecc7bcde648da452c88b26983fd4da8621c08fe.nq.gz
│   ├── 44f5a8454316612b6434363903a47fe6463df67a.nq.gz
│   ├── 4d2824f1178897120c1fe2327218b3f46ba5673f.nq.gz
│   ├── 51886dba722905fd8873e403d5cd287c59dd142f.nq.gz
│   ├── 5246000d665f2d38fbcbeb9424e6b26fdef33fb6.nq.gz
│   ├── 57aa9bbccf0a3944b7a1be90d3a1f45dfb09474c.nq.gz
│   ├── 6141026e3f41d727f6e34b81aa3bf98e4b84af55.nq.gz
│   ├── 6e0978475e0fdb2f52e5743b7298af42419c095d.nq.gz
│   ├── 87dde2072b3cb9ab02e233d88152aaaec686b7b8.nq.gz
│   ├── 89683cd30f259a8d85cfc0a0e1e43d728e7dbca8.nq.gz
│   ├── b66099863d4479922f0bdfdadab851a05cd456bd.nq.gz
│   ├── bbccba9a05f1e37310591fbc8906631533c44050.nq.gz
│   ├── bdaa0e07882276bd9231869f420b730dee9122fb.nq.gz
│   ├── bdd3c394fc7d1fb57c3beb38f9655fe327c4db0f.nq.gz
│   ├── c1ca392feaa48b046ffc56d4feed1887af232461.nq.gz
│   ├── d246e33f32b4f9b63899a2624d96dd9f605369da.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── dcfe776c4694c36cf527f4c5e950cb50c2c5b0f2.nq.gz
│   ├── e2cc3fb3b5fb92d90fc351fa062c9e084d236d6c.nq.gz
│   ├── e5b14f7749c177c10fe6ff3da5882484e315a915.nq.gz
│   ├── e74389fa247a1288ec96e46898902f41e08713f8.nq.gz
│   ├── f3a9530bd33bfc2f0140e283001d740dd5acaf41.nq.gz
│   └── fe5b0e2d06c0afe2c33d393fbe16ea271d99daea.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   ├── 42434ca1f85b264a88afcfd317487a7417e6004b.nq.gz
│   └── aaa37294df8b6d85c39acdae12f2a4a974d50459.nq.gz
├── filetree
│   ├── 42434ca1f85b264a88afcfd317487a7417e6004b.nq.gz
│   └── aaa37294df8b6d85c39acdae12f2a4a974d50459.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

16 directories, 47 files
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

[eslint/doctrine](https://github.com/eslint/doctrine)

---
*Parsed on 2026-09-15 by [repolex](https://repolex.ai)*
