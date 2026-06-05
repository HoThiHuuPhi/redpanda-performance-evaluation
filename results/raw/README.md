# Result Index

## Scenario 1: Gradual Load / Knee Point
Directory: `results/raw/scenario1-knee-point/`

Included examples:
- `256B_6MBps.txt`
- `256B_7MBps.txt`
- `1KB_10MBps.txt`
- `1KB_10MBps_run1.txt`
- `1KB_11MBps_run1.txt`
- `1KB_12MBps.txt`

Purpose:
- identify throughput and latency behavior as offered load approaches saturation
- inspect the knee point region for 1KB messages

## Scenario 1: Failure Cases
Directory: `results/raw/scenario1-failure-cases/`

Included examples:
- `1KB_11MBps_run2.txt`
- `1KB_15MBps.txt`

Purpose:
- preserve overload-side runs and problematic executions for comparison with stable runs

## Scenario 2: Burst Traffic and Netem
Directory: `results/raw/scenario2-burst-netem/`

Included examples:
- `burst_no_netem_acks1_cycle1.txt`
- `burst_no_netem_acksall_cycle1.txt`
- `burst_netem_acks1_cycle1.txt`
- `burst_netem_acksall_cycle1.txt`

Purpose:
- compare performance with and without network impairment
- compare durability settings `acks=1` and `acks=all`
- observe burst recovery across repeated cycles
