
<h1 align="center">🔥 Awesome-Epistemic-Exploration

"Epistemic Exploration Toward Artificial General Intelligence"  (ArXiv 2026) </h2>




<p align="center">
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
  </a>
  <a href=""><img src="https://img.shields.io/github/last-commit/banyikun/epistemic_exploration?color=lightgrey"></a>
</p>

<p align="center">
  <a href="https://github.com/banyikun/epistemic_exploration/stargazers"><img src="https://img.shields.io/github/stars/banyikun/epistemic_exploration?style=social" alt="GitHub stars"></a>
  <a href="https://github.com/banyikun/epistemic_exploration/network/members"><img src="https://img.shields.io/github/forks/banyikun/epistemic_exploration?style=social" alt="GitHub forks"></a>
</p>

<h4 align="center">If you find our survey helpful, please give it a star ⭐ to show your support！Thank you:)

</h4>




---

## 📣 Notices

> 🔥 This is a curated paper list for the survey **"Epistemic Exploration Toward Artificial General Intelligence"**, covering exploration mechanisms across reasoning, embodied AI, world models, and multi-agent systems.

> 🔥 **Stay tuned for our full paper release, incorporating the latest developments.**

> **[Always] [Add your papers]** We welcome all related papers! If you find any missed or new work, please open a Pull Request or contact us.

> **[Always] [Maintain]** We will keep this list updated frequently!

---


<br>



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

<br>

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

<br>

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

| Paradigm | Method | Key Idea |
|:---------|:-------|:---------|
| **Uncertainty-Driven (Active Perception)** | ActiveSplat | Gaussian splatting for information-maximizing viewpoint selection |
| | Conan | Active reasoning in open-world environments |
| | ActiveRIR | Cross-modal audio-visual exploration |
| | Fisher-info path planning | Balances information gain with localization robustness |
| **Competence-Driven** | **Offline RL-VLA**: Q-Transformer, Cal-QL | Scale value learning to static trajectories |
| | **Online RL-VLA**: VLA-RL, FLaRe, SimpleVLA-RL | Real-time interactive policy exploration |
| | **Hybrid**: ConRFT, SRPO, Dual-Actor | Stable offline-to-online transitions |
| | **Test-Time**: VLA-Reasoner (MCTS), DeepThinkVLA, Hume | Imagination before physical execution |
| | SayCan, Inner Monologue, LM-Nav | Language-guided objective-driven navigation |
| **Reachability-Driven** | Eureka | LLM-driven reward code synthesis |
| | Recovery RL, RECOVER, SafeVLA | Learned safety zones preserving reachable sets |
| | RND, CurricuLLM | Curiosity-driven and curriculum-based coverage |

---

<br>

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

<br>

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






### 5.2 Agentic Ensemble Papers




#### 5.2.1 Ensemble-During-Inference Papers



