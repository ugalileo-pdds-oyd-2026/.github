# Optimizaciones y Desempeño | Optimizations and Performance - Cloud Deployment Automation | 2026

This repository belongs to the `ugalileo-pdds-oyd-2026` organization and serves as the central hub for demos and solved exercises for the course.

The primary focus of this optimization is cloud deployment automation: taking a cloud architecture design and turning it into a reproducible, one-click deployment using Terraform, GitHub Actions, and optionally Kubernetes via Amazon EKS or Google Kubernetes Engine.

## Course Context

* **University:** Universidad Galileo
* **Faculty:** Facultad de Ingeniería de Sistemas, Informática y Ciencias de la Computación (FISICC)
* **Program:** Postgrado en Diseño y Desarrollo de Software (PDDS)
* **Trimester:** Second Trimester - April 20 to June 26, 2026
* **Instructor:** [Tito Alvarez](https://github.com/jatitoam) (augusto.alvarez@galileo.edu)
* **Course Assistant:** [Abner Pérez](https://github.com/abner-perez) (abner.perez@galileo.edu)

## Prerequisite Tools

To utilize the demos and exercises found in this repository, you must have the following tools installed:

* Terraform CLI (latest stable version)
* AWS CLI v2 or Google Cloud SDK (gcloud)
* Docker Desktop or Docker Engine
* Git
* kubectl

## Content Index

Materials are organized based on the course schedule and topics:

* **IaC Philosophy and Terraform Foundations:** Introduction to Infrastructure as Code and Terraform basics.
* **Kubernetes Basics and GitHub Actions CI:** Fundamentals of K8s and setting up Continuous Integration pipelines.
* **Compute Automation and EKS Provisioning:** Automating compute resources and provisioning Amazon EKS clusters.
* **Storage and Database Automation with Remote State:** Handling persistent storage, databases, and managing Terraform remote state.
* **Networking Automation:** Automating networking components.
* **Asynchronous Infrastructure and Full CD Pipeline:** Setting up asynchronous processing infrastructure and completing the continuous deployment pipeline.
* **IAM as Code and Security Automation:** Implementing security best practices through Identity and Access Management (IAM) as code.
* **Observability Automation:** Automating logs, metrics, and alarms.

## Solved Exercises

Reference solutions for in-class exercises, organized by session. Each solution repository contains a step-by-step commit history and the teacher's commentary explaining the intent behind each task.

| # | Exercise | Session | Description |
|:-:|----------|:-------:|-------------|
| 1.1 | [What Will Terraform Do?](https://github.com/ugalileo-pdds-oyd-2026/exercise-1-1) | 1 | Builds Terraform plan literacy without touching real infrastructure. Students read and interpret a `terraform plan` output — decoding `+`, `~`, and `-/+` symbols, explaining `(known after apply)` values, and articulating the critical difference between in-place updates and destroy-and-recreate. Reinforces that `plan` is a safe, read-only operation that never writes state. |
| 1.2 | [Break Apart the Monolith](https://github.com/ugalileo-pdds-oyd-2026/exercise-1-2) | 1 | Addresses the most common day-one Terraform anti-pattern: the single-file configuration. Students split a monolithic `everything.tf` into purpose-specific files (`provider.tf`, `variables.tf`, `locals.tf`, `main.tf`, `outputs.tf`), parameterize all hardcoded values with variables and locals, and use `tfvars` files to show that environment promotion becomes a single flag change — no code edits required. |

## Academic Integrity Policy

While this repository hosts solved exercises, please adhere to the course academic integrity standards:

* All submitted work must be the original work of the team.
* Although teams may discuss approaches and concepts, all code, configuration files, and written summaries must be written independently.
* Direct copying of Terraform code or pipeline definitions between teams is prohibited.
* **Note on AI:** Use of AI-assisted coding tools is permitted and encouraged, provided that every team member understands and can explain any code or configuration submitted. Presenting infrastructure code that a team member cannot explain during a presentation or exam is treated as a violation of academic integrity.
