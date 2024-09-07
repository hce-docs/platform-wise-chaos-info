### JVM Chaos

- Method Latency (Inbound, Outbound)
  - *Slows down the Java application by introducing delays in executing specific method calls.*
  
- Exception
  - *Injects a user-defined exception in the Java application while executing specific method calls*
    
- CPU Stress
  - *Consumes excessive CPU threads available to the JVM*
    
- Memory Stress
  - *Consumes stack memory resources allocated to the JVM*
    
- Heap Mem Utilization
  - *Consumes heap memory resources available to the JVM*
    
- Return Value Modification
  - *Modifies the return value of a method in a Java application for a specific duration.*
    
- Trigger GC
  - *Triggers the garbage collector on a specific process in Java that causes unused (or out of scope) objects, variables, and so on to be garbage collected and recycled*

### API Chaos 

- API Latency
  - *Injects the desired latency into specific API requests (made to another service, i.e., egress) or response (for requests coming in on a specific port i.e., ingress) on the baremetal/VM, the API being identified via path/route filters. Restores standard API  characteristics after the chaos duration*
    
- API Block
  - *Blocks specific API requests (made to another service, i.e., egress) or response (for requests coming in on a specific port i.e., ingress) on the baremetal/VM, the API being identified via path/route filters. Unblocks these API requests after the chaos duration*
  
- API Response Status/Body/Header Modification
  - *Changes the response status code, body, or header with desired values for specific APIs on the baremetal/VM, the API being identified via path/route filters. Restores standard API response after the chaos duration*
    
- API Request Header/Body Modification
  - *Changes the request header or body with desired values for specific APIs on the baremetal/VM, the API being identified via path/route filters. Restores standard API requests after the chaos duration*

### State Manipulation Chaos

- Process Kill
  - *Kills a desired process in the baremetal/VM, the process being identified either by name, ID or via process ID derivation command. Allows optional re-creation of the process via EoT (end-of-test) command hooks.*
    
- Service Restart
  - *Stops a desired service within the baremetal/VM, the service being identified by service name. Allows optional service restart (if no self-healing is built in already) via EoT command hooks.*

### System Resource Exhaustion Chaos

- CPU stress
  - *Hogs the desired number of CPU cores/load percentage within the baremetal/VM via a stress utility, thereby depriving the application processes of CPU resources. Withdraws the stress action and releases CPU cycles after the chaos duration*
    
- Memory Stress
  - *Hogs the available free memory in the system via a stress utility to simulate memory pressure/leaks. Withdraws the stress action and releases memory after the chaos duration*

- Disk I/O Stress
  - *Performs heavy I/O operations on the desired filesystem mount path via a stress utility to simulate disk bandwidth issues, slowness, and noisy neighbor conditions. Withdraws the stress action after the chaos duration* 

### Network Manipulation Chaos

- Network Latency
  - *Injects the desired latency into the baremetal/VM Network traffic for a specific interface, via a traffic-shaping utility. Simulates degraded/slow networks. Restores network characteristics after the chaos duration.*
  
- Network Packet Loss
  - *Injects the desired packet drop percentage into the baremetal/VM Network traffic for a specific interface, via a traffic-shaping utility. This fault can be used to simulate blackhole and split-brain conditions. Restores network characteristics after the chaos duration.*
    
- Network Rate Limit
  - *Performs network bandwidth rate limiting  on the baremetal/VM network traffic for a specific interface, via a traffic-shaping utility. Simulates reduced network capacity. Restores network characteristics after the chaos duration.*

### DNS Chaos

- DNS Error
  - *Injects DNS resolution errors for specific domains/hosts on the baremetal/VM for the given chaos duration*
    
- DNS Spoof
  - *Redirects the traffic to specific domains/hosts/service endpoints from the baremetal/VM, to a desired endpoint (often, an instrumented version of the service or a stub) for the given chaos duration*

### Time Chaos

- Time Drift
  - *Changes the system time by adding an offset, which is specified in a (+/-)[numeric-hours]h[numeric-minutes]m[numeric-seconds]s format for the given chaos duration*

