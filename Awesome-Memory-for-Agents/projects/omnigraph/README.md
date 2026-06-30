# Omnigraph

**收录日期:** 2026-04

**GitHub:** [https://github.com/ModernRelay/omnigraph](https://github.com/ModernRelay/omnigraph)

## 简述

Typed graph database where agents branch and merge like Git. S3-native, Rust, traversal + vector + BM25 in one runtime.

## GitHub README 摘要

> Omnigraph is the operational state and coordination layer for fleets of agents.\

## README 摘录（GitHub）

```markdown
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/omnigraph-wordmark-dark.svg">
    <img alt="OMNIGRAPH" src="assets/omnigraph-wordmark.svg" width="420">
  </picture>
</p>

<p align="center">
  <strong>Lakehouse graph database for context assembly &amp; multi-agent coordination</strong><br>
  <sub>Multimodal retrieval · Git-style branching · object-storage native</sub>
</p>

<p align="center">
  <a href="docs/user/quickstart.md">Quickstart</a> &nbsp;·&nbsp;
  <a href="docs/user/clusters/index.md">Docs</a> &nbsp;·&nbsp;
  <a href="https://github.com/ModernRelay/omnigraph-cookbooks">Cookbooks</a> &nbsp;·&nbsp;
  <a href="docs/user/cli/reference.md">CLI</a>
</p>

<p align="center">
  <a href="LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-1b1b1f?style=flat-square&labelColor=1b1b1f"></a>
  <a href="https://crates.io/crates/omnigraph-cli"><img alt="crates.io" src="https://img.shields.io/crates/v/omnigraph-cli?style=flat-square&color=d71921&labelColor=1b1b1f"></a>
  <a href="rust-toolchain.toml"><img alt="Rust" src="https://img.shields.io/badge/rust-stable-1b1b1f?style=flat-square&labelColor=1b1b1f"></a>
</p>

<hr>

Omnigraph is the operational state and coordination layer for fleets of agents.\
Run it as a server, declared as code; hundreds of agents operate and enrich the graph on parallel isolated branches, and every change is reviewed and merged safely.

## Key capabilities

| Capability | What it gives you |
|---|---|
| **Declared as code** | A `cluster.yaml` declares graphs, schemas, stored queries, embedding providers, and policies; `cluster apply` converges it and `omnigraph-server` brings every graph online at `/graphs/{id}/…`. |
| **Built for fleets of agents** | Hundreds of agents enrich the graph on **parallel isolated branches**; changes are reviewed and merged safely, Git-style, across the whole graph. |
| **Multimodal retrieval** | Graph traversal + vector ANN + full-text + Reciprocal Rank Fusion in **one** query runtime, for context assembly. |
| **Security as code** | Cedar policy enforced **server-side on every mutation**, per-graph and server-wide; bearer auth; actor/audit tracking. |
| **Runs on your infrastructure** | Any S3-compatible object store: **on-prem via RustFS / MinIO**, or AWS S3 / R2 / GCS. VPC, on-prem, hybrid; your data never leaves your store. |
| **Open, versioned storage** | [`Lance`](https://github.com/lance-format/lance) columnar format: branchable, time-travelable, with native blob-as-data (docs, images, video). |

## What you can build

| Use case | What it's for |
|---|---|
| **Company brain** | Org knowledge unified into one graph every agent can query |
| **Agentic memory** | Durable, versioned memory: a branch per agent or per task, merged on review |
| **Context graph** | Decision traces and codified tribal knowledge for retrieval |
| **Dev graph** | Issues & dependency model that coding agents read and write |
| **R&D / ML data layer** | Experiments and trials written into branches, versioned for training & eval |

## Install

```bash
curl -fsSL https://raw.githubusercontent.com/ModernRelay/omnigraph/main/scripts/install.sh | bash
```

This installs `omnigraph` (CLI) and `omnigraph-server` into `~/.local/bin` from
published release binaries. Or with Homebrew:

```bash
brew tap ModernRelay/tap
brew install ModernRelay/tap/omnigraph
```

## Set it up with an AI agent

Omnigraph is built to be run by coding agents. Two ways in:

**Teach your agent the playbook.** This repo ships the
[**`omnigraph` agent skill**](skills/omnigraph): the operational playbook
covering cluster mode, the two config surfaces, schema evolution, query linting,
data writes, branches, Cedar policy, and the common gotchas.

```bash
npx skills add ModernRelay/omnigraph@omnigraph
```

**Or have an agent set it up from scratch.** Paste this into Claude Code,
Codex, or any agent that can read a URL and run a shell command:

```text
Help me set up Omnigraph

1. Read the docs at https://github.com/ModernRelay/omnigraph, starting with
   docs/user/clusters/index.md, then docs/user/deployment.md.
2. Skim the starter graphs and seed data in the cookbooks:
   https://github.com/ModernRelay/omnigraph-cookbooks
3. Ask me what I want to build (company brain, agent memory, dev graph,
   research / R&D layer, …). Then stand up a cluster for it, load a little
   data, and run a query so I can see it working.
```

For ready-to-run graphs with real seed data (company brain, VC operating system,
pharma & industry intel),
[`ModernRelay/omnigraph-cookbooks`](https://github.com/ModernRelay/omnigraph-cookbooks)
is the fastest way to see Omnigraph shaped to a real domain.

## Deploy

A deployment is a **cluster**: a **multigraph** config directory that declares
its graphs, schemas, stored queries, and policies as code. You manage it
**Terraform-style**: `cluster plan` previews the diff, `cluster apply` converges
it. `omnigraph-server` then boots from the cluster and brings every graph online
at `/graphs/{id}/…`, each behind its own policy.

**1. Declare the cluster.**

```
company-brain/
├── cluster.yaml
├── people.pg          # schema for the "knowledge" graph
├── queries/           # stored queries: the .gq files ARE the declaration
│   └── people.gq
└── base.policy.yaml   # a Cedar policy bundle
```

```yaml
# cluster.yaml
version: 1
metadata:
  name: company-brain
storage: s3://company/clusters/company-brain   # ledger, catalog, and graph data live here
graphs:
  knowledge:
    schema: people.pg
    queries: queries/                          # every `query <name>` in queries/*.gq registers
policies:
  base:
    file: base.policy.yaml
    applies_to: [knowledge]                    # graph-bound; use [cluster] for server-level
```

**2. Stand up your object store.** On-prem, run RustFS (or MinIO); Omnigraph
writes [Lance](https://github.com/lance-format/lance) to it over the standard S3
API. In the cloud, point the same `AW

... (更多内容请访问上面 GitHub 链接)
```

