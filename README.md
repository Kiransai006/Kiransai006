<picture>
  <source media="(prefers-color-scheme: dark)" srcset="banner-dark.svg">
  <img alt="Kiran Bandaru – DevOps Engineer" src="banner-light.svg" width="100%">
</picture>

<p align="center">
  <a href="https://www.linkedin.com/in/kiransai006"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge"/></a>
  <a href="mailto:kiranssb23@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-Get%20in%20touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <img alt="Open to work" src="https://img.shields.io/badge/Open%20to-DevOps%20%7C%20Platform%20%7C%20SRE-2EA44F?style=for-the-badge"/>
</p>

<p align="center">
  <b>I build the path from <code>git push</code> to production – and the monitoring that proves it works.</b>
</p>

---

### About me

- **~4 years** in cloud and DevOps engineering: 3+ years at **Cognizant** on the RELX (LexisNexis) account, and before that **Cloud Support Engineer** at Debots, Hyderabad
- I design reusable CI/CD pipelines, run Kubernetes on **AKS** and **EKS**, manage infrastructure with **Terraform** and **Ansible**, and release through **GitOps**
- **MSc Computing Science**, Griffith College Dublin (2026) · **BTech Computer Science** (2021)
- **Now building:** SRE portfolio projects – SLOs, alerting and runbooks
- **Looking for:** DevOps, Platform or SRE roles in Ireland and the EU

### Experience

| Role | Company | Period |
|---|---|---|
| **DevOps Engineer** | Cognizant · client RELX (LexisNexis) | Sep 2021 – Jan 2025 |
| **Cloud Support Engineer** | Debots, Hyderabad | Jan 2021 – Sep 2021 |

<details>
<summary><b>What I delivered</b> (click to expand)</summary>
<br/>

- **CI/CD at scale** – reusable pipeline templates in Jenkins, GitHub Actions and Azure DevOps adopted by other teams; caching and parallel jobs to speed up builds; per-branch preview environments
- **Kubernetes platforms** – AKS and EKS clusters provisioned with Terraform; workloads shipped with Helm and ArgoCD, including blue/green releases
- **Security in the pipeline** – policy-as-code checks, secrets management and container image scanning built into delivery
- **Operations** – Prometheus, Grafana, ELK and Loki; log-based alerting; on-call rotation, runbooks and automated ITIL change requests
- **People** – mentored junior engineers; tracked DORA metrics to find delivery bottlenecks
- **Cloud foundations (Debots)** – AWS deployments with reusable Terraform modules for EC2, S3, VPC and IAM; Jenkins pipelines integrated with GitLab; CloudWatch monitoring

</details>

---

### Featured project · OmniShop Enterprise Platform

<a href="https://github.com/Kiransai006/OmniShop-Enterprise-Platform-main"><img alt="View repo" src="https://img.shields.io/badge/View%20repo-OmniShop-181717?style=flat-square&logo=github"/></a>
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![EKS](https://img.shields.io/badge/AWS%20EKS-232F3E?style=flat-square)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

A microservices e-commerce platform that takes code from commit to a **scanned, signed and monitored** deployment on Kubernetes.

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

| | |
|---|---|
| **Infrastructure** | Terraform for VPC, EKS and IAM · remote state in S3 with DynamoDB locking |
| **Keyless CI** | GitHub Actions authenticates to AWS with OIDC – no long-lived keys |
| **Supply chain** | Every image scanned with Trivy and signed with Cosign |
| **GitOps** | ArgoCD syncs one Helm chart across dev, stage and prod |
| **Observability** | Prometheus and Grafana, fed by a synthetic load generator |
| **Cost control** | Python (boto3) teardown script removes every resource after testing |
| **Try it** | `docker compose up --build` runs the full stack locally in ~2 minutes |

---

### Tech stack

<p align="center">
  <img alt="Core stack" src="https://skillicons.dev/icons?i=aws,azure,gcp,kubernetes,docker,terraform,ansible,githubactions,jenkins,gitlab,prometheus,grafana,linux,bash,python,go,git,postgres,mysql,mongodb,redis&perline=11"/>
</p>

<p align="center">
  <img alt="Helm" src="https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white"/>
  <img alt="ArgoCD" src="https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white"/>
  <img alt="Azure DevOps" src="https://img.shields.io/badge/Azure%20DevOps-0078D7?style=flat-square"/>
  <img alt="CloudFormation" src="https://img.shields.io/badge/CloudFormation-FF4F8B?style=flat-square"/>
  <img alt="ELK" src="https://img.shields.io/badge/ELK%20Stack-005571?style=flat-square&logo=elasticstack&logoColor=white"/>
  <img alt="Loki" src="https://img.shields.io/badge/Loki-F46800?style=flat-square&logo=grafana&logoColor=white"/>
  <img alt="Trivy" src="https://img.shields.io/badge/Trivy-1904DA?style=flat-square"/>
  <img alt="Cosign" src="https://img.shields.io/badge/Cosign-4B32C3?style=flat-square"/>
  <img alt="Kafka" src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white"/>
  <img alt="PowerShell" src="https://img.shields.io/badge/PowerShell-5391FE?style=flat-square"/>
</p>

---

### How I work

- **Everything in Git** – infrastructure, pipelines and config are reviewed and versioned like application code
- **Security early** – scanning, signing and policy checks run in the pipeline, not after release
- **Done means observable** – a service isn't finished until it has dashboards, alerts and a runbook
- **Templates over tickets** – reusable pipelines let teams ship without waiting on DevOps

---

### Certifications

![Azure Fundamentals](https://img.shields.io/badge/Microsoft-Azure%20Fundamentals-0078D4?style=flat-square)
![Azure Data Fundamentals](https://img.shields.io/badge/Microsoft-Azure%20Data%20Fundamentals-0078D4?style=flat-square)
![AWS Cloud Practitioner](https://img.shields.io/badge/AWS-Cloud%20Practitioner-FF9900?style=flat-square)

Verify: [Microsoft Learn profile](https://learn.microsoft.com/en-us/users/kiransubrahamanyasaibandarucogniza-1028/)

---

<p align="center">
  <sub>Open to DevOps, Platform and SRE roles in Ireland and the EU · <a href="https://www.linkedin.com/in/kiransai006">Let's talk on LinkedIn</a></sub>
</p>
