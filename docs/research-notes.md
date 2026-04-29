# tmux for prompt_agent: Prompt-Conditioned Session Adapter

## Purpose

This document records the research framing behind the static GitHub Pages site. The project studies how tmux can be adapted for prompt_agent as a durable terminal substrate for agentic work.

## Research Question

How can prompt_agent preserve reasoning context while tmux evolves through commands, panes, and partial failures?

## Working Thesis

The adapter compresses session history into prompt-relevant state while retaining enough provenance to support repair and reproducibility.

## Design Claims

- Prompt context is built from pane summaries, recent commands, and explicit artifacts.
- Repair loops keep failed outputs attached to the originating instruction.
- Context compression is evaluated against replayable terminal evidence.

## Evaluation Lens

- Prompt-state faithfulness
- Repair quality after command failure
- Compression loss in long sessions


## Threats to Validity

- Terminal state can be over-instrumented, causing an adapter to measure artifacts of the harness rather than real agent behavior.
- A final successful artifact may hide poor recovery behavior, repeated command attempts, or fragile focus management.
- Agent-specific adapters can become difficult to compare unless trace schemas remain explicit and documented.

## Hero Image Source

The GitHub Pages hero image uses a 700x500 version of the shared tmux CUA screenshot, copied into `docs/assets/hero.png` and displayed below the page title at its native size.
