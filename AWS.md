---
sticker: lucide//cloud-cog
---
Centralised security services and features - Allows to increase security
Reliability - Reduced tasks because AWS manages data centres. 
High availability and fault tolerance. 
Elasticity - Scale out performance or scale in for costs. 
Agility - Democratised advanced technologies, making them easier to adopt. 
PAYG pricing. 
Scalability - Horizontal scaling. 
Global reach 
Economy of scale

**Benefits**
- Cost transparency. 
- Switch tech as new tech becomes available. 
- Automatic recovery. 
- Global deployment without data centre management. 

**Cloud adoption framework**
- Business 
- People
- Governance
- Platform
- Security
- Operations 

To migrate storage consider the following:
- Cost
- Time
- Downtime
- Tools
- Security

DMS - Data migration service

**Cloud migration**
- Rehost - Migrate to EC2 with little changes
- Replatform - Change platform, with little changes
- Repurchase 
- Refactor - 
- Retire
- Retain - Keep running on prem
**Types of migration
- Physical to virtual - can be manual or automatic
- Virtual to virtual - Can be on prem 
- Cloud to Cloud - uncommon, Tools are not really provided for it

Pay less, using more - Storage and network traffic
Reservations to get discount - 1 to 3 years. 

Configuration drift causes instability 
KTLO often deals with licensing
AWS responsible for compliance 

**Design principles**
- Stop guessing capacity needs. 
- Test systems at production scale. 
- Automate. 
- Allow for evolutionary architecture. 
- Drive architectures using data. - Data driven improvement possibilities
- Improve through game days - Validate test on infrastructure frequently

**Well architected framework**
- Best practices for architecture
- Operational excellence - 
- Security
- Reliability - HA
	- Operate and test workload through life cycle
	- Scale horizontally
	- Automatically recover from failure
	- Manage change using automation. 
- Performance efficiency
- Cost optimisation
	- Deliver value at lowest price
	- Consumption model
	- Measure efficiency
	- Analyse and attribute expenditure
	- Use managed services to reduce cost of ownership
- Sustainability 
	- Focus on env impact - Energy consumption
	- Establish sustainability goals
	- Employ more efficient hardware and software offerings. 
## Security and compliance
**Shared responsibility model**
- AWS
	- Security of the cloud
	- Physical and environmental controls 
- Customer 
	- Security in the cloud
	- Region choices
	- Service features 
- Patching, config management and training is a shared responsibility. 
- Managed service has the least, Container service is a 50/50, [[IaaS]]has the most. 

**Compliance**
- Portals - Gives all docs needed for compliance. 
- Whitepapers
- Compliance programs - Frameworks (SOC, HIPAA)
- Region does not indicate if service is compliant, or if all features are. 

**Strategies**
- At rest encryption - EBS, EFS, RDS, SSE for storage and data
- In transit encryption - TLS on gateways, load balancers. 
- AWS Certificate Manager to create certificates. 
- [[Least Privilege]]
	- [[RBAC]] - Group memberships, instance profiles, federated identities. 
	- ABAC - Attribute based, access based on properties e.g. principal or resource tags. 
- AWS Security services
	- IAM Access analyser - Discovers cross account access permissions,
	- AWS Config - Inventory resources and identify their associations. 
	- Amazon Macies - Data classification in S3, find sensitive data and analyses access permissions
	- Guard Duty - AWS workload and credentials protection using ML
	- Inspector - Finds vulnerabilities in workloads as well as network exposure, CVE
	- Security Hub - Collections of all the security services, 
	- Detective - Visualisation allowing for analysis
	- Audit manager - Compliance specific reports 
	- Artifact - enabled by default for AWS security and compliance
	- Shield - [[DoS]] protection

**Access Management**
- AWS credentials and MFA
- AWS account - Container for resources, associated with only one account, cannot transfer ownership, allowing for organisation, billing and access. 
- Amazone Resource Name (ARN)
- AWS Root Account 
	- Use a distribution list for email or alias.  
	- Access to unique tasks e.g. Change account settings, Billing and Cost management, GovCloud, Close AWS Account. 
- Static and temporary ID  
- Can use Console, CLI and SDK to access AWS Services
- Can configure password policy. 
- AWS IAM - Identity and access management. 
	- AuthN
	- AuthZ
	- IAM User - Principal identity, associated with permissions, container for credentials. 
	- IAM Groups - Collection of users with similar permissions, No nested groups allowed. 
	- IAM Role - Identity, needs to be assumed by others. Similar to run as Admin. 
	- Managed policies - VC, Standalone resource, AWS or Customer managed. 
	- Inline policy - Embedded in IAM user, no VC. 

**Security support resources**
- VPC - Route tables
- NACLS
- Subnets 