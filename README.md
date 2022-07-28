# [ansible](https://docs.ansible.com)
<img src="Ansible_logo.svg" alt=""> | Ansible is an IT automation tool. It can configure systems, deploy software, and orchestrate more advanced IT tasks such as continuous deployments or zero downtime rolling updates.
-----------------------------------|-----------------------------------|

## commands
- ansible
  - runs an ad-hoc command
  - `ansible all -m ping`
- ansible-doc
  - documentation tool
- ansible-playbook
  - Runs Ansible playbooks, executing the defined tasks on the targeted hosts.
- ansible-inventory
  - Show Ansible inventory information
- ansible-pull
  - pulls playbooks from a VCS repo and executes them for the local host
- ansible-vault
  - encryption/decryption utility for Ansible data files
- ansible-config
  - View ansible configuration
- ansible-console
  - REPL console for executing Ansible tasks
- ansible-galaxy
  - Perform various Role and Collection related operations.
- ansible-test
- ansible-connection

## [Concepts](https://docs.ansible.com/ansible-core/devel/getting_started/index.html)
### [Control node](https://docs.ansible.com/ansible-core/devel/installation_guide/intro_installation.html)
<img src="control.svg" alt="" width="100px"> | From the control node, Ansible can manage an entire fleet of machines and other devices </br>`sudo dnf install ansible`</br>[ansible.cfg](ansible.cfg)
-----------------------------------|-----------------------------------|

### [Agentless](https://docs.ansible.com/ansible-core/devel/user_guide/connection_details.html)
<img src="ssh.svg" alt="" width="100px"> | with SSH, Powershell remoting, and numerous other transports, all from a simple command-line interface with no databases or daemons required.
-----------------------------------|-----------------------------------|

### [Inventory](https://docs.ansible.com/ansible-core/devel/user_guide/intro_inventory.html#intro-inventory)
<img src="inventory.svg" alt="" width="100px"> | a list of servers and devices to automate. </br>[/etc/ansible/hosts](inventory) </br>`ansible-playbook -i /path/to/my_inventory_file`
-----------------------------------|-----------------------------------|

### [Playbooks](https://docs.ansible.com/ansible-core/devel/playbook_guide/index.html)
<img src="playbook.svg" alt="" width="100px"> | Playbooks are automation blueprints, in YAML format, that Ansible uses to deploy and configure nodes in an inventory. [ansible.yaml](ansible.yaml) [facts.yaml](facts.yaml)
-----------------------------------|-----------------------------------|

- Plays
  - The Play contains variables, roles and an ordered lists of tasks and can be run repeatedly.
- Roles
  - A limited distribution of reusable ansible content (tasks, handlers, variables, plugins, templates and files) for use inside of a Play.
- Tasks
  - The definition of an ‘action’ to be applied to the managed host. Tasks must always be contained in a Play, directly or indirectly (Role, or imported/included task list file). 
- Handlers
  - Special form of a Task, that only execute when notified by a previous task which resulted in a ‘changed’ status.

### [Modules](https://docs.ansible.com/ansible-core/devel/user_guide/modules_intro.html)
<img src="module.svg" alt="" width="200px">  | Modules (also referred to as “task plugins” or “library plugins”) are discrete units of code that can be used from the command line or in a playbook task. Ansible executes each module, usually on the remote managed node, and collects return values.
-----------------------------------|-----------------------------------|
### [Plugins](https://docs.ansible.com/ansible-core/devel/plugins/plugins.html#working-with-plugins)
Plugins are pieces of code that augment Ansible’s core functionality. Ansible uses a plugin architecture to enable a rich, flexible and expandable feature set.
### [Collections](https://docs.ansible.com/ansible-core/devel/user_guide/collections_using.html#collections)
Collections are a distribution format for Ansible content that can include playbooks, roles, modules, and plugins.
## demo
<img src="demo.svg" alt="">

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

