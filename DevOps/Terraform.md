Automate and manage infrastructure and platform, as well as the services running on it. 
Infrastructure as code (IaC)  - Code use to provision resources. 

It is declarative, define what results you are trying to achieve

Infrastructure provisioning. 
1. Prepare infrastructure - [[AWS]], [[Docker]] -> This is where you'd use Terraform 
	1. Create users and permissions, install docker, spin up servers. 
2. Deploy application / containers on infrastructure. 

Allows for changes to the infrastructure or replicating it e.g dev and prod env. 

Differences with [[Ansible]]
- Both infrastructure as code, handling automation for provisioning, configuring and managing infrastructure. 
- Terraform focuses on infrastructure provisioning
- Can deploy apps
- Ansible would be used later to configure the infrastructure. 
- Terraform is more advanced in orchestration. 

**How does it work**
- Core
	- Uses 2 input sources
	- TF Config where you define what needs to be provisioned
- State
	- Current state of the setup. 
- Compares current vs desired state and makes changes to make sure we get to the desired state. 
- 2nd part is the cloud providers, or [[IaaS]] / [[PaaS]] Kubernetes. 
- Access to over 100 Providers to over 1000s resources. 

Once core creates execution plan from config and state it executes it with the providers, carrying out the execution steps. 

In config file we define the resource and its attributes. 

**Declarative approach**
- We only define the end state in the config file. 
- No need to go over each step or how to get there. 
- Has major benefits when updating the infrastructure. - adjust config file and re-execute
- Allows you to always know the current setup, whilst keeping a small config file. 

**Commands**
- Refresh - query provider to get current state. 
- Plan - creates execution plan -> What actions are needed to achieve desired state. 
- Apply - executes the plan and applies it. 
- Destroy - destroy the resources and infrastructure.