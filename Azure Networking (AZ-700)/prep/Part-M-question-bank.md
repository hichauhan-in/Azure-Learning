# Part M — Exam Question Bank (100+ Questions)

> Section goal: A comprehensive self-test across **every AZ-700 domain**. ~20% Basic, ~20% Intermediate, ~60% Advanced/scenario, plus a self-quiz tracker. Each question has a concise answer and a **→ Part cross-reference** so you can revise weak spots fast.

**How to use:** Cover the answers. Say each answer **out loud** (the exam tests recall, not recognition). Mark each Q in the tracker as ✅ confident / 🟡 shaky / ❌ missed. Re-drill the ❌/🟡 until all ✅.

---

## 🟢 Basic (Q1–Q24) — vocabulary & core facts

**Q1.** How many usable IPs in an Azure /24 subnet? → *251 (256 − 5 reserved).* **[A,C]**
**Q2.** Name the three RFC 1918 private ranges. → *10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16.* **[A]**
**Q3.** Smallest deployable Azure subnet size? → */29 (recommended /28+).* **[A,C]**
**Q4.** What does a /16 give vs a /24? → *65,536 vs 256 addresses.* **[A]**
**Q5.** Layer 4 vs Layer 7 in one line? → *L4 = IP+port (TCP/UDP); L7 = HTTP-aware.* **[A,G]**
**Q6.** TCP vs UDP? → *TCP reliable/connection-oriented; UDP fast/connectionless.* **[A]**
**Q7.** What is DNS? → *Resolves names to IPs (internet phone book).* **[A,D]**
**Q8.** A record vs CNAME? → *A → IPv4; CNAME → another name.* **[A,D]**
**Q9.** Default route notation? → *0.0.0.0/0 (catch-all).* **[A,E]**
**Q10.** Can a VNet span two regions? → *No; one region only.* **[B,C]**
**Q11.** Is a resource group a network boundary? → *No, just a logical folder.* **[B]**
**Q12.** Region vs availability zone? → *Region = geographic area; AZ = separate datacentre within it.* **[B]**
**Q13.** What is Azure Resource Manager? → *The unified control-plane/deployment API.* **[B]**
**Q14.** Which built-in role manages networking with least privilege? → *Network Contributor.* **[B]**
**Q15.** What address types can a VNet use? → *Private RFC 1918, non-overlapping.* **[C]**
**Q16.** Magic subnet name for a VPN gateway? → *GatewaySubnet (/27).* **[C,F]**
**Q17.** Minimum size for AzureFirewallSubnet? → */26.* **[C,I]**
**Q18.** What does NAT Gateway provide? → *Scalable outbound-only internet for a subnet.* **[C]**
**Q19.** Which public IP SKU is recommended and why? → *Standard — secure-by-default, static, zonal.* **[C]**
**Q20.** Azure's magic DNS/probe IP? → *168.63.129.16.* **[D,G,J]**
**Q21.** Is VNet peering transitive? → *No.* **[E]**
**Q22.** Which subnet hosts Azure Firewall? → *AzureFirewallSubnet (/26).* **[C,I]**
**Q23.** Are NSGs stateful? → *Yes.* **[I]**
**Q24.** Which services include a WAF? → *Application Gateway and Front Door.* **[G,I]**

---

## 🟡 Intermediate (Q25–Q48) — applying concepts

