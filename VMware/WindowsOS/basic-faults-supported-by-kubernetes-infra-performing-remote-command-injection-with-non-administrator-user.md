*Note: Assumes the vCenter user access for the experiments is equal to or greater than what is laid out [here](https://github.com/hce-docs/platform-wise-chaos-info/blob/main/VMware/vcenter-based-chaos-user-access-requirements.md)*

### VM State Manipulation Chaos

- VM Poweroff
  - *Performs a power off (i.e., vcenter-api-driven-shut-down operation) of the desired VM identified by its MOID (Managed Object ID). Restores the VM to a powered-on state after the chaos duration.*
    
- VM Process Kill (provided the process is itself not running as administrator)
  - *Kills a desired process in the VM, the process being identified either by name, ID, or via process ID derivation command. Allows optional re-creation of the process via EoT (end-of-test) command hooks.*
     
- VM Service Stop
  - *Stops a desired service within the VM, the service being identified by service name. Allows optional service restart (if no self-healing is built in already) via EoT command hooks.*
     
- VM Disk Loss
  - *Detaches the desired disks attached to the VM, the disks being identified by their VMDK names. Re-attaches the disk to the VM after the chaos duration, with optional re-mount of the filesystems via EoT command hooks.* 

### VM Resource Stress Chaos

- VM CPU Hog
  - *Hogs the desired number of CPU cores/load percentage within the VM via a stress utility, thereby depriving the application processes of CPU resources. Withdraws the stress action and releases CPU cycles after the chaos duration*
