

# **Optimizations and Performance**

## **Cloud Deployment Automation**

# Course Information

| Instructor | Tito Alvarez — [augusto.alvarez@galileo.edu](mailto:augusto.alvarez@galileo.edu) |
| :---- | :---- |
| Course Assistant | Abner Pérez — [abner.perez@galileo.edu](mailto:abner.perez@galileo.edu) |
| Trimester | Second Trimester — April 20 to June 26, 2026 |
| Schedule | Thursdays, 6:00 PM to 9:00 PM (Guatemala City time \- GMT-6) |
| Modality | Virtual (Zoom) for Sessions 1-4 and 6-9On-site for Sessions 5 and 10 |
| Program | PDDS — Second Trimester. |
| Minimum required attendance | 80% |

# Course Description

This course trains students to design and operate fully automated cloud deployment pipelines using industry-standard tools. While the official name is *Optimizations and Performance* (*Optimizaciones y Desempeño*), the primary focus of this optimization is cloud deployment automation: taking a cloud architecture design and turning it into a reproducible, one-click deployment using Terraform, GitHub Actions, and optionally Kubernetes via Amazon EKS or Google Kubernetes Engine.

Students work in the same teams as the concurrent course *Infraestructura en la Nube* (Cloud Infrastructure) and automate the full deployment of the system they design there. Each cloud component — compute, storage, databases, networking, asynchronous processing, security, and observability — is progressively automated throughout this course, with session topics deliberately scheduled one week after the equivalent topic in the cloud course. This ensures students are always automating services they have just understood architecturally.

The course culminates with a team presentation of a fully automated deployment pipeline: a single git push to the main branch that provisions all infrastructure, builds and pushes a container image, and deploys the complete system to the cloud from zero.

# Learning Objectives

By the end of the course, students will be able to:

* Write and organize Terraform configurations using modules, remote state backends, and CI-driven workflows.  
* Build GitHub Actions pipelines that validate, plan, and apply infrastructure changes automatically on every pull request and merge.  
* Automate the provisioning of compute, storage, database, networking, asynchronous processing, security, and observability components on AWS or Google Cloud.  
* Implement infrastructure security best practices: least-privilege IAM policies, Secrets Manager integration, KMS encryption, and OIDC-based CI authentication.  
* Define observable systems as code through CloudWatch log groups, metric filters, alarms, and cost budgets.  
* Understand Kubernetes fundamentals and, for the optional EKS track, provision and deploy containerized workloads as part of the automated pipeline.  
* Present and defend infrastructure design decisions to peers, articulating trade-offs and alternatives.

# Prerequisites

Students must be concurrently enrolled in *Infraestructura en la Nube*. The following background is assumed:

* Comfort with the Linux command line and basic shell scripting.  
* Working knowledge of Git and GitHub workflows: commits, branches, and pull requests.  
* Basic familiarity with cloud concepts: virtual machines, object storage, managed databases, and IAM.  
* Proficiency in at least one programming or scripting language.  
* An active AWS or Google Cloud account with permissions to create and destroy resources.

# Relationship with Cloud Infrastructure Course

This course runs in parallel with *Infraestructura en la Nube* and is structurally dependent on it. The project in this course is not a separate system. It is the automated deployment layer for the architecture that teams design in the cloud course. *Students do not choose a different project — they automate the same one*. 

# Course Schedule

| No. | Date | Modality | Topic |
| :---: | :---: | :---: | ----- |
| 1 | 04/23 | Zoom | IaC Philosophy and Terraform Foundations |
| 2 | 04/30 | Zoom | Kubernetes Basics and GitHub Actions CI |
| 3 | 05/07 | Zoom | Compute Automation and EKS Provisioning |
| 4 | 05/14 | Zoom | Storage and Database Automation with Remote State |
| 5 | 05/21 | On-site | Partial Exam and Mid-Course Presentations |
| 6 | 05/28 | Zoom | Networking Automation |
| 7 | 06/04 | Zoom | Asynchronous Infrastructure and Full CD Pipeline |
| 8 | 06/11 | Zoom | IAM as Code and Security Automation |
| 9 | 06/18 | Zoom | Observability Automation |
| 10 | 06/25 | On-site | Final Exam and Final Presentations |


