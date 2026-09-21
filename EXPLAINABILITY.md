# Explainability Contract: PerformanceMedic

## Decision

PerformanceMedic decides whether readable source contains a potential nested-loop pattern. A match is reported as an optimization signal rather than proof of a performance defect.

## Inputs

It uses source text captured by the scanner and applies a deterministic nested-loop pattern rule. The finding is tied to the observed code pattern.

## Limits

It does not benchmark execution time, analyze algorithmic complexity comprehensively, or account for data size and runtime behavior. Some nested loops are intentional and efficient.
