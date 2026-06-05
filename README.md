# Redpanda Performance Evaluation

Academic project on evaluating Redpanda performance in a distributed message streaming environment under varying workloads and network conditions.

## Project Summary
This project studies how a Redpanda cluster behaves when traffic increases, when burst traffic occurs, and when replication links are degraded. The evaluation focuses on throughput, latency, and consumer lag to identify performance limits and reliability trade-offs.

## Objectives
- Measure throughput as offered load increases
- Analyze average and tail latency under stress
- Observe consumer lag and backlog growth
- Compare behavior between `acks=1` and `acks=all`
- Evaluate system stability under burst traffic and network impairment

## Experimental Environment
- 3 Ubuntu virtual machines used as Redpanda brokers
- 1 Windows host machine used for tooling and orchestration
- Redpanda cluster configured for replicated message streaming
- Kafka CLI tools for producer benchmarking
- Linux traffic control with `tc netem` for network impairment simulation

## Evaluation Scenarios
### 1. Gradual Load Increase
The first scenario increases offered load progressively to identify the saturation point and observe how throughput and latency change near the knee point.

### 2. Burst Traffic and Network Degradation
The second scenario introduces bursty traffic and degraded inter-broker network conditions to study replication overhead, latency growth, and throughput stability.

### 3. Reliability vs Performance Comparison
The project compares acknowledgment modes to evaluate the trade-off between higher durability (`acks=all`) and lower write latency (`acks=1`).

## Metrics
- Throughput
- Average latency
- Tail latency (high-percentile latency)
- Consumer lag / backlog

## Repository Structure
```text
.
|-- README.md
|-- report/
|   `-- final-report.pdf
|-- scripts/
|-- configs/
|-- results/
`-- images/
```

## Key Outcomes
- Built and configured a multi-node Redpanda cluster for controlled benchmarking
- Designed repeatable test scenarios for progressive load and burst traffic
- Measured the effect of replication and network impairment on performance
- Analyzed the trade-off between reliability settings and observed latency/throughput

## Report
The full academic report is available at [report/final-report.pdf](report/final-report.pdf).

## Technologies
Redpanda, Ubuntu, VMware, Kafka CLI, Linux networking tools, distributed systems performance evaluation

## Notes
This repository currently contains the final report and project structure. Configuration files, scripts, benchmark outputs, and supporting images can be added incrementally to improve reproducibility.
