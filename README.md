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

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Wiz](https://www.wiz.io/)**

  **Agentless CNAPP** with a unified security graph correlating cloud infrastructure, workloads, identities, and code. Gartner reviewers highlight clear risk visualization, contextual prioritization, and quick onboarding across AWS, Azure, GCP, OCI, Alibaba Cloud, and Kubernetes . **Pricing**: Quote-only; enterprise contracts. **Free tier**: None. **Best for**: enterprises wanting agentless discovery with cross-cloud risk correlation—**trade-off**: reviewers note higher cost as environments scale and limited dashboard customization .



- **[CrowdStrike Falcon](https://www.crowdstrike.com/)**

  **Unified cloud-native security platform** combining endpoint, cloud, and identity protection. **Pricing**: Transparent per-device bundles from **$7.99/month** (Security Essentials) to **$19.99/month** (Advanced Protection); add-on modules for Identity Security and Next-Gen SIEM available . **Free tier**: None. **Best for**: organizations wanting endpoint and cloud security from a single platform with threat graph correlation—**trade-off**: cloud modules are add-ons; full CNAPP scope requires higher tiers.



- **[Microsoft Defender for Cloud](https://azure.microsoft.com/en-us/products/defender-for-cloud)**

  **Cloud-native protection** across Azure, other clouds, and on-premises. **Foundational CSPM is free**; workload protection plans are priced per resource: Containers at ¥0.096/vCore/hour, SQL on Azure at ¥0.2/Instance/hour, Storage at ¥20.35 per million transactions . **Free tier**: Yes, Foundational CSPM free. **Best for**: Azure-centric organizations wanting native cloud security with a free posture baseline—**trade-off**: workload protection costs scale with resource count.



- **[Palo Alto Prisma Cloud](https://www.paloaltonetworks.com/prisma/cloud)**

  **CNAPP with credit-based Enterprise Edition** covering code-to-cloud security. **Pricing**: Credit model with module bundles . **Free tier**: None. **Best for**: enterprises wanting comprehensive CNAPP within the Palo Alto ecosystem.



- **[Datadog Cloud Security](https://www.datadoghq.com/)**

  **Security posture within Datadog's observability platform**. Gartner reviewers value the unified platform—security, logs, and metrics in one place eliminates tool-switching during incidents—but note **complex and unpredictable pricing** and occasional dashboard query inaccuracies . **Pricing**: Consumption-based; complex model. **Free tier**: Limited. **Best for**: teams already on Datadog wanting security context alongside observability—**trade-off**: pricing opacity and bugs per reviewers .



- **[SentinelOne Singularity](https://www.sentinelone.com/)**

  **AI-native platform** with cloud workload protection. **Singularity Complete** at **$179.99/endpoint/year** includes cloud workload protection, AI security assistant, and 14-day data retention; **Commercial** at **$229.99/year** adds Identity Detection & Response and Managed Threat Hunting . **Free tier**: None. **Best for**: organizations wanting autonomous protection with transparent endpoint-based pricing—**trade-off**: cloud-specific modules may require higher tiers.



- **[Sysdig Secure](https://sysdig.com/)**

  **CNAPP with runtime insight** built on **Falco**, the open-source runtime security tool Sysdig created. Frost & Sullivan recognized Sysdig for container/K8s security leadership, noting Falco as the industry-standard runtime detection engine . **Pricing**: Agent-based per-container pricing with transparent model . **Free tier**: Trial available. **Best for**: teams wanting Falco-native runtime security with commercial support—**trade-off**: container-focused; broader CSPM may require additional tooling.



- **[Lacework (FortiCNAPP)](https://www.lacework.com/)**

  **AI-powered CNAPP** combining CWPP, CSPM, CIEM, and threat detection. Fortinet reports **75% reduction in compliance violations**, **100:1 alert-to-noise ratio**, and **80% faster investigations** for customers . **Pricing**: Quote-only. **Free tier**: None. **Best for**: organizations wanting consolidated CNAPP with behavioral anomaly detection—**trade-off**: integration into Fortinet ecosystem post-acquisition.



- **[Orca Security](https://orca.security/)**

  **Agentless CNAPP** using patented **SideScanning** for visibility across AWS, Azure, GCP, Oracle Cloud, Kubernetes, and serverless. Covers CSPM, CWPP, CIEM, DSPM, vulnerability management, malware detection, API security, and AI security in one platform . **Pricing**: Quote-only. **Free tier**: None. **Best for**: teams wanting agentless deployment with broad coverage across cloud providers .



- **[Atlassian Guard](https://www.atlassian.com/software/guard)**

  **Cloud security for Atlassian products** (Jira, Confluence, Bitbucket, Trello). **Premium** at **$8.18/user/month** adds proactive data loss prevention, suspicious activity detection, and threat response for Jira and Confluence Cloud . **Free tier**: Guard Standard included with Cloud Enterprise . **Best for**: Atlassian customers wanting native security controls for their Atlassian Cloud estate—**not** a general-purpose cloud threat detection platform.



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
