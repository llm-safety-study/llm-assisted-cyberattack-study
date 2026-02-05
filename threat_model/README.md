# Threat Model

This repository adopts the same threat model described in Section 3 of the paper. The goal is to enable reproducibility of experimental assumptions while maintaining appropriate ethical boundaries for security research.

## Human Adversary Model

We assume a human adversary with basic to intermediate technical skill, representative of a novice penetration tester, student attacker, or motivated individual. The adversary possesses general familiarity with operating systems, networking concepts, and common offensive security tools, but lacks advanced expertise in exploit development, malware engineering, or reverse engineering.

The adversary’s objective is not to invent novel attack techniques, but to reduce cognitive and technical effort by leveraging a large language model (LLM) for syntax recall, tool suggestions, code fragments, and troubleshooting guidance. All attack actions, including environment configuration, payload execution, error correction, and interpretation of results, are performed manually by the human operator.

## LLM Role and Capabilities

The LLM is treated strictly as an advisory-only system. It provides natural language explanations, procedural guidance, and code templates, but has no direct access to target systems, no ability to execute code, and no persistent memory across interactions.

The model cannot observe live system state and relies entirely on user-provided context such as screenshots, error messages, or textual descriptions. Prompt manipulation strategies such as character play, re-contextualization, and iterative refinement are permitted to approximate an upper bound on model assistance. Despite these favorable assumptions, the LLM remains constrained by its lack of system-level awareness, temporal continuity, and persistent state management.

## Attack Surface and Experimental Environment

All experiments are conducted in fully sandboxed virtual environments configured solely for research purposes. Targets include intentionally vulnerable systems such as Damn Vulnerable Web Application (DVWA) and isolated Windows virtual machines.

Systems are connected using host-only networking, preventing interaction with external infrastructure or live systems. Defensive mechanisms are weakened only when explicitly documented, such as lowering DVWA security levels to expose SQL injection vulnerabilities. These changes are treated as experimental controls rather than realistic defaults.

## Defender Assumptions

Defenders are assumed to employ baseline protections appropriate to each environment, including default firewall rules, endpoint protection mechanisms, and application-level defenses when enabled.

Advanced AI-aware defenses, such as prompt monitoring, AI-assisted intrusion detection, or LLM-aware filtering, are intentionally excluded. This isolates the contribution of attacker-side LLM assistance without conflating results with emerging defensive technologies.

## Out-of-Scope Claims

This work explicitly excludes:
- Fully autonomous AI-driven attackers
- Real-world, uncontrolled attack deployment
- Claims that LLM-assisted attacks outperform skilled human adversaries
- Long-term security implications or prevalence in the wild

The study does not aim to optimize attacks or measure real-world success rates. Instead, it systematically characterizes where LLM-assisted attack construction breaks down, even under permissive and controlled conditions.

## Multiple-Model Assumption

Multiple state-of-the-art LLMs are evaluated under identical experimental conditions. Each model is treated as an advisory-only system and subjected to the same prompt strategies, attack objectives, and sandboxed environments. This enables comparative analysis of whether observed capability boundaries are model-specific or structural across contemporary LLM architectures.

## Threat Model Diagram

![Human-in-the-loop threat model for LLM-assisted cyberattack construction](threat_model.png)

