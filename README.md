# Awesome-Cloud-Security-Threat-Detection

# Awesome-Cloud-Security-Threat-Detection

**Top Cloud Security Threat Detection (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on CNAPP, Runtime Threat Detection, CSPM, Cloud SIEM & Self-Hosted Security Operations*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Security & Threat Detection**. These tools enable organizations to detect threats across cloud workloads, containers, and identities, correlate security events, and respond to incidents—from fully managed CNAPP platforms with agentless scanning and unified graphs to self-hosted scanners and runtime sensors that give security teams complete control over their detection pipelines.



**Examples** include Wiz, CrowdStrike Falcon, Microsoft Defender for Cloud, Palo Alto Prisma Cloud, Datadog Security, SentinelOne, Sysdig, Lacework (FortiCNAPP), Orca Security, and Atlassian Guard (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted cloud security, runtime detection, and open posture management. **Critical note**: No single open-source project replicates the full scope of Wiz or CrowdStrike Falcon. The open-source landscape is **composable**: **Falco** dominates runtime detection , **Prowler** handles multi-cloud CSPM , **Magpie** provides a lightweight CSPM alternative , and newer projects like **container-runtime-security** offer eBPF-based enforcement with AI triage . You assemble the stack based on your gaps.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)



## Sector Overview & Market Dynamics

The global Cloud Security and Cloud-Native Application Protection Platform (CNAPP) market is projected to reach approximately **$45B to $48B+** in 2026 (with the standalone CNAPP segment expanding between **$12.6B and $17.8B** at a 19–22.5% CAGR). While the space historically emerged as a highly fragmented landscape of siloed point tools (disparate CSPM, CWPP, and CIEM scanners), it is rapidly consolidating into a **moderately-to-highly concentrated market** dominated by end-to-end platform consolidators and cybersecurity conglomerates executing winner-take-most platform plays.

## SaaS/Hosted Platforms

| Platform | Market Cap / Valuation | Starting Pricing | Free Tier / Trial Limits | Key Capabilities & Workload Focus |
| :--- | :--- | :--- | :--- | :--- |
| **[Microsoft Defender for Cloud](https://azure.microsoft.com/en-us/products/defender-for-cloud)** | ~$3.9T *(Market Cap)* | **$4.906/server/month** (Defender for Servers Plan 1; pay-as-you-go per resource) | **Free indefinitely** (Foundational CSPM); 30-day free trial per enhanced workload protection plan | Native Azure/multicloud protection with agentless & agent-based vulnerability scanning, posture, and CWPP. |
| **[Palo Alto Prisma Cloud](https://www.paloaltonetworks.com/prisma/cloud)** | ~$280B *(Market Cap)* | **~$18,000/year** (baseline 100 enterprise credit bundle; credit consumption model) | **30-day proof-of-concept / evaluation** via AWS Marketplace private offer or sales | Comprehensive code-to-cloud CNAPP covering CSPM, CWPP, CIEM, API security, and runtime defense. |
| **[CrowdStrike Falcon](https://www.crowdstrike.com/)** | ~$250B *(Market Cap)* | **$7.99/device/month** (Falcon Go / Essentials baseline tier) | **15-day free trial** (unlimited access without credit card; 30-day pre-configured virtual Test Drive) | Unified platform combining endpoint security (EDR), cloud runtime workload security, and identity protection. |
| **[FortiCNAPP (Lacework)](https://www.lacework.com/)** | ~$115B *(Fortinet Market Cap)* | **~$25,000/year** (baseline starter pack commitment via AWS Marketplace private offer) | **30-day evaluation trial** (or partner-led 14-day Cloud Security Assessment) | AI-powered CNAPP with behavioral anomaly detection, CIEM, CSPM, and workload threat monitoring. |
| **[Datadog Cloud Security](https://www.datadoghq.com/)** | ~$85B *(Market Cap)* | **$10/host/month** (CSM Pro posture baseline, billed annually; $15/host/month for CWP) | **14-day free trial** with full platform telemetry, log ingestion, and posture checks | Unified security posture and runtime workload detection directly inside the Datadog observability suite. |
| **[Atlassian Guard](https://www.atlassian.com/software/guard)** | ~$55B *(Market Cap)* | **$8.18/user/month** (Guard Premium tier; user-tier subscription) | **30-day free trial** across Jira, Confluence, and Bitbucket Cloud orgs | SaaS application security, threat detection, audit logging, and data loss prevention across Atlassian Cloud. |
| **[Wiz](https://www.wiz.io/)** | ~$32B *(Acquisition / Valuation)* | **$24,000/year** (Wiz Essential baseline; 100-workload annual commitment block on AWS Marketplace) | **14-day free trial** with unlimited access to scan cloud accounts and generate security graph | Agentless CNAPP with unified security graph correlating multicloud infrastructure, workloads, identities, and code. |
| **[SentinelOne Singularity](https://www.sentinelone.com/)** | ~$8.5B *(Market Cap)* | **$179.99/endpoint/year** (~$15/endpoint/month; Singularity Complete tier) | **30-day sales-guided Proof of Concept (PoC)** scoped to designated endpoints/workloads | Autonomous AI-native endpoint and cloud workload protection (CWPP) with 14-day telemetry retention. |
| **[Sysdig Secure](https://sysdig.com/)** | ~$2.5B *(Private Valuation)* | **$72/host/month** (CNAPP Enterprise list tier, typically 20-host minimum commitment) | **30-day free trial** available via direct signup or AWS/GCP Marketplace | Runtime threat detection and container security built on Falco, integrated with posture and vulnerability tools. |
| **[Orca Security](https://orca.security/)** | ~$1.8B *(Private Valuation)* | **$7,000/month** (~$84,000/year minimum starter workload tier on AWS Marketplace) | **30-day free trial** (risk-free assessment available on AWS Marketplace) | Agentless SideScanning CNAPP covering CSPM, CWPP, CIEM, DSPM, API security, and AI workload posture. |

## Open-Source GitHub Projects

Curated list of open-source tools for cloud security, runtime detection, CSPM, and posture enforcement, sorted by GitHub stars in descending order.

- **[Trivy](https://github.com/aquasecurity/trivy)** [![GitHub stars](https://img.shields.io/github/stars/aquasecurity/trivy?style=social&color=white)](https://github.com/aquasecurity/trivy/stargazers)
  **Comprehensive security scanner** (Apache 2.0) — Scans container images, file systems, Git repositories, virtual machine images, Kubernetes clusters, and AWS environments for known vulnerabilities (CVEs), IaC misconfigurations, sensitive secrets, and SBOM licenses. CI/CD native and developer-friendly. **Tech stack**: Go. **Deploy**: CLI, Docker, Kubernetes Operator. **Best for**: Shift-left security pipelines and pre-deployment vulnerability/IaC verification.

- **[Wazuh](https://github.com/wazuh/wazuh)** [![GitHub stars](https://img.shields.io/github/stars/wazuh/wazuh?style=social&color=white)](https://github.com/wazuh/wazuh/stargazers)
  **Unified open-source XDR & SIEM platform** (GPL 3.0) — Provides host and container-level threat detection, integrity monitoring (FIM), active incident response, and continuous compliance across endpoints, cloud instances (AWS, Azure, GCP), and containers. Correlates event data through an indexed search and visualization engine. **Tech stack**: C, Python, Go. **Deploy**: Self-hosted (manager, indexer, dashboard, and lightweight multi-platform endpoint agents). **Best for**: Teams seeking a unified self-hosted security monitoring and open SIEM solution.

- **[Prowler](https://github.com/prowler-cloud/prowler)** [![GitHub stars](https://img.shields.io/github/stars/prowler-cloud/prowler?style=social&color=white)](https://github.com/prowler-cloud/prowler/stargazers)
  **Multi-cloud security posture management (CSPM)** (Apache 2.0) — Industry standard open-source CSPM tool covering AWS, Azure, GCP, and Kubernetes. Features CLI scans, web UI (Prowler Local Server), and SDK support with hundreds of checks mapped to CIS Benchmarks, NIST, PCI-DSS, GDPR, HIPAA, SOC 2, and FedRAMP. **Tech stack**: Python. **Deploy**: Self-hosted (CLI, Docker, Local Server) or managed Prowler Cloud. **Best for**: Multi-cloud security posture audits, continuous compliance tracking, and CIS benchmark reporting.

- **[Kubescape](https://github.com/kubescape/kubescape)** [![GitHub stars](https://img.shields.io/github/stars/kubescape/kubescape?style=social&color=white)](https://github.com/kubescape/kubescape/stargazers)
  **Kubernetes open-source security platform** (Apache 2.0, CNCF Incubating) — Multi-faceted Kubernetes security suite providing posture management, risk analysis, image vulnerability scanning, RBAC visualization, and eBPF-based runtime anomaly detection directly within Kubernetes clusters. **Tech stack**: Go. **Deploy**: Self-hosted (CLI, Helm chart, cluster operator). **Best for**: Kubernetes-centric teams wanting unified posture and cluster security.

- **[Falco](https://github.com/falcosecurity/falco)** [![GitHub stars](https://img.shields.io/github/stars/falcosecurity/falco?style=social&color=white)](https://github.com/falcosecurity/falco/stargazers)
  **Cloud-native runtime threat detection** (Apache 2.0, CNCF Graduated) — The de facto standard for Linux, container, and Kubernetes runtime monitoring. Uses eBPF or kernel modules to parse kernel system calls in real time against a powerful YAML rule engine to catch privilege escalations, unexpected shells, namespace escapes, and cryptominers. **Tech stack**: C++, Go. **Deploy**: Self-hosted (DaemonSet on Kubernetes, Helm, systemd). **Best for**: High-performance, real-time runtime detection across production Kubernetes workloads.

- **[Checkov](https://github.com/bridgecrewio/checkov)** [![GitHub stars](https://img.shields.io/github/stars/bridgecrewio/checkov?style=social&color=white)](https://github.com/bridgecrewio/checkov/stargazers)
  **Static code analysis for Infrastructure as Code (IaC)** (Apache 2.0) — Analyzes Terraform, CloudFormation, Kubernetes manifests, Helm charts, Dockerfiles, and Serverless framework templates for cloud configuration errors, security risks, and compliance breaches before provisioning. **Tech stack**: Python. **Deploy**: CLI, pre-commit hooks, GitHub Actions, CI/CD runners. **Best for**: Catching cloud misconfigurations in pull requests prior to cloud resource deployment.

- **[Cloud Custodian](https://github.com/cloud-custodian/cloud-custodian)** [![GitHub stars](https://img.shields.io/github/stars/cloud-custodian/cloud-custodian?style=social&color=white)](https://github.com/cloud-custodian/cloud-custodian/stargazers)
  **Rules engine for cloud management and remediation** (Apache 2.0, CNCF Incubating) — Stateless, lightweight policy-as-code engine for AWS, Azure, and GCP. Allows writing simple YAML policies to enforce real-time compliance, cost optimization, garbage collection, and automated incident response (e.g., auto-remediating unencrypted storage buckets). **Tech stack**: Python. **Deploy**: Serverless functions (AWS Lambda, Azure Functions, Cloud Functions) or cron runners. **Best for**: Automated real-time posture policy enforcement and continuous remediation.

- **[Tetragon](https://github.com/cilium/tetragon)** [![GitHub stars](https://img.shields.io/github/stars/cilium/tetragon?style=social&color=white)](https://github.com/cilium/tetragon/stargazers)
  **eBPF-based security observability and real-time runtime enforcement** (Apache 2.0) — Provides deep kernel-level system visibility, network tracking, and security enforcement without modifying application code. Operates directly in kernel space to synchronously block or terminate malicious processes before system calls complete. **Tech stack**: Go, C (eBPF). **Deploy**: Kubernetes DaemonSet, Cilium plugin. **Best for**: Synchronous in-kernel attack blocking, container isolation, and execution telemetry.

- **[Tracee](https://github.com/aquasecurity/tracee)** [![GitHub stars](https://img.shields.io/github/stars/aquasecurity/tracee?style=social&color=white)](https://github.com/aquasecurity/tracee/stargazers)
  **Runtime security and system tracing using eBPF** (Apache 2.0) — Collects operating system events and system calls at high speeds, evaluating security signatures written in Go and Rego to detect behavioral indicators of attack (IoAs) including fileless malware execution and kernel exploit attempts. **Tech stack**: Go, C (eBPF). **Deploy**: Container, Kubernetes DaemonSet. **Best for**: Lightweight runtime event forensics and system behavioral tracing.

- **[Gatekeeper](https://github.com/open-policy-agent/gatekeeper)** [![GitHub stars](https://img.shields.io/github/stars/open-policy-agent/gatekeeper?style=social&color=white)](https://github.com/open-policy-agent/gatekeeper/stargazers)
  **Policy-as-code admission controller for Kubernetes** (Apache 2.0, CNCF Graduated) — Integrates the Open Policy Agent (OPA) with Kubernetes admission webhooks to enforce granular policies and governance (e.g., blocking root containers, mandating labels, restricting host volumes) at cluster entry. **Tech stack**: Go. **Deploy**: Kubernetes controller / Helm chart. **Best for**: Admission-time guardrails and compliance governance for Kubernetes.

- **[Magpie (OpenRaven)](https://github.com/openraven/magpie)** [![GitHub stars](https://img.shields.io/github/stars/openraven/magpie?style=social&color=white)](https://github.com/openraven/magpie/stargazers)
  **Cloud Security Posture Manager (CSPM)** (Apache 2.0) — Lightweight alternative CSPM focused on discovering modern cloud assets and identifying emerging risks such as cloud ransomware paths and supply chain vulnerabilities. **Tech stack**: Java. **Deploy**: Self-hosted CLI / containers. **Best for**: Teams seeking a lightweight cloud asset scanner tailored for ransomware posture assessments.

- **[container-runtime-security](https://github.com/aiagentmackenzie-lang/container-runtime-security)** [![GitHub stars](https://img.shields.io/github/stars/aiagentmackenzie-lang/container-runtime-security?style=social&color=white)](https://github.com/aiagentmackenzie-lang/container-runtime-security/stargazers)
  **eBPF-based container runtime security monitoring & enforcement** — Feature-complete open-source runtime enforcement engine with 30 detection rules across 9 threat categories, TC-based network blocking, multi-signal correlation, and AI-assisted triage at ~73k events/sec throughput. **Tech stack**: Go, C (eBPF). **Deploy**: Kubernetes DaemonSet. **Best for**: Teams researching eBPF-native active enforcement and AI-augmented alert triage.

### Building a Composable Open-Source Cloud Security Stack

While commercial CNAPP platforms (such as Wiz, Defender for Cloud, and CrowdStrike) provide a unified graph tying together posture, runtime, and identity, you can assemble a powerful self-hosted alternative by composing complementary open-source layers:
- **Shift-Left & Pre-deployment**: [Trivy](https://github.com/aquasecurity/trivy) (vulnerabilities & secrets) + [Checkov](https://github.com/bridgecrewio/checkov) (IaC static analysis).
- **Multi-Cloud Posture & Compliance**: [Prowler](https://github.com/prowler-cloud/prowler) (CIS benchmarks & audits) + [Cloud Custodian](https://github.com/cloud-custodian/cloud-custodian) (automated posture policy enforcement).
- **Cluster Governance**: [Gatekeeper](https://github.com/open-policy-agent/gatekeeper) + [Kubescape](https://github.com/kubescape/kubescape).
- **Runtime Threat Detection**: [Falco](https://github.com/falcosecurity/falco) + [Tracee](https://github.com/aquasecurity/tracee).
- **In-Kernel Enforcement**: [Tetragon](https://github.com/cilium/tetragon) + [container-runtime-security](https://github.com/aiagentmackenzie-lang/container-runtime-security).
- **Unified SIEM / Event Correlation**: [Wazuh](https://github.com/wazuh/wazuh).


## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Cloud security platforms handling credentials and security telemetry must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls.

- **The "unified CNAPP" vs. "runtime detection" vs. "CSPM" vs. "enforcement" distinction is critical.** **Wiz, CrowdStrike, Defender for Cloud, Prisma Cloud, Datadog, SentinelOne, Sysdig, Lacework, and Orca** are **commercial platforms**—they bundle multiple capabilities (CSPM, CWPP, CIEM, runtime) into one console. **Falco** is **runtime detection**—Kubernetes and container threats, not posture . **Prowler and Magpie** are **CSPM**—posture only . **container-runtime-security** is **runtime enforcement**—eBPF-based blocking with detection . **No single open-source project replaces a commercial CNAPP.** Compose the stack based on your gaps.

- **Falco is the runtime detection standard**—CNCF Graduated, eBPF-based, with 50+ integrations and upstream status for Sysdig Secure . **Pair it with Prowler for posture** to approximate a CNAPP.

- **Prowler is the most production-ready open-source CSPM** with CLI, Local Server, and Local Dashboard options . **Magpie is the lighter alternative** focused on ransomware and supply-chain threats, but has a much smaller community .

- **container-runtime-security is the most ambitious open-source runtime enforcement project**—30 rules, 7-rule safety protocol, and AI triage at ~73k events/sec . **The trade-off**: runtime path pending verification; newer project. **For teams wanting enforcement (not just detection), it is the most feature-complete option to evaluate.**

- **Pricing opacity varies.** CrowdStrike publishes per-device pricing ($7.99–$19.99/month) . SentinelOne publishes per-endpoint pricing ($179.99–$229.99/year) . Microsoft publishes resource-based pricing with free CSPM . Atlassian Guard Premium is $8.18/user/month . Wiz, Prisma Cloud, Datadog, Sysdig, Lacework, and Orca require sales contact. **Validate with direct vendor conversations against your cloud footprint and workload count.**

- Self-hosted open-source solutions require proper infrastructure (Kubernetes for Falco, servers for Prowler), security hardening for scanner credentials, and ongoing maintenance. **Security platforms have privileged access to cloud environments**—ensure your deployment meets your organization's security standards before connecting production accounts.



---



**Made for cloud security engineers, SOC teams, and organizations building transparent cloud threat detection solutions.**

Let's make Cloud Security & Threat Detection more open, data-driven, and runtime-aware.
