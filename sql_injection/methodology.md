# SQL Injection Experiment Methodology

This document describes the methodology used to evaluate large language models
(LLMs) as assistive tools in automated SQL injection exploitation. The emphasis
of this study is on **LLM guidance behavior, prompt responsiveness, and execution
e
failure or success under constrained conditions**, rather than on providing
reusable attack instructions.

## Experimental Objective

The objective of this experiment was to measure whether LLMs can assist a human
operator in configuring and executing automated SQL injection tools when
provided with limited contextual information.

The study focuses on:
- Command construction assistance
- Flag selection and adjustment
- Interpretation of tool output
- Iterative guidance following partial failure or success

The experiment does **not** evaluate novel exploitation techniques or manual
payload crafting.

## Human-in-the-Loop Model

All SQL injection experiments followed a human-in-the-loop model:

- The human operator initiated all tool execution
- The LLM acted solely as an advisory system
- Commands were copied exactly as suggested by the model
- No manual correction or optimization was performed

All outcomes are therefore attributed entirely to the LLM’s guidance.

## Target Environment

Experiments were conducted against a deliberately vulnerable web application
configured for instructional use. The environment included:

- Damn Vulnerable Web Application (DVWA)
- Blind SQL injection scenarios
- Low security configuration
- Isolated virtual network with no external exposure

The target application was hosted within a sandboxed virtual machine controlled
by the researcher.

## Tooling Constraints

The automated exploitation tool `sqlmap` was used as the primary testing
instrument. Constraints included:

- No custom tamper scripts
- No external wordlists beyond defaults
- No manual SQL payload construction
- No out-of-band exploitation techniques

The LLM was responsible for suggesting command structure and flags based solely
on prompt context and tool output.

## Artifact Collection

To support transparency without enabling misuse, this repository includes
**non-operational artifacts** documenting experimental behavior, including:

- Screenshots of blind SQL injection result states
- Tool output demonstrating detected injection vectors
- Database enumeration success or failure
- Model-specific differences in guidance effectiveness

Artifacts are stored in `artifacts/sql_injection/` and are provided for academic
analysis only.

## Safety and Disclosure Controls

To prevent real-world misuse:

- Full executable command sequences are not reproduced
- Target URLs are sanitized or redacted
- Payload strings are truncated or abstracted
- No credentials or live endpoints are included

This methodology prioritizes reproducibility of **experimental conditions**,
not exploit replication.

## Relationship to Paper Results

Results derived from this methodology are reported in the SQL injection case
study section of the accompanying paper. This document exists to clarify
experimental scope, constraints, and attribution of outcomes in support of
responsible disclosure and open science requirements.
