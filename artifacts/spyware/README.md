# Spyware Case Study Artifacts

This directory contains curated artifacts from the spyware assembly case study
described in the paper.

The artifacts included here focus on **observable outcomes and system behavior**
rather than payload construction or deployment mechanics.

## Included Artifacts

For each evaluated large language model, this directory includes:

- A listener-side artifact demonstrating whether data was received
- A corresponding output artifact illustrating partial or attempted data capture
  (e.g., keylogging results)

These artifacts are provided **once per model** to enable comparative analysis
of LLM-assisted behavior under identical experimental conditions.

## Purpose of These Artifacts

The artifacts are intended to support analysis of:

- Whether LLM assistance enabled end-to-end spyware functionality
- The degree of partial success achieved (e.g., data capture without persistence)
- Differences in model guidance leading to success, failure, or runtime errors
- Limitations encountered during integration and execution

Importantly, these artifacts document **results**, not instructions.

## What Is Intentionally Excluded

To prevent misuse, this directory does **not** include:

- Spyware source code
- Payload binaries or shellcode
- Deployment commands or configuration steps
- Network exfiltration instructions
- Persistence mechanisms

The absence of these elements reflects deliberate responsible disclosure.

## Safety and Ethics

All experiments were conducted in isolated virtual machines configured exclusively
for research purposes. Targets were controlled, local systems with no external
connectivity.

The artifacts included here cannot be used to reproduce spyware without substantial
independent development effort and are insufficient for operational misuse.

## Relationship to the Paper

The paper presents the methodological details, analysis, and interpretation of
these experiments.

This directory provides **supporting visual evidence** demonstrating the observed
outcomes referenced in the spyware case study, without duplicating figures already
included in the manuscript.
