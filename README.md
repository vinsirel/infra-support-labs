# Infrastructure Support Labs

Hands-on lab reports exploring networking, firewall troubleshooting, and virtualization support using tools such as Cisco Packet Tracer, Wireshark, vSphere, and vCenter.

This repository documents what I configure, test, deliberately break, troubleshoot, and learn. Each lab emphasizes evidence-based troubleshooting: establishing a working baseline, identifying symptoms, forming hypotheses, testing them, isolating the root cause, implementing a resolution, and verifying recovery.

> These labs are performed in controlled learning environments. Technical caveats and learning environment limitations are discussed in each lab.

## Lab Roadmap

| Lab                                             | Status  | Primary Focus                                            |
| ----------------------------------------------- | ------- | -------------------------------------------------------- |
| Packet Path, ARP, and Routed Traffic            | Planned | Following traffic within and between networks            |
| Firewall Rules and Traffic-Flow Troubleshooting | Planned | Evaluating rules and diagnosing blocked traffic          |
| vSphere and vCenter Operational Fundamentals    | Planned | Building familiarity with virtual infrastructure support |

---

## 1. Packet Path, ARP, and Routed Traffic

**Status:** In-Progress
**Tools:** Cisco Packet Tracer and Wireshark

This lab examines how traffic moves between endpoints on the same network and across routed networks. I'm using packet inspection and device-level evidence to follow ARP requests, Ethernet frames, IP packets, switch forwarding, and default-gateway behavior.

The lab focuses on questions such as:

* How does a host determine whether a destination is local or remote?
* When and why does a host send an ARP request?
* Which Layer 2 addresses change as traffic crosses a router?
* Which Layer 3 addresses remain consistent from source to destination?
* How can commands and packet captures identify where communication is failing?

After validating the working topology, I'm introducing a connectivity failure and documenting the process used to isolate, correct, and verify the problem.

**Evidence:**

* Network topology
* IP addressing and interface configuration
* ARP tables
* Switch MAC address tables
* Routing information
* Ping and traceroute results
* Packet captures showing ARP and ICMP traffic

---

## 2. Firewall Rules and Traffic-Flow Troubleshooting

**Status:** Planned

This lab will explore how firewall policy determines whether traffic is permitted or denied. The investigation will begin with the four core parts of a firewall rule:

1. Source
2. Destination
3. Service, port, or protocol
4. Action

It will also consider operational details such as traffic direction, security zones, rule order, and logging where applicable.

The troubleshooting portion will examine a scenario in which legitimate traffic is blocked because part of the rule does not match the actual traffic flow. I will document how I compare the intended communication path with the configured policy, use available evidence to find the mismatch, and verify that the corrected rule allows only the intended traffic.

**Planned evidence:**

* Network or traffic-flow diagram
* Relevant rule configuration
* Source and destination details
* Port and protocol validation
* Connectivity tests before and after correction
* Logs or packet evidence showing permitted or denied traffic

---

## 3. vSphere and vCenter Operational Fundamentals

**Status:** Planned
**Tools:** VMware vSphere and vCenter

This lab will build operational familiarity with VMware virtual infrastructure and the distinction between an ESXi host and centralized management through vCenter.

The lab will focus on common support tasks and investigative questions, including:

* What responsibilities belong to ESXi versus vCenter?
* How can an administrator inspect VM power state, health, and resource usage?
* How are virtual networking and datastore availability reflected in the management interface?
* What information is useful when triaging a VM or host alert?
* Why should snapshots not be treated as substitutes for backups?
* When should a support technician troubleshoot further, escalate, or follow a formal change process?

The final scope of the failure scenario will be documented after the working lab environment has been established and validated.

**Planned evidence:**

* Lab environment overview
* Host and VM inventory
* VM state and resource information
* Virtual networking configuration
* Datastore information
* Alerts, events, or task history
* Troubleshooting and post-resolution validation

---

## Report Structure

Each completed lab report will follow the same general structure:

* Objective
* Environment and topology
* Configuration summary
* Baseline validation
* Failure introduced or problem investigated
* Expected behavior and observed symptoms
* Troubleshooting process
* Root cause and resolution
* Post-resolution verification
* Technical observations
* Lessons learned
* Real-world application
* Screenshots, commands, logs, or packet evidence
* Limitations and next steps

During troubleshooting, I will organize meaningful diagnostic steps around four questions:

1. **Hypothesis:** What might be causing the symptom?
2. **Test:** What action or observation can evaluate that hypothesis?
3. **Evidence:** What does the result demonstrate?
4. **Conclusion:** What can be ruled in, ruled out, or investigated next?

## Purpose

These labs are intended to strengthen my ability to reason through infrastructure-support problems and communicate that reasoning clearly.

Although a controlled lab cannot reproduce the scale, risk, access controls, or operational pressures of a production environment, it provides a safe place to develop technical familiarity. In production, the same troubleshooting principles would be applied alongside organizational procedures for authorization, change control, documentation, escalation, and recovery planning.

## Progress

This repository is actively being developed. Reports and supporting evidence will be added as each lab is completed.
