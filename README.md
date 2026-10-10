# Repolex Knowledge Graph of jazzband/django-voting

RDF knowledge graph data for [jazzband/django-voting](https://github.com/jazzband/django-voting), parsed by [repolex](https://repolex.ai).

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
rlex download jazzband/django-voting
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5721fb664760d22ae49affb39255f6e3e186160b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5721fb664760d22ae49affb39255f6e3e186160b
│           └── chunk-001.nq.gz
├── blob
│   ├── 05f6c8c2e0c4178c193018fe1d21abcb401baf4c.nq.gz
│   ├── 140742ddbe248a7a9f643371a627e1f9d394080a.nq.gz
│   ├── 217b9f7d7d0d9bd94357d4f05646c8b697e91393.nq.gz
│   ├── 469d35ef219a8a7202e03a2d0adfd5facb34c034.nq.gz
│   ├── 5ef2e5c2eedd0fb3ba87c64f6c5ee159cea58d39.nq.gz
│   ├── 61c8a812766b3de900a4f59623c7a52f2cd08180.nq.gz
│   ├── 6d08b2c6a3bf8f7594de6ba34df7f2a99b45aff2.nq.gz
│   ├── 7be282aa34cef2fdb4f8df3cc4e8fb23ea82d7ee.nq.gz
│   ├── 7ca5fa1cc60cd0d18737b5e2db4440dad7be1898.nq.gz
│   ├── 87686f9f3f9779fde98f214f0dcf1ff42dff5618.nq.gz
│   ├── 8e34d026dc39ca8afa3f573a35b84e74b07ae57c.nq.gz
│   ├── 95f8998ede2048e81f97ee40ff84db41fc49369f.nq.gz
│   ├── 9c1cde8deb598c3bf3163fecfdeebf7925c090a9.nq.gz
│   ├── 9c1cea87faf10ed74ded0346a720fa835b338c54.nq.gz
│   ├── a0bb5d1abca241bc51ec2dda75c8d2b8fc648c0a.nq.gz
│   ├── a4949797d9588e7a85586507c2788e75a28609f5.nq.gz
│   ├── a559b601de79d3d68a6717cf4a7e20da3e321865.nq.gz
│   ├── b233f3339db9c0adebcd414f38b8e9c4390736f1.nq.gz
│   ├── b46c0f4aa35827e00b45209edb7825467f4bdf6e.nq.gz
│   ├── b92709493543e57e6333f764fb8ebe3a74cf8ba9.nq.gz
│   ├── d55a81acc77042ebf3806de62219be882b77f4a2.nq.gz
│   ├── e0d5efab56fb94577e7804603eb6f21f36977cb2.nq.gz
│   ├── e41820b5dc14bf00221d0efb3a4ec8a74667d33c.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ebaccd7e5e4cdac9a771288af539ad164e2902fe.nq.gz
│   ├── f10b71eac0f27145526ceef782e99557706d728c.nq.gz
│   ├── f1cb377960b0067987db510603aaf5da6a853e3d.nq.gz
│   ├── f2e2f64f7e86273114a794a8d57af22c3a51416c.nq.gz
│   └── fdf965f9e9285fdf7580adccc1591ec60782eb79.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5721fb664760d22ae49affb39255f6e3e186160b.nq.gz
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

[jazzband/django-voting](https://github.com/jazzband/django-voting)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
