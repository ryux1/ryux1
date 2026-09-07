<div align="center">

# Hi, I'm Ryu

**Systems engineer focused on runtime correctness, infrastructure, networking, reliability, and security.**

![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

[Pull requests](https://github.com/search?q=is%3Apr+author%3Aryux1&type=pullrequests) · [Repositories](https://github.com/ryux1?tab=repositories)

</div>

## About me

I like working on software that has to remain predictable once it leaves the happy path. My interests sit around systems and infrastructure: runtime behavior, distributed coordination, networking, resource use, compatibility, reliability, and security boundaries.

A lot of that work begins in an unfamiliar codebase. I reproduce the problem, trace it through the relevant layers, and try to leave behind a focused change with regression coverage. Depending on the project, that has taken me through Rust, C++, Go, Python, TypeScript, Java, and Elixir.

This profile collects my own projects and the upstream work I do in open source. The examples below cover performance, state management, authorization, and API consistency; the complete history is available through my pull requests.

## Selected contributions

| Project | Contribution |
| --- | --- |
| [Apache DataFusion](https://github.com/apache/datafusion/pull/24319) | Reworked Arrow memory accounting, with measured 3.4–9.4× speedups while preserving shared-buffer correctness. |
| [Apache Hudi](https://github.com/apache/hudi/pull/19849) | Removed unused serialized Spark table state and deferred avoidable file-index initialization. |
| [Supabase Realtime](https://github.com/supabase/realtime/pull/2089) | Scoped authorization checks to the Realtime extension actually being written. |
| [NASA F´](https://github.com/nasa/fprime/pull/5670) | Centralized four-state parameter-validity semantics across the framework and services. |

<p align="center">
  <a href="https://github.com/search?q=is%3Apr+author%3Aryux1&type=pullrequests"><strong>View all pull requests →</strong></a>
</p>
