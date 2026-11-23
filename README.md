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



- [SaaS / Hosted Platforms](#saas--hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS / Hosted Platforms



These are popular commercial or fully managed cloud orchestration and serverless platforms (closed-source / hosted):



- **[AWS ECS](https://aws.amazon.com/ecs/)** (Elastic Container Service) + Fargate — Amazon’s container orchestration service with serverless compute option.

- **[Google Cloud Run](https://cloud.google.com/run)** — Fully managed serverless platform for containers that scales to zero.

- **[Azure Container Apps](https://azure.microsoft.com/en-us/products/container-apps)** — Microsoft’s serverless container platform built on Kubernetes technology.

- **[Red Hat OpenShift](https://www.redhat.com/en/technologies/cloud-computing/openshift)** — Enterprise Kubernetes platform with managed and self-managed offerings (strong commercial focus).

- **[Rancher](https://www.rancher.com/)** (SUSE) — Multi-cluster Kubernetes management platform with commercial support and hosted options.

- **[Fly.io](https://fly.io/)** — Global application platform that runs containers close to users with a developer-friendly experience.

- **[Railway](https://railway.app/)** — Modern PaaS for deploying apps, databases, and services with minimal configuration.

- **[Scaleway Serverless](https://www.scaleway.com/)** — European cloud provider’s serverless containers and functions offerings.

- **Kubernetes Cloud / Managed Kubernetes** (EKS, GKE, AKS, etc.) — Hosted control planes for Kubernetes offered by major cloud providers.

- **HashiCorp Nomad Cloud / enterprise offerings** — Managed or supported versions of Nomad for production workloads.



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
