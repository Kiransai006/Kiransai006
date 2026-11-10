<h1 align="center">Kiran Subrahamanya Sai Bandaru</h1>

<p align="center">
  <b>DevOps Engineer</b> · Kubernetes · Terraform · CI/CD · GitOps · AWS &amp; Azure
  <br/>
  Dublin, Ireland · Open to DevOps, Platform and SRE roles across Ireland and the EU
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/kiransai006"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-kiransai006-0A66C2?style=flat-square"/></a>
  <a href="mailto:kiranssb23@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-kiranssb23%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white"/></a>
  <img alt="Location" src="https://img.shields.io/badge/Based%20in-Dublin%2C%20Ireland-169B62?style=flat-square"/>
</p>

---

## About

- DevOps engineer with about 4 years in cloud and platform roles: 3+ years at **Cognizant** on the RELX (LexisNexis) account, and before that Cloud Support Engineer at **Debots**, Hyderabad
- I own the delivery path end to end: reusable CI/CD pipelines, infrastructure as code, Kubernetes platforms on AKS and EKS, GitOps releases and the monitoring that tells us when something breaks
- MSc in Computing Science, Griffith College Dublin (2026) · BTech in Computer Science (2021)
- Current focus: platform engineering, software supply-chain security and SRE practice (SLOs, on-call, DORA metrics)

## What I've delivered at work

- **CI/CD at scale** – built reusable pipeline templates in Jenkins, GitHub Actions and Azure DevOps that other teams adopted; added caching and parallel jobs to speed up builds; set up per-branch preview environments
- **Kubernetes platforms** – provisioned and ran AKS and EKS clusters with Terraform; shipped workloads with Helm and ArgoCD, including blue/green releases
- **Security in the pipeline** – policy-as-code checks, secrets management and container image scanning built into delivery, not bolted on after
- **Operations** – Prometheus, Grafana, ELK and Loki for observability; moved alerting to log-based signals; on-call rotation, runbooks and automated ITIL change requests
- **People** – mentored junior engineers and tracked DORA metrics to show where delivery was slowing down
- **Cloud foundations (Debots)** – AWS deployments with reusable Terraform modules for EC2, S3, VPC and IAM; Jenkins pipelines integrated with GitLab; CloudWatch monitoring; Git branching and code review

## Featured project · OmniShop Enterprise Platform

A microservices e-commerce platform I built to show the full path from `git push` to a signed, scanned, monitored deployment on Kubernetes.
**Repo:** [OmniShop-Enterprise-Platform](https://github.com/Kiransai006/OmniShop-Enterprise-Platform-main)

```mermaid
flowchart LR
    A["git push"] --> B["GitHub Actions<br/>build + test"]
    B --> C["Trivy<br/>image scan"]
    C --> D["Cosign<br/>image signing"]
    D --> E[("Docker Hub")]
    G["ArgoCD<br/>Helm chart from Git"] --> F["AWS EKS<br/>dev / stage / prod"]
    E -. "image pull" .-> F
    T["Terraform<br/>VPC, EKS, IAM"] --> F
    F --> M["Prometheus + Grafana"]
```

- **Infrastructure as code** – Terraform for VPC, EKS and IAM, with remote state in S3 and DynamoDB state locking
- **Keyless CI** – GitHub Actions authenticates to AWS through OIDC, so no long-lived access keys sit in the repo
- **Supply-chain security** – every image is scanned with Trivy and signed with Cosign before it reaches the registry
- **GitOps** – ArgoCD syncs one Helm chart across dev, stage and prod
- **Observability** – Prometheus and Grafana dashboards, with a load generator feeding live traffic
- **Cost control** – a Python (boto3) teardown script removes every resource after a test run
- **Runs locally** – `docker compose up --build` brings up the full stack in about two minutes, no AWS account needed

`React` `Flask` `Docker` `Kubernetes` `Helm` `Terraform` `ArgoCD` `GitHub Actions` `Trivy` `Cosign` `Prometheus` `Grafana` `AWS EKS`

## Tech stack

| Area | Tools |
|---|---|
| **Cloud** | ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square) ![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square) ![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white) |
| **Containers** | ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white) ![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white) |
| **IaC &amp; config** | ![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white) ![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white) ![CloudFormation](https://img.shields.io/badge/CloudFormation-FF4F8B?style=flat-square) |
| **CI/CD** | ![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white) ![Azure DevOps](https://img.shields.io/badge/Azure%20DevOps-0078D7?style=flat-square) ![GitLab CI](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white) |
| **Observability** | ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white) ![ELK](https://img.shields.io/badge/ELK%20Stack-005571?style=flat-square&logo=elasticstack&logoColor=white) ![Loki](https://img.shields.io/badge/Loki-F46800?style=flat-square&logo=grafana&logoColor=white) |
| **Security** | ![Trivy](https://img.shields.io/badge/Trivy-1904DA?style=flat-square) ![Cosign](https://img.shields.io/badge/Cosign-4B32C3?style=flat-square) ![Policy as Code](https://img.shields.io/badge/Policy%20as%20Code-555555?style=flat-square) |
| **Languages** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white) ![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white) ![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square) |
| **Data &amp; messaging** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white) |
| **Platform** | ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) |

## Certifications

- Microsoft Certified: Azure Fundamentals
- Microsoft Certified: Azure Data Fundamentals
- AWS Certified Cloud Practitioner

Verified credentials: [Microsoft Learn profile](https://learn.microsoft.com/en-us/users/kiransubrahamanyasaibandarucogniza-1028/)

---

<p align="center">
  Open to DevOps, Platform and SRE roles in Ireland and the EU.<br/>
  Happy to talk CI/CD design, Kubernetes platforms and GitOps – <a href="https://www.linkedin.com/in/kiransai006">connect on LinkedIn</a>.
</p>
