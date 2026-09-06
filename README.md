<h1 align="center">Ryu</h1>

<p align="center">
  <strong>Systems engineer working across runtimes, distributed infrastructure, reliability, and security.</strong>
</p>

<p align="center">
  <code>runtime behavior</code>&nbsp;&nbsp;
  <code>systems correctness</code>&nbsp;&nbsp;
  <code>failure semantics</code>&nbsp;&nbsp;
  <code>performance</code>
</p>

---

I work on the parts of software where behavior becomes difficult to reason about:
compatibility boundaries, concurrency, resource accounting, authorization,
failure recovery, and the gap between an interface's promise and its runtime
behavior.

My public work is mostly upstream engineering. I reproduce the condition, find
the violated invariant, make the narrowest defensible change, and leave behind
tests that explain why the behavior matters.

## Selected upstream work

| Project | Change | Engineering result |
| --- | --- | --- |
| **Apache DataFusion** | [Reduce record-batch memory accounting overhead](https://github.com/apache/datafusion/pull/24319) | Removed repeated Arrow accounting work while preserving view-array and shared-buffer correctness. **Merged.** |
| **Supabase Realtime** | [Check extension write policies lazily](https://github.com/supabase/realtime/pull/2089) | Preserved explicit Broadcast and Presence authorization without performing unrelated extension reads. **Merged.** |
| **NASA F´** | [Add a parameter validation macro](https://github.com/nasa/fprime/pull/5670) | Centralized four-state parameter-validity semantics across the C++ framework API and its tests. **Merged.** |
| **Apache Hudi** | [Reject unsupported procedure filter functions](https://github.com/apache/hudi/pull/19850) | Converted invalid Spark procedure filters into explicit validation failures with focused coverage. **Merged.** |
| **Google gVisor** | [Return `ESPIPE` for positional PTY I/O](https://github.com/google/gvisor/pull/14097) | Matched Linux VFS and devpts behavior with syscall and filesystem regression coverage. **Approved.** |
| **pyasn1** | [Reject bare constructed schemas](https://github.com/pysnmp/pyasn1/pull/173) | Tightened constructed-type validation and added regression coverage across the affected schema paths. **Merged.** |

Additional contributions span
[aiohttp](https://github.com/aio-libs/aiohttp),
[typeshed](https://github.com/python/typeshed),
[Click](https://github.com/pallets/click),
[Apache Sedona](https://github.com/apache/sedona),
[Sentry CLI](https://github.com/getsentry/sentry-cli), and other established
projects.

[View all pull requests](https://github.com/search?q=is%3Apr+author%3Aryux1&type=pullrequests)

## Engineering range

<table>
  <tr>
    <td width="33%" valign="top">
      <strong>Systems</strong><br><br>
      Linux semantics, runtimes, filesystems, memory, concurrency, compilers,
      and native interfaces.
    </td>
    <td width="33%" valign="top">
      <strong>Distributed software</strong><br><br>
      Networking, realtime systems, service boundaries, authorization,
      observability, and recovery.
    </td>
    <td width="33%" valign="top">
      <strong>Engineering assurance</strong><br><br>
      Reproducible tests, explicit invariants, security boundaries, performance
      evidence, and deterministic tooling.
    </td>
  </tr>
</table>

```text
reproduce → isolate → understand the invariant → change narrowly → prove it
```

Rust · C++ · Go · Elixir · Python · Java · TypeScript
