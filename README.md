# Jenkins agent role

This directory contains role used for setting up jenkins agent.

[Ansible role by lean-delivery](https://github.com/lean-delivery/ansible-role-jenkins-slave) was used as reference.

Available tags:
```
- setup
- add-agent
```

Available variables:
```
#Add jenkins agent node to master node
add_jenkins_node: true

#SSH keys that will be added to authorized
jenkins_user_auth_pubkeys: |
    ssh-rsa AAAAB3Nza... username@your-machine1
    ssh-rsa AAAAB3Nza... username@your-machine2

#Credentials for Jenkins master
master_username: "admin"
master_password: "d73ef534f98349d2835ae49abf8d473d"
master_url: "https://jenkins.k8s.myhomelab.xyz/"

#Name for jenkins agent node
node_agent_name: testing-ansible

#Agent labels
node_linux_labels:
    - molecule-virtualbox

#Agent homedir
node_linux_home: /home/jenkins

#Available executors
node_executors_num: 6
```