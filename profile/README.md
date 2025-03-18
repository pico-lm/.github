# Pico: A Lightweight Framework for Studying Language Model Learning Dynamics

Welcome to **Pico LM** 👋, a research initiative dedicated to **demystifying language model learning**. We create two complementary frameworks (pico-train and pico-analyze) for training and analyzing small to mid-scale language models (1M–1B parameters). Our mission is to provide a transparent, research-oriented workflow that illuminates how these models learn.

1. [**pico-train**](https://github.com/pico-lm/pico-train) 🚀  
   A **minimalistic yet powerful** training framework designed to let you **build, scale, and experiment** with your own suite of language models. It currently supports a **pico-decoder** (LLAMA-style auto-regressive transformer) but is designed to accommodate additional architectures (e.g., pico-diffusion, pico-statespace) in the future. Checkpoints are **richly annotated** with activations and gradients, making it easy to study learning dynamics. It provides a **config-driven** approach (YAML-based) for hyperparameters and logging, and supports **multi-GPU / multi-node** setups out of the box via Lightning Fabric.

2. [**pico-analyze**](https://github.com/pico-lm/pico-analyze) 📊  
   A **specialized toolkit** for exploring and **visualizing** how your models evolve throughout training. It includes metrics like **CKA**, **PWCCA**, **sparsity** (Gini, Hoyer), **condition number**, and more, helping you measure changes in weights, gradients, or activations across checkpoints. This framework is **highly configurable**, allowing you to target specific layers or combine multiple layers into compound components. With built-in **comparative analysis**, you can track how a single model’s internals change over time or contrast different model sizes at key steps. The system is also **extensible**, enabling you to register new metrics or define custom components that align with your research needs, and integrates easily with Weights & Biases for detailed logging and interactive dashboards.

---

## **Further Resources**

**Pico Decoder Model Suite**: We use **pico-train** to train a suite of pico-decoder models from from **10M** to **500** parameters. 
  - Each checkpoint includes weights, optimizer states, **gradients**, and **activations**
  - Available on 🤗 [Hugging Face](https://huggingface.co/pico-lm)

**Datasets**: Curated and **pre-tokenized** 420B token corpora derived from [Dolma](https://allenai.org/dolma) for model training. 
  - Stream-ready and **consistently shuffled** for easy training
  - Available on 🤗 [Hugging Face](https://huggingface.co/pico-lm)
    
**Documentation & Tutorials**: Visit [picolm.io](https://picolm.io) for step-by-step tutorial to help you get setup with:
  - Training with pico-train  
  - Analyzing checkpoints with pico-analyze  
  - Configuring your own experiments

---
## **Our Philosophy: What Makes Pico Special?**

Pico is designed for **transparency**, **interpretability**, and **open collaboration** in language model research. Here’s how we stand apart:

1. **Full Access to Training Checkpoints**  
   We expose **every** training step, allowing researchers to observe how a model’s parameters evolve over time. This granular access is invaluable for studying convergence patterns, overfitting behaviors, and step-by-step layer changes.

2. **Advanced Gradient and Activation Data**  
   Each checkpoint includes **gradient and activation** snapshots, enabling **post-hoc** interpretability studies. Dive deep into how layers respond to different inputs, track gradient flow issues, or uncover subtle architecture-specific phenomena.

3. **Detailed Learning Trajectories**  
   Want to examine induction head evolution, data memorization, or early-phase overfitting? With Pico’s **rich checkpoints**, you can systematically explore these learning dynamics in a **small-to-medium-scale** context without incurring massive compute costs.

4. **Pico-Analyze Toolkit**  
   Our companion project, **pico-analyze**, simplifies the computation of key interpretability metrics. Effortlessly measure representation similarity (CKA, PWCCA), sparsity (Gini, Hoyer), effective rank, and more—no need to integrate multiple disparate libraries.

5. **Lightweight & Modular Codebase**  
   Pico’s code is **easy to fork, extend, and adapt**. By focusing on smaller models (1M–1B parameters), we ensure that rigorous experimentation is both **affordable** and accessible to a broader research community.

6. **Open-Source Commitment**  
   - **Code, Checkpoints, and Datasets**: Everything is released under a permissive license, encouraging transparent and reproducible science.  
   - **Collaboration-Ready**: Researchers, educators, and developers can iterate, modify, and innovate freely—no hidden data or proprietary code.

In essence, Pico aims to **demystify** how language models learn by giving you **unprecedented visibility** into their training processes, all within a framework that is simple enough to adapt yet robust enough for cutting-edge interpretability research.

---

## **Stay Connected**

- **Website**: [picolm.io](https://picolm.io) for tutorials, documentation, and blog updates  
- **GitHub**: Star our repositories or open issues/pull requests to get involved  
- **Hugging Face**: [pico-lm](https://huggingface.co/pico-lm) organization for all our published models

---

## **License**

All Pico software is open-source under the [Apache License 2.0](LICENSE).

---

## **Citation**

If you use **Pico** in your research, please cite:

```bibtex
@software{pico2024,
    author = {Diehl Martinez, Richard},
    title = {Pico: Framework for Training Tiny Language Models},
    year = {2024},
    url = {https://github.com/rdiehlmartinez/pico}
}
```

**Happy experimenting!**  
We hope Pico helps you gain deeper insights into **how language models learn** and encourages new discoveries in model interpretability and design.


