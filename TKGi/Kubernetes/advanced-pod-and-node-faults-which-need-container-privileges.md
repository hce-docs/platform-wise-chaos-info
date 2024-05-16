### Application (JVM/Spring) Chaos

- Method Latency (Inbound, Outbound)
- Exception
- CPU Stress
- Memory Stress
- Heap Mem Utilization
- Return Value Modification
- Trigger GC 

### API Manipulation Chaos

- API Latency
- API Block
- API Status Code Modification
- API Response Header Modification
- API Response Body Modification

### (Pod-Wide) HTTP Chaos

- Pod HTTP Latency
- Pod HTTP Status Code Modification
- Pod HTTP Header Modification
- Pod HTTP Response Body Modification
- Pod HTTP Reset Peer

### State Manipulation Chaos

- Pod Delete
- Container Kill
- Node Drain
- Node Taint For Eviction
- Node Restart

### Scale Chaos

- Pod Scale
- Kubelet Density

### Resource Exhaustion Chaos

- Pod CPU Hog (supported via remote injection as well as exec-based injection)
- Pod Memory Hog (supported via remote injection as well as exec-based injection)
- Pod IO Stress
- Pod Disk Fill

### Network Manipulation Chaos

- Pod Network Latency
- Pod Network Loss
- Pod Network Duplication
- Pod Network Corruption
- Pod Network Partition
- Node Network Latency
- Node Network Loss

### Filesystem I/O Chaos

- Pod IO Error
- Pod IO Latency
- Pod IO Attribute Override

### Kubernetes Platform Services Chaos

- Kubelet Service Kill
- Container Runtime Service Kill

### DNS Chaos

- Pod DNS Error
- Pod DNS Spoof

### Load Chaos

- Locust Loadgen
- K6 Loadgen



