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

# Cloud Infrastructure Migration Project - Telco

## 🚀 Purpose of the Project

The goal of this project is to simulate a full-scale migration of an on-premises telco IT infrastructure to the cloud. This includes the planning, execution, governance, and closure phases of a cloud migration project tailored to the telecommunications industry. The project follows best practices in cloud security, stakeholder engagement, and IT service management.

This repository demonstrates the structured delivery of cloud migration using a phased project management approach, ensuring minimal downtime, compliance with regulatory standards, and a secure, scalable infrastructure.

---

## 🛠️ Tools and Technologies Used

| Category               | Tools/Technologies                                               |
| ---------------------- | ---------------------------------------------------------------- |
| Cloud Platform         | **Simulated AWS/Azure** (no real infra used for privacy reasons) |
| Infrastructure-as-Code | **Terraform**, **AWS CLI**, **CloudFormation (planned)**         |
| CI/CD Automation       | **GitHub Actions**, **Shell Scripts** (mocked)                   |
| Monitoring & Logging   | **CloudWatch** (planned), **Prometheus**/**Grafana** (simulated) |
| Project Management     | **GitHub Projects**, **Excel-based Gantt Charts**                |
| Security               | IAM Policy Design, RBAC, Encryption (at-rest + in-transit)       |
| Documentation          | Word Docs, Markdown, PDF                                         |
| Architecture           | Draw\.io, Lucidchart (see `/docs/architecture`)                  |

---

## 📌 Summary of Phases

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
* GitHub Actions CI/CD Pipeline
* Cloud Asset Inventory
* Compliance Mapping

### 4. **Monitoring & Control**

* Issue and Risk Logs
* GitHub Issues / Agile Tracking
* Quality Checks (Document Audits)
* Logging & Observability Strategy

### 5. **Closure Phase**

* Post-Implementation Review
* Benefits Realization Report
* Transition to Operations
* Stakeholder Satisfaction Survey

---

## 🌍 Real-World Relevance

This project reflects real-world enterprise cloud migration practices including:

* End-to-end lifecycle documentation
* Alignment with ISO 27001, GDPR, and telco-specific compliance
* Use of risk registers, stakeholder engagement models
* Governance of telco-specific systems like OSS/BSS, M-PESA/CRM integration
* Infrastructure automation (Terraform, GitHub Actions)
* Monitoring/observability (planned with Grafana/CloudWatch)

---

## 💻 Sample Infrastructure-as-Code (Terraform)

```hcl
provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "telco_web" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"

  tags = {
    Name = "TelcoWebServer"
  }
}
```

> Note: Additional Terraform files planned for:
>
> * VPC and Subnets
> * IAM Role creation
> * S3 backup bucket
> * RDS setup (mocked)

---

## ⚙️ Sample CI/CD Workflow (GitHub Actions)

```yaml
name: Terraform Apply
on:
  push:
    branches: [ "main" ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repo
        uses: actions/checkout@v2

      - name: Setup Terraform
        uses: hashicorp/setup-terraform@v1

      - name: Terraform Init & Apply
        run: |
          terraform init
          terraform apply -auto-approve
```

> Note: This simulates automated infrastructure deployment during execution phase.

---

## 📊 Agile Tracking (GitHub Projects & Issues)

* A Kanban board is used for tracking: [GitHub Projects Board](https://github.com/BarbaraMalei07/Cloud-I-nfrastucture-migration-project-Telco/projects)
* Issues simulate user stories and blockers such as:

  * "Create Terraform Plan for RDS"
  * "Simulate IAM Role Permissions"
  * "Update Risk Log for vendor delays"
* Labels used: `risk`, `infrastructure`, `documentation`, `high-priority`

---

## 🖼️ Architecture and IAM Diagrams

### 🧱 Cloud Architecture (Lift-and-Shift - Simulated)

* On-prem servers → AWS EC2 instances
* Database → RDS
* CRM/M-PESA APIs routed via API Gateway
* IAM for role-based access to CloudOps team

![Cloud Architecture](docs/cloud-architecture-diagram.png)

### 🔐 IAM Policy Snapshot

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

## 🗂 Directory Structure (Planned)

```
├── README.md
├── /terraform
│   └── main.tf
├── /.github/workflows
│   └── terraform.yml
├── /docs
│   ├── cloud-architecture-diagram.png
│   └── iam-role-diagram.png
├── /phases
│   ├── initiation
│   ├── planning
│   ├── execution
│   └── closure
```

---

## 📎 Next Steps

* Add full Terraform modules for VPC, IAM, S3, and RDS
* Add simulated logs and monitoring dashboards
* Implement cost estimator using AWS Pricing Calculator
* Enable GitHub Actions secrets for AWS access
* Upload architecture diagrams to `/docs`
* Track all tasks using Issues with due dates and assignees

---

## 👩‍💻 Author

**Barbara Malei**
Cloud/IT Project Coordinator | Aspiring Senior Cloud PM
[GitHub Profile](https://github.com/BarbaraMalei07)

---

Feel free to raise issues or fork the repo to contribute! ☁️


