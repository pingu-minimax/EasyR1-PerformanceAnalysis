# Performance Benchmarks

## Benchmark Suite for Protocol Changes Investigation

### Purpose
This directory contains benchmark scripts and results for investigating performance regressions related to commit `098931530606d22f867fd121b1dcb3225a43661f`.

### Key Files

- `verl/protocol.py` - Protocol implementation under investigation
- `examples/config.yaml` - Configuration file with changed defaults

### Running Benchmarks

```bash
# Install dependencies
pip install -r requirements.txt

# Run baseline benchmark
python run_benchmark.py --mode baseline

# Run comparison benchmark
python run_benchmark.py --mode comparison --commit 098931530606d22f867fd121b1dcb3225a43661f
```

### Expected Outputs

- `results/baseline.json` - Baseline performance metrics
- `results/comparison.json` - Post-change performance metrics
- `results/regression_report.md` - Detailed regression analysis

### Metrics Collected

| Metric | Description | Unit |
|--------|-------------|------|
| throughput | Requests processed per second | req/s |
| latency_p50 | 50th percentile latency | ms |
| latency_p95 | 95th percentile latency | ms |
| latency_p99 | 99th percentile latency | ms |
| memory_peak | Peak memory usage | MB |
| memory_avg | Average memory usage | MB |
