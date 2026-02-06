# Spyware Experiment Methodology

This document describes the methodology used to evaluate large language models
(LLMs) as assistive tools in spyware-style capability assembly. The focus of this
study is on **model behavior, guidance patterns, and failure modes**, rather than
on producing or deploying operational malware.

## Experimental Objective

The objective of this experiment was to assess whether LLMs can meaningfully
assist a human adversary in assembling components commonly associated with
spyware, such as:

- Input capture
- Local data collection
- Network-based data transmission
- Listener configuration and coordination

The study evaluates **partial success, misconfiguration, refusal behavior,
and error propagation**, rather than full end-to-end compromise.

## Human-in-the-Loop Model

All experiments followed a human-in-the-loop threat model:

- The human operator initiated all actions
- The LLM served only in an advisory capacity
- No autonomous execution was performed by the model
- The human operator followed model guidance verbatim, without correction

This approach mirrors realistic misuse scenarios while preserving experimental
control.

## Environment and Constraints

Experiments were conducted exclusively within sandboxed virtual machines owned
and controlled by the researcher. The environment included:

- A Windows 11 virtual machine acting as a simulated victim
- A Kali Linux virtual machine acting as a simulated attacker
- Host-only networking with no external connectivity
- Test files and synthetic input data only

No real user data, credentials, or third-party systems were involved.

## Artifact Collection

Rather than releasing functional spyware code, this repository includes
**non-operational artifacts** documenting experimental outcomes, including:

- Screenshots of LLM-generated instructional diagrams
- Listener setup attempts and resulting behavior
- Evidence of partial data capture or transmission
- Error messages, refusals, and failed execution paths

Artifacts are provided in the `artifacts/spyware/` directory and are intended
solely for transparency and academic analysis.

## Safety and Disclosure Controls

To prevent misuse:

- Executable scripts are not included
- Reusable payloads are excluded
- Step-by-step execution instructions are omitted
- Code excerpts, where present, are incomplete or abstracted

This methodology prioritizes reproducibility of *experimental context* without
enabling real-world exploitation.

## Relationship to Paper Results

Findings derived from this methodology are reported in the spyware case study
section of the accompanying paper. This document exists to support open science
requirements by clarifying experimental scope, constraints, and ethical limits.
