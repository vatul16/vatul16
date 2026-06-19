<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=F79000&center=true&vCenter=true&width=600&lines=Hey+there%2C+I'm+Atul+%F0%9F%91%8B;Cloud+%26+DevOps+Engineer;I+build%2C+break%2C+and+automate+things." alt="Typing SVG" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/vatul16)
[![dev.to](https://img.shields.io/badge/dev.to-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white)](https://dev.to/vatul16)
[![Hashnode](https://img.shields.io/badge/Hashnode-2962FF?style=for-the-badge&logo=hashnode&logoColor=white)](https://atulcodes.hashnode.dev)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:vishwa.atul16@gmail.com)
[![AWS Certified](https://img.shields.io/badge/AWS_Certified-Cloud_Practitioner-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/certification/)

<img src="https://komarev.com/ghpvc/?username=vatul16&label=Profile+Views&color=F79000&style=flat" alt="Profile Views" />

</div>

---

## 🧠 About Me

Cloud & DevOps Engineer with **2+ years** of hands-on experience designing and operating scalable cloud-native infrastructure on AWS. I'm currently the **sole Cloud & DevOps owner** at [ShypBUDDY](https://shypbuddy.com), where I have end-to-end ownership of a high-throughput logistics platform that processes **2,000+ daily orders**.

- 🚀 Reduced deployment cycles by **80%** (2 weeks → 3 days) via CI/CD automation
- 🔍 Cut MTTD by **40%** with CloudWatch observability pipelines
- 🔒 Enforced SOC2-aligned security through RBAC and AWS Secrets Manager
- ✍️ Publicly document my infra work — **12+ AWS projects** written up on dev.to
- 📍 Based in Thane, Maharashtra, India

---

## 🛠️ Tech Stack

**Cloud & Infrastructure**

![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![AWS CloudFormation](https://img.shields.io/badge/CloudFormation-FF4F8B?style=flat-square&logo=amazonaws&logoColor=white)

**Containers & Orchestration**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![ECS Fargate](https://img.shields.io/badge/ECS_Fargate-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)

**CI/CD & Automation**

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![AWS CodeBuild](https://img.shields.io/badge/CodeBuild-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![AWS CodeDeploy](https://img.shields.io/badge/CodeDeploy-FF9900?style=flat-square&logo=amazonaws&logoColor=white)

**Observability**

![CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=flat-square&logo=amazonaws&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)
![Kibana](https://img.shields.io/badge/Kibana-005571?style=flat-square&logo=kibana&logoColor=white)

**Languages & Scripting**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

**Databases**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

---

## 🏗️ Featured Projects

> Building and shipping production-grade infrastructure, one Terraform module at a time.

### 🔷 [TerraTier — Production-Grade 3-Tier AWS Architecture](https://github.com/vatul16/terratier)

[![Terraform](https://img.shields.io/badge/Terraform->=1.13-844FBA?style=flat-square&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![AWS](https://img.shields.io/badge/AWS_Provider-~>6.0-FF9900?style=flat-square&logo=amazonaws&logoColor=white)](https://registry.terraform.io/providers/hashicorp/aws/latest)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](https://github.com/vatul16/terratier/blob/main/LICENSE)

A fully isolated, auto-scaling 3-tier web architecture on AWS — provisioned entirely with Terraform. Built around a **Go REST API** and a **Node.js frontend** running behind two Application Load Balancers, with subnet-level security isolation, Secrets Manager credential management, and CloudWatch observability baked in.

**Key design decisions:**
- 🔒 **4 subnet tiers** (not the usual 3) — frontend and backend private subnets isolated from each other
- ⚖️ **2 ALBs** — public-facing for the frontend, internal-only for the backend; backend API is never internet-reachable
- 🛡️ **IMDSv2 enforced** on every EC2 resource — closes the classic SSRF credential-theft path
- 🔑 **Zero hardcoded secrets** — RDS credentials generated by `random_password`, stored in Secrets Manager, fetched at boot via AWS CLI
- 🖥️ **SSM Session Manager** — no SSH keys distributed to app instances

**Stack:** `Terraform` · `AWS EC2 ASG` · `RDS PostgreSQL` · `ALB` · `Secrets Manager` · `CloudWatch` · `Go` · `Node.js` · `Docker`

📝 **Deep-dive write-up:** [Design Decisions & Trade-offs →](https://dev.to/vatul16/building-a-production-grade-3-tier-aws-architecture-with-terraform-design-decisions-trade-offs-370f)

---

<!-- PROJECTS_PLACEHOLDER: Add more projects below as you build them -->

> 🚧 **More projects coming soon** — EKS with custom Terraform modules, CI/CD pipeline templates, and an observability stack. Stay tuned!

---

## ✍️ Latest Blog Posts

<!-- The links below are picked from your most recent/popular posts across dev.to and Hashnode -->

### 🟣 [dev.to/vatul16](https://dev.to/vatul16)

| Post | Tags |
|------|------|
| [Building a Production-Grade 3-Tier AWS Architecture with Terraform: Design Decisions, Trade-offs, and Lessons Learned](https://dev.to/vatul16/building-a-production-grade-3-tier-aws-architecture-with-terraform-design-decisions-trade-offs-370f) | `#aws` `#terraform` `#devops` |
| [Stop Deploying Manually: How to Build Your First CI/CD Pipeline with GitHub Actions](https://dev.to/vatul16/stop-deploying-manually-how-to-build-your-first-cicd-pipeline-with-github-actions-80c) | `#cicd` `#githubactions` `#devops` |
| [Mastering GitOps: Bridging Infrastructure and Application Delivery with Terraform & ArgoCD](https://dev.to/vatul16/mastering-gitops-bridging-infrastructure-and-application-delivery-with-terraform-argocd-4385) | `#terraform` `#devops` `#automation` |
| [Building Production-Grade Observability with Terraform](https://dev.to/vatul16/building-production-grade-observability-with-terraform-2i3e) | `#terraform` `#aws` `#devops` |
| [Setting Up the ELK Stack on AWS EC2 for Log Monitoring](https://dev.to/vatul16/setting-up-the-elk-stack-on-aws-ec2-for-log-monitoring-1eme) | `#elasticsearch` `#devops` `#aws` |
| [Mastering Blue-Green Deployments with Terraform & AWS Elastic Beanstalk](https://dev.to/vatul16/mastering-blue-green-deployments-with-terraform-aws-elastic-beanstalk-3gpm) | `#terraform` `#aws` `#devops` |

➡️ [View all 22 posts on dev.to →](https://dev.to/vatul16)

### 🟡 [atulcodes.hashnode.dev](https://atulcodes.hashnode.dev)

➡️ [Read on Hashnode →](https://atulcodes.hashnode.dev)

---

## 📊 GitHub Stats

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=vatul16&show_icons=true&locale=en&theme=tokyonight&hide_border=true" />
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs?username=vatul16&show_icons=true&locale=en&layout=compact&theme=tokyonight&hide_border=true" />

<br/>

[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=vatul16&theme=tokyonight&hide_border=true)](https://git.io/streak-stats)

</div>

---

## 📜 Publication

**Unveiling the Cloud: An Evaluation of AWS Infrastructure Against Traditional On-Premise Solutions**  
Atul Vishwakarma, Parth Dalvi · IJARSCT (Jun 2024) · [DOI: 10.48175/IJARSCT-18932](https://doi.org/10.48175/IJARSCT-18932)

---

## 🤝 Let's Connect

I'm always happy to talk AWS architecture, Terraform patterns, or DevOps war stories. Drop me a message!

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Let's_connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/vatul16)
[![Email](https://img.shields.io/badge/Email-Say_hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:vishwa.atul16@gmail.com)
[![dev.to](https://img.shields.io/badge/dev.to-Read_my_blog-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white)](https://dev.to/vatul16)

</div>

---

<div align="center">
  <sub>⚡ <em>Automate everything. Document what you automate. Share what you document.</em></sub>
</div>