# Assessment

| Component | Points | Qty | Total | Notes |
| ----- | :---: | :---: | :---: | ----- |
| In-class exercises | 1.25 | 16 | **20** | 2 exercises per session |
| Exams | 10 | 2 | **20** | 45-min on-site exams |
| Project deliveries | 8 | 5 | **40** | Project partial deliveries |
| Project presentations | 10 | 2 | **20** | On-site presentations |
| **Total** |  |  | **100** |  |

 

# Late Deliveries

In-class exercises and project deliveries may be submitted late. A correction factor will be applied as follows:

* **On-time submission:** full score  
* **Submitted up to 24 hours late:** 80% of the score  
* **Submitted up to one week late:** 50% of the score  
* **Submitted more than one week late:** no score

# Project Overview

The course project is the automated deployment layer for the cloud system that teams design in *Infraestructura en la Nube*. Teams of three students — the same teams as in the cloud course — build a Terraform codebase and a GitHub Actions pipeline that provisions and deploys their entire cloud architecture with a single push to the main branch.

The project does not prescribe which cloud system to build. That decision is made in the cloud course. This course prescribes how it must be deployed: infrastructure as code, an automated CI/CD pipeline, fully reproducible from zero, and covering all the required cloud components. Refer to the project document from *Infraestructura en la Nube* for the full specification of system requirements. That document governs the architecture; this course governs the automation.

*The project scope will be largely defined in its own separate project assignment documents (project deliveries).*

# Tools and Resources

The following tools are required for this course:

* Terraform CLI (latest stable version) — [developer.hashicorp.com/terraform](https://developer.hashicorp.com/terraform)  
* AWS CLI v2 or Google Cloud SDK (gcloud) — depending on the chosen cloud provider  
* Docker Desktop or Docker Engine — for building and testing container images  
* Git and a GitHub account — all project code must live in a GitHub repository  
* kubectl — required for the EKS track; recommended for all students  
* Visual Studio Code with the HashiCorp Terraform extension (recommended)

## Reference documentation:

* Terraform documentation — [developer.hashicorp.com/terraform/docs](https://developer.hashicorp.com/terraform/docs)  
* AWS Provider for Terraform — [registry.terraform.io/providers/hashicorp/aws](https://registry.terraform.io/providers/hashicorp/aws)  
* Google Provider for Terraform — [registry.terraform.io/providers/hashicorp/google](https://registry.terraform.io/providers/hashicorp/google)  
* GitHub Actions documentation — [docs.github.com/en/actions](https://docs.github.com/en/actions)  
* AWS Well-Architected Framework — [aws.amazon.com/architecture/well-architected](https://aws.amazon.com/architecture/well-architected)  
* Kubernetes documentation — [kubernetes.io/docs/home](https://kubernetes.io/docs/home)  
* terraform-aws-modules on GitHub — [github.com/terraform-aws-modules](https://github.com/terraform-aws-modules) (EKS, VPC, RDS, and others)

# Academic Integrity

All submitted work must be the original work of the team. Teams may discuss approaches and concepts with other teams, but all code, configuration files, and written summaries must be written independently. Use of AI-assisted coding tools is permitted and encouraged, provided that every team member understands and can explain any code or configuration submitted. Presenting infrastructure code that a team member cannot explain during a presentation or exam is treated as a violation of academic integrity.

Direct copying of Terraform code or pipeline definitions between teams will result in a grade of zero for all involved parties for the affected delivery, with no opportunity for resubmission.

# Communication with Instructors

Course and project questions should be posted in the [WhatsApp group](https://chat.whatsapp.com/IWYD4S45avV6Vhui8BztGN) to encourage group discussion and benefit all students. **Direct private messages via WhatsApp to instructors about course content or assignments are discouraged.**

For matters regarding grades or special accommodations, email both instructors: [augusto.alvarez@galileo.edu](mailto:augusto.alvarez@galileo.edu) and [abner.perez@galileo.edu](mailto:abner.perez@galileo.edu).

