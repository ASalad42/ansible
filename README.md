# Ansible

- Control node: server which has ansible installed 
- Managed nodes: remote hosts/servers which are configured 
- two ways to configure in ansible: Ad-hoc commands (Command-line) or Playbooks
- Tasks: things  that need to be configured on remote servers (using playbooks). playbook have hosts, play name and tasks. 
- The remote servers or hosts which need to be configured are in the Inventory. 
- Dynamic Inventory: used if hosts are running on top of the cloud or in a container engine where the hosts are up and down frequently
