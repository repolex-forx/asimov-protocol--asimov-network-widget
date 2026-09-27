# Repolex Knowledge Graph of asimov-protocol/asimov-network-widget

RDF knowledge graph data for [asimov-protocol/asimov-network-widget](https://github.com/asimov-protocol/asimov-network-widget), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-protocol/asimov-network-widget
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9c90abd0e9b226f4cd03dac9020d5454701a070d
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9c90abd0e9b226f4cd03dac9020d5454701a070d.nq.gz
│   └── repolex
│       └── 9c90abd0e9b226f4cd03dac9020d5454701a070d
│           └── chunk-001.nq.gz
├── blob
│   ├── 092408a9f09eae19150818b4f0db5d1b70744828.nq.gz
│   ├── 096817513af8c977ec94f514e1951052404881fe.nq.gz
│   ├── 0af58648636cf5e10bb736f52919a7bbce768fe0.nq.gz
│   ├── 11d266966d6a1b9093fff440ea58df328c979591.nq.gz
│   ├── 11f02fe2a0061d6e6e1f271b21da95423b448b32.nq.gz
│   ├── 1ffef600d959ec9e396d5a260bd3f5b927b2cef8.nq.gz
│   ├── 2bd5a0a98a36cc08ada88b804d3be047e6aa5b8a.nq.gz
│   ├── 2bf684d70e442729cad9595b2a6f26bfee560cf8.nq.gz
│   ├── 32d9dfa7f17dd8a4dbe649d9638bd097bed7ec1e.nq.gz
│   ├── 3b875a5594180d8a038fd6d0b377e63c1c550611.nq.gz
│   ├── 415a3fb5f1ef8d46a25f078ea8795807e93a2d1a.nq.gz
│   ├── 5a6eed633e56ef2725cd38cc60e52359011b9f74.nq.gz
│   ├── 77304f5c4a4e8214dfe185670d2e152540477d27.nq.gz
│   ├── 978b02cd40a557837f13c747445664be30b295ee.nq.gz
│   ├── a547bf36d8d11a4f89c59c144f24795749086dd1.nq.gz
│   ├── bef5202a32cbd0632c43de40f6e908532903fd42.nq.gz
│   ├── db0becc8b033a4a78144f4a3bb852082fe91cd62.nq.gz
│   ├── e16b053394ebbee0c42ee8c765cba931244d83d9.nq.gz
│   ├── e7564f71227f44ac1edbb32b28a6e6240b8be3cd.nq.gz
│   ├── ec3d2bd94fdedb3cd35d97a017d4c551f93bbff7.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9c90abd0e9b226f4cd03dac9020d5454701a070d.nq.gz
├── filetree
│   └── 9c90abd0e9b226f4cd03dac9020d5454701a070d.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 30 files
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

[asimov-protocol/asimov-network-widget](https://github.com/asimov-protocol/asimov-network-widget)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
