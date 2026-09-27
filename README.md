# Repolex Knowledge Graph of asimov-modules/.github

RDF knowledge graph data for [asimov-modules/.github](https://github.com/asimov-modules/.github), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/.github
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 574083f728dfe484719fd145b68b3c6de550d637
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 574083f728dfe484719fd145b68b3c6de550d637.nq.gz
│   └── repolex
│       └── 574083f728dfe484719fd145b68b3c6de550d637
│           └── chunk-001.nq.gz
├── blob
│   ├── 2279ceea5329a0b33be20112019aa726177513ec.nq.gz
│   ├── 26b36c1cf26b3333a7ec35d8a5cdce66601dbbc4.nq.gz
│   ├── 2f1fd3e486cca1cb6f7c1b552a46840aa29c5ed0.nq.gz
│   ├── 588f71b3567e8a6d30e531c390512396c0caf513.nq.gz
│   ├── 5ada1ae10000285960d596686188bb5dd2234acc.nq.gz
│   ├── 786caf7933ff493c1d3844e377ae1148750251be.nq.gz
│   ├── 8b0bd234485097945177b6c3cbbb5be6de860e52.nq.gz
│   ├── 98a75f76fd7355b159a03ae3a414883782f84070.nq.gz
│   ├── 9ced600728d2f48cec1724f52162a096c2b2428f.nq.gz
│   ├── bb67c988519445888ae76a7c7c4041de9dee75cf.nq.gz
│   ├── c2fc69c4b0ace56a03d3c5dcb7ac703e1e047ddf.nq.gz
│   ├── cf19849b2a08f0237e2f83c558721aa6605ecf0d.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── f38e5018be2f5622b08cea6dd9b259f6e63c4cf2.nq.gz
│   ├── f87bec9f1ff19b3bd44bd1c0174260a7cdf6d55c.nq.gz
│   └── fe644387ceac8e405951847ef6b05580be6aba08.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 574083f728dfe484719fd145b68b3c6de550d637.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[asimov-modules/.github](https://github.com/asimov-modules/.github)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
