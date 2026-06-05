# Redpanda Performance Evaluation

## Overview
This project evaluates the performance of Redpanda in a distributed message streaming environment under different workloads and network conditions.

## Objectives
- Measure throughput under increasing load
- Analyze latency under burst traffic
- Observe consumer lag and backlog behavior
- Compare `acks=1` and `acks=all`

## Environment
- 3 Ubuntu virtual machines
- 1 Windows host machine
- Redpanda cluster
- Kafka CLI tools
- Linux traffic control (`tc netem`)

## Repository Structure
- `report/`: final report
- `scripts/`: experiment scripts
- `configs/`: configuration files
- `results/`: benchmark outputs
- `images/`: topology and charts

## Notes
This repository is based on an academic project for network performance evaluation.
