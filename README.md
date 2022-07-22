# [ansible](https://docs.ansible.com)

<img src="Ansible_logo.svg" alt="">

Ansible is an IT automation tool. It can configure systems, deploy software, and orchestrate more advanced IT tasks such as continuous deployments or zero downtime rolling updates.

## commands

- ansible
  - runs an ad-hoc command
- ansible-doc
  - documentation tool
- ansible-playbook
  - Runs Ansible playbooks, executing the defined tasks on the targeted hosts.
- ansible-inventory
  - Show Ansible inventory information
- ansible-pull
- ansible-vault                                           
- ansible-config
- ansible-console
- ansible-connection
- ansible-galaxy
- ansible-test

## Concepts
### Control node
<img src="control.svg" alt="" width="100px">

### Agentless
<img src="ssh.svg" alt="" width="100px">

### Managed nodes
<img src="nodes.svg" alt="" width="100px">

### Inventory
<img src="inventory.svg" alt="" width="100px">

### Playbooks
<img src="playbook.svg" alt="" width="100px">

#### Plays
##### Roles
##### Tasks
##### Handlers
### Modules
### Plugins
### Collections
### AAP
## demo
`ansible-playbook ansible.yaml`
## connections
`ansible-doc -t connection -l`
```
ansible.netcommon.httpapi      Use httpapi to run command on network appliances                                                             
ansible.netcommon.libssh       (Tech preview) Run tasks using libssh for ssh connection                                                     
ansible.netcommon.napalm       Provides persistent connection using NAPALM                                                                  
ansible.netcommon.netconf      Provides a persistent connection using the netconf protocol                                                  
ansible.netcommon.network_cli  Use network_cli to run command on network appliances                                                         
ansible.netcommon.persistent   Use a persistent unix socket for connection                                                                  
community.aws.aws_ssm          execute via AWS Systems Manager                                                                              
community.docker.docker        Run tasks in docker containers                                                                               
community.docker.docker_api    Run tasks in docker containers                                                                               
community.docker.nsenter       execute on host running controller container                                                                 
community.general.chroot       Interact with local chroot                                                                                   
community.general.funcd        Use funcd to connect to target                                                                               
community.general.iocage       Run tasks in iocage jails                                                                                    
community.general.jail         Run tasks in jails                                                                                           
community.general.lxc          Run tasks in lxc containers via lxc python library                                                           
community.general.lxd          Run tasks in lxc containers via lxc CLI                                                                      
community.general.qubes        Interact with an existing QubesOS AppVM                                                                      
community.general.saltstack    Allow ansible to piggyback on salt minions                                                                   
community.general.zone         Run tasks in a zone instance                                                                                 
community.kubernetes.kubectl   Execute tasks in pods running on Kubernetes                                                                  
community.libvirt.libvirt_lxc  Run tasks in lxc containers via libvirt                                                                      
community.libvirt.libvirt_qemu Run tasks on libvirt/qemu virtual machines                                                                   
community.okd.oc               Execute tasks in pods running on OpenShift                                                                   
community.vmware.vmware_tools  Execute tasks inside a VM via VMware Tools                                                                   
community.zabbix.httpapi       Use httpapi to run command on network appliances                                                             
containers.podman.buildah      Interact with an existing buildah container                                                                  
containers.podman.podman       Interact with an existing podman container                                                                   
kubernetes.core.kubectl        Execute tasks in pods running on Kubernetes                                                                  
local                          execute on controller                                                                                        
paramiko_ssh                   Run tasks via python ssh (paramiko)                                                                          
psrp                           Run tasks over Microsoft PowerShell Remoting Protocol                                                        
ssh                            connect via SSH client binary                                                                                
winrm                          Run tasks over Microsoft's WinRM                                                                             

```

## tower

## Watson AI Ops 
