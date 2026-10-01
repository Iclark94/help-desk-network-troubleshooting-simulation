# help-desk-network-troubleshooting-simulation
Self-directed Help Desk simulations practicing network troubleshooting, DNS, gateways, ports, Wi-Fi issues, and systematic problem-solving.

## Overview

This repository documents a self-directed Help Desk troubleshooting simulation designed to strengthen practical network troubleshooting and systematic problem-solving skills.

The simulations focus on common Tier 1 scenarios involving Wi-Fi connectivity, internet access, internal websites, DNS, default gateways, network adapters, and TCP ports.

The goal was to practice thinking through an issue systematically rather than simply memorizing commands.

---

## Troubleshooting Method

The primary troubleshooting framework used throughout the simulations was:

**Symptom → Hypothesis → Test → Result → Conclusion → Next Test**

Instead of asking:

> "What command should I run?"

The approach was:

> "What do I need to prove?"

This helps determine which test is appropriate and what the result means.

---

# Scenario 1: Connected to Wi-Fi but No Internet

### Problem

A user reports:

> "My computer says it's connected to Wi-Fi, but I can't get on the Internet. Everyone else is online."

### My Initial Reasoning

Because other users are able to access the Internet, the issue is less likely to be an organization-wide or ISP-wide outage.

The investigation should focus on the affected computer and its network path.

### Troubleshooting Path

```powershell
ipconfig

Purpose:

Determine what network configuration the computer received.

Important information includes:

IPv4 address
Subnet mask
Default gateway
DNS servers

Next:

ping <default-gateway>

Purpose:

Determine whether the computer can communicate with the local network gateway.
