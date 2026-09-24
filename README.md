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
│   │   ├── 335ff67fccdf5ca38e88cf42a6260625eda9009f
│   │   │   └── chunk-001.nq.gz
│   │   └── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   ├── 335ff67fccdf5ca38e88cf42a6260625eda9009f.nq.gz
│   │   └── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8.nq.gz
│   └── repolex
│       ├── 335ff67fccdf5ca38e88cf42a6260625eda9009f
│       │   └── chunk-001.nq.gz
│       └── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8
│           └── chunk-001.nq.gz
├── blob
│   ├── 06c50517a8b2ea74a94d3ea4144ac5d3d1e5cae9.nq.gz
│   ├── 0e6f5083353ccef289c910928215696ece0bea83.nq.gz
│   ├── 0ec0a90ee20d5c0937bdc49b3d359d228c8da10a.nq.gz
│   ├── 101a3228cf561f499956680130bb2cdc472abbf3.nq.gz
│   ├── 15c3fe711a259fa7a9f18fa0bf64d0e1ca8074fb.nq.gz
│   ├── 280c65159f9d38565ff2d4419af9513feeadc386.nq.gz
│   ├── 2812c698c356f2c76d61c3644869d2fc024c26c0.nq.gz
│   ├── 2884ca58ef80f11cb5647b697f208fae2b930e1f.nq.gz
│   ├── 2aa1780bc80699de53e43a05adcef43339a86291.nq.gz
│   ├── 2ab8904173e506a4c8e90cdf0db087175f7c76c1.nq.gz
│   ├── 3041a1046aaa9c220cead771a8003bc6552ae592.nq.gz
│   ├── 33ced61d632b493ec1df0a3a34cb6eb71b4d2ec6.nq.gz
│   ├── 392b3f040cca0f31463c6e5342df2b5b793b65fe.nq.gz
│   ├── 3e43dfb2d091b64424f1ee65aa03c477b322274a.nq.gz
│   ├── 427566cf9c78eedef1eeae1d2aa69e53376a736c.nq.gz
│   ├── 47ee34aec3be1878524815597645e4fa1a1d1206.nq.gz
│   ├── 4c1fa4c5dd4bb5892f107a8fe664c012b4df538c.nq.gz
│   ├── 4c5ee0adb56ced430d62250baaa598e5f8ee6ae3.nq.gz
│   ├── 4c6296a055052765329c02dbd1fc90a2ca5d2f4f.nq.gz
│   ├── 4dccd1e4cde7a406489e37c9e1bb38b4b9fb8a64.nq.gz
│   ├── 5642ccbbce7cf46645bd06e931da00dc51a01c3c.nq.gz
│   ├── 5740f2e514b4fdf9f18f7316fbf0bea63d087483.nq.gz
│   ├── 59d1a668630a08f9fdc711df6c98acfaa1bbe03f.nq.gz
│   ├── 5cf9b7b534b51da425370166cf76ed7beb959ead.nq.gz
│   ├── 5da4ff8cbbb18b8c0eab105775d4a5d1dd9e2624.nq.gz
│   ├── 60b399f0d79cc2fa1f257c8e709e7768b225dda3.nq.gz
│   ├── 61067c2e7dd01f2b0c9f2a50cd6502dfecf8c60d.nq.gz
│   ├── 6d12cc0e419a40cd788ef806525ceb07186e853a.nq.gz
│   ├── 705937e76957702f99d83ca40043673543686328.nq.gz
│   ├── 765b7e86364aaca8ca8736d1db2bfde9d934c05d.nq.gz
│   ├── 7e7ca36a1c2bd7d00bbdc5f12c0c2946c17e3323.nq.gz
│   ├── 82a897bc48d39185a9f4983cb41dc28fa211e144.nq.gz
│   ├── 8434ff37e699095961ee840ab56e3b0a2fbf7fee.nq.gz
│   ├── 84bd9d91ab10ad6a16adec5cbd8ab25f8d0df6ee.nq.gz
│   ├── 87ece7e1b14a2ab0db63f0f5ffdc9d8962ba98d7.nq.gz
│   ├── 8c732d723b241bfde7adc80d18b99cd76e4e0c3a.nq.gz
│   ├── 91271292ca8d4c34e8814fb9acba53227ccf1a8e.nq.gz
│   ├── 94f0ed1241cd1d83521b523abda00cb49aa9894b.nq.gz
│   ├── 98da8b4d600fc2d59e8bd27f320ebe927cce5d10.nq.gz
│   ├── 9befd54dd636acf45407d9108e7720e2d99c44f8.nq.gz
│   ├── a1738df7defa7a273d3e673f6096d303754407b6.nq.gz
│   ├── a3f141396b7cfac3d668f67456bebcf49a085dbb.nq.gz
│   ├── a5d53af891302ecbd46fae1ca539ad513df61f42.nq.gz
│   ├── a673088bdf28d7b2e9d575ec755399adfe3fac79.nq.gz
│   ├── a8b5b3f492dd2d7d946737710348e880c76644d4.nq.gz
│   ├── aafb2288cca71b5b00a3fbd635aef9d8840408b1.nq.gz
│   ├── b6fc983927a025847c4ead09190b8f2e30fa67c8.nq.gz
│   ├── b7100e673120c1134f93c414c9c28136797fff42.nq.gz
│   ├── bb1dbce42e016c5efd21583a35b7b24ec8190206.nq.gz
│   ├── c2df30118c807d53b181063962b6672cfe2f484c.nq.gz
│   ├── c33cb049eefaac226eb04943ce4ed5f1f894da5e.nq.gz
│   ├── c46a605f3d8ed45649e8f40fbffb8546f10dfbc0.nq.gz
│   ├── c5f847547a93229c9441dd72fdec003598093344.nq.gz
│   ├── c7746e647a33ebb2f49ba468527b537bdbb2fd3b.nq.gz
│   ├── db1f7bea9b314cdbfa79a7675e57725659208362.nq.gz
│   ├── ebe6db300479c0fd5020466a722531b6be8027b3.nq.gz
│   ├── ec2d77135968130c75b6d530c8068d1cc4f81631.nq.gz
│   ├── ecbd5bb65a9fab1df60b4522fc1bffa6dcf26bcf.nq.gz
│   ├── ed4f200dbc18195085f5a6c1964a594f079ed5c7.nq.gz
│   ├── ee6b256b06360e92bfa985e716ef7d25e8e43e0d.nq.gz
│   ├── ee9530229e0841cd604252685028f7e839632c0b.nq.gz
│   ├── f0ce93aa9a9b96d469ffd6e96f776985603ca094.nq.gz
│   ├── f3f36cb94f44d453fd4cdb26f36386a83948163a.nq.gz
│   ├── f48ce1a4812de7986c8968212790d2f6d49cb1ae.nq.gz
│   ├── f54019515bd1ada6d10cdf84ed63db0a4578d0d8.nq.gz
│   └── fe1319d55047d35633b2df1ce3485eb98ee592ff.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   ├── 335ff67fccdf5ca38e88cf42a6260625eda9009f.nq.gz
│   └── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8.nq.gz
├── filetree
│   ├── 22c79b34c8337c3489ce46249b9010acf23fa040.nq.gz
│   ├── 335ff67fccdf5ca38e88cf42a6260625eda9009f.nq.gz
│   ├── 550a8e5a1a7b121bd970eff3e7575acd158f6bb8.nq.gz
│   ├── 6bcefe8a86f740eaafac4b0a50814d3a4046f1aa.nq.gz
│   ├── 77a6a8c614d88ee0b5e92ddb4fa21407d8cec238.nq.gz
│   ├── aa4df24901ac9e9bbce2ee9b45ee43c2cbaec519.nq.gz
│   ├── ad503ab07efb5c94e9166103ca75f996a2787e72.nq.gz
│   ├── bc7e632fa62bd2f1e3d9c4eeca0211d5b255c120.nq.gz
│   ├── e21b18bc274481417c3a275ad059cd9f6239ad5f.nq.gz
│   └── e93221f106ab2d1ae81ca68cf24954f94299fe56.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

16 directories, 88 files
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
*Parsed on 2026-09-24 by [repolex](https://repolex.ai)*
