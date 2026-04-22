# 🔥 Epistemic Exploration Toward Artificial General Intelligence

<p align="center">
  <b>"Epistemic Exploration Toward Artificial General Intelligence"</b>
  <br>
  <i>ArXiv 2026</i>
  <br><br>
  <b>◇ Responder → Reasoner → Agent → Prospector → Ecosystem ◇</b>
  <br>
  <i>Exploration as the Transition Mechanism</i>
</p>

<p align="center"><img src="fig/5levels.png" width="900"/></p>

<p align="center">
  <!-- <a href="#"><img src="https://img.shields.io/badge/📄_Paper-ArXiv-red" alt="Paper"></a> -->
  <!-- <a href="#"><img src="https://img.shields.io/badge/🌐_Website-Project_Page-blue" alt="Website"></a> -->
  <a href="https://github.com/banyikun/epistemic_exploration"><img src="https://img.shields.io/badge/GitHub-Repository-181717?logo=github" alt="GitHub"></a>
  <a href="#"><img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License"></a>
  <a href="#"><img src="https://img.shields.io/badge/Maintained%3F-Yes-brightgreen.svg" alt="Maintained"></a>
  <a href="#"><img src="https://img.shields.io/badge/PRs-Welcome-orange.svg" alt="PRs Welcome"></a>
</p>

<p align="center">
  <a href="https://github.com/banyikun/epistemic_exploration/stargazers"><img src="https://img.shields.io/github/stars/banyikun/epistemic_exploration?style=social" alt="GitHub stars"></a>
  <a href="https://github.com/banyikun/epistemic_exploration/network/members"><img src="https://img.shields.io/github/forks/banyikun/epistemic_exploration?style=social" alt="GitHub forks"></a>
</p>

> **If you find our survey helpful, please give it a ⭐ star to show your support! Thank you :)**

---

## 📣 Notices

> 🔥 This is a curated paper list for the survey **"Epistemic Exploration Toward Artificial General Intelligence"**, covering exploration mechanisms across reasoning, embodied AI, world models, and multi-agent systems.

> 🔥 **[Stay tuned for our full paper release, incorporating the latest developments.]**

> **[Always] [Add your papers]** We welcome all related papers! If you find any missed or new work, please open a Pull Request or contact us.

> **[Always] [Maintain]** We will keep this list updated frequently!

---

## 📑 Table of Contents

