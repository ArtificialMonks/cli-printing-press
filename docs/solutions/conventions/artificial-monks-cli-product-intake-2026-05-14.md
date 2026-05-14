---
title: "Artificial Monks CLI product intake: start in the Printing Press, split only after validation"
module: product-intake
tags:
  - artificial-monks
  - cli-products
  - printing-press
problem_type: convention
---

# Artificial Monks CLI Product Intake

Artificial Monks CLI product ideas should start inside the Printing Press flow, not as a fresh standalone repository per idea.

## Rule

When an Artificial Monks product needs a CLI:

1. Add or reuse a Printing Press catalog target.
2. Print or reprint the CLI into the local Printing Press library.
3. Keep product-specific research, proof, and polish artifacts in the Printing Press manuscript/library flow.
4. Publish or share from the library flow when it is useful to others.
5. Split into a dedicated repo only after the CLI has a validated product surface, install story, and maintenance owner.

## Why

Separate repos are tempting during prototyping, but they make every CLI carry its own install logic, verification habits, release decisions, and product docs. The Printing Press already provides the shared loop: source discovery, generation, MCP/CLI parity, dogfood, verification, publish packaging, and repeatable updates.

For early AM product CLIs, the standalone repo should be treated as product evidence or a legacy source to absorb, not as the long-term codebase.

## Rekordbox Amigo Application

`ArtificialMonks/rekordbox-amigo-cli` proved the product direction: local-first Rekordbox XML audits, tagging suggestions, set-prep prompts, privacy boundaries, and a hosted browser audit.

The next implementation step should happen under `ArtificialMonks/cli-printing-press`:

- Catalog target: `catalog/rekordbox-amigo.yaml`
- CLI shape: read-only Rekordbox XML audit, folder/crate matching, tag suggestions, set planning, privacy report, and guided Amigo workflow
- Safe default: no direct Rekordbox database writes and no silent edits to music files
- Public story: useful for all Rekordbox users, not only one artist, label, or folder

Once the printed CLI has a stable Go implementation and install story, it can be published from the Printing Press library or split into a dedicated product repo if there is a clear reason.
