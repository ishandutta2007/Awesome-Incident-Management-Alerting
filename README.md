# Awesome-Incident-Management-Alerting

## Top Incident Management & Alerting Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on On-Call Scheduling, Alert Routing & Self-Hosted Incident Response*  

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Incident Management & Alerting**. These tools enable engineering and operations teams to detect critical issues, route alerts to the right responders, coordinate resolution, and learn from post-incident reviews—minimizing downtime and restoring service quickly.



**Examples** include Opsgenie, PagerDuty, VictorOps (Splunk On-Call), Datadog Incident Management, Better Stack, incident.io, Squadcast, Splunk On-Call, BigPanda, and Rootly (the category leaders).



**Open-source emphasis**: Incident Management & Alerting is a domain where open-source tooling is **genuinely mature for on-call scheduling and alert routing, but fragmented across the incident lifecycle**. **GoAlert** is the standout self-hosted PagerDuty alternative—a single-binary, Apache-2.0 licensed platform for on-call scheduling, automated escalations, and multi-channel notifications (SMS, voice, Slack, email) . **Keep** provides the strongest alert management and AIOps layer—deduplicating, correlating, and prioritizing alerts from multiple monitoring tools with a workflow engine for automated remediation; it was acquired by Elastic in 2025 and remains open source . **OneUptime** bundles incident management with observability, on-call rotations, and status pages . The critical caveat: **Grafana OnCall OSS was archived on March 24, 2026**—the repository is now read-only, with active development moved to Grafana Cloud IRM . **No open-source project matches the integrated incident response workflow** of PagerDuty or incident.io—those platforms combine alerting, on-call, status pages, retrospectives, and Slack-native coordination in one product.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[PagerDuty](https://www.pagerduty.com/)**  

  The market-leading incident response platform; on-call scheduling, alert routing, escalation policies, status pages, and post-incident reviews with extensive integrations.



- **[Opsgenie (Atlassian)](https://www.atlassian.com/software/opsgenie)**  

  Incident management and alerting within the Atlassian ecosystem; on-call schedules, routing rules, escalation, and Slack/Teams integration.



- **[VictorOps (Splunk On-Call)](https://www.splunk.com/)**  

  Incident management with on-call scheduling and alert routing; integrates with Splunk observability for unified incident response.



- **[Datadog Incident Management](https://www.datadoghq.com/)**  

  Incident response integrated with Datadog's observability platform; correlates incidents with metrics, logs, and traces for faster root cause analysis.



- **[Better Stack](https://betterstack.com/)**  

  Observability and incident management with uptime monitoring, on-call scheduling, and status pages; includes AI post-mortems and SOC 2 Type 2 / ISO 27001 compliance.



- **[incident.io](https://incident.io/)**  

  Incident management platform with automated Slack-based workflows, status page generation, and post-incident retrospectives; focused on engineering-led response.



- **[Squadcast](https://www.squadcast.com/)**  

  Incident management platform for SRE teams; Intelligent Alert Grouping, Live Call Routing, Stakeholder Groups, and AI Suggestions for faster response.



- **[BigPanda](https://www.bigpanda.io/)**  

  AIOps platform for event correlation and incident intelligence; aggregates alerts across monitoring tools and reduces noise through machine learning.



- **[Rootly](https://rootly.com/)**  

  Incident management platform with Slack-native workflows, automated retrospectives, and on-call scheduling.



## Open-Source GitHub Projects



### On-Call Scheduling & Escalation (GoAlert, emu-oncall)



- **[GoAlert](https://github.com/target/goalert)**  

  The **leading open-source self-hosted PagerDuty alternative** (Apache 2.0, built by Target) . Features: **on-call scheduling**, **automated escalations**, and **multi-channel notifications** (SMS, voice, Slack, email); distributed as a **single binary** with Docker images; no per-user pricing . **Best for teams wanting proven on-call scheduling and escalation** without commercial licensing—but it is on-call/alerting-focused rather than a full incident response platform with status pages and retrospectives.



- **[emu-oncall](https://github.com/ebogdanov/emu-oncall)**  

  An **open-source REST API template for on-premise Grafana OnCall** compatibility (Go, v0.0.11) . Routes alerts to HTTP APIs, VoIP, or custom systems; supports SMS plugins and schedule tracking via ICal . **Best for teams already using Grafana OnCall on-premise** wanting custom notification channels—but it has **no UI** and is a template rather than a standalone product .



### Alert Management & AIOps (Keep)



- **[Keep](https://github.com/keephq/keep)**  

  The **leading open-source alert management and AIOps platform** (Apache 2.0, acquired by Elastic in 2025, remains open source) . Features: **single pane of glass** for all alerts and incidents; **deduplication, correlation, filtering, and enrichment**; **bi-directional integrations** with monitoring tools; **workflow engine** (YAML-based "GitHub Actions for monitoring") for automated remediation; and **AIOps 2.0** for AI-powered correlation and summarization . **Best for teams wanting to reduce alert noise and automate workflows**—but it is an alert correlation layer, not a full on-call scheduling platform (pair with GoAlert).



### Full Incident Management Platforms (OneUptime, TheHive)



- **[OneUptime](https://github.com/OneUptime/oneuptime)**  

  A **complete open-source observability platform** including **incident management, on-call rotations, log analysis, performance tracking, and status pages** . **Best for teams wanting an all-in-one observability + incident stack**—but it is a substantial platform requiring deployment and maintenance.



- **[TheHive](https://github.com/TheHive-Project/TheHive)**  

  Open-source **security incident response platform** (AGPL-3.0) for collaborative investigation of security incidents; case management, observable analysis, and task tracking . **Best for security operations (SOC) teams** handling security incidents—not general IT incident management with on-call paging.



### Additional Strong Open-Source Options



- **StackStorm** — Event-driven automation platform that connects monitoring tools to actions; rule engine with YAML-based workflows, ChatOps support, and pause-for-approval steps . **Best for automating incident response actions**—not an alerting or on-call tool on its own .

- **Netdata** — Real-time infrastructure monitoring with per-second granularity and a built-in alerting engine that notifies via Slack, email, PagerDuty, or custom webhooks . **Best for fast detection**—but it lacks built-in on-call scheduling or escalation logic .

- **Grafana OnCall OSS** — **CAUTION**: archived on March 24, 2026; repository is read-only, with development moved to Grafana Cloud IRM . **Do not adopt for new projects**—use GoAlert or Keep instead.



**Frameworks for building custom systems**: For **on-call scheduling and escalation**, GoAlert is the mature open-source standard . For **alert deduplication, correlation, and workflow automation**, Keep provides the AIOps layer . For an **all-in-one observability + incident platform**, OneUptime . For **security incident response**, TheHive . **Avoid Grafana OnCall OSS**—it is archived and no longer maintained . **No open-source project matches the integrated incident response workflow** of PagerDuty or incident.io—choose based on whether you need on-call (GoAlert), alert management (Keep), or a full platform (OneUptime).



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Incident management platforms handling production alerts and responder data must comply with organizational security policies; **self-hosted solutions place full responsibility for uptime, notification deliverability, and integration maintenance on the operator**.

- **Open-source incident management is mature for on-call and alerting but fragmented**—GoAlert provides production-grade on-call scheduling , and Keep provides alert correlation and AIOps . However, **Grafana OnCall OSS was archived in March 2026** , and **no open-source project matches the integrated incident response workflow** (alerting + on-call + status pages + retrospectives) of PagerDuty or incident.io. Choose based on whether you need on-call (GoAlert), alert management (Keep), or a full platform (OneUptime).

- Verify license terms for commercial use; GoAlert uses Apache 2.0 , and Keep uses Apache 2.0 for its core .



---



**Made for SREs, DevOps engineers, on-call responders, and IT operations teams.**  

Let's make incident management more open, but with clear eyes about the archived Grafana OnCall project and the integrated incident response gaps that commercial platforms still fill.
