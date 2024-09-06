*Note: Assumes the vCenter user access for the experiments is equal to or greater than what is laid out [here](https://github.com/hce-docs/platform-wise-chaos-info/blob/main/VMware/vcenter-based-chaos-user-access-requirements.md)*

### VM State Manipulation Chaos

- VM Poweroff
  - *Performs a power off (i.e., vcenter-api-driven-shut-down operation) of the desired VM identified by its MOID (Managed Object ID). Restores the VM to a powered-on state after the chaos duration.*
    
- VM Process Kill (provided the process is itself not running as root)
  - *Kills a desired process in the VM, the process being identified either by name, ID or via process ID derivation command. Allows optional re-creation of the process via EoT (end-of-test) command hooks.*
    
- VM Disk Loss
  - *Detaches the desired disks attached to the VM, the disks being identified by their VMDK names. Re-attaches the disk to the VM after the chaos duration, with optional re-mount of the filesystems via EoT command hooks.*

### VM Resource Stress Chaos

- VM CPU Hog
  - *Hogs the desired number of CPU cores/load percentage within the VM via a stress utility, thereby depriving the application processes of CPU resources. Withdraws the stress action and releases CPU cycles after the chaos duration*
    
- VM Memory Hog
  - *Hogs the available free memory in the system via a stress utility to simulate memory pressure/leaks. Withdraws the stress action and releases memory after the chaos duration*

- VM Disk I/O Stress
  - *Performs heavy I/O operations on the desired filesystem mount path via a stress utility to simulate disk bandwidth issues, slowness, and noisy neighbor conditions. Withdraws the stress action after the chaos duration* 
