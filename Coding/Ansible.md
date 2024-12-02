Tool to manage cloud and on-prem infrastructure, allows for cross platform automation of infrastructure management and configuration tasks, at a scale.

Config management, infrastructure provisioning and application deployment (Hybrid, on-prem, IoT)

Control and managed nodes.

Connects from control node, any machine with Ansible installed, to the managed nodes, sending command instructions to them. 

Modules - Units of code that are executed on managed nodes. 
Each module is invoked by a task. 
Ordered list of tasks create a playbook.  

Write playbooks with tasks and modules to define state of the systems. 

Machines are represented in inventory file, grouping nodes into categories. 

Uses [[YAML]]to define playbooks in human readable data format. 

No installation of extra agents on managed nodes is needed. 

Only thing needed is a terminal and text editor to define configuration files. 

**Advantages of Ansible**
- Free and open source
- Well tested
- Easy to start
- Simple deployment, without needing extra agents
- Features with modularity and reusability. 
- Extensively documented. 

Written in Python, 
Focus on security and reliability. 
OpenSSH for transport

