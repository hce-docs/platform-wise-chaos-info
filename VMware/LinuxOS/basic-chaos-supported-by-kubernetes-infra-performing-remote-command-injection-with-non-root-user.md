*Note: Assumes the vCenter user access for the experiments is equal to or greater than what is laid out [here](https://github.com/hce-docs/platform-wise-chaos-info/blob/main/VMware/vcenter-based-chaos-user-access-requirements.md)*

### VM State Manipulation Chaos

- VM Poweroff
- VM Process Kill (provided the process is itself not running as root) 
- VM Disk Loss

### VM Resource Stress Chaos

- VM CPU Hog
- VM Memory Hog
- VM Disk I/O Stress
