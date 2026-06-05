# Benchmark Results

This directory contains raw benchmark outputs collected from the Redpanda evaluation.

## Result Groups
- `raw/scenario1-knee-point/`: gradual-load and knee-point measurements for 256B and 1KB message sizes
- `raw/scenario1-failure-cases/`: overload and failure-side observations near or beyond saturation
- `raw/scenario2-burst-netem/`: burst traffic results across `acks=1` / `acks=all` with and without `tc netem`

## Representative Observations
- Scenario 1 includes measurements around 10-12 MB/s for 1KB messages to identify the knee point.
- Scenario 2 captures the impact of burst traffic and degraded inter-broker conditions on throughput and latency.
- Several result files include average latency, max latency, and percentile latency summaries from Kafka CLI tooling.

## Notes
These are raw command outputs kept in their original form for traceability.
