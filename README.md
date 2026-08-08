# Diffusers - Xavier JP5

This fork is the Xavier-controlled source for diffusion pipelines, schedulers, and model-component behavior used by the worker dependency set.

## Role in the Xavier stack

- Pins behavior needed by the Horde Worker v13 backend.
- Provides a place to investigate FLUX and SDXL component lifetime on shared 32 GB memory.
- Preserves the normal worker safety and bridge contract.
- Does not claim FLUX production stability merely because a manual pipeline can fit in memory.

## Project status

This is an experimental integration fork. Full success requires repeated end-to-end worker jobs, safety processing, submission, and recovery-free operation.

## Build discipline

Native builds must use exactly one compiler worker.

## Upstream

Forked from `huggingface/diffusers`. Upstream documentation covers normal Diffusers usage; this fork carries Xavier-specific integration and backports.
