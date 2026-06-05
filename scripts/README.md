# Experiment Scripts

This directory is reserved for automation scripts used to execute benchmark scenarios and supporting checks.

## Expected Scripts
- gradual load benchmark script
- burst traffic benchmark script
- consumer lag monitoring script
- network impairment script using `tc netem`

## Suggested Naming
- `scenario1-gradual-load.sh`
- `scenario2-burst-traffic.sh`
- `lag-monitor.sh`
- `apply-netem.sh`

## Notes
The report describes scenarios for progressive load increase, burst traffic, and degraded network conditions. Scripts placed here should follow those experiment definitions.