**Q25.** Why must connected VNets not overlap? → *Routing is by prefix; overlaps make destinations ambiguous.* **[A,C,E]**
**Q26.** How do spokes share the hub's gateway? → *Hub: allow gateway transit; spoke: use remote gateways.* **[E,F]**
**Q27.** How to force spoke egress through a firewall? → *UDR 0.0.0.0/0 → firewall private IP.* **[E,I]**
**Q28.** Route tie-break order? → *Most specific prefix, then UDR > BGP > system.* **[E]**
**Q29.** Next hop "None" does what? → *Drops (blackholes) traffic.* **[E]**
**Q30.** S2S vs P2S VPN? → *Whole site (Local Network Gateway) vs single device (client software).* **[F]**
**Q31.** Is ExpressRoute encrypted by default? → *No; add IPsec/MACsec.* **[F,L]**
**Q32.** ExpressRoute private vs Microsoft peering? → *VNets (private IPs) vs Microsoft PaaS public endpoints.* **[F]**
**Q33.** Service Endpoint vs Private Endpoint — DNS? → *SE: no DNS change; PE: needs privatelink zone.* **[H]**
**Q34.** Can on-prem use a Service Endpoint? → *No; use Private Endpoint.* **[H]**
**Q35.** privatelink zone for Azure SQL? → *privatelink.database.windows.net.* **[D,H]**
**Q36.** What does an ASG do? → *Lets NSG rules target role-groups, not IPs.* **[I]**
**Q37.** What is a Service Tag? → *Microsoft-managed label for IP ranges (e.g. Internet, Storage).* **[I]**
**Q38.** NSG rule evaluation order? → *Priority lowest-first, first match wins.* **[I]**
**Q39.** Traffic Manager works at which layer? → *DNS-based (global), not a proxy.* **[G]**
**Q40.** Front Door vs Traffic Manager? → *AFD = global L7 proxy + CDN + WAF; TM = DNS only.* **[G]**
**Q41.** When use Application Gateway? → *Regional L7: URL/host routing, TLS, WAF.* **[G]**
**Q42.** Tool to find which NSG rule blocked a packet? → *IP Flow Verify / NSG Diagnostics.* **[J]**
**Q43.** Tool to verify routing path? → *Next Hop / Effective Routes.* **[J]**
**Q44.** Flow logs need what destinations? → *Storage (logs) + Log Analytics (Traffic Analytics).* **[J]**
**Q45.** Why no logs in Log Analytics? → *Diagnostic settings not configured.* **[J]**
**Q46.** Bastion solves what, in which subnet? → *RDP/SSH without public IPs; AzureBastionSubnet /26.* **[L]**
**Q47.** App Service VNet integration direction? → *Outbound (app → VNet).* **[L]**
**Q48.** Which traffic direction is billed? → *Egress; ingress generally free.* **[L]**

---

## 🔴 Advanced / Scenario (Q49–Q108)

