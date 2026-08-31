<div align="center">

# jacob valdez

**i build systems in which models can act on computers, robots, simulations, and scientific instruments — then retain inspectable evidence of what happened.**

founder, [CommandAGI](https://commandagi.com) · founding architect, [SuperCognition Labs](https://supercognitionlabs.com) · san francisco

[jvboid.dev](https://jvboid.dev) · [x / @jvboid](https://x.com/jvboid) · [linkedin](https://www.linkedin.com/in/jacob-f-valdez)

</div>

---

## what i'm building

### [CommandAGI](https://github.com/CommandAGI/commandagi) — branchable execution environments for agents

i'm building a live agent platform around a stricter primitive than “chat with tools”: give an agent a realtime environment with actual state, let people watch and intervene, and make the state snapshotable, forkable, resumable, and billable.

the current system includes:

- a Next.js 15 / React 19 web + mobile PWA;
- a Cloudflare control plane using Hono, Durable Objects, D1, and KV for per-session realtime state, compute-pool capacity, and prepaid metering;
- keyless GCE provisioning for ephemeral Ubuntu computer-use environments;
- a Python runtime that closes the screenshot → model → mouse/keyboard action loop inside each VM;
- data-driven 3d simulation worlds plus bring-your-own-robot registration;
- Python and TypeScript SDKs, an early Go SDK, and runnable SO-101 / Android / iOS robot clients;
- WebRTC voice intervention and live observation while an agent is operating;
- machine-checkable service contracts, escrow, and objective arbitration for agent-to-human and agent-to-agent work.

the architectural invariant is that compute is finite, environment state is first-class, and every useful action should be attributable to a session, actor, machine state, and settlement path.

### [WIN / B-WIN](https://github.com/JacobFV/win) — a heterogeneous interaction substrate for world models

WIN is my attempt to stop flattening heterogeneous evidence into one tensor before learning begins. state variables retain their native support, coordinate frame, clock, units, uncertainty, and update law; explicitly typed interactions connect them, and a lazy resolver materializes only the paths required by a query.

the substrate currently implements:

- fully qualified world-state addresses over `(entity, domain, support, channel, clock)`;
- native-clock relations, coordinate transforms, gaussian-splat supports, covers, overlap algebra, and uncertainty propagation;
- typed interactions, pressure composition, hybrid execution, overlap reconciliation, and path-following learning;
- source cards whose evidence roles and missingness constraints become runtime-forbidden update paths;
- provenance-aware release gates and per-artifact licence lineage;
- a domain-independent demo world, with a hard dependency boundary preventing `win` from importing the brain-specific realization.

B-WIN instantiates that substrate for brain, body, environment, measurement, and intervention dynamics. the current code contains cortical splat banks, head electromagnetism validated against analytic solutions, fitted held deposits, and an end-to-end visual/EEG slice from eye state to predicted volts at named electrodes. results are stored beside their baselines and controls, including negative results; “implemented” and “works” are deliberately different fields.

## selected 2026 systems and experiments

### [recursive omnimodal video-action model](https://github.com/JacobFV/recursive-omnimodal-video-action-model)

ran **26 architecture experiments / 236 training runs** across three looped video-transformer generations, then preserved the complete null results instead of retrofitting a triumph narrative.

measured findings include:

- recurrent looping behaved as weight-sharing regularization, not iterative reasoning, across three independent null tests;
- three loops were optimal across the tested freeze levels and model scales;
- a 350k-parameter frozen loop beat an 11.5m-parameter unfrozen alternative on action prediction;
- mild progressive sharpening improved contact-detection f1 by 1.30×;
- omnimodal capability tracked the canvas topology rather than recurrence itself.

the current program grafts and ablates alternative information-routing topologies inside CogVideoX-2B, with matched parameter budgets, fixed seeds, explicit condition manifests, and per-run artifacts.

### [chem-0](https://github.com/JacobFV/chem-0) — inspectable low-cost robot control

built a local research platform in which an llm operates a LeRobot SO-101/SO-100 arm through the same typed tool surface used by both an Electron console and a stdio MCP server.

the shared TypeScript backend owns experiment/event logging, SQLite state, blob artifacts, streamed model sessions, and voice i/o. a line-delimited JSON bridge dispatches into the Python/OpenCV/LeRobot hardware core. joint-space and Cartesian commands pass through calibrated limits, workspace checks, maximum-step bounds, interpolation, repo-local URDF kinematics, and `placo` fk/ik before reaching the Feetech bus. camera frames, pose tables, arm state, and motion commands remain inspectable through the agent interface.

active follow-on work lives in [phys-0](https://github.com/JacobFV/phys-0).

### [eeg acquisition chain](https://github.com/JacobFV/eeg-acquisition-chain)

built an interactive, deterministic model of the physical path from cortical population current dipoles to a multiplexed adc input: volume conductor → csf → skull → scalp → contact mechanics → electrode/electrolyte interface → afe → filtering/pga → amux.

the model separates attenuation from irreversible spatial mixing; derives frequency-dependent complex contact impedance from geometry, force, skin state, electrolyte, and a cpe interface; exposes finite-cmrr and impedance-imbalance leakage independently; itemizes input-referred Johnson, voltage, current, and quantization noise; and simulates settling, charge injection, channel leakage, sampling skew, quantization, and actual alias folding. every numeric input is marked literature, datasheet, fitted/derived, engineering assumption, measured, or latent.

### [yt2ctx](https://github.com/JacobFV/yt2ctx) — youtube → executable visual context

built one TypeScript pipeline exposed as a Next.js app, cli, http api, and MCP server. it downloads video, demuxes/transcribes audio, samples and vision-scores frames, embeds descriptions for semantic novelty, selects representative frames, and compiles the result into a style bible, Blender/Remotion shot specs, agent implementation prompts, anti-slop checks, markdown/json/jpg artifacts, and a portable zip.

the web path adds HttpOnly auth, Postgres job state, Vercel Blob artifacts, and per-stage realtime progress; the cli and MCP surfaces share the same core instead of reimplementing the pipeline.

## earlier systems work

at **AGI, Inc.** (2025–2026), i worked across the agent runtime, mobile integration, and evaluation tooling, then owned API/SDK/partner integration surfaces spanning iOS, on-device llms, quantization, schemas, and the agent control plane. i also built VibeStartup, an agent-workflow system for taking a startup from structured intent through execution.

earlier public work includes [bsbr](https://github.com/JacobFV/bsbr), a chunk-attention + block-retrieval approach to near-linear long-sequence modeling; [jnumpy](https://github.com/JacobFV/jnumpy), a neural-network stack built on NumPy; TensorCode; MPNets; Node Tree; MLN Dashboard; computer-use simulations; and physical builds going back to cnc machines, actuators, and embedded control.

## what i optimize for

- runtime state over screenshots of outcomes;
- typed boundaries over ambient convention;
- provenance, controls, and baselines over naked metrics;
- native clocks and coordinate frames over premature homogenization;
- simulators that can be challenged by an oracle, not simulators that grade themselves;
- systems where humans and agents can both inspect, interrupt, fork, and resume the causal trace.

most of this work is open because architectures compound faster when their interfaces, failures, and negative results are legible.

<sub>last structural rewrite: 2026-08-31</sub>
