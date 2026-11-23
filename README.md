# Awesome-Cloud-Orchestration-Serverless-Deployments

<FollowUp>
Would you like to **add a dedicated section for open-source GitOps & service mesh tools** (like `Argo CD`, `Flux`, `Istio`, `Cilium`) or **generate the next `README.md` repository**?
</FollowUp>
# Awesome-Cloud-Orchestration-Serverless-Deployments

# Awesome Cloud Orchestration & Serverless Deployments 🌟



> **Top Cloud Orchestration Serverless Deployments (Opensource)**  

> A curated list of the best cloud orchestration, container scheduling, and serverless deployment platforms — with a strong focus on **open-source** and self-hostable alternatives.  

> 🌟 **Star if you like it!** 🌟



Modern cloud orchestration and serverless platforms let teams deploy, scale, and manage containers and functions without managing every server. Commercial services such as AWS ECS, Google Cloud Run, Azure Container Apps, Fly.io, and Railway provide polished managed experiences, while a rich open-source ecosystem offers full control through Kubernetes, Nomad, Knative, OpenFaaS, and related projects.



This list prioritizes **open-source GitHub projects and self-hostable tools** while keeping SaaS/hosted platforms clearly separated.



## Table of Contents



- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS / Hosted Platforms](#saas--hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## Sector Overview & Market Dynamics

The global cloud container orchestration market is valued between $1.4B and $10B+ (growing at ~18–24% CAGR), while the serverless computing sector accounts for $22B to $32B+ (growing at ~15–23% CAGR). The sector exhibits a **highly concentrated core** dominated by hyperscalers (AWS, Microsoft Azure, Google Cloud) that capture the majority of enterprise workload spend, alongside a **moderately fragmented periphery** of specialized PaaS providers, edge runtimes, and developer-centric deployment platforms catering to niche workflows.

## SaaS / Hosted Platforms

These are popular commercial or fully managed cloud orchestration and serverless platforms (closed-source / hosted), sorted descending by company size (valuation / revenue / market cap):

| Platform | Provider / Parent | Company Size (Valuation / Revenue) | Starting Tier Pricing | Free Tier / Trial Limits | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **[Azure Container Apps](https://azure.microsoft.com/en-us/products/container-apps)** | Microsoft | ~$3.8T Market Cap (~$245B+ ARR) | Pay-as-you-go from $0.000024/vCPU-s ($0.0864/vCPU-hr) active compute + $0.000003/GiB-s memory | **Free Forever:** 180,000 vCPU-seconds (~50 vCPU-hrs), 360,000 GiB-seconds (~100 GiB-hrs), and 2M HTTP requests per month. | Serverless container platform built on Kubernetes & KEDA, scaling to zero without managing underlying infrastructure. |
| **[Google Cloud Run](https://cloud.google.com/run)** | Google (Alphabet) | ~$3.4T Market Cap (~$350B+ ARR) | Pay-as-you-go from $0.000024/vCPU-s ($0.0864/vCPU-hr) request-based compute + $0.0000025/GiB-s memory | **Free Forever:** 180,000 vCPU-seconds (~50 vCPU-hrs), 360,000 GiB-seconds, 2M requests, and 1 GB egress/mo. | Fully managed serverless container runtime that executes containers directly via HTTP requests with instant scale-to-zero. |
| **[AWS ECS](https://aws.amazon.com/ecs/) + Fargate** | Amazon (AWS) | ~$2.8T Market Cap (~$105B+ AWS ARR) | Pay-as-you-go from $0.04048 per vCPU-hour + $0.004445 per GB-hour (US East Linux/x86) | **No Free vCPU Tier:** Compute billed from first second; includes 20 GB free ephemeral storage per task/pod (EC2 Free Tier offers 750 hrs/mo on t2/t3.micro). | Amazon's fully managed container orchestration service offering serverless container execution via AWS Fargate. |
| **Managed Kubernetes (EKS / GKE / AKS)** | AWS / Google / Microsoft | Hyperscalers ($2.8T – $3.8T Market Cap) | Control plane from $0.00/hr (AKS Free Tier) to $0.10/cluster-hour (~$73/mo for EKS/GKE) + underlying worker node compute | **Varies by Provider:** AKS has permanent free control plane ($0 SLA); GKE gives $74.40/mo credit (covers 1 Zonal/Autopilot cluster); EKS has no free tier (12-month AWS Free Tier only covers EC2 nodes). | Managed enterprise Kubernetes control planes automating cluster provisioning, upgrades, and high availability. |
| **[Red Hat OpenShift](https://www.redhat.com/en/technologies/cloud-computing/openshift)** | IBM (Red Hat) | $34B Acquisition ($190B+ IBM Market Cap, Red Hat ARR ~$4B+) | Self-managed subscriptions start at core-pair licensing (~$1,000–$2,000+/core-pair/yr); ROSA/ARO managed cloud starts at hourly compute add-on (~$0.07–$0.17/vCPU-hr) | **60-Day Free Trial:** Full product access on own infrastructure; or free Developer Sandbox (shared hosted environment renewable in 30-day blocks with 12-hr pod timeout). | Enterprise Kubernetes application platform with developer tooling, security, and multicloud deployment capabilities. |
| **[HashiCorp Nomad Enterprise / Cloud (HCP)](https://www.hashicorp.com/products/nomad)** | IBM (HashiCorp) | $6.4B Acquisition ($580M+ ARR) | Self-hosted Community Edition is free (BSL); HCP Nomad managed clusters start at hourly development tiers (~$0.05–$0.15/cluster-hr) | **Free Forever (Self-Hosted):** Nomad binary free to self-manage; HCP Cloud provides a 30-day trial with $500 free credits across HashiCorp Cloud Platform services (no permanent free managed cluster). | Workload orchestrator deploying containers, non-containerized legacy binaries, and microservices across hybrid infrastructures. |
| **[Rancher Prime](https://www.rancher.com/)** | SUSE (EQT) | ~$2.9B Take-Private Valuation (~$778M ARR) | Open-source core is free; SUSE Rancher Prime subscriptions start around €2,113/yr per 2-core/4-vCPU block; AWS Marketplace edition starts at ~$168/mo for 24 vCPUs | **Free Forever (Community Edition):** Unrestricted full open-source cluster management; Rancher Prime offers a 30-day free trial on AWS Marketplace / SUSE customer portal. | Complete multi-cluster management stack for running containers across on-prem bare-metal, edge devices, and public clouds. |
| **[Scaleway Serverless](https://www.scaleway.com/)** | Scaleway (Iliad Group) | €11B+ Iliad Market Cap (Scaleway ARR ~€150M) | Serverless Containers start at €0.00001/vCPU-s (€0.036/vCPU-hr) + €0.000002/GB-s; Functions at €0.000005/GB-s + €0.15/1M requests | **Free Forever:** 200,000 vCPU-seconds and 400,000 GB-seconds free monthly for Containers; 400,000 GB-seconds and 1,000,000 requests free monthly for Functions. | European sovereign cloud platform providing managed serverless container execution and serverless micro-functions. |
| **[Railway](https://railway.app/)** | Railway | ~$500M–$1B Valuation ($124M funding, ~2M users) | Hobby plan starting at **$5.00/month** (includes $5 of resource credits, then $20/vCPU-mo & $10/GB RAM-mo) | **Free Forever:** $1.00/mo recurring resource credit, 1 project with up to 3 services (up to 0.5 GB RAM, 1 vCPU, auto-sleep after idle) plus a 30-day initial trial with $5 credit. | Developer-centric PaaS providing instant git-based deployments, automated container builds, and database provisioning. |
| **[Fly.io](https://fly.io/)** | Fly.io | ~$470M Valuation ($136M funding, ~$12M ARR) | Pay-as-you-go starting at ~$2.19/month for continuous `shared-cpu-1x` (256MB RAM) micro-machine; Hobby subscription at $5.00/month | **Pay-As-You-Go / Trial:** No permanent free VM plan for new accounts ($1 trial credit / pay-per-second); includes free perpetual 10 GB volume snapshots, 10 SSL certificates, and shared IPv4/IPv6. | Global application delivery platform running micro-VM containers directly on bare metal close to users. |



## Open-Source GitHub Projects



Open-source alternatives and self-hostable tools for container orchestration, serverless functions, and cloud-native deployments. These give you full control over the control plane and can run on any infrastructure.



### Container Orchestration & Scheduling



- **[kubernetes/kubernetes](https://github.com/kubernetes/kubernetes)**  

  The de-facto open-source standard for container orchestration. Automates deployment, scaling, and management of containerized applications. Massive ecosystem of operators, Helm charts, and CNCF projects. Apache-2.0.



- **[hashicorp/nomad](https://github.com/hashicorp/nomad)**  

  Flexible workload orchestrator that schedules containers, binaries, Java applications, and VMs. Simpler operational model than Kubernetes with a single binary. Supports multi-region and mixed workloads. (Note: license model changed; check current terms for your use case.)



- **[k3s-io/k3s](https://github.com/k3s-io/k3s)**  

  Lightweight, certified Kubernetes distribution optimized for edge, IoT, CI, and resource-constrained environments. Single binary, low resource usage, fully compatible with upstream Kubernetes.



- **Docker Swarm** (built into Docker Engine)  

  Simple native clustering and orchestration for Docker containers. Easy to adopt for teams already using Docker Compose.



- **Rancher / RKE / RKE2** open-source components  

  Multi-cluster Kubernetes management and lightweight Kubernetes distributions that remain largely open-source.



### Serverless & Function Platforms



- **[knative/serving](https://github.com/knative/serving)** (+ Knative Eventing)  

  Kubernetes-based platform that adds serverless capabilities: request-driven containers, scale-to-zero, traffic splitting, and event-driven architecture. Widely used as the foundation for many managed serverless offerings.



- **[openfaas/faas](https://github.com/openfaas/faas)** (OpenFaaS)  

  Popular open-source serverless framework for deploying functions and microservices as containers. Supports Kubernetes, K3s, OpenShift, and standalone modes. Strong developer experience and community.



- **[apache/openwhisk](https://github.com/apache/openwhisk)**  

  Apache OpenWhisk — mature open-source serverless platform that executes functions in response to events. Supports multiple languages, triggers, rules, and sequences. Can run on Kubernetes or standalone.



- **Fission, Nuclio, and related Kubernetes-native FaaS frameworks**  

  Additional open-source serverless platforms that emphasize fast cold starts, language flexibility, and tight Kubernetes integration.



### Deployment & Platform Tools



- **[yuechen-li-dev/Aetheris](https://github.com/yuechen-li-dev/Aetheris)**  

  Next-generation open-source geometric modeling kernel and engineering runtime (primarily CAD-focused). Included as referenced by the community; useful in specialized engineering and digital-twin deployment contexts.



- **Kamal, Dokku, CapRover, and lightweight PaaS tools**  

  Open-source “Heroku-like” platforms that simplify deploying applications on your own servers with minimal orchestration overhead.



- **Argo CD, Argo Workflows, Flux, and GitOps toolchains**  

  Open-source continuous delivery and workflow engines that complement orchestration platforms for declarative deployments.



> **Tip**: For full control and portability start with **Kubernetes** (or **K3s** for lighter needs). For simpler mixed workloads consider **Nomad**. For serverless functions on Kubernetes use **Knative** or **OpenFaaS**. Many of these tools interoperate and can be combined (e.g., Knative on Kubernetes, OpenFaaS on K3s).



## How to Contribute



Contributions are welcome and encouraged!



1. Fork the repository

2. Add a new tool under the appropriate section (keep SaaS and Open-Source strictly separate)

3. Use the same format: **Name** — short description + key features + license/link

4. Prefer actively maintained projects with clear documentation, reproducible examples, and preferably cross-platform or multi-cloud support

5. Submit a Pull Request



Please keep descriptions neutral and factual. Open-source and self-hostable projects are the primary focus of this list. Note any license changes or enterprise editions clearly.



## Disclaimer



This is a community-curated list for informational and educational purposes only.  

Inclusion does not constitute an endorsement. Always review licenses (especially recent changes such as those affecting Nomad), operational complexity, security practices, and total cost of ownership before adopting any platform.



Managed cloud services (ECS, Cloud Run, etc.) abstract away infrastructure but introduce vendor lock-in and ongoing costs. Self-hosted open-source solutions give maximum control but require operational expertise. Choose according to your team size, compliance needs, and scale.



---



**Made with ❤️ for the open-source cloud-native community**  

If this list helped you, please ⭐ the repo!