Methods that explore how to combine or choose token candidates from multiple LLMs at each decoding step, either by merging next-token distributions or by selecting the token from one model directly:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------:|:---------|:------|:---:|
| 2025-10 | **SAFE** | Only ensembles at a few well-chosen token steps to keep decoding stable and fast | [When to Ensemble: Identifying Token-Level Points for Stable and Fast LLM Ensembling](https://arxiv.org/abs/2510.15346) | - |
| 2025-10 | **CoRe** | Uses token and model agreement to downweight unreliable signals | [Harnessing Consistency for Robust Test-Time LLM Ensemble](https://arxiv.org/abs/2510.13855) | - |
| 2025-05 | **Transformer Copilot** | A Copilot learns from past token mistakes and fixes the Pilot’s logits | [Transformer Copilot: Learning from The Mistake Log in LLM Fine-tuning](https://arxiv.org/abs/2505.16270) | [![GitHub Stars](https://img.shields.io/github/stars/jiaruzouu/TransformerCopilot?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/jiaruzouu/TransformerCopilot) |
| 2025-02 | **ABE** | Makes different-vocabulary models agree on the same surface token before choosing it | [Token-level Ensembling of Models with Different Vocabularies](https://arxiv.org/abs/2502.21265) | [![GitHub Stars](https://img.shields.io/github/stars/mjpost/abe?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/mjpost/abe) |
| 2025-02 | **CITER** | Sends easy tokens to a small model and hard ones to a large model | [CITER: Collaborative Inference for Efficient Large Language Model Decoding with Token-Level Routing](https://arxiv.org/abs/2502.01976) | [![GitHub Stars](https://img.shields.io/github/stars/aiming-lab/CITER?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/aiming-lab/CITER) |
| 2024-10 | **UniTe** | Ensembles only the union of top-*k* tokens instead of the full vocabulary | [Determine-Then-Ensemble: Necessity of Top-k Union for Large Language Model Ensembling](https://arxiv.org/abs/2410.03777) | - |
| 2024-06 | **GaC** | Treats next-token generation like classification and averages token probabilities | [Breaking the Ceiling of the LLM Community by Treating Token Generation as a Classification for Ensembling](https://arxiv.org/abs/2406.12585) | [![GitHub Stars](https://img.shields.io/github/stars/yaoching0/GaC?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/yaoching0/GaC) |
| 2024-04 | **DeePEn** | Maps different vocabularies into a shared space before merging token distributions | [Ensemble Learning for Heterogeneous Large Language Models with Deep Parallel Collaboration](https://arxiv.org/abs/2404.12715) | [![GitHub Stars](https://img.shields.io/github/stars/OrangeInSouth/DeePEn?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/OrangeInSouth/DeePEn) |
| 2024-04 | **PackLLM** | Gives more weight to models that fit the prompt better | [Pack of LLMs: Model Fusion at Test-Time via Perplexity Optimization](https://arxiv.org/abs/2404.11531) | [![GitHub Stars](https://img.shields.io/github/stars/cmavro/PackLLM?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/cmavro/PackLLM) |
| 2024-04 | **EVA** | Learns vocabulary mappings so different models can ensemble token by token | [Bridging the Gap between Different Vocabularies for LLM Ensemble](https://arxiv.org/abs/2404.09492) | [![GitHub Stars](https://img.shields.io/github/stars/xydaytoy/EVA?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/xydaytoy/EVA) |
| 2024-02 | **-** | Uses a benign small model to pull token probabilities away from harmful outputs | [Purifying large language models by ensembling a small language model](https://arxiv.org/abs/2402.14845) | - |




Methods that explore how to generate, assess, and select short text spans from multiple LLMs during decoding, so that the best segment can be fed back for the next step:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------:|:---------|:------|:---:|
| 2025-06 | **RLAE** | Adjusts model weights on the fly as generation goes on | [RLAE: Reinforcement Learning-Assisted Ensemble for LLMs](https://arxiv.org/abs/2506.00439) | - |
| 2024-12 | **SpecFuse** | Lets models draft short spans, then picks the best one for the next step | [SpecFuse: Ensembling Large Language Models via Next-Segment Prediction](https://arxiv.org/abs/2412.07380) | - |
| 2025-02 | **Speculative Ensemble** | Lets one model draft a span and others verify it for faster decoding | [Speculative Ensemble: Fast Large Language Model Ensemble via Speculation](https://arxiv.org/abs/2502.01662) | [![GitHub Stars](https://img.shields.io/github/stars/Kamichanw/Speculative-Ensemble?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/Kamichanw/Speculative-Ensemble/) |
| 2024-09 | **SweetSpan** | Lets each model write a short span, then uses mutual scoring to choose one | [Hit the Sweet Spot! Span-Level Ensemble for Large Language Models](https://arxiv.org/abs/2409.18583) | - |
| 2024-07 | **Cool-Fusion** | Waits for a shared word boundary, then selects the best whole span | [Cool-Fusion: Fuse Large Language Models without Training](https://arxiv.org/abs/2407.19807) | - |




Methods that explore multiple reasoning steps across LLMs during multi-step problem solving, and choose the most promising next step or reasoning path along the way:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------:|:---------|:------|:---:|
| 2025-11 | **CBS** | Explores many next reasoning steps, then keeps the ones backed by collective consensus | [Collaborative Beam Search: Enhancing LLM Reasoning via Collective Consensus](https://aclanthology.org/2025.emnlp-main.574/) | - |
| 2024-12 | **LE-MCTS** | Searches over next reasoning steps and keeps the path with the best process reward | [Ensembling Large Language Models with Process Reward-Guided Tree Search for Better Complex Reasoning](https://arxiv.org/abs/2412.15797) | - |

#### 5.2.2  Ensemble-After-Inference Papers


Methods that explore how to compare multiple complete responses after generation, either by selecting the single best answer or by choosing a strong subset for regeneration:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------:|:---------|:------|:---:|
| 2025-12 | **LLM-PeerReview** | Lets LLM judges score candidate answers and picks the best-reviewed one | [Scoring, Reasoning, and Selecting the Best! Ensembling Large Language Models via a Peer-Review Process](https://arxiv.org/abs/2512.23213) | [![GitHub Stars](https://img.shields.io/github/stars/zeyuji/LLM-PeerReview?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/zeyuji/LLM-PeerReview) |
| 2025-10 | **LLMartini** | Aligns answer parts so users can compare and compose a final response | [LLMartini: Seamless and Interactive Leveraging of Multiple LLMs through Comparison and Composition](https://arxiv.org/abs/2510.19252) | - |
| 2025-10 | **Beyond Consensus** | Uses minority veto to stop overly agreeable judges from accepting bad answers | [Beyond Consensus: Mitigating the Agreeableness Bias in LLM Judge Evaluations](https://arxiv.org/abs/2510.11822) | [![GitHub Stars](https://img.shields.io/github/stars/ai-cet/paper-arxiv-llm-judge-calibration?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ai-cet/paper-arxiv-llm-judge-calibration) |
| 2025-10 | **OW/ISP** | Uses who agrees with whom, not just vote counts | [Beyond Majority Voting: LLM Aggregation by Leveraging Higher-Order Information](https://www.arxiv.org/abs/2510.01499) | - |
| 2025-09 | **FLAME** | Aggregates line-level annotations from several LLMs to rank bug locations | [Explainable Fault Localization for Programming Assignments via LLM-Guided Annotation](https://arxiv.org/pdf/2509.25676v1) | [![GitHub Stars](https://img.shields.io/github/stars/FLAME-FL/FLAME?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/FLAME-FL/FLAME) |
| 2025-09 | **CARGO** | Uses confidence-aware scoring to decide which model to trust more | [CARGO: A Framework for Confidence-Aware Routing of Large Language Models](https://arxiv.org/abs/2509.14899) | - |
| 2025-07 | **LENS** | Learns how much to trust each answer from internal states | [LENS: Learning Ensemble Confidence from Neural States for Multi-LLM Answer Integration](https://arxiv.org/abs/2507.23167) | - |
| 2025-05 | **EL4NER** | Merges small-LLM NER outputs and self-checks the final spans | [EL4NER: Ensemble Learning for Named Entity Recognition via Multiple Small-Parameter Large Language Models](https://arxiv.org/abs/2505.23038) | - |
| 2025-03 | **Symbolic-MoE** | Selects skill-matched experts and then combines their finished reasonings | [Symbolic Mixture-of-Experts: Adaptive Skill-based Routing for Heterogeneous Reasoning](https://arxiv.org/abs/2503.05641) | [![GitHub Stars](https://img.shields.io/github/stars/dinobby/Symbolic-MoE?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/dinobby/Symbolic-MoE/) |
| 2025-01 | **DFPE** | Keeps diverse strong models, filters weak ones, and reweights the rest | [DFPE: A Diverse Fingerprint Ensemble for Enhancing LLM Performance](https://arxiv.org/abs/2501.17479) | [![GitHub Stars](https://img.shields.io/github/stars/nivgold/DFPE?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/nivgold/DFPE) |
| 2025-01 | **DMoA** | Balances diversity and consistency before mixing answers | [Balancing Act: Diversity and Consistency in Large Language Model Ensembles](https://openreview.net/pdf?id=Dl6nkKKvlX) | - |
| 2024-12 | **Smoothie** | Picks the answer most supported by the others, without labels | [Smoothie: Label Free Language Model Routing](https://arxiv.org/abs/2412.04692) | [![GitHub Stars](https://img.shields.io/github/stars/HazyResearch/smoothie?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/HazyResearch/smoothie) |
| 2024-10 | **LLM-Forest** | Uses weighted voting across graph-guided prompt variants | [LLM-Forest: Ensemble Learning of LLMs with Graph-Augmented Prompts for Data Imputation](https://arxiv.org/abs/2410.21520) | [![GitHub Stars](https://img.shields.io/github/stars/Xinrui17/LLM-Forest?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/Xinrui17/LLM-Forest) |
| 2024-10 | **LLM-TOPLA** | Selects a diverse top-*k* set before regeneration | [LLM-TOPLA: Efficient LLM Ensemble by Maximising Diversity](https://arxiv.org/abs/2410.03953) | [![GitHub Stars](https://img.shields.io/github/stars/git-disl/llm-topla?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/git-disl/llm-topla) |
| 2024-10 | **MLKF** | Fuses complementary reasoning from multiple LLMs into one answer | [Two Heads are Better than One: Zero-shot Cognitive Reasoning via Multi-LLM Knowledge Fusion](https://dl.acm.org/doi/abs/10.1145/3627673.3679744) | [![GitHub Stars](https://img.shields.io/github/stars/trueBatty/MLKF?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/trueBatty/MLKF) |
| 2024-08 | **URG** | Learns ranking and regeneration together | [URG: A Unified Ranking and Generation Method for Ensembling Language Models](https://aclanthology.org/2024.findings-acl.261/) | - |
| 2024-02 | **Agent-Forest** | Samples many answers and keeps the one most supported by voting | [More Agents Is All You Need](https://arxiv.org/abs/2402.05120) | [![GitHub Stars](https://img.shields.io/github/stars/MoreAgentsIsAllYouNeed/AgentForest?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/MoreAgentsIsAllYouNeed/AgentForest) |
| 2023-06 | **LLM-Blender** | Ranks answers first, then fuses the best few into one | [LLM-Blender: Ensembling Large Language Models with Pairwise Ranking and Generative Fusion](https://arxiv.org/abs/2306.02561) | [![GitHub Stars](https://img.shields.io/github/stars/yuchenlin/LLM-Blender?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/yuchenlin/LLM-Blender) |
| 2023-05 | **MoRE** | Uses agreement among reasoning experts to choose an answer or abstain | [Getting MoRE out of Mixture of Language Model Reasoning Experts](https://arxiv.org/abs/2305.14628) | [![GitHub Stars](https://img.shields.io/github/stars/NoviScl/MoRE?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/NoviScl/MoRE) |





#### 5.2.3 Ensemble-Before-Inference Papers


Methods that route each query by predicting discrete model utility—such as whether a model is likely to be good enough, or which model is better than another under the query:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------:|:---------|:------|:---:|
| 2025-10 | **DiSRouter** | Lets models help decide which peer should answer | [DISROUTER: Distributed Self-Routing for LLM Selections](https://arxiv.org/abs/2510.19208) | - |
| 2025-06 | **TagRouter** | Matches queries to model tags instead of training a heavy router | [TAGROUTER: Learning Route to LLMs through Tags for Open-Domain Text Generation Tasks](https://arxiv.org/abs/2506.12473) | - |
| 2025-06 | **Router-R1** | Learns multi-round routing to choose and combine models better | [Router-R1: Teaching LLMs Multi-Round Routing and Aggregation via Reinforcement Learning](https://arxiv.org/abs/2506.09033) | [![GitHub Stars](https://img.shields.io/github/stars/ulab-uiuc/Router-R1?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ulab-uiuc/Router-R1) |
| 2025-06 | **RadialRouter** | Builds a structured query view for more robust routing | [RadialRouter: Structured Representation for Efficient and Robust Large Language Models Routing](https://www.arxiv.org/abs/2506.03880) | - |
| 2025-05 | **RTR** | Chooses both the model and the reasoning style | [Route to Reason: Adaptive Routing for LLM and Reasoning Strategy Selection](https://arxiv.org/abs/2505.19435) | [![GitHub Stars](https://img.shields.io/github/stars/goodmanpzh/Route-To-Reason?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/goodmanpzh/Route-To-Reason) |
| 2024-12 | **Bench-CoE** | Routes queries using benchmark-based model strengths | [Bench-CoE: a Framework for Collaboration of Experts from Benchmark](https://arxiv.org/abs/2412.04167) | [![GitHub Stars](https://img.shields.io/github/stars/ZhangXJ199/Bench-CoE?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ZhangXJ199/Bench-CoE) |
| 2024-10 | **GraphRouter** | Uses graph structure to choose the best model | [GraphRouter: A Graph-based Router for LLM Selections](https://arxiv.org/abs/2410.03834) | [![GitHub Stars](https://img.shields.io/github/stars/ulab-uiuc/GraphRouter?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ulab-uiuc/GraphRouter) |
| 2024-09 | **Eagle** | Compares candidate models without extra router training | [Eagle: Efficient Training-Free Router for Multi-LLM Inference](https://arxiv.org/abs/2409.15518) | - |
| 2024-08 | **SelectLLM** | Scores each query and picks an efficient model | [SelectLLM: Query-Aware Efficient Selection Algorithm for Large Language Models](https://arxiv.org/abs/2408.08545) | - |
| 2024-06 | **RouteLLM** | Learns when a cheaper model can replace a stronger one | [RouteLLM: Learning to Route LLMs with Preference Data](https://arxiv.org/abs/2406.18665) | [![GitHub Stars](https://img.shields.io/github/stars/lm-sys/RouteLLM?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/lm-sys/RouteLLM) |
| 2024-05 | **LLM Routing Lessons** | Shows which prompt cues help choose the right model | [Harnessing the Power of Multiple Minds: Lessons Learned from LLM Routing](https://arxiv.org/abs/2405.00467) | [![GitHub Stars](https://img.shields.io/github/stars/kvadityasrivatsa/llm-routing?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/kvadityasrivatsa/llm-routing) |
| 2024-04 | **Hybrid-LLM** | Balances answer quality and cost before choosing a model | [Hybrid LLM: Cost-Efficient and Quality-Aware Query Routing](https://arxiv.org/abs/2404.14618) | [![GitHub Stars](https://img.shields.io/github/stars/m365-core/hybrid_llm_routing?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/m365-core/hybrid_llm_routing) |
| 2024-03 | **ETR** | Routes expert tokens to the most suitable specialist model | [An Expert is Worth One Token: Synergizing Multiple Expert LLMs as Generalist via Expert Token Routing](https://arxiv.org/abs/2403.16854) | [![GitHub Stars](https://img.shields.io/github/stars/zjunet/ETR?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/zjunet/ETR) |
| 2024-01 | **Routoo** | Learns to send each query to the model most likely to work | [Routoo: Learning to Route to Large Language Models Effectively](https://arxiv.org/abs/2401.13979) | - |
| 2024 | **RouterDC** | Learns query embeddings that make routing easier | [RouterDC: Query-Based Router by Dual Contrastive Learning for Assembling Large Language Models](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7a641b8ec86162fc875fb9f6456a542f-Abstract-Conference.html) | [![GitHub Stars](https://img.shields.io/github/stars/shuhao02/RouterDC?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/shuhao02/RouterDC) |
| 2023-11 | **ZOOTER** | Uses reward signals to pick the right expert model | [Routing to the Expert: Efficient Reward-guided Ensemble of Large Language Models](https://arxiv.org/abs/2311.08692) | - |
| 2023-08 | **FORC** | Chooses the cheapest model that is still good enough | [Fly-Swat or Cannon? Cost-Effective Language Model Choice via Meta-Modeling](https://arxiv.org/abs/2308.06077) | [![GitHub Stars](https://img.shields.io/github/stars/epfl-dlab/forc?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/epfl-dlab/forc) |
| 2023 | **Benchmark Routing** | Builds routing rules from benchmark-level model performance | [LLM Routing with Benchmark Datasets](https://openreview.net/forum?id=k9EfAJhFZc) | - |



Methods that route each query by predicting continuous model utility—such as performance scores, costs, latency, or combined rewards—so the router can make finer trade-offs:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------:|:---------|:------|:---:|
| 2025-10 | **WebRouter** | Compresses web-agent prompts and routes with cost in mind | [WebRouter: Query-specific Router via Variational Information Bottleneck for Cost-sensitive Web Agent](https://arxiv.org/abs/2510.11221) | - |
| 2025-10 | **LLMRank** | Uses rich query features to rank which model should answer | [LLMRank: Understanding LLM Strengths for Model Routing](https://arxiv.org/abs/2510.01234) | - |
| 2025-05 | **Avengers** | Combines small models by routing queries to their strengths | [The Avengers: A Simple Recipe for Uniting Smaller Language Models to Challenge Proprietary Giants](https://arxiv.org/abs/2505.19797) | [![GitHub Stars](https://img.shields.io/github/stars/ZhangYiqun018/Avengers?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ZhangYiqun018/Avengers) |
| 2025-05 | **InferenceDynamics** | Profiles model skills and knowledge before routing | [InferenceDynamics: Efficient Routing Across LLMs through Structured Capability and Knowledge Profiling](https://arxiv.org/abs/2505.16303) | - |
| 2025-05 | **kNN Router** | Uses nearest past queries instead of a complex learned router | [Rethinking Predictive Modeling for LLM Routing: When Simple kNN Beats Complex Learned Routers](https://arxiv.org/abs/2505.12601) | - |
| 2025 | **RELM** | Learns recommendation and evaluation together for model selection | [Co-optimizing Recommendation and Evaluation for LLM Selection](https://openreview.net/pdf?id=gWi4ZcPQRl) | - |
| 2025-02 | **LLM Bandit** | Explores cheap options first and learns cost-aware routing online | [LLM Bandit: Cost-Efficient LLM Generation via Preference-Conditioned Dynamic Routing](https://arxiv.org/abs/2502.02743) | - |
| 2024-12 | **PickLLM** | Uses RL to pick the best model from context and budget cues | [PickLLM: Context-Aware RL-Assisted Large Language Model Routing](https://arxiv.org/abs/2412.12170) | - |
| 2024-08 | **TO-Router** | Predicts utility under latency and cost constraints | [TensorOpera Router: A Multi-Model Router for Efficient LLM Inference](https://arxiv.org/abs/2408.12320) | - |
| 2024-07 | **MetaLLM** | Wraps several models and picks one using predicted utility | [MetaLLM: A High-performant and Cost-efficient Dynamic Framework for Wrapping LLMs](https://arxiv.org/abs/2407.10834) | [![GitHub Stars](https://img.shields.io/github/stars/mail-research/MetaLLM-wrapper?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/mail-research/MetaLLM-wrapper/) |
| 2024-06 | **HomoRouter** | Routes queries among similar tools with fine-grained scoring | [Query Routing for Homogeneous Tools: An Instantiation in the RAG Scenario](https://arxiv.org/abs/2406.12429) | - |
| 2024-01 | **Blending** | Blends model strengths as a cheaper alternative to one giant model | [Blending Is All You Need: Cheaper, Better Alternative to Trillion-Parameters LLM](https://arxiv.org/abs/2401.02994) | - |

#### 5.2.4 Cascaded-Based Papers




Methods that explore an ordered chain of models—typically from cheaper/weaker ones to more capable/costlier ones—to decide whether a query can stop early, should defer upward, or should switch routes to obtain a better answer under a desired cost-performance trade-off:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------:|:---------|:------|:---:|
| 2025-12 | **RoBoN** | Routes best-of-n samples across multiple LLMs, exploring which model adds the highest next-response gain via reward and agreement signals | [RoBoN: Routed Online Best-of-n for Test-Time Scaling with Multiple LLMs](https://arxiv.org/abs/2512.05542) | [![GitHub Stars](https://img.shields.io/github/stars/j-geuter/RoBoN?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/j-geuter/RoBoN) |
| 2025-09 | **Semantic Agreement** | Uses meaning-level agreement between model outputs to explore whether a query can stop at a smaller model or should defer upward | [Semantic Agreement Enables Efficient Open-Ended LLM Cascades](https://arxiv.org/abs/2509.21837) | - |
| 2025-04 | **EMAFusion** | Combines taxonomy routing, learned routing, and confidence-triggered escalation to explore the cheapest reliable model path for each query | [EMAFusion: A Self-Optimizing System for Seamless LLM Selection and Integration](https://arxiv.org/abs/2504.10681) | - |
| 2025-04 | **ModelSwitch** | Uses sample consistency to explore when repeated sampling should stay with the current model or switch to a complementary one | [Do We Truly Need So Many Samples? Multi-LLM Repeated Sampling Efficiently Scales Test-Time Compute](https://arxiv.org/abs/2504.00762) | [![GitHub Stars](https://img.shields.io/github/stars/JianhaoChen-nju/ModelSwitch?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/JianhaoChen-nju/ModelSwitch) |
| 2024-12 | **DER** | Treats expert selection as sequential route exploration, choosing the next LLM to add complementary knowledge with minimal compute | [Dynamic Ensemble Reasoning for LLM Experts](https://arxiv.org/abs/2412.07448) | - |
| 2024-10 | **Cascade Routing** | Unifies routing and cascading to explore the model chain only when quality estimates suggest extra capacity will pay off | [A Unified Approach to Routing and Cascading for LLMs](https://arxiv.org/abs/2410.10347) | [![GitHub Stars](https://img.shields.io/github/stars/eth-sri/cascade-routing?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/eth-sri/cascade-routing) |
| 2024-04 | **LM Cascades** | Uses token-level uncertainty to explore whether a generative response is reliable enough to stop or should be deferred to a larger model | [Language Model Cascades: Token-level Uncertainty and Beyond](https://arxiv.org/abs/2404.10136) | - |
| 2023-10 | **AutoMix** | Uses self-verification and POMDP routing to explore whether a weaker model is sufficient or a larger model is needed | [AutoMix: Automatically Mixing Language Models](https://arxiv.org/abs/2310.12963) | [![GitHub Stars](https://img.shields.io/github/stars/automix-llm/automix?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/automix-llm/automix) |
| 2023-10 | **Neural Caching** | Uses active selection to explore which queries a continuously distilled student can absorb and which should still go to the teacher | [Cache & Distil: Optimising API Calls to Large Language Models](https://arxiv.org/abs/2310.13561) | [![GitHub Stars](https://img.shields.io/github/stars/guillemram97/neural-caching?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/guillemram97/neural-caching) |
| 2023-10 | **MoT Cascade** | Uses weak-model answer consistency, enriched with CoT/PoT thought mixtures, to explore whether escalation is necessary | [Large Language Model Cascades with Mixture of Thoughts Representations for Cost-efficient Reasoning](https://arxiv.org/abs/2310.03094) | [![GitHub Stars](https://img.shields.io/github/stars/MurongYue/LLM_MoT_cascade?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/MurongYue/LLM_MoT_cascade) |
| 2023-10 | **EcoAssistant** | Explores a hierarchy of assistants, refining with execution feedback and backing off to stronger models only when needed | [EcoAssistant: Using LLM Assistant More Affordably and Accurately](https://arxiv.org/abs/2310.03046) | [![GitHub Stars](https://img.shields.io/github/stars/JieyuZ2/EcoAssistant?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/JieyuZ2/EcoAssistant) |
| 2023-05 | **FrugalGPT** | Explores budget-aware combinations of LLMs, adaptively choosing a query-specific cascade for cost-efficient accuracy | [FrugalGPT: How to Use Large Language Models While Reducing Cost and Improving Performance](https://arxiv.org/abs/2305.05176) | - |
| 2023-01 | **Confidence Deferral** | Clarifies when confidence-only deferral can explore the cascade effectively and when downstream-aware signals are required | [When Does Confidence-Based Cascade Deferral Suffice?](https://proceedings.neurips.cc/paper_files/paper/2023/hash/1f09e1ee5035a4c3fe38a5681cae5815-Abstract-Conference.html) | - |
| 2022-10 | **Model Cascading** | Explores early exit across models of increasing capacity, reserving large-model compute for harder inputs | [Model Cascading: Towards Jointly Improving Efficiency and Accuracy of NLP Systems](https://arxiv.org/abs/2210.05528) | - |
---

<br>


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

<br>

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
