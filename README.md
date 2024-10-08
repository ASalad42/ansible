# Ansible

![image](https://github.com/user-attachments/assets/c7b133ea-5d25-4c39-927d-1911da8bcc9d)


- Control node: server which has ansible installed 
- Managed nodes: remote hosts/servers which are configured 
- two ways to configure in ansible: Ad-hoc commands (Command-line) or Playbooks
- Tasks: things  that need to be configured on remote servers (using playbooks). playbook have hosts, play name and tasks. 
- The remote servers or hosts which need to be configured are in the Inventory. 
- Dynamic Inventory: used if hosts are running on top of the cloud or in a container engine where the hosts are up and down frequently

## Set up Ansible Stack
![image](https://github.com/user-attachments/assets/e39a904b-1532-4155-b2f1-12de277277a4)
![image](https://github.com/user-attachments/assets/55caa534-facc-45f5-84b5-72344c77e188)
![image](https://github.com/user-attachments/assets/4f62bd5d-cff7-44c9-9727-99688e8239ff)


- scp -i C:\Users\AyanleSalad\.ssh\ansible-key.pem C:\Users\AyanleSalad\.ssh\ansible-key.pem ubuntu@52.215.75.9:/home/ubuntu/.ssh/
- ![image](https://github.com/user-attachments/assets/fb8174ae-4332-4960-bcf7-44409af8381b)
- sudo nano /etc/ansible/hosts
- chmod 600 /home/ubuntu/.ssh/ansible-key.pem
- ansible servers -m ping
- ansible all -m ping
- ![image](https://github.com/user-attachments/assets/fa16ef1d-1738-4a69-8fda-96b047387aa0)
- ansible all -a "df -h" -u ubuntu
- ![image](https://github.com/user-attachments/assets/70132bd4-c90c-4dd1-b988-62eec96f7ba5)

## Deploy simple html webpage on servers using Ansible
- ansible-playbook web.yml
- ![image](https://github.com/user-attachments/assets/0be0e1d1-aaad-4818-80e7-390ba45bc088)
- ![image](https://github.com/user-attachments/assets/6e202823-e4c7-40f4-aa9a-612789b0411f)
- ![image](https://github.com/user-attachments/assets/71014198-cd95-45ce-add6-e9be6b51d625)

## Install DevOps tools on servers using Ansible
- ansible-playbook dev.yml
- ![image](https://github.com/user-attachments/assets/a4f6b8b3-8400-489d-b290-ee934a481975)
- ![image](https://github.com/user-attachments/assets/38476608-3d28-48a2-b0c9-a99ed9cbe06b)

## Using Ansible - setup server monitoring with Prometheus and Grafana 

- ansible-vault encrypt_string "password" --ask-vault-pass
- ansible-playbook -i ansible/inventories/hosts.yml -u TheUserToExecuteWith ansible/playbooks/monitoring.yml -t controller --ask-vault-pass
- ansible-playbook -i ansible/inventories/hosts.yml -u TheUserToExecuteWith ansible/playbooks/monitoring.yml -t target --ask-vault-pass









