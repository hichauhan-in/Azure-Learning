# Azure Networking (AZ-700) — Study Guide

> **Goal:** Go from *new to networking and Azure* to *confidently passing AZ-700 (Designing and Implementing Microsoft Azure Networking Solutions)* — never blank out, understand the **concept behind every answer**, and recognise exam traps.
>
> **Mode:** Exam prep. Every Part ends with **⭐ Likely Exam Questions** and **🧠 Memory Hooks**, plus a giant **Exam Question Bank** and an **Exam-Day Strategy** Part near the end.
>
> **Pitched for:** A beginner — every term is explained in plain English with a real-world analogy *before* it's used. No assumed networking knowledge.

---

## How to use this guide

1. Read the Parts **in order** — each one builds on the last (foundations → core Azure networking → connectivity → security → design → exam drills).
2. Each Part goes **beginner → advanced**, calls out **🎯 exam-specific gotchas**, and ends with a **🛠️ Hands-on Lab** so you build a real project as you learn.
3. After each Part, do the **⭐ Likely Exam Questions** out loud before peeking at answers.
4. When a Part references another, follow the link.
5. Tell me **"next"** (or name a Part) and I'll write the next file. I create Parts **one at a time** so each gets full depth.

> **🛠️ The running project:** Across the Parts you'll incrementally build a **secure hub-and-spoke enterprise network in Azure** — VNets, DNS, peering, a VPN to "on-prem", load-balanced web apps, private database access, a firewall, and monitoring. By Part K you'll have a portfolio-grade architecture.

---

## The Plan — Grouped Index

### 🟢 Group 1 — Foundations (start here, zero knowledge assumed)
- **Part A — Networking Fundamentals From Scratch** — IP addresses, binary, CIDR/subnets, public vs private IP, DNS, ports, TCP/UDP, the OSI model, how routing works. *The vocabulary everything else depends on.*
- **Part B — Azure & Cloud Basics for Networking** — subscriptions, regions, availability zones, resource groups, Azure Resource Manager (ARM), how the Azure "software-defined network" actually works.

### 🔵 Group 2 — Core Networking Infrastructure *(AZ-700 domain: 20–25%)*
- **Part C — Virtual Networks, Subnets & IP Addressing** — VNets, subnets, address spaces, public IPs, NAT Gateway, IP planning that won't overlap.
- **Part D — Name Resolution & Azure DNS** — public DNS zones, Private DNS zones, the Private Resolver, custom DNS.

### 🟣 Group 3 — Routing & Connectivity *(AZ-700 domains: routing 15–20%, connectivity 15–20%)*
- **Part E — VNet Connectivity & Routing** — VNet peering, system routes, User-Defined Routes (UDRs), service chaining, gateway transit, BGP basics.
- **Part F — Hybrid Connectivity** — VPN Gateway (Site-to-Site & Point-to-Site), ExpressRoute, Virtual WAN. Connecting on-premises to Azure.

### 🟠 Group 4 — Delivering & Securing Applications
- **Part G — Load Balancing & Application Delivery** — Azure Load Balancer, Application Gateway, Traffic Manager, Azure Front Door (when to use which).
- **Part H — Private Access to Azure Services** *(AZ-700 domain: 10–15%)* — Service Endpoints, Private Endpoints, Private Link.
- **Part I — Network Security** *(part of Secure & Monitor, 15–20%)* — NSGs, ASGs, Azure Firewall, Web Application Firewall (WAF), DDoS Protection.
- **Part J — Monitoring & Troubleshooting** *(rest of Secure & Monitor)* — Network Watcher, flow logs, Connection Monitor, diagnostics.

### 🔴 Group 5 — Putting It Together & Exam Drills
- **Part K — Design Scenarios & Architecture Patterns** — hub-and-spoke, secured hub, common AZ-700 case-study layouts.
- **Part L — Miscellaneous & Deeper Topics** — IPv6, cost optimisation, encryption in transit, current Azure networking trends, exam "extra edge".
- **Part M — Exam Question Bank (100+ questions)** — ~20% Basic / 20% Intermediate / 60% Advanced, with answers, hints and Part cross-references, plus a self-quiz tracker.
- **Part N — Exam-Day Strategy & Cheat Sheet** — how AZ-700 is scored, case-study technique, time management, "decision tree" quick-pick tables, and a one-page night-before cheat sheet.

---

## Progress Tracker

| Part | Title | Group | Status |
|------|-------|-------|--------|
| A | [Networking Fundamentals From Scratch](prep/Part-A-networking-fundamentals.md) | Foundations | ✅ Done |
| B | [Azure & Cloud Basics for Networking](prep/Part-B-azure-cloud-basics.md) | Foundations | ✅ Done |
| C | [Virtual Networks, Subnets & IP Addressing](prep/Part-C-vnets-subnets-ip.md) | Core Infra | ✅ Done |
| D | [Name Resolution & Azure DNS](prep/Part-D-name-resolution-dns.md) | Core Infra | ✅ Done |
| E | [VNet Connectivity & Routing](prep/Part-E-connectivity-routing.md) | Routing & Connectivity | ✅ Done |
| F | [Hybrid Connectivity](prep/Part-F-hybrid-connectivity.md) | Routing & Connectivity | ✅ Done |
| G | [Load Balancing & Application Delivery](prep/Part-G-load-balancing.md) | Apps & Security | ✅ Done |
| H | [Private Access to Azure Services](prep/Part-H-private-access.md) | Apps & Security | ✅ Done |
| I | [Network Security](prep/Part-I-network-security.md) | Apps & Security | ✅ Done |
| J | [Monitoring & Troubleshooting](prep/Part-J-monitoring-troubleshooting.md) | Apps & Security | ✅ Done |
| K | [Design Scenarios & Architecture Patterns](prep/Part-K-design-scenarios.md) | Drills | ✅ Done |
| L | [Miscellaneous & Deeper Topics](prep/Part-L-misc-deeper-topics.md) | Drills | ✅ Done |
| M | [Exam Question Bank (100+)](prep/Part-M-question-bank.md) | Drills | ✅ Done |
| N | [Exam-Day Strategy & Cheat Sheet](prep/Part-N-exam-day-strategy.md) | Drills | ✅ Done |

**Legend:** ⬜ Not started · 🟨 In progress · ✅ Done — **All 14 Parts complete! 🎉**

---

## What to do now (revision plan)

1. **Read Parts A→N in order** — each builds on the last with plain-English explanations, analogies, Mermaid diagrams, 🎯 exam gotchas, and a 🛠️ hands-on lab.
2. **Build the running project** as you go (hub-and-spoke in `rg-az700-lab`) — by [Part K](prep/Part-K-design-scenarios.md) you have a portfolio-grade architecture; export it as code.
3. **Drill [Part M](prep/Part-M-question-bank.md)** (100+ Qs) *out loud*; use the self-quiz tracker until every domain is ✅.
4. **Read [Part N](prep/Part-N-exam-day-strategy.md)** the week before and the night before — strategy + one-page cheat sheet.
5. **Clean up Azure** when done: `az group delete --name rg-az700-lab --yes --no-wait`.

*Tell me to expand any Part, add more practice questions, generate a printable cheat sheet, or run a mock interview / mock exam.*
