# PerformanceMedic

> Portable agent for surfacing obvious nested-loop patterns that deserve performance review.

## What it does

PerformanceMedic scans source text for recognizable nested-loop structures and reports them as review candidates. It intentionally avoids turning a syntactic pattern into a guaranteed performance verdict.

### Diagnostic fingerprint

**Code pattern → performance signal → evidence → review action**

## Why this agent is distinct

PerformanceMedic is designed as an early warning layer. Its job is to identify code shapes that may deserve deeper profiling, not to replace benchmarks or production telemetry.

That boundary is important because static pattern detection and actual runtime performance are not the same thing.

## Workflow

```text
Source code
   ↓
Pattern scanner
   ↓
Nested-loop rule
   ↓
Observed evidence
   ↓
Profiling / optimization recommendation
```

## Verification

The repository contains an OpenGAP passport, performance-focused fixture, explainability and duty contracts, four framework adapters, and automated adapter verification.

OpenGAP validation passed and all four framework exports have been exercised successfully.

## Design principle

**Flag candidates, not certainties.** PerformanceMedic recommends review where a pattern is visible and avoids claiming measured latency that it never observed.

## Medic family

PerformanceMedic provides the performance-analysis lens in a portable family of focused engineering agents.