# Cloud-I-nfrastucture-migration-project-Telco
Telco Cloud Migration Project Profile
1.	Telco Company Name: Telco net company
2.	Cloud Model: Hybrid Cloud (Private Cloud for core services + Public Cloud for CRM/Analytics)
3.	Main Drivers:
o	Legacy infrastructure modernization
o	Improved service agility
o	Reduced CAPEX
o	M-PESA/Fintech integration
4.	Migration Strategy:
o	Lift & Shift for OSS/Network systems
o	Replatforming for BSS & CRM (e.g., to microservices on Kubernetes)
5.	Key Systems to be Migrated:
o	OSS/BSS
o	CRM with M-PESA Integration
o	Network Element Manager (NEM)
o	Customer Support Portal & Billing Engine
6.	Cloud Provider:
o	AWS for public-facing services
o	Private Cloud using OpenStack hosted in Nairobi data center
7.	Project Duration: 9 Months
8.	Team Size:
o	1 Project Manager
o	2 Cloud Architects
o	3 DevOps Engineers
o	2 QA/Testers
o	1 Data Security Officer
o	1 Business Analyst
o	Vendor Consultants
9.	Regulatory Scope:
o	GDPR
o	ISO 27001
o	CAK Compliance (Communications Authority of Kenya)
# Cloud Infrastructure Migration Project - Telco

##  Purpose of the Project

The goal of this project is to simulate a full-scale migration of an on-premises telco IT infrastructure to the cloud. This includes the planning, execution, governance, and closure phases of a cloud migration project tailored to the telecommunications industry. The project follows best practices in cloud security, stakeholder engagement, and IT service management.

This repository demonstrates the structured delivery of cloud migration using a phased project management approach, ensuring minimal downtime, compliance with regulatory standards, and a secure, scalable infrastructure.

---

## 🛠️ Tools and Technologies Used

| Category               | Tools/Technologies                                               |
| ---------------------- | ---------------------------------------------------------------- |
| Cloud Platform         | **Simulated AWS/Azure** (no real infra used for privacy reasons) |
| Infrastructure-as-Code | **Terraform** (sample provided below)                            |
| Project Management     | **GitHub Projects**, **Excel-based plans**                       |
| Security               | IAM Policy Design (Role-Based Access Control)                    |
| Documentation          | Word Docs, Markdown                                              |
| Architecture           | Draw\.io, Lucidchart (sample diagrams)                           |

---

##  Summary of Phases

### 1. **Initiation Phase**

* Project Charter
* Stakeholder Register
* High-level requirements and constraints

### 2. **Planning Phase**

* Communication Plan
* Risk Management Plan
* Migration Strategy (Lift-and-Shift)
* Budget and Timeline (Gantt Chart)
* Security Plan (IAM, Encryption)

### 3. **Execution Phase**

* Knowledge Transfer Planning
* Infrastructure Simulation (Terraform Sample)
* Cloud Asset Inventory
* Compliance Mapping

### 4. **Monitoring & Control**

* Issue and Risk Logs
* Progress Tracking (GitHub Projects)
* Quality Checks (Document Audits)

### 5. **Closure Phase**

* Post-Implementation Review
* Benefits Realization Report
* Transition to Operations
* Stakeholder Satisfaction Survey

---

##  Real-World Relevance

This project reflects real-world enterprise cloud migration practices including:

* End-to-end lifecycle documentation
* Alignment with ISO 27001 and GDPR principles
* Use of risk registers, stakeholder engagement models
* Governance of telco-specific systems like OSS/BSS, M-PESA/CRM integration
* Consideration of hybrid cloud models and business continuity

---

## Sample Infrastructure-as-Code (Terraform)

```hcl
provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "telco_web" {
  ami           = "ami-0c55b159cbfafe1f0" # example AMI ID
  instance_type = "t2.micro"

  tags = {
    Name = "TelcoWebServer"
  }
}
```

> Note: This is a mock configuration. In real production, modules and VPCs would be included.

---

##  Agile Tracking (GitHub Projects)

* Tasks and issues are organized in [GitHub Projects](https://github.com/BarbaraMalei07/Cloud-I-nfrastucture-migration-project-Telco/projects)
* Kanban style: Backlog → In Progress → Review → Done
* Issues used to simulate user stories and blockers

---

## Architecture and IAM Diagrams

###  Cloud Architecture (Lift-and-Shift - Simulated)

* On-prem servers → AWS EC2 instances
* Database → RDS
* CRM/M-PESA APIs routed via API Gateway
* IAM for role-based access to CloudOps team

![Cloud Architecture](docs/cloud-architecture-diagram.png)

### IAM Policy Snapshot

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": ["ec2:StartInstances", "ec2:StopInstances"],
      "Resource": "*"
    }
  ]
}
```

---

##  Next Steps

* Upload Terraform-based automation for backup and monitoring
* Add detailed simulation logs
* Upload diagrams to `/docs` folder
* Implement GitHub Actions for auto-validation of configs

---

##  Author

**Barbara Malei**
Cloud/IT Project Manager
[GitHub Profile](https://github.com/BarbaraMalei07)


