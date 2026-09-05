# Repolex Knowledge Graph of repolex-ai/rlex

RDF knowledge graph data for [repolex-ai/rlex](https://github.com/repolex-ai/rlex), parsed by [repolex](https://repolex.ai).

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
lexq download repolex-ai/rlex
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8.nq.gz
│   └── repolex
│       └── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ec0a90ee20d5c0937bdc49b3d359d228c8da10a.nq.gz
│   ├── 101a3228cf561f499956680130bb2cdc472abbf3.nq.gz
│   ├── 15c3fe711a259fa7a9f18fa0bf64d0e1ca8074fb.nq.gz
│   ├── 2ab8904173e506a4c8e90cdf0db087175f7c76c1.nq.gz
│   ├── 3e43dfb2d091b64424f1ee65aa03c477b322274a.nq.gz
│   ├── 4c5ee0adb56ced430d62250baaa598e5f8ee6ae3.nq.gz
│   ├── 4dccd1e4cde7a406489e37c9e1bb38b4b9fb8a64.nq.gz
│   ├── 5642ccbbce7cf46645bd06e931da00dc51a01c3c.nq.gz
│   ├── 5cf9b7b534b51da425370166cf76ed7beb959ead.nq.gz
│   ├── 765b7e86364aaca8ca8736d1db2bfde9d934c05d.nq.gz
│   ├── 8434ff37e699095961ee840ab56e3b0a2fbf7fee.nq.gz
│   ├── a3f141396b7cfac3d668f67456bebcf49a085dbb.nq.gz
│   ├── a5d53af891302ecbd46fae1ca539ad513df61f42.nq.gz
│   ├── db1f7bea9b314cdbfa79a7675e57725659208362.nq.gz
│   ├── ecbd5bb65a9fab1df60b4522fc1bffa6dcf26bcf.nq.gz
│   ├── ee9530229e0841cd604252685028f7e839632c0b.nq.gz
│   ├── f0ce93aa9a9b96d469ffd6e96f776985603ca094.nq.gz
│   └── f48ce1a4812de7986c8968212790d2f6d49cb1ae.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8.nq.gz
├── filetree
│   └── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8.nq.gz
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

## Source repository

[repolex-ai/rlex](https://github.com/repolex-ai/rlex)

---
*Parsed on 2026-09-05 by [repolex](https://repolex.ai)*
