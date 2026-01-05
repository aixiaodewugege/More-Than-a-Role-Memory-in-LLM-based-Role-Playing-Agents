# True-to-Role, Tailored-to-You: A Survey of Role-Playing LLM Agents

<p align="center">
  <a href="teaser.pdf" target="_blank">
    <img src="teaser.png" alt="Teaser Figure" width="90%" style="border: 1px solid #ddd; border-radius: 4px;">
  </a>
</p>

## Introduction

This is the official repository of the paper **"True-to-Role, Tailored-to-You: A Survey of Role-Playing LLM Agents"**.

> **Abstract:** To truly inhabit a role, skilled actors typically anchor their performance in the core identity of a character while allowing it to evolve through the narrative journey. Mirroring this artistry, LLM-based Role-Playing Agents (RPAs) are expected to combine a prescriptive identity with evolving experience. However, existing works often treat these dimensions in isolation.
> To bridge this gap, we present the first survey examining RPAs through a **Static–Dynamic perspective**:
> * **Static Persona**: A *prescriptive anchor of identity* (who the agent is).
> * **Dynamic Memory**: *Experience evolved through interactions*, decomposed into:
> * **(i) Self Memory**: Supports agent-centric internal experience.
> * **(ii) User Memory**: Drives user-centric external experience.

We maintain this list to track the latest advancements in RPA architectures, memory systems, and evaluations.

## News

* **[2026.01]** 🚀 We released the first version of our survey on arXiv!


## Table of Contents

