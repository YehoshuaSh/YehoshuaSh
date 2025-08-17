# Josh — Engineering Leadership | Python • TestStand • C • C#

> Driving high‑impact, production‑grade solutions across test automation and systems engineering. I build resilient pipelines, accelerate verification, and de‑risk deployments.


![Python](https://img.shields.io/badge/Python-3.11%2B-blue)
![C](https://img.shields.io/badge/C-Embedded%20%7C%20Systems-informational)
![C%23](https://img.shields.io/badge/C%23-.NET%206%2F7%20%7C%20Win%20Apps-512BD4)
![NI TestStand](https://img.shields.io/badge/NI-TestStand-005B82)
![PyTest](https://img.shields.io/badge/pytest-automation-success)
![.NET](https://img.shields.io/badge/.NET-6%2B-68217A)
![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-2088FF)
![Docker](https://img.shields.io/badge/Docker-Containers-2496ED)
![CI/CD](https://img.shields.io/badge/CI%2FCD-Release%20Ops-brightgreen)

---

## Executive Summary
Seasoned engineer with an end‑to‑end mindset: requirements → architecture → implementation → validation → continuous delivery. I specialize in Python frameworks, NI TestStand orchestration, and low‑level C/C# integrations to deliver scalable test solutions and reliable software.

- **Business Outcomes:** faster time‑to‑test, higher coverage, fewer regressions, cleaner releases.
- **Technical Edge:** robust tooling, strong observability, deterministic builds, and repeatable results.

---

## Core Competencies
- **Python:** tooling, CLIs, services, data handling, test frameworks (pytest, unittest), packaging (poetry/pip), type safety (mypy/pyright), linters (ruff/flake8), docs (Sphinx/Markdown).
- **NI TestStand:** sequence architecture, step customizations, process models, hardware‑in‑loop, LabVIEW/C# adapters, result processing, report/DB logging, parallel execution, operator UI.
- **C & C#:** device integration, performance‑critical modules, P/Invoke and interop, .NET 6/7, WPF/WinForms utilities, REST/GRPC clients, instrumentation drivers.
- **Quality Engineering:** CI/CD (GitHub Actions), artifact/versioning, test analytics, coverage, reproducible environments (Docker/venv), code reviews, static/dynamic analysis.
- **Systems & Tooling:** Windows & Linux, Git, Make/CMake, PowerShell/Bash, networking fundamentals, monitoring/telemetry.

---

## Signature Deliverables
- **Automated Test Platforms:** Modular, maintainable TestStand sequences with Python/C# plug‑ins, standardized reporting, database sinks, and headless runners.
- **Device & Protocol Toolkits:** C/C# libraries and Python bindings for instrument control and high‑throughput data capture.
- **Verification Pipelines:** Multi‑stage CI with gated merges, matrix testing, signed artifacts, and release notes on autopilot.

---

## Selected Projects
> Replace placeholders with your repos; keep it outcome‑centric.

- **TestStand Enterprise Template** — Opinionated starter for parallel test, custom process models, and unified result logging.  
  _Impact:_ cut onboarding time by **>50%**, standardized reporting across products.

- **Python Instrument SDK** — Cross‑platform drivers + async acquisition with clean APIs and examples.  
  _Impact:_ enabled rapid feature development, reduced bug surface in integration.

- **C# Operator Console** — WPF app for station control, calibration, and diagnostics with role‑based access & telemetry.  
  _Impact:_ decreased MTTR and improved traceability in production lines.

---

## Tech Stack Deep Dive
**Languages:** Python, C, C#  
**Test & QA:** pytest, unittest, NUnit/xUnit, coverage, TestStand sequences & process models  
**Build & CI:** GitHub Actions, Docker, Make/CMake, MSBuild, NuGet, Poetry  
**Packaging:** PyPI wheels, internal feeds, semver, changelogs  
**Observability:** structured logs, metrics, traces; log aggregation & dashboards  
**Data/IO:** binary protocols, serial/TCP, file formats (CSV/Parquet/HDF5), streaming  

---

## Code Snippets (Representative)

<details>
<summary><strong>Python · CLI harness around pytest</strong></summary>

```python
# tools/test_harness.py
import subprocess, sys

if __name__ == "__main__":
    cmd = [sys.executable, "-m", "pytest", "-q", "--maxfail=1", "--disable-warnings"]
    sys.exit(subprocess.call(cmd))
```
</details>

<details>
<summary><strong>C · robust read loop</strong></summary>

```c
// io/read_loop.c
#include <stdio.h>
#include <errno.h>
size_t robust_read(FILE* f, void* buf, size_t n) {
    size_t total = 0; int retries = 3;
    while (total < n && retries--) {
        size_t r = fread((char*)buf + total, 1, n - total, f);
        if (r == 0 && ferror(f)) clearerr(f); // retry transient
        total += r;
    }
    return total;
}
```
</details>

<details>
<summary><strong>C# · P/Invoke boundary</strong></summary>

```csharp
// Interop/Native.cs
using System;
using System.Runtime.InteropServices;

internal static class Native {
    [DllImport("device.dll", CallingConvention = CallingConvention.Cdecl)]
    internal static extern int Capture(IntPtr buffer, int length);
}
```
</details>

<details>
<summary><strong>TestStand · result processing concept</strong></summary>

```ini
; ResultProcessing.cfg (concept)
[Logging]
ModelPlugin = DatabaseLogger; ReportFormat = JUnitXML; FlushInterval=5s
```
</details>

---

## Operating Principles
- **Production first:** code and tests shaped for real stations and real users.
- **Repeatability:** deterministic builds, seeded randomness, pinned deps.
- **Observability by default:** logs/metrics/traces from day one.
- **Documentation as a deliverable:** READMEs, ADRs, and diagrams ship with code.

---

## Metrics That Matter
- Test cycle time ↓, coverage ↑, flake rate ↓, MTTR ↓, deployment lead time ↓.  
- Track with dashboards wired to CI and station telemetry.

---

## Certifications & Tools (sample)
- NI TestStand (version‑specific) • ISTQB (if applicable) • Microsoft/.NET • Docker • Git

---

## Contact & Links
- **GitHub:** YehoshuaSh 
- **LinkedIn:** [Yehoshua Shamir  ](https://www.linkedin.com/in/yehoshua-shamir-69881417?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3B7J%2B%2FMgj8QxaDdK338yDV%2FA%3D%3D)
- **Email:** josh839@gmail.com

---