- [1. Overview](#1-overview)
  - [1.1 What is Epistemic Exploration?](#11-what-is-epistemic-exploration)
  - [1.2 Three Criteria](#12-three-criteria)
  - [1.3 Five-Level Trajectory Toward AGI](#13-five-level-trajectory-toward-agi)
  - [1.4 3×5 Taxonomy](#14-3×5-taxonomy)
- [2. Level 1–2: Responder → Reasoner (Reasoning-Space Exploration)](#2-levels-12-responder--reasoner--reasoning-space-exploration)
  - [2.1 Uncertainty-Driven Exploration](#21-uncertainty-driven-exploration)
  - [2.2 Competence-Driven Exploration](#22-competence-driven-exploration)
  - [2.3 Reachability-Driven Exploration](#23-reachability-driven-exploration)
- [3. Level 3: Reasoner → Agent (Perception- & Action-Space Exploration)](#3-level-3-reasoner--agent--perception--action-space-exploration)
  - [3.1 Digital Agents](#31-digital-agents)
  - [3.2 Embodied Agents](#32-embodied-agents)
- [4. Level 4: Agent → Prospector (Imagination-Space Exploration)](#4-level-4-agent--prospector--imagination-space-exploration)
- [5. Level 5: Prospector → Ecosystem (Coordination-Space Exploration)](#5-level-5-prospector--ecosystem--coordination-space-exploration)
- [6. Cross-Cutting Topics](#6-cross-cutting-topics)
- [7. Citation](#7-citation)

---

## 1. Overview

### 1.1 What is Epistemic Exploration?

> **Epistemic exploration** is the agent's capacity to actively acquire information that reduces its uncertainty about the world, convert that reduction into durable policy improvement, and keep future acquisition possible.

Unlike undirected exploration (e.g., ε-greedy), epistemic exploration is *intentional*, *belief-driven*, and *multi-scale*: the agent reasons about which actions are most informative and plans multi-step information-gathering strategies across reasoning trajectories, tool-use policies, embodied sensorimotor loops, world-model rollouts, and multi-agent coordination protocols.

### 1.2 Three Criteria

<p align="center"><img src="fig/3criteria.png" width="800"/></p>
<p align="center"><i>Figure: Foundation of Epistemic Exploration — Why, What, and How.</i></p>

We ground epistemic exploration in **three jointly necessary criteria**, each addressing a distinct failure mode of static optimisation:

| Criterion | What It Does | Failure Mode Addressed | Explores... |
|:---------:|:-------------|:-----------------------|:------------|
| **C1: Information Gain** | Actively reduces epistemic uncertainty via belief-updating observations | *Belief Stagnation* — frozen internal model under distribution shift | ...where it knows least |
| **C2: Value Improvement** | Converts new information into durable policy improvement | *Value Stagnation* — local optima lock-in, surrogate misalignment | ...what it cannot yet do well |
| **C3: Epistemic Reachability** | Preserves positive visitation over belief-consistent regions | *Reachability Collapse* — irreversible contraction of behavioural diversity | ...where it might otherwise never go |

These form a closed loop: **gain information → convert to value → keep the capacity to gain information alive → ...**

### 1.3 Five-Level Trajectory Toward AGI

We propose exploration as the **transition mechanism** between five levels of increasing agent sophistication. Each level introduces a qualitatively new exploration space that the previous level cannot access:

| Transition | Exploration Space | What Becomes Explorable |
|:-----------|:------------------|:------------------------|
| **L1→L2: Responder → Reasoner** | **Reasoning space** | Hypotheses, reasoning trajectories, latent thought representations |
| **L2→L3: Reasoner → Agent** | **Perception & action space** | Tool invocation, sensorimotor loops, memory management |
| **L3→L4: Agent → Prospector** | **Imagination space** | Counterfactual futures in learned world models, dual real-imagined exploration |
| **L4→L5: Prospector → Ecosystem** | **Coordination space** | Communication topologies, role assignments, shared world models |

### 1.4 3×5 Taxonomy

Our survey is organized as a **3×5 taxonomy** crossing three signal-driven methodologies with the five levels:

|  | **L1 Responder** | **L2 Reasoner** | **L3 Agent** | **L4 Prospector** | **L5 Ecosystem** |
|:-|:---|:---|:---|:---|:---|
| **Uncertainty-Driven** | Token entropy | Ensemble disagreement, semantic uncertainty | Active SLAM, prediction variance | Epistemic disagreement in latent space | Joint-belief uncertainty |
| **Competence-Driven** | Input difficulty | Iterative curricula, self-play | Skill bootstrapping, RL-VLA | Imagination-based skill discovery | Multi-agent self-play curricula |
| **Reachability-Driven** | Anti-repetition | Beam diversity, reasoning-path anti-foreclosure | Go-Explore, coverage curricula | Latent-space diversity bonuses | Role-diversity, anti-specialisation |

---

## 2. Levels 1–2: Responder → Reasoner — Reasoning-Space Exploration

The transition from **Responder** to **Reasoner** requires exploration in *reasoning space*: branching over token sequences, reasoning trajectories, and latent thought representations. The agent must search for informative hypotheses rather than simply produce reactive outputs.

<p align="center"><img src="fig/level1_reasoner.png" width="850"/></p>
<p align="center"><i>Figure: Levels 1–2 Reasoning-Space Exploration — Why (entropy escalation & reward stagnation), Where (tokens → turns → latent trajectories), and How (uncertainty / competence / reachability-driven).</i></p>

### 2.1 Uncertainty-Driven Exploration

Methods that prioritise exploration at high-uncertainty branching points in the reasoning process:

| Method | Strategy | Paper |
|:-------|:---------|:------|
| **CURE** | High-entropy tokens as re-branching anchors | Uncertainty-aware Reasoning Enhancement (2025) |
| **SPINE** | Concentrates updates on high-entropy branching points | Sparse Inference with Entropy (2025) |
| **TreeRL** | On-policy tree search from high-entropy steps | Tree-Structured RL for Reasoning (2025) |
| **CE-GPPO** | Coordinating entropy-gradient preservation | CE-GPPO (2025) |
| **SIREN** | Top-p & peak-entropy masks for meaningful exploration | Rethinking Entropy in LLM Reasoning (2025) |
| **AEPO** | Anchors entropy to user-specified target level | Arbitrary Entropy Policy Optimization (2025) |
| **ICPO** | Intrinsic confidence from relative generation probabilities | Intrinsic Confidence Policy Optimization (2025) |
| **REAL** | Categorical labels replacing scalar rewards | Rewards as Labels (2026) |

### 2.2 Competence-Driven Exploration

Methods that match problem difficulty to the model's evolving competence frontier:

| Method | Strategy | Paper |
|:-------|:---------|:------|
| **E2H** | Easy-to-hard curriculum with gradual fade-out | Easy to Hard Curriculum (2025) |
| **RLAAR** | Ability-gated curriculum with abstention reward | RL with Abstention-Aware Rewards (2025) |
| **Online Difficulty Filtering** | Selects medium-difficulty samples by current success rate | Dynamic Difficulty Filtering (2025) |
| **CDAS** | Historical performance gaps for robust difficulty estimation | Competence-Driven Adaptive Sampling (2025) |
| **HA-DW** | Tracks evolving competence, reweights difficulty | Hardness-Aware Dynamic Weighting (2026) |
| **SvS** | Self-synthesized harder variants from solved examples | Solve via Self-play (2025) |
| **Absolute Zero** | Reinforced self-play with zero external data | Absolute Zero Reasoner (2025) |

### 2.3 Reachability-Driven Exploration

Methods that prevent irreversible contraction of reasoning trajectory distributions:

| Method | Strategy | Paper |
|:-------|:---------|:------|
| **Trust-region methods** | KL penalties, PPO clipping to preserve pre-trained breadth | Various (2025) |
| **Anti-degeneration penalties** | Repetition penalties, length-budget constraints | Welleck et al. (2020), various (2025) |
| **SPO / KTAE** | Step-level credit assignment preserving alternative trajectories | Step Policy Optimization / KTAE (2025) |
| **VRPRM** | Process-level dense supervision for intermediate steps | Verifiable Reward PRM (2025) |
| **RLVRR** | Content coverage + style constraints for denser rewards | RL with Verifiable & Reward-Rich feedback (2026) |

---

## 3. Level 3: Reasoner → Agent — Perception- & Action-Space Exploration

At Level 3, the agent crosses from internal reasoning into **situated interaction with external environments**. Exploration unfolds in perception and action space, where every step incurs real cost.

### 3.1 Digital Agents

Agents operating in software-mediated environments (web, APIs, code interpreters):

| Paradigm | Method | Key Idea |
|:---------|:-------|:---------|
| **Uncertainty-Driven** | JitRL | Count-based exploration bonus for unseen state-action pairs |
| | Agent Q | MCTS with UCB for strategic state exploration |
| | KnowSelf | Self-perceived capability boundaries trigger reflection |
| | Search-o1 | Invokes web search upon encountering unfamiliar knowledge |
| **Competence-Driven** | PilotRL | Three-stage progressive RL curriculum |
| | Planner-R1 | Dense process-level rewards as priors |
| | RLTR | Tool-use completeness rewards |
| | Agent0-VL | Self-Evolving Reasoning Cycle (SERC) |
| | Absolute Zero | Joint proposer-solver self-play |
| **Reachability-Driven** | EGPO | Entropy bonus in advantage over CoT tokens |
| | EPO | Three-part entropy control for multi-turn RL |
| | RAPO | Retrieval-augmented policy optimization |
| | E³-TIR | Expert-guided branching at high-entropy prefixes |

### 3.2 Embodied Agents

<p align="center"><img src="fig/level3_embodied.png" width="850"/></p>
<p align="center"><i>Figure: Level 3 Embodied Agent Exploration — Uncertainty-driven active perception, competence-driven RL & test-time compute, and reachability-driven safety & reward engineering.</i></p>

Agents operating in physical/simulated environments with continuous action spaces:

| Paradigm | Method | Key Idea | Project |
|:---------|:-------|:---------|:--------|
| **Uncertainty-Driven (Active Perception)** | [ActiveSplat](https://arxiv.org/abs/2410.21955) | Gaussian splatting for information-maximizing viewpoint selection | [🔗](https://github.com/Li-Yuetao/ActiveSplat) |
| | [Conan](https://arxiv.org/abs/2311.02018) | Active reasoning in open-world environments | [🔗](https://github.com/ariesssxu/Conan-Active-Reasoning) |
| | [ActiveRIR](https://arxiv.org/abs/2404.16216) | Cross-modal audio-visual exploration | - |
| | [Fisher-info path planning](https://arxiv.org/abs/2410.17422) | Balances information gain with localization robustness | [🔗](https://github.com/JiangWenPL/multimodal-active) |
| **Competence-Driven** | **Offline RL-VLA**: [Q-Transformer](https://arxiv.org/abs/2309.10150), [Cal-QL](https://arxiv.org/abs/2303.05479) | Scale value learning to static trajectories | - |
| | **Online RL-VLA**: [VLA-RL](https://arxiv.org/abs/2505.18719), [FLaRe](https://arxiv.org/abs/2409.16578), [SimpleVLA-RL](https://arxiv.org/abs/2509.09674) | Real-time interactive policy exploration | [🔗](https://github.com/GuanxingLu/vlarl) / [🔗](https://github.com/JiahengHu/FLaRe) / [🔗](https://github.com/PRIME-RL/SimpleVLA-RL) |
| | **Hybrid**: [ConRFT](https://arxiv.org/abs/2502.05450), [SRPO](https://arxiv.org/abs/2511.15605), [Dual-Actor](https://arxiv.org/abs/2509.13774) | Stable offline-to-online transitions | [🔗](https://github.com/cccedric/conrft) / [🔗](https://github.com/SUSTechBruce/SRPO_MLLMs) |
| | **Test-Time**: [VLA-Reasoner](https://arxiv.org/abs/2509.22643) (MCTS), [DeepThinkVLA](https://arxiv.org/abs/2511.15669), [Hume](https://arxiv.org/abs/2505.21432) | Imagination before physical execution | [🔗](https://github.com/OpenBMB/DeepThinkVLA) / [🔗](https://github.com/hume-vla/hume) |
| | [SayCan](https://arxiv.org/abs/2204.01691), [Inner Monologue](https://arxiv.org/abs/2207.05608), [LM-Nav](https://arxiv.org/abs/2207.04429) | Language-guided objective-driven navigation | [🔗](https://github.com/google-research/google-research/tree/master/saycan) / [🔗](https://github.com/blazejosinski/lm_nav) |
| **Reachability-Driven** | [Eureka](https://arxiv.org/abs/2310.12931) | LLM-driven reward code synthesis | [🔗](https://github.com/eureka-research/eureka) |
| | [Recovery RL](https://arxiv.org/abs/2010.15920), [RECOVER](https://arxiv.org/abs/2404.00756), [SafeVLA](https://arxiv.org/abs/2503.03480) | Learned safety zones preserving reachable sets | [🔗](https://github.com/abalakrishna123/recovery-rl) / [🔗](https://github.com/PKU-Alignment/SafeVLA) |
| | [RND](https://arxiv.org/abs/1810.12894), [CurricuLLM](https://arxiv.org/abs/2409.18382) | Curiosity-driven and curriculum-based coverage | [🔗](https://github.com/openai/random-network-distillation) / [🔗](https://github.com/labicon/CurricuLLM) |

---

## 4. Level 4: Agent → Prospector — Imagination-Space Exploration

<p align="center"><img src="fig/level4_worldmodel.png" width="850"/></p>
<p align="center"><i>Figure: Level 4 Imagination-Space Exploration — Why (the dual exploration problem), Where (simulated rollouts, hazard zones, latent value landscapes), and How (MBRL, video generation, autonomous driving, social dynamics).</i></p>

The Prospector internalises a **world model** and faces a **dual exploration problem**: simultaneously gathering real data to refine the model AND searching imagined trajectories to extract policies.

| Challenge | Description | Key Methods |
|:----------|:------------|:------------|
| **Compounding Errors** | Single-step prediction errors accumulate exponentially over imagined horizons | MBPO, PETS, Dreamer v4 |
| **Noise-Hijacking Trap** | Curiosity wasted on irreducible stochasticity (noisy-TV problem) | RND, RIDES, learning-progress monitoring |
| **Fatal Detail Loss** | Safety-critical information lost in latent compression | Structured latent representations, 4D sparse voxels |

**Core World Model Families:**

| Method | Key Contribution |
|:-------|:-----------------|
| **Dreamer v1/v2/v3/v4** | Progressive imagination-based skill discovery in learned latent spaces |
| **DayDreamer** | Transfers imagination-based paradigm to physical robots |
| **PETS** | Ensemble-based disentanglement of aleatoric vs. epistemic uncertainty |
| **Plan2Explore** | Task-agnostic exploration via maximizing future ensemble disagreement |
| **MuZero** | Learned dynamics model with MCTS for planning |
| **iVideoGPT** | Interactive video generation as scalable world models |
| **World-Env / WMPO** | Internal simulators for safe GRPO/PPO updates in VLA |

---

## 5. Level 5: Prospector → Ecosystem — Coordination-Space Exploration

<p align="center"><img src="fig/level5_ecosystem.png" width="850"/></p>
<p align="center"><i>Figure: Level 5 Coordination-Space Exploration — Why (single-agent limitations), Where (communication, collaboration, role, deployment), and How (orchestration, ensemble, MARL, self-evolving agents).</i></p>

At the highest level, exploration enters **coordination space**: heterogeneous agents discover communication topologies, role specialisations, shared representations, and collaborative strategies.

| Challenge | Description |
|:----------|:------------|
| **Scalable Coordination Exploration** | The search space is combinatorial, hierarchical, and dynamic—which agents to activate, what communication to establish, how information flows |
| **Ecosystem-Level Credit Assignment** | Disentangling behavioural contribution from structural contribution under sparse, delayed feedback |
| **Diversity vs. Convergence Tension** | Balancing ecological diversity against system-level coherence |
| **Role–Communication Co-evolution** | Jointly evolving functional specialisation and information exchange protocols |

**Key Systems & Methods:**

| Method | Key Contribution |
|:-------|:-----------------|
| **MetaGPT** | Structured multi-agent coordination with role-based workflows |
| **AutoGen** | Flexible conversational multi-agent framework |
| **CAMEL** | Communicative agents for mind exploration |
| **Multi-agent Debate** | Structured deliberation improving collective reasoning (Du et al.) |
| **Learnable orchestration** | RL-evolved coordination topologies, optimisable agent graphs |

---

## 6. Cross-Cutting Topics

### Foundations
- **Three failure modes of static optimisation**: Belief Stagnation, Value Stagnation, Reachability Collapse
- **Unified Epistemic Exploration Objective**: Combines Bayes-optimal value (C2), cumulative information gain bonus (C1), and reachability constraint (C3)
- **Convergence**: As beliefs converge to truth, exploration automatically gives way to exploitation

### Biological Exploration Parallels
- **Sensory-motor embodiment** → Lévy flights, whisking, saccades
- **Intrinsic curiosity** → Dopaminergic information prediction errors
- **Meta-control** → Locus coeruleus-norepinephrine regulation
- **Cognitive simulation** → Hippocampal preplay sequences
- **Social exploration** → Swarm intelligence, Theory of Mind

### Evaluation Principles
- Benchmarks for epistemic exploration across reasoning, embodied AI, world models, and multi-agent settings
- Design principles for exploration-centric evaluation

### Open Challenges
- Open-domain scalable exploration for reasoning beyond verifiable tasks
- Safe exploration with predictive world action models
- Causal and counterfactual reasoning in imagination space
- Dynamic temporal abstraction for long-horizon planning
- Epistemic uncertainty quantification in imagination
- Scalable coordination-space exploration without combinatorial explosion

---

## 7. Citation

If you find this survey useful, please cite:

```bibtex
@article{ban2026epistemic,
  title={Epistemic Exploration Toward Artificial General Intelligence},
  author={Ban, Yikun and others},
  journal={arXiv preprint arXiv:XXXX.XXXXX},
  year={2026}
}
```

---

<p align="center">
  <i>This repository is actively maintained. If you find any errors or have new papers to suggest, please open an issue or submit a pull request!</i>
</p>
