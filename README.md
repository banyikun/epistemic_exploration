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
| | [TTRL](https://arxiv.org/abs/2504.16084) | Test-time RL via majority-voted pseudo-rewards turns inference disagreement into exploration |
| **Competence-Driven** | PilotRL | Three-stage progressive RL curriculum |
| | [WebRL](https://arxiv.org/abs/2411.02337) | Self-evolving online curriculum from failure trajectories for web agents |
| | Planner-R1 | Dense process-level rewards as priors |
| | RLTR | Tool-use completeness rewards |
| | [ReTool](https://arxiv.org/abs/2504.11536) | RL rewards strategic tool-invocation patterns, penalises redundant calls |
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
| | **Real-world RL foundations**: [SERL](https://github.com/rail-berkeley/serl), [HIL-SERL](https://hil-serl.github.io/), [DPPO](https://arxiv.org/abs/2409.00588) | Sample-efficient on-robot RL with demos, human-in-the-loop interventions, and the first stable PPO through diffusion denoising trajectories | [🔗](https://github.com/rail-berkeley/serl) / [🔗](https://github.com/rail-berkeley/hil-serl) / [🔗](https://github.com/irom-princeton/dppo) |
| | **Online RL-VLA**: [VLA-RL](https://arxiv.org/abs/2505.18719), [FLaRe](https://arxiv.org/abs/2409.16578), [SimpleVLA-RL](https://arxiv.org/abs/2509.09674) | Real-time interactive policy exploration | [🔗](https://github.com/GuanxingLu/vlarl) / [🔗](https://github.com/JiahengHu/FLaRe) / [🔗](https://github.com/PRIME-RL/SimpleVLA-RL) |
| | **Hybrid**: [ConRFT](https://arxiv.org/abs/2502.05450) (extends HIL-SERL with consistency policy), [SRPO](https://arxiv.org/abs/2511.15605), [Dual-Actor](https://arxiv.org/abs/2509.13774) | Stable offline-to-online transitions on real hardware | [🔗](https://github.com/cccedric/conrft) / [🔗](https://github.com/SUSTechBruce/SRPO_MLLMs) |
| | **Test-Time**: [VLA-Reasoner](https://arxiv.org/abs/2509.22643) (MCTS), [DeepThinkVLA](https://arxiv.org/abs/2511.15669), [Hume](https://arxiv.org/abs/2505.21432) | Imagination before physical execution | [🔗](https://github.com/OpenBMB/DeepThinkVLA) / [🔗](https://github.com/hume-vla/hume) |
| | [SayCan](https://arxiv.org/abs/2204.01691), [Inner Monologue](https://arxiv.org/abs/2207.05608), [LM-Nav](https://arxiv.org/abs/2207.04429) | Language-guided objective-driven navigation | [🔗](https://github.com/google-research/google-research/tree/master/saycan) / [🔗](https://github.com/blazejosinski/lm_nav) |
| **Reachability-Driven** | [Eureka](https://arxiv.org/abs/2310.12931) | LLM-driven reward code synthesis | [🔗](https://github.com/eureka-research/eureka) |
| | [Recovery RL](https://arxiv.org/abs/2010.15920), [RECOVER](https://arxiv.org/abs/2404.00756), [SafeVLA](https://arxiv.org/abs/2503.03480) | Learned safety zones preserving reachable sets | [🔗](https://github.com/abalakrishna123/recovery-rl) / [🔗](https://github.com/PKU-Alignment/SafeVLA) |
| | [RND](https://arxiv.org/abs/1810.12894), [CurricuLLM](https://arxiv.org/abs/2409.18382) | Curiosity-driven and curriculum-based coverage | [🔗](https://github.com/openai/random-network-distillation) / [🔗](https://github.com/labicon/CurricuLLM) |

### 📚 RL-VLA Paper Collection

**Legend:**
- **Action:** AR (Autoregressive), Diffusion, Flow (Flow-matching)
- **Reward:** D (Dense Reward), S (Sparse Reward)
- **Model Type:** MB (Model-based), MF (Model-free)
- **Environment:** Sim. (Simulation), Real (Real-world)
- **Task:** MT (Multi-task), ST (Single-task)

#### Offline RL-VLA

Offline RL trains VLA models on pre-collected static datasets, enabling learning independently from environment interactions. This paradigm is suitable for high-risk or resource-constrained deployment scenarios.

**Key Research Directions:**
- **Data Utilization:** Effective utilization of static datasets for policy improvement
- **Objective Modification:** Customizing RL objectives for novel architectures and data augmentation

| Method | Date | Publication | Sim. | Real | Base VLA Model | Action | Reward | Algorithm | Type | Project |
|:---|:---|:---|:---:|:---:|:---|:---|:---:|:---|:---:|:---|
| [Q-Transformer](https://arxiv.org/abs/2309.10150) | 2023.10 | [CoRL23](https://proceedings.mlr.press/v229/) | ✓ | ✗ | Transformer | AR | S | CQL | MF | - |
| [PAC](https://arxiv.org/abs/2412.06685) | 2024.02 | [ICML24](https://proceedings.mlr.press/v267/) | ✓ | ✓ | Perceiver-Actor-Critic | AR | S | AC | MF | [🔗](https://github.com/MaxSobolMark/PolicyAgnosticRL) |
| [GeRM](https://arxiv.org/abs/2403.13358) | 2024.03 | [IROS24](https://ieee-iros.org/) | ✓ | ✗ | Transformer-MoE | AR | S | CQL | MF | [🔗](https://github.com/Songwxuan/GeRM) |
| [MoRE](https://arxiv.org/abs/2503.08007) | 2025.03 | [ICRA25](https://2025.ieee-icra.org/) | ✗ | ✓ | MLLM-MoE | AR | S | CQL | MF | - |
| [ReinboT](https://arxiv.org/abs/2505.07395) | 2025.05 | [ICML25](https://proceedings.mlr.press/v267/zhang25dr.html) | ✓ | ✓ | ReinboT | AR | D | DT + RTG | MF | [🔗](https://github.com/COST-97/reinboT) |
| [CO-RFT](https://arxiv.org/abs/2508.02219) | 2025.08 | - | ✗ | ✓ | RoboVLMs | AR | D | Cal-QL + TD3 | MF | - |
| [ARFM](https://arxiv.org/abs/2509.04063) | 2025.09 | [AAAI26](https://ojs.aaai.org/index.php/AAAI/article/view/38944) | ✓ | ✓ | π₀ | Flow | D | ARFM | MF | - |
| [π\*₀.₆](https://arxiv.org/abs/2511.14759) | 2025.11 | - | ✗ | ✓ | π₀.₆ | Flow | D | RECAP | MF | - |
| [NORA-1.5](https://arxiv.org/abs/2511.14659) | 2025.11 | - | ✓ | ✓ | NORA-1.5 | AR / Flow | D | DPO | MB | [🔗](https://github.com/declare-lab/nora-1.5) |
| [GigaBrain-0.5M\*](https://arxiv.org/abs/2602.12099) | 2026.2 | - | ✗ | ✓ | GigaBrain-0.5 | Flow | D | RAMP | MB | [🔗](https://github.com/open-gigaai/giga-brain-0) |
| [ARM](https://arxiv.org/abs/2604.03037) | 2026.4 | - | ✗ | ✓ | GR00T N1.5 | Flow | D | AW-BC | MF | - |

#### Online RL-VLA

Online RL-VLA enables interactive policy learning through continuous environment interaction, empowering pre-trained VLAs with adaptive closed-loop control capability for real-world OOD environments.

**Key Research Directions:**
- **Policy Optimization:** Direct policy improvement based on environmental rewards
- **Sample Efficiency:** Learning effective policies with limited interaction budget
- **Active Exploration:** Efficient exploration strategies for higher performance gains
- **Training Stability:** Ensuring consistent policy updates and convergence
- **Infrastructure:** Scalable frameworks for online RL-VLA training

| Method | Date | Publication | Sim. | Real | Base VLA Model | Action | Reward | Algorithm | Type | Project |
|:---|:---|:---|:---:|:---:|:---|:---|:---:|:---|:---:|:---|
| [DPPO](https://arxiv.org/abs/2409.00588) | 2024.09 | [RSS25](https://roboticsconference.org/) | ✓ (ST) | ✓ (ST) | Diffusion Policy | Diffusion | D | PPO (denoising MDP) | MF | [🔗](https://github.com/irom-princeton/dppo) |
| [FLaRe](https://arxiv.org/abs/2409.16578) | 2024.09 | [ICRA25](https://2025.ieee-icra.org/) | ✓ (ST) | ✓ (ST) | SPOC | AR | S | PPO | MF | [🔗](https://github.com/JiahengHu/FLaRe) |
| [HIL-SERL](https://arxiv.org/abs/2410.21845) | 2024.10 | [Science Robotics 25](https://www.science.org/journal/scirobotics) | ✗ | ✓ (ST) | ResNet-based actor | AR | S | RLPD + human interventions | MF | [🔗](https://github.com/rail-berkeley/hil-serl) |
| [PA-RL](https://arxiv.org/abs/2412.06685) | 2024.12 | [ICLR25 Workshop](https://openreview.net/) | ✓ (ST) | ✓ (ST) | OpenVLA | AR | S | PA-RL | MF | [🔗](https://github.com/MaxSobolMark/PolicyAgnosticRL) |
| [RLDG](https://arxiv.org/abs/2412.09858) | 2024.12 | [RSS25](https://roboticsconference.org/) | ✗ | ✓ (ST) | OpenVLA / Octo | AR / Diffusion | S | RLPD | MF | [🔗](https://generalist-distillation.github.io/) |
| [iRe-VLA](https://arxiv.org/abs/2501.16664) | 2025.01 | [ICRA25](https://2025.ieee-icra.org/) | ✓ (MT) | ✓ (MT) | iRe-VLA | AR | S | SACfD + SFT | MF | - |
| [GRAPE](https://arxiv.org/abs/2411.19309) | 2025.02 | [ICRA25 Poster](https://2025.ieee-icra.org/) | ✓ (MT) | ✓ (MT) | OpenVLA | AR | D | TPO | MF | [🔗](https://github.com/aiming-lab/GRAPE) |
| [SafeVLA](https://arxiv.org/abs/2503.03480) | 2025.03 | [NeurIPS25 Poster](https://neurips.cc/) | ✓ (ST) | ✗ | SPOC | AR | S | PPO | MF | [🔗](https://github.com/PKU-Alignment/SafeVLA) |
| [RIPT-VLA](https://arxiv.org/abs/2505.17016) | 2025.05 | - | ✓ (MT) | ✗ | QueST / OpenVLA-OFT | AR | S | LOOP | MF | [🔗](https://github.com/Ariostgx/ript-vla) |
| [VLA-RL](https://arxiv.org/abs/2505.18719) | 2025.05 | - | ✓ (MT) | ✗ | OpenVLA | AR | D | PPO | MF | [🔗](https://github.com/GuanxingLu/vlarl) |
| [RLVLA](https://arxiv.org/abs/2505.19789) | 2025.05 | [NeurIPS25 Poster](https://neurips.cc/) | ✓ (MT) | ✗ | OpenVLA | AR | S | PPO / GRPO / DPO | MF | [🔗](https://github.com/gen-robot/RL4VLA) |
| [RFTF](https://arxiv.org/abs/2505.19767) | 2025.05 | - | ✓ (MT) | ✗ | GR-MG, Seer | AR | D | PPO | MF | - |
| [TGRPO](https://arxiv.org/abs/2506.08440) | 2025.06 | - | ✓ (ST) | ✗ | OpenVLA | AR | D | GRPO | MF | - |
| [RLRC](https://arxiv.org/abs/2506.17639) | 2025.06 | - | ✓ (MT) | ✗ | OpenVLA | AR | S | PPO | MF | - |
| [ThinkAct](https://arxiv.org/abs/2507.16815) | 2025.07 | [NeurIPS25 Poster](https://neurips.cc/) | ✓ (MT) | ✗ | MLLM + DiT | AR / Diffusion | D | GRPO (System 2) | MF | - |
| [SimpleVLA-RL](https://arxiv.org/abs/2509.09674) | 2025.09 | [ICLR26 Poster](https://iclr.cc/) | ✓ (MT) | ✓ (ST) | OpenVLA-OFT | AR | S | GRPO | MF | [🔗](https://github.com/PRIME-RL/SimpleVLA-RL) |
| [Dual-Actor FT](https://arxiv.org/abs/2509.13774) | 2025.09 | IROS25 Workshop | ✓ (MT) | ✓ (MT) | Octo / SmolVLA | Diffusion | S | QL + BC | MF | - |
| [Generalist](https://arxiv.org/abs/2509.15155) | 2025.09 | [NeurIPS25 Poster](https://neurips.cc/) | ✓ (MT) | ✓ (MT) | PaLI 3B | AR | D | REINFORCE | MF | - |
| [VLAC](https://arxiv.org/abs/2509.15937) | 2025.09 | - | ✗ | ✓ (MT) | VLAC | AR | D | PPO | MF | [🔗](https://github.com/InternRobotics/VLAC) |
| [AC PPO](https://arxiv.org/abs/2509.25718) | 2025.09 | - | ✓ (ST) | ✗ | Octo-small | AR | S | PPO+BC | MF | - |
| [VLA-RFT](https://arxiv.org/abs/2510.00406) | 2025.10 | - | ✓ (MT) | ✗ | VLA-Adapter | Flow | D | GRPO | MB | [🔗](https://github.com/OpenHelix-Team/VLA-RFT) |
| [RLinf-VLA](https://arxiv.org/abs/2510.06710) | 2025.10 | - | ✓ (MT) | ✓ (MT) | OpenVLA / OpenVLA-OFT | AR | S | PPO / GRPO | MF | [🔗](https://github.com/RLinf/RLinf) |
| [FPO](https://arxiv.org/abs/2510.09976) | 2025.10 | - | ✓ (MT) | ✗ | π₀ | Flow | S | FPO | MF | - |
| [ReSA](https://arxiv.org/abs/2510.12710) | 2025.10 | - | ✓ (MT) | ✗ | OpenVLA | AR | D | PPO + SFT | MF | - |
| [π\_RL](https://arxiv.org/abs/2510.25889) | 2025.10 | - | ✓ (MT) | ✗ | π₀ / π₀.₅ | Flow | S | PPO / GRPO | MF | [🔗](https://github.com/RLinf/RLinf) |
| [PLD](https://arxiv.org/abs/2511.00091) | 2025.10 | [ICLR26 Poster](https://iclr.cc/) | ✓ (MT) | ✓ (MT) | OpenVLA / π₀ / Octo | AR / Flow | S | Cal-QL + SAC | MF | - |
| [DeepThinkVLA](https://arxiv.org/abs/2511.15669) | 2025.10 | - | ✓ (MT) | ✗ | π₀-Fast | AR | S | GRPO | MF | [🔗](https://github.com/OpenBMB/DeepThinkVLA) |
| [World-Env](https://arxiv.org/abs/2509.24948) | 2025.11 | - | ✓ (ST) | ✓ (ST) | OpenVLA-OFT | AR | D | PPO | MB | [🔗](https://github.com/amap-cvlab/world-env) |
| [RobustVLA](https://arxiv.org/abs/2511.01331) | 2025.11 | - | ✓ (MT) | ✗ | OpenVLA-OFT | AR | D | PPO | MF | - |
| [WMPO](https://arxiv.org/abs/2511.09515) | 2025.11 | [ICLR26 Poster](https://iclr.cc/) | ✓ (MT) | ✓ (MT) | OpenVLA-OFT | AR | S | GRPO | MB | [🔗](https://github.com/WM-PO/WMPO) |
| [ProphRL](https://arxiv.org/abs/2511.20633) | 2025.11 | - | ✓ (ST) | ✓ (ST) | VLA-Adapter / π0.5 / OpenVLA-OFT | Flow | S | FA-GRPO | MB | [🔗](https://github.com/LogosRoboticsGroup/ProphRL) |
| [Robo-Dopamine](https://arxiv.org/abs/2512.23703) | 2025.12 | [CVPR26](https://cvpr.thecvf.com/) | ✓ (MT) | ✓ (MT) | Pi0.5 | Flow | D | PPO | MF | [🔗](https://github.com/FlagOpen/Robo-Dopamine) |
| [EVOLVE-VLA](https://arxiv.org/abs/2512.14666) | 2025.12 | - | ✓ (MT) | ✗ | OpenVLA-OFT | AR | D | GRPO | MB(VLAC) | [🔗](https://github.com/showlab/EVOLVE-VLA) |
| [SOP](https://arxiv.org/abs/2601.03044) | 2026.1 | - | ✗ | ✓ (MT) | π0.5 | Flow | S | HG-DAgger / RECAP | MF | - |
| [Green-VLA](https://arxiv.org/abs/2602.00919) | 2026.1 | - | ✓ (MT) | ✓ (MT) | Green-VLA | Flow | S | IQL + actor-critic | MF | [🔗](https://github.com/greenvla/GreenVLA) |
| [SA-VLA](https://arxiv.org/abs/2602.00743) | 2026.1 | - | ✓ (MT) | ✗ | π0.5 | Flow | D | PPO | MF | - |
| [World-Gymnast](https://arxiv.org/abs/2602.02454) | 2026.2 | [ICLR26 Workshop](https://iclr.cc/) | ✓ (MT) | ✓ (MT) | OpenVLA-OFT | AR | S | GRPO | MB | [🔗](https://github.com/world-gymnast/world-gymnast) |
| [RL-VLA3](https://arxiv.org/abs/2602.05765) | 2026.2 | [ICLR26 Workshop](https://iclr.cc/) | ✓ (MT) | ✗ | π0 / π0.5 / GR00T N1.5 / OpenVLA-OFT | Flow / AR | S | - | MF | — |
| [World-VLA-Loop](https://arxiv.org/abs/2602.06508) | 2026.2 | - | ✓ (ST) | ✓ (ST) | OpenVLA-OFT | AR | S | GRPO | MB | [🔗](https://github.com/showlab/World-VLA-Loop) |
| [RISE](https://arxiv.org/abs/2602.11075) | 2026.2 | - | ✗ | ✓ (ST) | π0.5 | Flow | D | RISE | MB | - |
| [WoVR](https://arxiv.org/abs/2602.13977) | 2026.2 | - | ✓ (MT) | ✓ (MT) | OpenVLA-OFT | AR | S | GRPO | MB | [🔗](https://github.com/RLinf/RLinf) |
| [ALOE](https://arxiv.org/abs/2602.12691) | 2026.2 | - | ✗ | ✓ (ST) | π₀.₅ | Flow | S | AWR | MF | - |
| [TwinRL-VLA](https://arxiv.org/abs/2602.09023) | 2026.2 | - | ✗ | ✓ (ST) | Octo | Diffusion | S | Actor-Critic | MF | — |
| [RL-Co](https://arxiv.org/abs/2602.12628) | 2026.3 | - | ✓ (ST) | ✓ (ST) | OpenVLA / π0.5 | AR / Flow | D | ReinFlow / GRPO | MF | — |
| [π\_StepNFT](https://arxiv.org/abs/2603.02083) | 2026.3 | - | ✓ (MT) | ✗ | π₀ / π₀.₅ | Flow | S | NFT | MF | [🔗](https://github.com/wangst0181/pi-StepNFT) |
| [ROBOMETER](https://arxiv.org/abs/2603.02115) | 2026.3 | - | ✗ | ✓ (MT) | π₀ | Flow | D | DSRL | MF | [🔗](https://github.com/robometer/robometer) |
| [AtomVLA](https://arxiv.org/abs/2603.08519) | 2026.3 | - | ✓ (MT) | ✓ (ST) | AtomVLA | Flow | D | GRPO | MB | — |
| [NS-VLA](https://arxiv.org/abs/2603.09542) | 2026.3 | - | ✓ (MT) | ✗ | NS-VLA | AR | D | GRPO | MF | [🔗](https://github.com/Zuzuzzy/NS-VLA) |

#### Offline + Online RL-VLA

| Method | Date | Publication | Sim. | Real | Base VLA Model | Action | Reward | Algorithm | Type | Project |
|:---|:---|:---|:---:|:---:|:---|:---|:---:|:---|:---:|:---|
| [ConRFT](https://arxiv.org/abs/2502.05450) | 2025.4 | [RSS26](https://roboticsconference.org/) | ✗ | ✓ | Octo-small | Diffusion | S | Cal-QL + BC (on [HIL-SERL](https://arxiv.org/abs/2410.21845) framework + consistency policy) | MF | [🔗](https://github.com/cccedric/conrft) |
| [DiffusionRL-VLA](https://arxiv.org/abs/2509.19752) | 2025.9 | - | ✓ | ✗ | π₀ | Flow | S | PPO(DP) + BC(VLA) | MF | - |
| [SRPO](https://arxiv.org/abs/2511.15605) | 2025.11 | - | ✓ | ✓ | OpenVLA\* / π₀ / π₀-Fast | AR / Flow | D | SRPO | MF | [🔗](https://github.com/SUSTechBruce/SRPO_MLLMs) |
| [DLR](https://arxiv.org/abs/2503.05833) | 2025.11 | - | ✓ | ✗ | π₀ / OpenVLA | Flow / AR | S | PPO(MLP) + SFT(VLA) | MF | [🔗](https://github.com/Refined-Policy-Distillation/RPD) |
| [GR-RL](https://arxiv.org/abs/2512.01801) | 2025.12 | - | ✗ | ✓ | GR-3 | Flow | S | TD3 / DSRL | MF | - |
| [STARE-VLA](https://arxiv.org/abs/2512.05107) | 2025.12 | - | ✓ | ✗ | OpenVLA / π₀.₅ | AR / Flow | D | PPO / TPO / SFT | MF | [🔗](https://github.com/starVLA/starVLA) |

#### Test-time RL-VLA

Test-time RL-VLA adapts behavior during deployment through lightweight updates, addressing the expensive cost of full model fine-tuning in real-world scenarios.

**Key Adaptation Mechanisms:**
- **Value Guidance:** Using pre-trained value functions to influence action selection
- **Memory Buffer Guidance:** Retrieving relevant historical experiences during inference
- **Planning-guided Adaptation:** Explicit reasoning over future action sequences

| Method | Date | Publication | Base VLA Model | Mechanism | Project |
|:---|:---|:---|:---|:---|:---|
| [Steering Your Generalists (V-GPS)](https://arxiv.org/abs/2410.13816) | 2024.10 | - | Octo / OpenVLA | Value Guidance | [🔗](https://github.com/nakamotoo/V-GPS) |
| [GVL (In-Context Value Learners)](https://arxiv.org/abs/2411.04549) | 2024.11 | - | VLM | Value Guidance | - |
| [STRAP](https://arxiv.org/abs/2412.15182) | 2024.12 | [ICLR25](https://iclr.cc/) | Any | Memory Buffer Guidance | [🔗](https://github.com/WEIRDLabUW/STRAP) |
| [MAP-VLA](https://arxiv.org/abs/2511.09516) | 2025.11 | - | VLA | Memory Buffer Guidance | - |
| [VLA-Reasoner](https://arxiv.org/abs/2509.22643) | 2025.09 | - | VLA | Planning-guided Adaptation | - |

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
