# Cybersecurity Intrusion Detection Simulation — Agent Based Modeling

An agent-based simulation of network intrusion attacks and defense mechanisms, built in NetLogo.

---

## Overview

This project simulates a 17-node network under cyberattack from multiple malicious agents, while defender agents respond in real time. It demonstrates how Agent Based Modeling can capture the emergent, dynamic nature of cybersecurity threats that traditional analytical models cannot replicate.

---

## How It Works

The simulation models a 17-node network arranged in three rings centered around a main server. Each node can be attacked, compromised, quarantined, or recovered depending on the agents operating within the environment.

**Attacker Agents:**

| Agent | Behavior |
|---|---|
| Bot | Automated low-level attacks with moderate threat score |
| Hacker | Targeted high-threat attacks on specific nodes |
| Worm | Self-propagating — spreads to neighboring nodes with 35% probability |

**Defender Agents** patrol the network and respond to compromised nodes using two configurable defense mechanisms:

- **Firewall** — blocks 60% of incoming attacks before they reach nodes
- **Intrusion Detection System (IDS)** — monitors traffic, assigns threat scores, and logs suspicious behavior with configurable detection accuracy

---

## Results

| Scenario | Detection Rate |
|---|---|
| No defense | Low — attacks propagate freely |
| Firewall only | Moderate — blocks attacks at entry |
| IDS only | Moderate — detects but does not block |
| Firewall + IDS combined | 85%+ detection with significantly fewer successful breaches |

Three attack patterns were identified during simulation: threat level anomalies, repeated attack detection, and worm propagation clustering.

---

## Setup

1. Download and install [NetLogo](https://ccl.northwestern.edu/netlogo/)
2. Open `CYBERSECURITY INTRUSION DETECTION SIMULATION.nlogox` in NetLogo
3. Use the interface controls to toggle Firewall and IDS on/off and run the simulation
