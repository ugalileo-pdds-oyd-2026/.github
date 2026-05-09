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

## Class Demos

Live-coded walkthroughs from each session, organized by topic. Each repository captures the full demo in a step-by-step commit history.

### Session 1 — IaC Philosophy and Terraform Foundations

* **[Demo 1: Terraform Core Mechanics](https://github.com/ugalileo-pdds-oyd-2026/session-1-demo-1-terraform-core-mechanics):** Introduces Infrastructure as Code and walks through the full Terraform lifecycle — init, validate, plan, apply, and state inspection — using a single AWS S3 bucket as the target resource.
* **[Demo 2: Terraform Monolith Split](https://github.com/ugalileo-pdds-oyd-2026/session-1-demo-2-terraform-monolith-split):** Refactors a working but monolithic `everything.tf` into purpose-specific files (provider, variables, locals, main, outputs) and environment-specific tfvars, showing how proper structure makes a configuration maintainable and environment-promotable without any logic changes.

### Session 2 — Kubernetes Basics and GitHub Actions CI

* **[Demo 1: Kubernetes with FastAPI](https://github.com/ugalileo-pdds-oyd-2026/session-2-demo-1-k8s-fastapi):** Containerizes a Python FastAPI application and deploys it to a local Kubernetes cluster, covering the core K8s objects — Namespace, ConfigMap, Deployment, Service — and how environment variables flow from a ConfigMap into a running container.
* **[Demo 2: Terraform CI with GitHub Actions](https://github.com/ugalileo-pdds-oyd-2026/session-2-demo-2-github-actions):** Builds a GitHub Actions CI pipeline for Terraform incrementally on a live PR — from format checks and validation to posting the plan output as a collapsible PR comment — covering secrets injection, action version pinning, and safe pipeline design.

### Session 3 — Compute Automation and EKS Provisioning

* **[Demo 1: EC2 Module](https://github.com/ugalileo-pdds-oyd-2026/session-3-demo-1-ec2):** Deploys a Go HTTP server to a Graviton2 EC2 instance using a self-contained Terraform module that provisions the full IAM chain, security groups, and user-data bootstrap — illustrating how Terraform resolves resource creation order from the dependency graph.
* **[Demo 2: Lambda + API Gateway](https://github.com/ugalileo-pdds-oyd-2026/session-3-demo-2-lambda):** Runs the same Go handler on AWS Lambda fronted by API Gateway v2, using Go build tags to switch entrypoints without touching business logic, with all infrastructure provisioned by a Terraform module.
* **[Demo 3: ECS Fargate + ALB](https://github.com/ugalileo-pdds-oyd-2026/session-3-demo-3-ecs):** Deploys the containerized Go service on ECS Fargate behind an Application Load Balancer, covering the distinction between execution and task IAM roles, ARM64 runtime configuration, and an explicit `depends_on` that Terraform cannot infer from references alone.
* **[Demo 4: EKS Cluster](https://github.com/ugalileo-pdds-oyd-2026/session-3-demo-4-eks):** Provisions an EKS cluster with Terraform and deploys the same Go API via Kubernetes manifests, showing how the two automation layers — Terraform for the platform, manifests for the application — work together and where their responsibilities divide.

## Solved Exercises

Reference solutions for in-class exercises, organized by session. Each solution repository contains a step-by-step commit history and the teacher's commentary explaining the intent behind each task.

### Session 1 — IaC Philosophy and Terraform Foundations

* **[Exercise 1.1: What Will Terraform Do?](https://github.com/ugalileo-pdds-oyd-2026/exercise-1-1):** Builds Terraform plan literacy without touching real infrastructure — students read and interpret a plan output, decode the `+`, `~`, and `-/+` symbols, and articulate why `plan` is a safe, read-only operation that never writes state.
* **[Exercise 1.2: Break Apart the Monolith](https://github.com/ugalileo-pdds-oyd-2026/exercise-1-2):** Splits a single-file Terraform configuration into purpose-specific files, parameterizes all hardcoded values with variables and locals, and uses tfvars files to demonstrate that environment promotion requires no code changes at all.

## Academic Integrity Policy

While this repository hosts solved exercises, please adhere to the course academic integrity standards:

* All submitted work must be the original work of the team.
* Although teams may discuss approaches and concepts, all code, configuration files, and written summaries must be written independently.
* Direct copying of Terraform code or pipeline definitions between teams is prohibited.
* **Note on AI:** Use of AI-assisted coding tools is permitted and encouraged, provided that every team member understands and can explain any code or configuration submitted. Presenting infrastructure code that a team member cannot explain during a presentation or exam is treated as a violation of academic integrity.
