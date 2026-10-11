# Repolex Knowledge Graph of pytest-dev/pytest-describe

RDF knowledge graph data for [pytest-dev/pytest-describe](https://github.com/pytest-dev/pytest-describe), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-describe
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f609497f3a10062baf773fed89cd0a414b1213a0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f609497f3a10062baf773fed89cd0a414b1213a0
│           └── chunk-001.nq.gz
├── blob
│   ├── 0613a478a24ff7dce196ff275fe8f3e4181d79ba.nq.gz
│   ├── 108fad79449b9169d93bde0fb8ff9382fa9a4c0e.nq.gz
│   ├── 1611e2462ca9dec3804b9a6eed90ce56babf7ed5.nq.gz
│   ├── 1f68fa51f57fc216849cffc1b01652fddfad4b21.nq.gz
│   ├── 3757f0bb9d93be24656c697d53d63f75bb471847.nq.gz
│   ├── 3bd3bbb2549446e678611a111bd511bbf8e63637.nq.gz
│   ├── 3cb4121281dc2d1f5c4faf2287cd17a270350758.nq.gz
│   ├── 4baebd529cfbb5bdea802f490eb6a1a2eb437280.nq.gz
│   ├── 6eb39b14604e8cc0623948e165c6899a36c1aea8.nq.gz
│   ├── 6f26b246fffd8f15f6e6fca8ff4d641b73c57e49.nq.gz
│   ├── 77ec4c7f8046fb3f916cb33996a37cef910dc952.nq.gz
│   ├── 7afab954b8b2dddaccc8ac732794e61099d5a861.nq.gz
│   ├── 94e1b55c96d3d84a816ae39b0dda05d76b11a0fd.nq.gz
│   ├── 9b99f7ed52aa607147c36642960492da101de255.nq.gz
│   ├── 9c502e8aa9ada26dae2f46480872aa2082259d99.nq.gz
│   ├── af6963d1a8260aa56b0872cf7ceac88f4d4400f9.nq.gz
│   ├── d5c35e0a76dd70dcd62f7513053c2522f0ad4d36.nq.gz
│   ├── df7d748d1dcfc7ee7be30fe0ee843ba2e91b480b.nq.gz
│   ├── e527aa193387ef9d5f5ef3c3c02824b066cb2214.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ee88efd6ff647158d27c5f0ed5f2121da46c1614.nq.gz
│   ├── f5ff62a752be0805bb1c5f5cb300479fa7ba7940.nq.gz
│   └── f7067d64042f852e9b164c3f200a63858a09a16b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f609497f3a10062baf773fed89cd0a414b1213a0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[pytest-dev/pytest-describe](https://github.com/pytest-dev/pytest-describe)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
