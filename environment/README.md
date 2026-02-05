# Experimental Environment

This document describes the experimental environment used across all case studies.

## Virtualization Setup

- Host system: Single physical machine
- Hypervisor: Oracle VirtualBox
- Networking: Host-only network
- External connectivity: Disabled

## Attacker Environment

- OS: Kali Linux
- Purpose: Tool execution and result collection
- No persistent services exposed

## Target Environments

### Web Application Target
- Damn Vulnerable Web Application (DVWA)
- Security level adjusted only when explicitly stated
- Hosted locally on a Windows VM

### Endpoint Target
- Windows 11 virtual machine
- Default firewall and endpoint protections enabled unless stated otherwise

## Isolation Guarantees

- No internet access
- No interaction with real systems
- No real user data
