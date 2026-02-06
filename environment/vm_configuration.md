# Virtual Machine Configuration

This document describes the virtualized environment used to conduct all experiments
in the study. The goal of this configuration is to enable reproducibility of the
experimental *context* while maintaining strong isolation and preventing real-world
impact.

All experiments were performed in sandboxed virtual machines configured exclusively
for research purposes.

## Host System

- Virtualization platform: Oracle VirtualBox
- Host operating system: Desktop system capable of running multiple VMs concurrently
- No external cloud infrastructure was used

## Virtual Machines

Two virtual machines were used throughout the experiments:

### Attacker Environment

- Operating system: Kali Linux
- Role: Human-controlled attacker workstation
- Purpose:
  - Interacting with intentionally vulnerable targets
  - Running standard offensive security tools
  - Receiving data generated during controlled experiments

The Kali VM served as the platform through which the human adversary interacted
with the target systems, with guidance provided by the evaluated LLMs.

### Victim Environment

- Operating system: Windows 11
- Role: Target system
- Purpose:
  - Executing isolated test programs
  - Observing system behavior and partial attack outcomes
  - Collecting host-level artifacts (e.g., process activity, file output)

The Windows 11 VM was configured solely for experimentation and did not contain
personal data or production software.

## Networking Configuration

- Network type: Host-only virtual network
- Internet connectivity: Disabled
- External access: None

The host-only network ensured that:
- Virtual machines could communicate with each other
- No traffic could reach external networks or real systems
- All activity remained contained within the local host

## Safety and Isolation Controls

Several controls were enforced to prevent unintended impact:

- No bridged or NAT networking
- No interaction with live services
- No reuse of virtual machines outside the experiment
- Snapshots used to reset state between trials

All targets were either intentionally vulnerable applications or controlled
test programs created for research purposes.

## Relationship to the Paper

The paper provides the analytical interpretation of experiments conducted in this
environment.

This document exists to clarify the experimental setup and support reproducibility
without disclosing operational details that could enable misuse.
