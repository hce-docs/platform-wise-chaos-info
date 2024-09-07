### JVM Chaos

*Note: This assumes that the java processes are themselves as non-root*

- Method Latency (Inbound, Outbound)
  - *Slows down the Java application by introducing delays in executing specific method calls, for the given chaos duration*
    
- Exception
  - *Injects a user-defined exception in the Java application while executing specific method calls, for the given chaos duration*
    
- CPU Stress
  - *Consumes excessive CPU threads available to the JVM, for the given chaos duration*

- Memory Stress
  - *Consumes stack memory resources allocated to the JVM, for the given chaos duration*
    
- Heap Mem Utilization
  - *Consumes heap memory resources available to the JVM, for the given chaos duration*
  
- Return Value Modification
  - *Modifies the return value of a method in a Java application, for the given chaos duration.*
    
- Trigger GC
  - *Triggers the garbage collector on a specific process in Java that causes unused (or out of scope) objects, variables, and so on to be garbage collected and recycled*

### System Resource Exhaustion Chaos

- CPU stress
  - *Hogs the desired number of CPU cores/load percentage within the baremetal/VM via a stress utility, thereby depriving the application processes of CPU resources. Withdraws the stress action and releases CPU cycles after the chaos duration*
    
- Memory Stress
  - *Hogs the available free memory in the system via a stress utility to simulate memory pressure/leaks. Withdraws the stress action and releases memory after the chaos duration*
    
- Disk I/O Stress
  - *Performs heavy I/O operations on the desired filesystem mount path via a stress utility to simulate disk bandwidth issues, slowness, and noisy neighbor conditions. Withdraws the stress action after the chaos duration*

### State Manipulation Chaos

- Process Kill
  - *Kills a desired process in the baremetal/VM, the process being identified either by name, ID or via process ID derivation command. Allows optional re-creation of the process via EoT (end-of-test) command hooks.*
