# Benchmark Results

This directory is intended for benchmark outputs collected during evaluation.

## Typical Result Files
- throughput measurements
- average latency results
- tail latency summaries
- consumer lag observations
- scenario comparison tables

## Suggested Files
- `throughput.csv`
- `latency.csv`
- `lag-summary.csv`
- `scenario-notes.md`

## Interpretation Focus
The main analysis in this project focuses on:
- saturation point under increasing load
- throughput degradation under burst traffic
- latency growth under network impairment
- trade-off between `acks=1` and `acks=all`