* [🎭 Static Persona (The Anchor)](#-static-persona-the-anchor)
  * [Construction & Extraction](#construction--extraction)
  * [Alignment & Fidelity](#alignment--fidelity)
* [🧠 Dynamic Memory (The Evolution)](#-dynamic-memory-the-evolution)
  * [🏗️ Structure Design](#-structure-design)
  * [💾 Storage Forms](#-storage-forms)
  * [🔄 Evolution & Reflection](#-evolution--reflection)
  * [🎯 Memory Alignment](#-memory-alignment)
* [🤝 Intersection: Persona-Memory Coordination](#-intersection-persona-memory-coordination)
  * [System Design](#system-design)
  * [Applications](#applications)
* [⚖️ Evaluation](#-evaluation)
* [🌱 Contribution](#-contribution)
* [🔖 Citation](#-citation)

---

<h2 id="-static-persona-the-anchor">🎭 Static Persona (The Anchor)</h2>

Focuses on the prescriptive specification of the agent’s core identity (*e.g.*, background, worldview, style).

<h3 id="construction--extraction">Construction & Extraction</h3>

| Date | Authors | Venue | Paper |
| --- | --- | --- | --- |
| 2025 | Wang et al. | arXiv | [OpenCharacter: Training Customizable Role-Playing LLMs with Large-Scale Synthetic Personas](https://arxiv.org/abs/2501.15427) |
| 2024 | Liu et al. | NeurIPS | [RoleAgent: Building, Interacting, and Benchmarking High-quality Role-Playing Agents from Scripts](https://arxiv.org/abs/2412.05631) |
| 2023 | Shao et al. | EMNLP | [Character-LLM: A Trainable Agent for Role-Playing](https://arxiv.org/abs/2310.17976) |
| 2023 | Li et al. | arXiv | [ChatHaruhi: Reviving Anime Character in Reality via Large Language Model](https://arxiv.org/abs/2308.09597) |

<h3 id="alignment--fidelity">Alignment & Fidelity</h3>

| Date | Authors | Venue | Paper |
| --- | --- | --- | --- |
| 2025 | Ji et al. | ACL | [Enhancing Persona Consistency for LLMs' Role-Playing using Persona-Aware Contrastive Learning](https://aclanthology.org/2025.findings-acl.1344/) |
| 2024 | Wang et al. | ACL | [RoleLLM: Benchmarking, Eliciting, and Enhancing Role-Playing Abilities of Large Language Models](https://arxiv.org/abs/2404.03565) |
| 2024 | Wang et al. | ACL | [InCharacter: Evaluating Personality Fidelity in Role-Playing Agents](https://arxiv.org/abs/2310.17976) |

---

<h2 id="-dynamic-memory-the-evolution">🧠 Dynamic Memory (The Evolution)</h2>

Focuses on experience accumulated in interactions. Divided into **Self Memory** (Internal) and **User Memory** (External).

<p align="center">
<img src="memory.png" alt="Memory Operation Process" width="80%" height="auto">
</p>

<h3 id="-structure-design">🏗️ Structure Design</h3>

Includes **Hierarchical** and **Modular** structures for organizing history.

| Date | Authors | Venue | Paper | Category |
| --- | --- | --- | --- | --- |
| 2025 | Sun et al. | arXiv | [Hierarchical Memory for High-Efficiency Long-Term Reasoning in LLM Agents (H-MEM)](https://arxiv.org/abs/2507.22925) | Hierarchical |
| 2025 | Wang et al. | arXiv | [MIRIX: Multi-Agent Memory System for LLM-Based Agents](https://arxiv.org/abs/2507.07957) | Modular |
| 2025 | Hu et al. | ACL | [HiAgent: Hierarchical Working Memory Management](https://aclanthology.org/2025.acl-long.1575/) | Hierarchical |

<h3 id="-storage-forms">💾 Storage Forms</h3>

Covering **Graph-based** storage and **Indexing-enhanced** methods.

| Date | Authors | Venue | Paper | Form |
| --- | --- | --- | --- | --- |
| 2025 | Chhikara et al. | arXiv | [Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory](https://arxiv.org/abs/2504.19413) | Graph |
| 2025 | Li et al. | arXiv | [MemOS: An Operating System for Memory-Augmented Generation](https://arxiv.org/abs/2505.22101) | Graph+Index |
| 2024 | Wang et al. | EMNLP | [Crafting Personalized Agents through RAG on Editable Memory Graphs (EMG-RAG)](https://arxiv.org/abs/2405.00175) | Graph |
| 2024 | Zhong et al. | AAAI | [MemoryBank: Enhancing Large Language Models with Long-Term Memory](https://arxiv.org/abs/2305.10250) | Indexing |

<h3 id="-evolution--reflection">🔄 Evolution & Reflection</h3>

Mechanisms for **Self Reflection** (correction) and **Long-term Maintenance** (pruning/summarization).

| Date | Authors | Venue | Paper |
| --- | --- | --- | --- |
| 2025 | Ong et al. | NAACL | [THEANINE: Towards Lifelong Dialogue Agents via Timeline-based Memory Management](https://arxiv.org/abs/2504.10147) |
| 2024 | Gutierrez et al. | NeurIPS | [HippoRAG: Neurobiologically Inspired Long-Term Memory](https://arxiv.org/abs/2405.14831) |
| 2024 | Zhao et al. | AAAI | [Expel: LLM Agents Are Experiential Learners](https://arxiv.org/abs/2308.10144) |
| 2023 | Park et al. | UIST | [Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442) |
| 2023 | Packer et al. | arXiv | [MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) |

<h3 id="-memory-alignment">🎯 Memory Alignment</h3>

Aligning memory retrieval with user preferences (User Memory) or agent consistency.

| Date | Authors | Venue | Paper | Method |
| --- | --- | --- | --- | --- |
| 2025 | Tan et al. | arXiv | [Democratizing Large Language Models via Personalized PEFT](https://arxiv.org/abs/2402.04401) | Tuning |
| 2024 | Salemi et al. | ACL | [LaMP: When Large Language Models Meet Personalization](https://arxiv.org/abs/2304.11406) | RAG |
| 2024 | Rafailov et al. | NeurIPS | [Direct Preference Optimization (DPO)](https://arxiv.org/abs/2305.18290) | RL/Alignment |

---

<h2 id="-intersection-persona-memory-coordination">🤝 Intersection: Persona-Memory Coordination</h2>

Works that tightly couple the **Static Persona** (Identity) with **Dynamic Memory** (Experience).

<h3 id="system-design">System Design</h3>

| Date | Authors | Venue | Paper |
| --- | --- | --- | --- |
| 2025 | Zhang et al. | arXiv | [PersonaAgent: When LLM Agents Meet Personalization at Test Time](https://arxiv.org/abs/2506.06254) |
| 2025 | Wang et al. | ICML | [CoSER: Coordinating LLM-Based Persona Simulation of Established Roles](https://openreview.net/forum?id=BOrR7YqKUt) |
| 2025 | Liu et al. | ACL | [A Persona-Aware LLM-Enhanced Framework for Multi-Session Personalized Dialogue](https://aclanthology.org/2025.findings-acl.5/) |

<h3 id="applications">Applications</h3>

* **Social Simulation:** *Generative Agents*, *WarAgent*, *CharacterBox*.
* **Companionship:** *Silicon Friends*, *SoulChat*.
* **Training/Education:** *EduAgent*, *GuideLLM*.

---

<h2 id="-evaluation">⚖️ Evaluation</h2>

Metrics and benchmarks for assessing Persona Consistency and Memory Dynamics.

| Date | Authors | Venue | Paper | Focus |
| --- | --- | --- | --- | --- |
| 2025 | Tan et al. | ACL | [MemBench: Towards More Comprehensive Evaluation on the Memory of LLM-based Agents](https://aclanthology.org/2025.findings-acl.989/) | Memory |
| 2025 | Yuan et al. | AAAI | [DMT-RoleBench: Dynamic Multi-Turn Dialogue Benchmark](https://arxiv.org/abs/2502.10575) | Role-Play |
| 2024 | Maharana et al. | ACL | [Evaluating Very Long-Term Conversational Memory of LLM Agents (LOCOMO)](https://aclanthology.org/2024.acl-long.747/) | Long Context |
| 2024 | Joko et al. | SIGIR | [Doing Personal LAPS: Personalized Multi-Session Conversational Search](https://arxiv.org/abs/2402.16288) | Personalization |

---

<h2 id="-contribution">🌱 Contribution</h2>

We welcome contributions to this reading list! Please refer to the format below and submit a Pull Request.

```markdown
| Date | Authors | Venue | Paper |
|:---:|:---:|:---:|:---|
| 2026 | Doe et al. | Conf | [Title](Link) |

```

<h2 id="-citation">🔖 Citation</h2>

If you find this survey useful, please cite our paper:

```bibtex
@article{Wu2026TrueToRole,
  title={True-to-Role, Tailored-to-You: A Survey of Role-Playing LLM Agents},
  author={Your Name and Co-Authors},
  journal={arXiv preprint arXiv:25XX.XXXXX},
  year={2026}
}

```

---

<p align="center">
<img src="https://img.shields.io/badge/Maintained%20with-❤️-blueviolet" alt="Maintenance">
</p>
