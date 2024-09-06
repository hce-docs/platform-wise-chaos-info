*Note: Assumes the vCenter user access for the experiments is equal to or greater than what is laid out [here](https://github.com/hce-docs/platform-wise-chaos-info/blob/main/VMware/vcenter-based-chaos-user-access-requirements.md)*

### VM State Manipulation Chaos

- VM Poweroff
  - *Performs a power off (i.e., vcenter-api-driven-shut-down operation) of the desired VM identified by its MOID (Managed Object ID). Restores the VM to a powered-on state after the chaos duration.*
    
- VM Process Kill
  - *Kills a desired process in the VM, the process being identified either by name, ID, or via process ID derivation command. Allows optional re-creation of the process via EoT (end-of-test) command hooks.*
    
- VM Service Stop
  - *Stops a desired service within the VM, the service being identified by service name. Allows optional service restart (if no self-healing is built in already) via EoT command hooks.*
      
- VM Disk Loss
  - *Detaches the desired disks attached to the VM, the disks being identified by their VMDK names. Re-attaches the disk to the VM after the chaos duration, with optional re-mount of the filesystems via EoT command hooks.* 

### VM Resource Stress Chaos

- VM CPU Hog
  -  *Hogs the desired number of CPU cores/load percentage within the VM via a stress utility, thereby depriving the application processes of CPU resources. Withdraws the stress action and releases CPU cycles after the chaos duration*
    
- VM Memory Hog
  - *Hogs the available free memory in the system via a stress utility to simulate memory pressure/leaks. Withdraws the stress action and releases memory after the chaos duration*
    
- VM Disk I/O Stress
  - *Performs heavy I/O operations on the desired filesystem mount path via a stress utility to simulate disk bandwidth issues, slowness, and noisy neighbor conditions. Withdraws the stress action after the chaos duration*  

### VM Network Manipulation Chaos

- VM Network Latency
  - *Injects the desired latency into the VM Network traffic for specific filters (TCP/UDP, IPs, Hosts, inbound/outbound), via a traffic-shaping utility. Simulates degraded/slow networks. Restores network characteristics after the chaos duration.*
     
- VM Network Packet Loss
  - *Injects the desired packet drop percentage into the VM Network traffic for specific filters (TCP/UDP, IPs, Hosts, inbound/outbound), via a traffic-shaping utility. This fault can be used to simulate split-brain conditions. Restores network characteristics after the chaos duration.*
    
- VM Network Corruption
  - *Injects the desired packet corruption percentage into the VM Network traffic for specific filters (TCP/UDP, IPs, Hosts, inbound/outbound), via a traffic-shaping utility. This fault can be used to test application stability while dealing with corrupted data over the network. Restores network characteristics after the chaos duration.*
    
- VM Network Duplication
  - *Injects the desired packet duplication percentage into the VM Network traffic for specific filters (TCP/UDP, IPs, Hosts, inbound/outbound), via a traffic-shaping utility. Restores network characteristics after the chaos duration.*
    
- VM Network Blackhole
  - *Blocks both inbout and outbound traffic for specific host(s) or globally, from the VM using temporary firewall rules. Restores network characteristics after the chaos duration.*
