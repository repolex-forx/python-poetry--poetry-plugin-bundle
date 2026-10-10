# Repolex Knowledge Graph of python-poetry/poetry-plugin-bundle

RDF knowledge graph data for [python-poetry/poetry-plugin-bundle](https://github.com/python-poetry/poetry-plugin-bundle), parsed by [repolex](https://repolex.ai).

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
rlex download python-poetry/poetry-plugin-bundle
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 188ee040b6b260e329fd1b59b88252c4c96c92d0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 188ee040b6b260e329fd1b59b88252c4c96c92d0
│           └── chunk-001.nq.gz
├── blob
│   ├── 039340ef7a327e37fc8af3fc2b2b73e41974dbac.nq.gz
│   ├── 04ccd4f14dc4d67010833df19b00eef1813fe5a2.nq.gz
│   ├── 0b3e53db96ef08447a3c6b063bb058127b3eaa51.nq.gz
│   ├── 0e811aa6863134bf609741c3112867b1b619e2bc.nq.gz
│   ├── 0ee69aeb76b07f9195e6dd36e79730cafbd35da0.nq.gz
│   ├── 14a7a38bec1d2d252c5e2bf93cda35d5cd9cda20.nq.gz
│   ├── 2328493807cab7256cf381e4de9bc1a2ca86ae64.nq.gz
│   ├── 2f84d8d2610cdb8cbf7173e49437f788b985851b.nq.gz
│   ├── 31ea28d98868e4ce4879aff64eedc16ba1f19db6.nq.gz
│   ├── 353afe7ef61e536b5955dbe9e8d1cfd65c0cfa51.nq.gz
│   ├── 37ca710a7559ccb97ca6a548b44f504fa83ac7e5.nq.gz
│   ├── 3936d4aae245759583539112d984fa3db21d859f.nq.gz
│   ├── 39b83c5084faa3f1205638b829b27880eb3fe2a1.nq.gz
│   ├── 49aba2ef0b7ae35aa32c1f31618143027d43dafb.nq.gz
│   ├── 4a0a992d89ce719a191966db3087081c64e57426.nq.gz
│   ├── 5e5e021f22955cc3ba6c694d9d66d539d57de67a.nq.gz
│   ├── 5ee074839e04865d189ee5f63a9fe755685b738c.nq.gz
│   ├── 634d88ffbf32a8432a83529afcb75ad3f6fec45b.nq.gz
│   ├── 6a3929a13d4b6039b5610e54c3967262a77243ed.nq.gz
│   ├── 70eaf9967459c134f0044853d0700eae0ce80567.nq.gz
│   ├── 7ab5da9a50084348fc9d51b518e4311e416f5163.nq.gz
│   ├── 7ce319e2c7a7c05e7ab2746d0ab6a502da87fb9c.nq.gz
│   ├── 7f4d2bd104d74846cb5110acb7d87f046faf1954.nq.gz
│   ├── 81ae92eecf2ce262ae2337eb42993fd944fe28f2.nq.gz
│   ├── 85376614cb4f599eada132dfaf671f3f2c01471c.nq.gz
│   ├── 9231b902ccfa6fc11706a5c67c3eafe337c48ea7.nq.gz
│   ├── 979323b5599285be670fa1e7c6407caddd0568a6.nq.gz
│   ├── a19e58577bf85afdc13aebcaa736afa76597350f.nq.gz
│   ├── a5d6dd5059105743d60d5a32ba3fdf8705c87b85.nq.gz
│   ├── af4bce30161082044baa5aa3d10fef235432a05f.nq.gz
│   ├── bd2b67e14068caa9e185a03c31e05391c10ea59c.nq.gz
│   ├── d51fae894c478b5bb6684686279457aeef9d57bb.nq.gz
│   ├── da7a69b5eb71604b64efd42b748b2f94b6cfea82.nq.gz
│   ├── e5e3ff06c29bb0877ed3891c5d5c0af9f6b30e48.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f45e7fa8d70b36f21148d1e343069fd8b6310d06.nq.gz
│   ├── f7fe15470f932e8589b3711d7456e282f7c92a6a.nq.gz
│   └── fb788873c639240ae105d99949f8d4a4c14b5f20.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 188ee040b6b260e329fd1b59b88252c4c96c92d0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[python-poetry/poetry-plugin-bundle](https://github.com/python-poetry/poetry-plugin-bundle)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
