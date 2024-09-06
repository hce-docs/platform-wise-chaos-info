### State Manipulation Chaos

- Process Kill
  - *Kills a desired process in the baremetal/VM, the process being identified either by name, ID, or via process ID derivation command. Allows optional re-creation of the process via EoT (end-of-test) command hooks.*
    
- Service Stop
  - *Stops a desired service within the baremetal/VM, the service being identified by service name. Allows optional service restart (if no self-healing is built in already) via EoT command hooks.*


### Resource Utilization Chaos

- CPU Stress
  - *Hogs the desired number of CPU cores/load percentage within the baremetal/VM via a stress utility, thereby depriving the application processes of CPU resources. Withdraws the stress action and releases CPU cycles after the chaos duration*
  
- Memory Stress
  - *Hogs the available free memory in the system via a stress utility to simulate memory pressure/leaks. Withdraws the stress action and releases memory after the chaos duration*
 
- Disk I/O Stress
  - *Performs heavy I/O operations on the desired filesystem mount path via a stress utility to simulate disk bandwidth issues, slowness, and noisy neighbor conditions. Withdraws the stress action after the chaos duration*

### Network Manipulation Chaos

- Network Latency
  - *Injects the desired latency into the baremetal/VM Network traffic for specific filters (TCP/UDP, IPs, Hosts, inbound/outbound), via a traffic-shaping utility. Simulates degraded/slow networks. Restores network characteristics after the chaos duration.*
     
- Network Packet Loss
  - *Injects the desired packet drop percentage into the baremetal/VM Network traffic for specific filters (TCP/UDP, IPs, Hosts, inbound/outbound), via a traffic-shaping utility. This fault can be used to simulate split-brain conditions. Restores network characteristics after the chaos duration.*
    
- Network Corruption
  - *Injects the desired packet corruption percentage into the baremetal/VM Network traffic for specific filters (TCP/UDP, IPs, Hosts, inbound/outbound), via a traffic-shaping utility. This fault can be used to test application stability while dealing with corrupted data over the network. Restores network characteristics after the chaos duration.*
    
- Network Duplication
  - *Injects the desired packet duplication percentage into the baremetal/VM Network traffic for specific filters (TCP/UDP, IPs, Hosts, inbound/outbound), via a traffic-shaping utility. Restores network characteristics after the chaos duration.*

- Network BlackHole
  - *Blocks both inbout and outbound traffic for specific host(s) or globally, from the baremetal/VM using temporary firewall rules. Restores network characteristics after the chaos duration.* 
