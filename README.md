# Awesome-Structural-Biology-AI

# Top Structural Biology & AI Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Protein Structure Prediction, Molecular Docking & AI-Driven Drug Discovery*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Structural Biology & AI**. These tools use deep learning, physics-based simulation, and molecular modeling to predict protein structures, simulate biomolecular interactions, and accelerate drug discovery — turning amino acid sequences into actionable 3D models and binding affinity predictions.

**Examples** include Schrödinger PyMOL, Rosetta Commons, AlphaFold Server, Boltz, Chai-1, OpenFold, GNINA, Insilico Medicine, Recursion, and DNAnexus (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, open-weight structure prediction, and transparent molecular modeling — ideal for academic researchers, biotech startups, and developers building computational biology pipelines without restrictive commercial licenses.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Schrödinger PyMOL](https://pymol.org/)**  
  **The industry-standard molecular visualization system.** Open-Source PyMOL is freely available under a permissive license from Schrödinger, LLC, allowing use, copy, modification, and distribution for any purpose without fee, provided copyright notices remain intact[citation:8]. The commercial Incentive PyMOL adds features like ray tracing and advanced rendering. Used universally for structure analysis, figure generation, and drug discovery workflows.

- **[AlphaFold Server](https://alphafoldserver.com/)**  
  **Google DeepMind's hosted AlphaFold3 service** for non-commercial research. Predicts structures of protein complexes including proteins, nucleic acids, small molecules, ions, and modified residues[citation:11]. Free with a **20 predictions per day limit** for academic users[citation:1]. DeepMind released the underlying inference code on GitHub in November 2024 under a **noncommercial license**, with model weights available to academics via application[citation:1][citation:11]. The portal remains the practical choice for groups with limited computing power[citation:1].

- **[Rosetta Commons](https://www.rosettacommons.org/)**  
  **The foundational macromolecular modeling suite** with decades of development. Downloads available for **academic and non-commercial users under the Rosetta Software Non-Commercial License Agreement**[citation:7]. **Commercial use requires a separate license** — including fee-for-service work by academic users[citation:7]. Provides protein structure prediction, design, docking, and refinement. The most recent development version is on GitHub[citation:7].

- **[Insilico Medicine](https://insilico.com/)**  
  AI-driven drug discovery company with end-to-end pipeline from target identification to clinical trials. Uses generative AI for molecular design and structural biology for validation.

- **[Recursion](https://www.recursion.com/)**  
  Tech-bio company using machine learning and computer vision for drug discovery at scale. Combines biological imaging with AI to map cellular relationships.

- **[DNAnexus](https://www.dnanexus.com/)**  
  Cloud platform for biomedical data analysis with structural biology workflows and secure data management.

## Open-Source GitHub Projects

- **[Boltz-2](https://github.com/jwohlwend/boltz)**  
  **The leading fully open-source biomolecular foundation model** — **MIT licensed for both academic and commercial use**, including drug discovery[citation:2][citation:12]. **Boltz-1 was the first fully open source model to approach AlphaFold3 accuracy**[citation:2]. **Boltz-2 goes beyond AlphaFold3** by jointly modeling complex structures and binding affinities, making it the **first deep learning model to approach physics-based FEP accuracy while running 1000x faster**[citation:2]. Install via `pip install boltz[cuda] -U`[citation:2]. Predict structures and affinities with `boltz predict input.yaml --use_msa_server`[citation:2]. Outputs include `affinity_pred_value` (log10 IC50) for ligand optimization and `affinity_probability_binary` (0-1) for binder detection[citation:2]. Runs on NVIDIA GPUs with cuEquivariance acceleration and also supports Tenstorrent hardware[citation:12].

- **[Chai-1](https://github.com/chaidiscovery/chai-lab)**  
  **Open-source multi-modal foundation model for molecular structure prediction** — **Apache-2.0 licensed for academic and commercial use**[citation:13]. Folds proteins together with **small-molecule ligands, nucleic acids, glycans, and covalent modifications** in a single model[citation:13]. Uses all-atom co-folding approach similar to AlphaFold3 with diffusion-based structure generation. **Token limit: 2,048 per complex** (1 per amino-acid residue, 1 per heavy atom for ligands)[citation:13]. Reports per-atom **pLDDT**, **PAE**, **pTM**, and **ipTM** confidence metrics[citation:13]. Supports ESM embeddings and ColabFold MSAs for protein conditioning[citation:13].

- **[OpenFold-3](https://github.com/aqlaboratory/openfold-3)**  
  **Fully open-source biomolecular structure prediction model based on AlphaFold3**[citation:4]. Part of the OpenFold consortium's mission to provide implementations free from restrictive user licenses[citation:1]. Documentation at openfold-3.readthedocs.io[citation:4].

- **[OpenFold (AlphaFold2 Reproduction)](https://github.com/aqlaboratory/openfold)**  
  **Trainable, memory-efficient, GPU-friendly PyTorch reproduction of AlphaFold2**[citation:15]. Provides the foundation for many downstream structure prediction tools. Includes **SoloSeq** mode using ESM-1b embeddings (sequence limit ~1022 residues) and standard MSA-based prediction[citation:14]. Training pipeline requires precomputed alignments from UniRef90, MGnify, and PDB70 databases[citation:14].

- **[GNINA 1.3](https://github.com/gnina/gnina)**  
  **Open-source molecular docking software with deep learning scoring functions**[citation:6]. **Version 1.3** updates the deep learning framework to **PyTorch** for more computationally efficient docking, retrained CNN scoring functions on CrossDocked2020 v1.3, introduces **knowledge-distilled CNNs** for high-throughput virtual screening, and adds **covalent docking** functionality[citation:6]. User-friendly framework for protein-ligand docking[citation:6].

- **[EasyDock 1.3](https://github.com/ci-lab-cz/easydock)**  
  **Automated pipeline for molecular docking** with **client-server architecture** distributing docking engines as Apptainer/Docker containers[citation:16]. Supports **CarsiDock** and **SurfDock** deep-learning docking methods, plus **GPU-accelerated Vina** family tools[citation:16]. **Ligand preparation** uses open-source protonation (MolGpKa, pkasolver, Uni-pKa), removing commercial software dependency[citation:16]. **PLIF computation** and **PoseBusters-based pose validation** integrated[citation:16]. Accessible via CLI (`easydock`) and Python API[citation:16].

### Additional Strong Open-Source Options

- **ESMFold** — Meta's protein language model for structure prediction without MSAs. Single-sequence, fast.
- **OmegaFold** — Single-sequence language-model-based prediction network[citation:15].
- **HelixFold** — PaddlePaddle-based efficient AlphaFold2 implementation[citation:15].
- **ColabFold** — AlphaFold2 using MMseqs2 for accessible MSA generation[citation:15].
- **PIMD** — Open-source molecular simulation package with **path integral molecular dynamics, metadynamics, and QM/MM** support. **Apache 2.0 licensed**. **v2.7** adds N2P2 neural network potentials and VASP 6 interface for ab initio DFT[citation:10].
- **TorchSim** — **Open-source atomistic simulation engine for the MLIP era**. **MIT licensed**. Rewrites core primitives in PyTorch for **up to 100x speedup** over ASE with popular MLIPs (MACE, Fairchem, SevenNet, ORB, MatterSim)[citation:20]. Supports batched MD, relaxation, and Monte Carlo algorithms with GPU memory management[citation:20].
- **CryoSPARC / cisTEM / RELION** — Cryo-EM data processing suites for experimental structure determination[citation:19].

**Frameworks for building custom systems**: Combine **Boltz-2** for structure prediction and binding affinity in one MIT-licensed model, **Chai-1** for protein-ligand-glycan complex prediction under Apache-2.0, **GNINA** or **EasyDock** for molecular docking with deep learning scoring, **PyMOL** for visualization and figure generation, and **TorchSim** for atomistic simulation with machine learning potentials — to build a complete open-source structural biology pipeline from sequence to binding affinity.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Structural biology AI tools differ significantly in licensing terms and intended use. **Boltz-2 and Chai-1 are MIT/Apache-2.0 licensed for commercial use** — a critical advantage over AlphaFold3's noncommercial license[citation:1][citation:2][citation:13]. **Rosetta requires commercial licensing for fee-for-service work by academic users**[citation:7]. **AlphaFold3 weights require an application for academic access** and are not freely redistributable[citation:1]. Predicted structures and binding affinities are computational estimates — **experimental validation remains essential** before clinical or manufacturing decisions. Accuracy varies by target class and complex composition.
- Self-hosted open-source solutions require proper GPU infrastructure, database access for MSAs, and domain expertise for interpretation.

---

**Made for structural biologists, computational chemists, drug discovery researchers, and developers building molecular modeling platforms.**  
Let's make structural biology AI more open, accurate, and commercially accessible.
