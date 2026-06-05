# Script Inventory

This directory now contains the original Windows batch files used to run the Redpanda performance evaluation.

## Included Scripts
- `run_kb1.bat`: step-load benchmark for Scenario 1
- `script3_1kb_kneepoint.bat`: repeated measurements around the 1KB knee point
- `script5_kb2_start_consumer.bat`: starts the consumer used in Scenario 2
- `script6_kb2_monitor_lag.bat`: monitors consumer lag during burst tests
- `script7_kb2_burst_no_netem_acks1.bat`: burst test without network impairment, `acks=1`
- `script8_kb2_burst_no_netem_acksall.bat`: burst test without network impairment, `acks=all`
- `script9_kb2_burst_netem_acks1.bat`: burst test with network impairment, `acks=1`
- `script10_kb2_burst_netem_acksall.bat`: burst test with network impairment, `acks=all`

## Notes
The scripts were executed from a Windows host using Kafka CLI tools against the Redpanda cluster.
