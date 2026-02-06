# SQL Injection Case Study Artifacts

This directory contains curated artifacts from the SQL injection case study
described in the paper.

The artifacts included here provide **visual evidence of observed behavior**
during blind SQL injection experiments conducted with LLM assistance, under
controlled and intentionally vulnerable conditions.

## Included Artifacts

The artifacts in this directory illustrate the following stages and outcomes:

- Blind SQL injection responses indicating whether a queried condition evaluated
  as true or false (e.g., record exists vs. record missing)
- Identification of injectable parameters by automated tooling
- Enumeration of database contents in cases where exploitation progressed
- Comparative outcomes across different LLM-assisted runs

These artifacts are representative examples selected to demonstrate key
behaviors and decision points discussed in the paper.

## Purpose of These Artifacts

The purpose of including these artifacts is to support analysis of:

- Whether LLM assistance enabled progress beyond vulnerability detection
- How inference-based (blind) SQL injection was confirmed
- Differences in exploitation success across models
- The limits of automation even when vulnerabilities are present

The artifacts document **results and system responses**, not exploitation
instructions.

## What Is Intentionally Excluded

To prevent misuse and ensure responsible disclosure, this directory does not
include:

- sqlmap command invocations
- Payload strings or injection syntax
- Session cookies or authentication material
- Full database dumps beyond illustrative examples

Reproducing these results requires independent configuration of a vulnerable
environment and informed human decision-making.

## Experimental Context

All experiments were conducted against Damn Vulnerable Web Application (DVWA)
instances configured explicitly for research purposes. Security settings were
adjusted only as documented in the paper to expose known vulnerabilities.

No experiments targeted real-world systems or external infrastructure.

## Relationship to the Paper

The paper provides the full methodological description and interpretation of
these experiments.

This directory supplies **supporting visual artifacts** referenced by the
analysis, without duplicating figures already included in the manuscript.
