<h1 align="center">Ryu</h1>

<p align="center">
  <strong>Software Engineer · Systems Architect</strong><br>
  Systems · Networks · Scale · Reliability · Security · Observability
</p>

<p align="center">
  <a href="https://github.com/ryux1/mcp-trace"><strong>MCP Trace</strong></a>
  ·
  <a href="#open-source"><strong>Open Source</strong></a>
  ·
  <a href="#engineering-surface"><strong>Engineering Surface</strong></a>
</p>

<p align="center"><code>architecture &gt; isolated features · evidence &gt; assumptions · reliability &gt; hype</code></p>

---

I design software as systems, not isolated features.

My work centers on failure-aware architecture, runtime behavior, networking, observability, security, and performance. I prefer explicit invariants, reproducible tests, narrow interfaces, measurable behavior, and telemetry that remains useful when a system is under pressure.

Most commercial work is private. The public work below is selected engineering evidence.

## Selected Work

### [MCP Trace](https://github.com/ryux1/mcp-trace)

[![CI](https://github.com/ryux1/mcp-trace/actions/workflows/ci.yml/badge.svg)](https://github.com/ryux1/mcp-trace/actions/workflows/ci.yml)
[![CodeQL](https://github.com/ryux1/mcp-trace/actions/workflows/codeql.yml/badge.svg)](https://github.com/ryux1/mcp-trace/actions/workflows/codeql.yml)
[![Release](https://img.shields.io/github/v/release/ryux1/mcp-trace?include_prereleases&label=release)](https://github.com/ryux1/mcp-trace/releases)
[![License](https://img.shields.io/github/license/ryux1/mcp-trace)](https://github.com/ryux1/mcp-trace/blob/main/LICENSE)

A security-conscious observability gateway for the Model Context Protocol over Streamable HTTP.

```text
MCP client  ──────▶  MCP Trace  ──────▶  upstream MCP server
                         │
                         ├── Prometheus metrics
                         ├── OpenTelemetry traces
                         └── sanitized NDJSON recording + controlled replay
```

- Transparent JSON and SSE proxying without taking protocol authority away from the upstream server.
- Prometheus-compatible metrics, OpenTelemetry spans, W3C Trace Context, structured logs, and MCP-aware inspection.
- Metadata-only recording by default, explicit body capture, credential redaction, hashed legacy session identifiers, and owner-only recording permissions.
- Replay is dry-run-first with explicit execution, concurrency, rate, and timeout controls.
- Compatibility across modern 2026 Streamable HTTP and the 2025 MCP transport revisions.

[Architecture](https://github.com/ryux1/mcp-trace/blob/main/docs/architecture.md) · [Security model](https://github.com/ryux1/mcp-trace/blob/main/docs/security.md) · [Recording schema](https://github.com/ryux1/mcp-trace/blob/main/docs/recording-schema.md) · [Releases](https://github.com/ryux1/mcp-trace/releases)

## Open Source

Current upstream patches under maintainer review:

| Project | Contribution | Engineering scope |
| --- | --- | --- |
| **NASA F´** · [`nasa/fprime`](https://github.com/nasa/fprime) | [#5670 — parameter validation macro](https://github.com/nasa/fprime/pull/5670) | C++ framework API; centralized parameter-validity semantics; refactor across 9 files; four-state coverage; 129/129 unit-test targets |
| **Google gVisor** · [`google/gvisor`](https://github.com/google/gvisor) | [#14097 — PTY positional-write semantics](https://github.com/google/gvisor/pull/14097) | Linux VFS/devpts behavior; `ESPIPE` compatibility for positional PTY writes; syscall and filesystem regression coverage |
| **Cloudflare Workers SDK** · [`cloudflare/workers-sdk`](https://github.com/cloudflare/workers-sdk) | [#15158 — Workflow batch deletion results](https://github.com/cloudflare/workers-sdk/pull/15158) | Runtime behavior; not-found/failure propagation; duplicate-safe result mapping; regression coverage across success and failure paths |
| **OpenAI Cookbook** · [`openai/openai-cookbook`](https://github.com/openai/openai-cookbook) | [#2495 — Windows path portability](https://github.com/openai/openai-cookbook/pull/2495) | Cross-platform repository integrity; Windows-compatible checkout; tested path-portability guard across 3,070 tracked paths |

I am deliberately focusing on contributions where the patch exposes real engineering judgment: compatibility semantics, failure behavior, tests, invariants, portability, and maintainability rather than drive-by cosmetic changes.

## Engineering Surface

| Layer | Working set |
| --- | --- |
| **Systems & runtime** | C, C++, Rust, Go, Linux, VFS/filesystem semantics, process and network behavior |
| **Services & infrastructure** | TypeScript, Node.js, REST, WebSockets, PostgreSQL, Redis, Docker, CI/CD |
| **Observability** | OpenTelemetry, Prometheus, structured logging, tracing, recording, replay, operational diagnostics |
| **Application engineering** | React, Next.js, realtime interfaces, performance-sensitive frontend systems |
| **Security & delivery** | threat-aware design, input validation, access-control boundaries, CodeQL, secret scanning, GitHub Actions |
| **Automation** | Python, Bash/Shell, PowerShell, repository tooling, validation and release workflows |

## Operating Principles

- Architecture before implementation.
- Design for failure, not ideal conditions.
- Treat security, performance, and observability as initial constraints rather than cleanup work.
- Prefer behavior that can be tested, measured, reproduced, and explained.
- Keep interfaces narrow and operational failure modes explicit.
- Optimize for systems that remain understandable after the original implementation context is gone.

## Current Direction

`runtime systems` · `distributed infrastructure` · `networking` · `observability tooling` · `performance` · `open-source engineering`

The objective is simple: build systems whose correctness is visible in their behavior, tests, architecture, and failure handling—not in the number of technologies listed beside them.