**Q49.** *Spoke A can't reach spoke B in hub-and-spoke.* Cause + fix? → *Peering non-transitive; add UDRs via hub firewall, allow forwarded traffic, configure firewall.* **[E,K]**
**Q50.** *Private endpoint created; app still hits public IP.* Fix? → *Configure privatelink Private DNS zone linked to VNet (+ Resolver for on-prem).* **[D,H]**
**Q51.** *50 global branches, minimal ops, any-to-any, central security.* Design? → *Virtual WAN + Secured Virtual Hub.* **[F,K]**
**Q52.** *Global web app needs edge caching + WAF + fast failover.* → *Azure Front Door.* **[G]**
**Q53.** *Regional app needs path-based routing + protect from SQLi.* → *Application Gateway with WAF (Prevention).* **[G,I]**
**Q54.** *Thousands of outbound connections, no inbound, no SNAT exhaustion.* → *NAT Gateway.* **[C]**
**Q55.** *High-bandwidth private hybrid link with strong SLA, no internet.* → *ExpressRoute (+VPN failover for HA).* **[F]**
**Q56.** *Make a VPN gateway highly available.* → *Active-active and/or zone-redundant AZ SKU.* **[F]**
**Q57.** *Filter outbound by domain name (e.g. *.windowsupdate.com).* → *Azure Firewall application rule (FQDN).* **[I]**
**Q58.** *TLS inspection + IDPS required.* → *Azure Firewall Premium.* **[I,L]**
**Q59.** *Bidirectional DNS Azure↔on-prem, no DNS VMs.* → *Azure DNS Private Resolver (inbound+outbound+ruleset).* **[D]**
**Q60.** *Lock storage to one subnet, cloud-only, free.* → *Service Endpoint.* **[H]**
**Q61.** *Sensitive DB private to one resource, reachable from on-prem.* → *Private Endpoint + privatelink DNS over VPN/ER.* **[H]**
**Q62.** *Connect two on-prem sites THROUGH Azure.* → *ExpressRoute Global Reach.* **[F]**
**Q63.** *Lower ExpressRoute data-path latency, bypass gateway.* → *FastPath.* **[F,L]**
**Q64.** *Dynamic route exchange with an NVA, no manual UDRs.* → *Azure Route Server (RouteServerSubnet /27).* **[E,L]**
**Q65.** *NVA traffic not forwarding.* Likely cause? → *IP forwarding not enabled on NIC.* **[L]**
**Q66.** *Global HA stack for web tier?* → *Front Door → App Gateway → Load Balancer; zone-redundant + multi-region.* **[G,K]**
**Q67.** *Standard LB backend gets no traffic.* Common cause? → *NSG blocks it (secure-by-default) or failing health probe.* **[G,I]**
**Q68.** *Probe failing though app is up.* Check? → *168.63.129.16 reachable; correct probe port/path.* **[G,J]**
**Q69.** *Reduce cross-region networking cost.* → *Keep traffic regional/private; minimise egress.* **[L]**
**Q70.** *Admins need VM access without exposing 3389/22.* → *Azure Bastion.* **[L]**
**Q71.** *Two VNets same region need private connectivity.* → *Regional VNet peering.* **[E]**
**Q72.** *Cross-region private VNet connectivity.* → *Global VNet peering (or vWAN).* **[E]**
**Q73.** *Central egress inspection for all spokes.* → *Azure Firewall in hub + UDRs.* **[I,K]**
**Q74.** *Inbound DNAT to a backend via firewall.* → *Azure Firewall NAT rule.* **[I]**
**Q75.** *Web app must reach private SQL backend (outbound).* → *App Service VNet integration + Private Endpoint on SQL.* **[H,L]**
**Q76.** *Restrict which storage accounts a SE subnet can reach.* → *Service endpoint policies.* **[H,L]**
**Q77.** *Continuous A→B reachability with alerts.* → *Connection Monitor.* **[J]**
**Q78.** *One-time A→B test with latency/hops.* → *Connection Troubleshoot.* **[J]**
**Q79.** *See combined NSG effect on a NIC.* → *Effective Security Rules.* **[J]**
**Q80.** *Visualise who-talks-to-whom + blocked flows over time.* → *VNet Flow Logs + Traffic Analytics.* **[J]**
**Q81.** *Alert when VPN tunnel drops or SNAT near exhaustion.* → *Azure Monitor metric alerts.* **[J]**
**Q82.** *Need IPv6 for internet clients.* → *Dual-stack VNet with Standard public IP/LB.* **[L]**
**Q83.** *ExpressRoute global connectivity + higher VNet limits.* → *ExpressRoute Premium SKU.* **[L]**
**Q84.** *Unlimited data to nearby region, low cost.* → *ExpressRoute Local SKU.* **[L]**
**Q85.** *Encrypt traffic over ExpressRoute.* → *IPsec over ER, or MACsec with ER Direct.* **[F,L]**
**Q86.** *Share one gateway across many spokes.* → *Gateway transit + use remote gateways.* **[E,F]**
**Q87.** *Hub firewall private IP must match what?* → *The UDR next-hop IP on spokes.* **[E,I]**
**Q88.** *Why prefer Standard over Basic public IP/LB?* → *Zone-redundant, secure-by-default, supported; Basic retiring.* **[C,G]**
**Q89.** *Where do firewall/gateway logs go for analysis?* → *Log Analytics via Diagnostic settings.* **[J]**
**Q90.** *Resolve Azure private zone from on-prem.* → *Private Resolver inbound endpoint.* **[D]**
**Q91.** *Forward Azure queries for corp.local to on-prem DNS.* → *Private Resolver outbound endpoint + forwarding ruleset.* **[D]**
**Q92.** *Stop a VNet using its own gateway and force the hub's.* → *Spoke: use remote gateways (no local gateway).* **[E,F]**
**Q93.** *Block a specific malicious route entirely.* → *UDR next hop None.* **[E]**
**Q94.** *DDoS volumetric protection with tuning + analytics.* → *DDoS Network/IP Protection (paid).* **[I]**
**Q95.** *Protect public entry at L3–L7.* → *DDoS (L3/4) + WAF (L7) together.* **[I]**
**Q96.** *Many storage accounts but only allow one — anti-exfiltration.* → *Private Endpoint (specific resource).* **[H]**
**Q97.** *Choose vWAN vs manual hub-spoke.* → *vWAN = many regions/low ops; manual = control/NVA/single region.* **[K]**
**Q98.** *Document the whole network as code.* → *az group export / ARM/Bicep template.* **[K]**
**Q99.** *App Gateway can't route to backend pool.* Checks? → *Health probe, NSG, backend port, TLS settings.* **[G,J]**
**Q100.** *Disable a storage account's public access but keep app access.* → *Public access Disabled + Private Endpoint + DNS.* **[H]**
**Q101.** *Cross-subscription VNet connectivity.* → *VNet peering supports cross-subscription/cross-tenant.* **[E]**
**Q102.** *Reduce blast radius between workloads.* → *Separate spokes + NSG/ASG micro-segmentation.* **[I,K]**
**Q103.** *Why might 168.63.129.16 cause an outage if blocked?* → *Breaks DNS + LB health probes.* **[D,J]**
**Q104.** *Choose NVA over Azure Firewall.* → *Vendor features/licenses/control; you manage HA/patching.* **[L]**
**Q105.** *Lowest-latency global routing to nearest region for any protocol via DNS.* → *Traffic Manager Performance method.* **[G]**
**Q106.** *Route users by country for compliance.* → *Traffic Manager Geographic method.* **[G]**
**Q107.** *Active/passive regional failover via DNS.* → *Traffic Manager Priority method.* **[G]**
**Q108.** *Add IPv6 to an existing VNet.* → *Add IPv6 address space/subnet prefix (dual-stack), Standard SKUs.* **[L]**

