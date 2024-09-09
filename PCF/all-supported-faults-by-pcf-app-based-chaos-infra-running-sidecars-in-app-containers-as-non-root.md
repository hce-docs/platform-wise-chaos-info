
### PCF App JVM Chaos

- Method Latency (Inbound, Outbound)
  - *Slows down the Java application by introducing delays in executing specific method calls, for the given chaos duration*
     
- Exception
  - *Injects a user-defined exception in the Java application while executing specific method calls, for the given chaos duration*
    
- Heap Mem Utilization
  - *Consumes heap memory resources available to the JVM, for the given chaos duration*
    
- Return Value Modification
  - *Modifies the return value of a method in a Java application, for the given chaos duration.*

### PCF App State Manipulation Chaos

- App Stop
  - *Stops the specified PCF app by leveraging the CF/Cloud Controller API & restarts it after the chaos duration*
    
- App Route Unmap
  - *Temporarily unmaps a specific app route for a given PCF app and after the chaos duration, maps it back to the app*
    
- App Unbind Service
  - *Temporarily unbinds a specific service for a given PCF app and after the chaos duration, binds it back to the app*

### System Resource Exhaustion Chaos

- App Instance CPU stress
  - *Hogs the desired number of CPU cores/load percentage within the PCF app instances via a stress utility, thereby depriving the application processes of CPU resources. Withdraws the stress action and releases CPU cycles after the chaos duration*
  
- App Instance Memory Stress
  *Hogs the available free memory in the PCF app instances via a stress utility to simulate memory pressure/leaks. Withdraws the stress action and releases memory after the chaos duration*
