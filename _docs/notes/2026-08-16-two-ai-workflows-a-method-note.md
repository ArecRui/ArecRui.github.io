---
title: "Two AI Workflows, One Method Note"
date: 2026-08-16
category: "AI and Society"
note: "yes"
excerpt: "A communication researcher automates scholarly intelligence and homepage maintenance with AI agents — and re-reads selective exposure for the algorithmic age."
layout: single
sidebar:
  nav: "main"
share: false
comments: false
---

A communication researcher wires two AI-agent pipelines — one that gathers, analyses and presents scholarly intelligence, another that maintains the academic front-page — and something unexpected happens: the setup becomes a live re-reading of **selective exposure** for the algorithmic age. The agent broadens what you would never look at; the human keeps the judgment and the creation. This note distils that setup into a reusable method.

## The one-line core

Automating "intelligence intake → analysis → presentation" and "academic-front maintenance" is, at bottom, a scholar outsourcing exposure breadth to a machine while reserving exposure depth for themselves — a small, repeatable autoethnography of AI-mediated scholarship.

## Three claims

**1. The automated intelligence stream is a scholar's "external memory + bias-correction" device.**
Selective exposure theory (the three-element model) predicts that, under algorithmic distribution, people narrow their information horizon and reinforce prior positions. A fixed-schedule agent that force-pulls full-spectrum signal (frontiers / policy / side-hustle / weekly digests) counteracts the filter bubble from the outside. This is a ready-made empirical scene for **computational communication** and **AI & communication** — the "human–agent division of labour" is itself the object of study.

**2. Homepage automation turns "scholarly identity capital" into a compoundable asset.**
A static-site template plus an API-writing loop lets the front-page update with output and drives maintenance friction toward zero. Underneath is the **AI literacy** kernel: the researcher drives the tool rather than being defined by it. The face is no longer frozen for three years; it becomes a continuously accumulating, presentable asset.

**3. The layered architecture is a transferable "personal research infrastructure" paradigm.**
Both pipelines share one skeleton: **collect → private sink → relay hub → public access**. The key move is isolating sensitive raw data in the private layer and exposing only finished products in the public layer. The layering is reproducible by any researcher with regular information needs, independent of discipline.

## Traps (what not to do)

- **Treating automation as "no-thinking."** A report without a human review gate lets topic drift pollute the scholarly face. The gate is already set: private by default, a single yes/no, used to kill drift.
- **Publishing the tutorial instead of the idea.** Exposing repo names, public links, or key workflows leaks unpublished research intelligence and personal infrastructure. Reframe as *argument*, not *steps*.
- **Collecting heavily, judging lightly.** A report that only lists, with no value judgment, is unused. The academic value of an intelligence stream is in filtering and ranking, not in搬运 (carrying).

## Boundaries

- **Truthfulness is the academic lifeline.** The intelligence stream must hang on a live retrieval connector; otherwise the generated content is not real search and carries no citation value (current hazard: daily reports not yet wired to a search connector — to be fixed).
- Fits researchers with *regular* information needs; pure ad-hoc research does not.
- Separate the language strategy: the public site in English (international audience); reports may mix Chinese and English (self-use + convertible to Chinese content).

## The sentence to take away

> The agent does not think for you, but it can see what you would never look at. The new division of labour: delegate exposure to the machine, keep judgment for yourself.

## Appendix: the speakable skeleton (sanitised, publishable)

- **Pipeline A (academic face):** local output → static-site generation → templated deployment → custom-domain public access.
- **Pipeline B (intelligence hub):** scheduled retrieval → self-contained HTML generation → private-repo sink → relay-hub aggregation → single public entry point.
- **Unifying principle:** private layer stores raw, public layer exposes only finished products; automation owns *breadth of exposure*, the human owns *depth of judgment*.