---

## 🧭 Behavioral / "Why" prep (for interview mode — optional)
- "Why are you moving into cloud networking?" → tie to the hands-on project you built here.
- "Describe a time you troubleshot connectivity." → use the Part J playbook (NSG→Route→DNS→Probe) as a STAR structure.

(Full STAR/behavioral coverage is in **Part N**'s closing section.)

---

## 📊 Self-Quiz Tracker

Fill this in as you drill. Target: **all ✅** before booking the exam.

| Domain (Part) | Qs | ✅ Confident | 🟡 Shaky | ❌ Missed | Re-drill date |
|---------------|----|-----------|---------|----------|---------------|
| Fundamentals (A,B) | Q1–14 | | | | |
| VNets/IP/DNS (C,D) | Q15–20, 33–35, 50, 59–60 | | | | |
| Routing/Connectivity (E,F) | Q21,26–32,49,55–56,62–64,86,92 | | | | |
| Load Balancing (G) | Q39–41,52–53,66–68,105–107 | | | | |
| Private Access (H) | Q33–35,60–61,75–76,96,100 | | | | |
| Security (I) | Q23–24,36–38,57–58,73–74,94–95,102 | | | | |
| Monitoring (J) | Q42–45,77–81,89,103 | | | | |
| Design/Misc (K,L) | Q46–48,51,69–70,82–85,97–98,104,108 | | | | |

> 🎯 **Readiness rule of thumb:** consistently scoring **80%+** across all domains, *out loud*, on the Advanced section = a strong sign you're exam-ready. Anything below 70% in a domain → re-read that Part.

---

## 🧠 30-Second Memory Hooks (bank-wide)
- **Numbers:** /24=251, smallest /29, AzFwSubnet /26, GatewaySubnet /27, Bastion /26, magic IP **168.63.129.16**.
- **Picks:** L4→LB, regional L7→App Gw, global DNS→Traffic Manager, global L7→Front Door.
- **Private:** SE=cheap/subnet/no-DNS; PE=private IP/specific/DNS/on-prem.
- **Hybrid:** VPN cheap/internet; ExpressRoute private/unencrypted; vWAN managed mesh.
- **Security:** NSG(L3/4)+ASG; Firewall(L3–7 FQDN); WAF(L7 OWASP); DDoS(volumetric).
- **Debug:** IP Flow Verify→NSG; Next Hop→route; Connection Monitor→over time.

---

*Next suggested section:* **Part N — Exam-Day Strategy & Cheat Sheet** (how AZ-700 is scored, case-study technique, time management, a master decision-table, and a one-page night-before cheat sheet).
