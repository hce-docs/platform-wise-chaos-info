### PCF App JVM Chaos

- Method Latency (Inbound, Outbound)
  - *Slows down the Java application by introducing delays in executing specific method calls, for the given chaos duration*
    
- Exception
  - *Injects a user-defined exception in the Java application while executing specific method calls, for the given chaos duration*
  
- Heap Mem Utilization
  - *Consumes heap memory resources available to the JVM, for the given chaos duration*
  
- Return Value Modification
  - *Modifies the return value of a method in a Java application, for the given chaos duration.* 

### PCF App API Chaos 

- API Latency
  - *Injects the desired latency into specific API requests (made to another service, i.e., egress) or response (for requests coming in on a specific port i.e., ingress) on the PCF app instance/Container, the API being identified via path/route filters. Restores standard API characteristics after the chaos duration*
    
- API Block
  - *Blocks specific API requests (made to another service, i.e., egress) or response (for requests coming in on a specific port i.e., ingress) on the PCF app instance/Container, the API being identified via path/route filters. Unblocks these API requests after the chaos duration*
    
- API Status Code Modification
  - *Changes the response status code, body, or header with desired values for specific APIs on the PCF app instance/Container, the API being identified via path/route filters. Restores standard API response after the chaos duration*
    
- API Response Header Modification
  - *Changes the request header or body with desired values for specific APIs on the PCF app instance/Container, the API being identified via path/route filters. Restores standard API requests after the chaos duration*
- API Response Body Modification 

### PCF App State Manipulation Chaos

- App Stop
  - *Stops the specified PCF app by leveraging the CF/Cloud Controller API & restarts it after the chaos duration*
    
- App Instance / Container Kill
  - *Kills/crashes the app instance/container of the specified PCF app and verifies automatic restart. The number of iterations can be configured as desired*
    
- App Route Unmap
  - *Temporarily unmaps a specific app route for a given PCF app and after the chaos duration, maps it back to the app*
  
- App Unbind Service
  - *Temporarily unbinds a specific service for a given PCF app and after the chaos duration, binds it back to the app* 

### System Resource Exhaustion Chaos

- App Instance CPU stress
  - *Hogs the desired number of CPU cores/load percentage within the PCF app instances via a stress utility, thereby depriving the application processes of CPU resources. Withdraws the stress action and releases CPU cycles after the chaos duration*
  
- App Instance Memory Stress
  - *Hogs the available free memory in the PCF app instances via a stress utility to simulate memory pressure/leaks. Withdraws the stress action and releases memory after the chaos duration*

### Network Manipulation Chaos

- App Instance Network Latency
  - *Injects the desired latency into a given PCF app instance's Network traffic, via a traffic-shaping utility. Simulates degraded/slow networks. Restores network characteristics after the chaos duration.*
    
- App Instance Network Packet Loss
  - *Injects the desired packet drop percentage into the PCF app instance's Network traffic, via a traffic-shaping utility. This fault can be used to simulate blackhole and split-brain conditions. Restores network characteristics after the chaos duration.*
    
- App Instance Network Packet Corruption
  - *Injects the desired packet corruption percentage into the PCF app instance's Network traffic, via a traffic-shaping utility. This fault can be used to test application stability while dealing with corrupted data over the network. Restores network characteristics after the chaos duration.*
    
- App Instance Network Packet Duplication
  - *Injects the desired packet duplication percentage into the PCF app instance's Network traffic, via a traffic-shaping utility. Restores network characteristics after the chaos duration.*
