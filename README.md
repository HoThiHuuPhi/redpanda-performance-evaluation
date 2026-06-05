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

## Included Artifacts
- Final report in `report/final-report.pdf`
- Original benchmark scripts in `scripts/windows-batch/`
- Raw result files grouped by scenario in `results/raw/`
- Repository notes for configs, figures, and future reproducibility material

## Repository Structure
```text
.
|-- README.md
|-- report/
|   `-- final-report.pdf
|-- scripts/
|   |-- README.md
|   `-- windows-batch/
|-- configs/
|-- results/
|   |-- README.md
|   `-- raw/
`-- images/
```

## Key Outcomes
- Built and configured a multi-node Redpanda cluster for controlled benchmarking
- Designed repeatable test scenarios for progressive load and burst traffic
- Measured the effect of replication and network impairment on performance
- Preserved the original scripts and raw outputs used in the academic evaluation

## Technologies
Redpanda, Ubuntu, VMware, Kafka CLI, Windows batch scripting, Linux networking tools, distributed systems performance evaluation

## Notes
The repository now includes the original execution artifacts used in the project. Additional sanitized broker configuration files and charts can be added later to further improve reproducibility and presentation quality.
