# Repolex Knowledge Graph of modelcontextprotocol/agents-wg

RDF knowledge graph data for [modelcontextprotocol/agents-wg](https://github.com/modelcontextprotocol/agents-wg), parsed by [repolex](https://repolex.ai).

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
rlex download modelcontextprotocol/agents-wg
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a7be70f1f5806949e2196bc0a9c2771f6a135a4d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a7be70f1f5806949e2196bc0a9c2771f6a135a4d
│           └── chunk-001.nq.gz
├── blob
│   ├── 004bf4a765d904735c5480d5143fb1d6ac3afc72.nq.gz
│   ├── 04bb47b80bc1cca5167cbe4c5c7ce4330ba50c75.nq.gz
│   ├── 0d015334620c80ee579fa6d4c8eb98509b6aa9dd.nq.gz
│   ├── 17538acfe630489a99ef8ae48080d01e8b55f430.nq.gz
│   ├── 17a035b7493cbcf19984a99bc971dbe8c6a34807.nq.gz
│   ├── 25792a662cfee44f8d1d32cddcf32ce2e1d84753.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2af2e708956b21510085104d9dd046c51d1b318e.nq.gz
│   ├── 2d450aa2d3ecb952b56fac011ea56b43778fb15f.nq.gz
│   ├── 2ff1239f5ab6b56b22ef38587728fdf7e891fb81.nq.gz
│   ├── 334cc648005c010e7ad62b47e47d39bad64261eb.nq.gz
│   ├── 355b75a2c6391e08316d2b5f988f48a7cc91a401.nq.gz
│   ├── 3c05d43dfded35a1d2a0d75f3e1a948a4d0fef80.nq.gz
│   ├── 496ee2ca6a2f08396a4076fe43dedf3dc0da8b6d.nq.gz
│   ├── 4bb5d226f719f58c995eb1b8f91353dd3e8b9477.nq.gz
│   ├── 4cb48e36c7a7f55c399faeb3e4440a090cae3a8b.nq.gz
│   ├── 4d126dbb4402b3a3b47221b6c181f8cf341655bf.nq.gz
│   ├── 536168c22de59e1a2a5d2b96fdc72853d70b9471.nq.gz
│   ├── 62bd93283908d4a21b8aafc7c47e689f3731d294.nq.gz
│   ├── 67090383d36f641ffa0911af521e903ac6082f8d.nq.gz
│   ├── 6ee9a2e04bb7270a98410729d6ab238b33bd2d71.nq.gz
│   ├── 848731c7bd88abe3201e61cf5c7ae14c383a5562.nq.gz
│   ├── 9a1a711876992e56f3fd0437a768a8318d6d0366.nq.gz
│   ├── 9d8287a004df826eda3610d9927d66d3ea8f523e.nq.gz
│   ├── 9de1efe8243b33c54db4aa096c2bcc895c686624.nq.gz
│   ├── a61c8fe340441e0796044ab7f044e59384f8f39a.nq.gz
│   ├── ac276ae2196c8be350d08d732e8449bc0ace55f8.nq.gz
│   ├── c8b3984d4052c955820671e953004bb749e3aa4c.nq.gz
│   ├── cfb117b953ecaa12cdb4b6c9e6e591aae23ec075.nq.gz
│   ├── d3f5e9a37646d5a758ffb7b6af056e67e8e45e64.nq.gz
│   ├── d95fb00846f3655de88c1f30f9c15a4aa4818a81.nq.gz
│   └── f490ee8fc7153fb38c4e5c0e8493b7cc89636235.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a7be70f1f5806949e2196bc0a9c2771f6a135a4d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[modelcontextprotocol/agents-wg](https://github.com/modelcontextprotocol/agents-wg)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
