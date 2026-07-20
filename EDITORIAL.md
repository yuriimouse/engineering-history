# Editorial roles

This document formally records the roles used in the `engineering-history`
project.

## Author, project owner, and primary source

**Yurii Prudius (`yuriimouse`)**

Responsibilities:

- owns and maintains the repository;
- provides the original recollections, surviving materials, and corrections;
- decides which statements accurately represent his experience;
- approves the final wording and publication of reconstructed material;
- remains the final authority when editorial interpretation conflicts with
  remembered fact.

## Technical editor and reconstruction assistant

**ChatGPT**

Responsibilities:

- structures raw recollections into coherent technical documents;
- prepares Markdown files and Git patches;
- separates confirmed memory, probable reconstruction, open questions, and
  documentary evidence;
- checks new details against previously recorded material;
- identifies contradictions, missing links, and questions worth revisiting;
- explains architectural decisions without replacing the historical context
  with modern terminology;
- preserves the author's voice while improving clarity and technical precision.

The editor does not claim independent authorship of the historical events and
must not invent missing technical details. Any inference must be explicitly
marked as interpretation or hypothesis.

## Working agreement

The project uses the following workflow:

1. Yurii recalls a fact, event, constraint, decision, or uncertainty.
2. ChatGPT records or restructures it in a proposed patch.
3. Yurii reviews and applies the patch.
4. Git records the development of the reconstruction.
5. Later corrections are added transparently rather than silently rewriting
   the history of how the reconstruction evolved.

## Editorial principle

The purpose of this repository is twofold:

1. to preserve Yurii's engineering history;
2. to show how architecture emerges from a problem model and real constraints.

The repository is not intended to turn recollections into legend. Technical
accuracy, uncertainty, context, and causality take priority over dramatic
presentation.

## Effective date

This working agreement was established on **2026-07-20**, after the first
repository bootstrap was successfully pushed to GitHub.
