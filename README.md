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



- **[Falco](https://github.com/falcosecurity/falco)**

  **Cloud-native runtime security** (Apache 2.0, CNCF Graduated) — **the de facto standard for container and Kubernetes runtime threat detection** . **Features**: **eBPF-based** monitoring of system calls across hosts, containers, Kubernetes, and cloud services (via plugins for AWS CloudTrail, GitHub, Okta); **YAML rule engine** with out-of-the-box rules for container escapes, cryptojacking, reverse shells, and privilege escalation; **50+ integrations** for forwarding alerts to SIEM, Slack, and data lakes; streaming detection minimizes storage costs . **Tech stack**: C++, Go. **Deploy**: Self-hosted (DaemonSet on Kubernetes, Helm chart). **Trade-off**: **Runtime detection only**—no posture management, vulnerability scanning, or CIEM. Requires rule tuning. **Best for**: teams needing runtime threat detection for Kubernetes and containers—the foundation of the runtime layer in any open-source cloud security stack.



- **[Prowler](https://github.com/prowler-cloud/prowler)**

  **Open-source multi-cloud security posture management** (Apache 2.0) — **the most widely adopted open-source CSPM**. **Features**: **Prowler CLI** for security scans across all supported providers; **Prowler Local Server** (formerly Prowler App) for self-hosted web application and API to run scans and visualize findings; **Prowler Local Dashboard** for visualizing CLI CSV outputs; **Prowler SDK** powering CLI and server . Hundreds of checks mapped to CIS, NIST, PCI-DSS, GDPR, HIPAA, SOC 2, and FedRAMP. **Tech stack**: Python. **Deploy**: Self-hosted (CLI, Local Server, Docker) or Prowler Cloud. **Trade-off**: **CSPM only**—no runtime detection or workload protection. Findings are lists, not graph-correlated attack paths. **Best for**: security teams wanting production-ready open-source CSPM with broad compliance coverage.



- **[Magpie (OpenRaven)](https://github.com/openraven/magpie)**

  **Cloud Security Posture Manager (CSPM)** (Apache 2.0, ~188 stars) — **a lightweight alternative to Prowler** focused on modern cloud threats. **Features**: Security analysis for modern cloud stacks with focus on **emerging threats like cloud ransomware and supply chain attacks** . **Tech stack**: Java. **Deploy**: Self-hosted. **Trade-off**: **Smaller community than Prowler** (~188 stars vs. Prowler's thousands); last push ~10 months ago per metadata . **Best for**: teams wanting a focused CSPM with an emphasis on ransomware and supply-chain threat patterns—evaluate activity cadence before adoption.



- **[container-runtime-security](https://github.com/aiagentmackenzie-lang/container-runtime-security)**

  **eBPF-based container runtime security monitoring and enforcement** (license per repo) — **the most feature-complete open-source runtime enforcement project** with AI triage. **Features**: **30 detection rules** across 9 categories (Container Escape, Cryptojacking, Reverse Shell, Credential Access, Privilege Escalation, Container Drift, Network Anomaly, Process Injection, Known CVE); **7-rule enforcement safety protocol** with TC-based network blocking; **multi-signal correlation** (shell→network, DNS+TLS); **AI triage** via gRPC (advisory); **~73k events/sec** single-core throughput . **Tech stack**: Go, C (eBPF). **Deploy**: Self-hosted (Kubernetes). **Trade-off**: **eBPF kernel load/attach path code-complete but pending Linux runtime verification** (Phase C); AI triage degrades to neutral . Newer project with limited community validation. **Best for**: teams wanting eBPF-native enforcement (not just detection) with AI-assisted triage—willing to validate the runtime path before production use.



### Additional Strong Open-Source Options



- **Trivy** — Comprehensive scanner (Apache 2.0). Vulnerability, IaC, secrets, and SBOM scanning; CI/CD native. **Note**: Scanner only—pair with Falco for runtime and Prowler for posture. **Best for**: shift-left security in CI/CD pipelines.

- **Tetragon** — eBPF-native runtime security from Isovalent (Apache 2.0). In-kernel enforcement can kill processes before syscalls complete. **Note**: Runtime enforcement only—no posture or CSPM. **Best for**: teams wanting enforcement alongside Falco's detection.

- **Kubescape** — Kubernetes security platform (Apache 2.0, CNCF incubating). Posture, vulnerability, and runtime for K8s clusters. **Note**: Kubernetes-only—not multi-cloud CSPM. **Best for**: teams wanting a single tool for Kubernetes security.



**Frameworks for building custom systems**: Combine **Falco** for runtime detection with **Prowler** or **Magpie** for CSPM, **container-runtime-security** for eBPF enforcement, and **Trivy** for shift-left scanning—creating a composable open-source cloud security stack. **None of these match Wiz's unified graph or CrowdStrike's threat intelligence correlation**; those require commercial platforms or significant integration engineering.



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
