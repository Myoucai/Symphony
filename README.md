# 🎻 Symphony

> **A programming language without source code.**

[![Conceptual](https://img.shields.io/badge/status-thought%20experiment-blue)](./Symphony.md#6-currently-unrealizable)
[![License: CC BY 4.0](https://img.shields.io/badge/license-CC%20BY%204.0-green)](https://creativecommons.org/licenses/by/4.0/)

Programs are high-dimensional vectors. Execution is a diffusion process.  
No syntax. No compiler. No instruction sequences.

---

## 🧠 Core Idea

Traditional programming languages are **text**. You write code, compile it, and a CPU executes instructions one after another.

**Symphony breaks this completely.**

- A Symphony program is an **embedding vector** — a list of floating-point numbers (e.g., 768 dimensions).
- There is **no source code**, no variable names, no syntax tree.
- You don't write programs. You **describe intent**, and an AI crystallizes that intent directly into a program vector.
- Execution means running a **diffusion model** that transforms the program vector + input into output, step by denoising step.

---

## ⚙️ How It Works (in theory)

```
Intent (NL / examples)
        │
        ▼
   Crystallizer AI          ←  One-shot: intent → program vector
        │
        ▼
   Program Vector P          ←  768 floats, encodes full program semantics
        │
        ▼
   ExecNet (diffusion)       ←  Iterative denoising: P + input → output
        │
        ▼
      Output Y
```

1. **Express** your intent through natural language, input/output examples, or a visual graph.
2. **Crystallize** — a powerful AI converts intent into a fixed program vector `P`.
3. **Execute** — `ExecNet`, a diffusion model, denoises `P + input` into the output. No program counter, no stack, no heap.

---

## 🔐 Key Innovations

### Capability Fields (Geometric Security)
Security is not enforced by syscall filters — it's **geometry**. External resources (files, network) are sub-spaces in latent space. If a program vector tries to access a sub-space it isn't authorized for, the diffusion process *cannot produce a valid trajectory*. Security is fundamentally un-bypassable.

### Types as Manifold Topology
Types aren't discrete sets — they're **shapes in latent space**. `integer` is a spiral manifold. An email address is a twisted knot. Type checking is manifold containment testing: does the value lie inside the parameter manifold? This naturally supports **probabilistic types** — "87% likely a valid email."

### Adaptive & Self-Evolving
Symphony programs **never stop learning**. Bug fixes are **patch vectors** added to the original program vector — no text editing, no recompilation.

---

## 📊 Traditional vs. Symphony

| Traditional Languages          | Symphony                                        |
| ------------------------------ | ----------------------------------------------- |
| Text, tokens                   | High-dimensional vectors (a few KB)             |
| Sequential instructions        | Parallel diffusion steps                        |
| Syntax errors, type errors     | Manifold containment failures (soft)            |
| Security via syscall filters   | Geometric capability fields                     |
| Human-readable                 | Not readable — verifiable by exhaustive testing |
| Fixed behavior                 | Continuously adapts at runtime                  |

---

## ⚠️ Currently Unrealizable

**Symphony is a thought experiment.** It cannot be built with today's technology.

| Requirement                             | State of the Art                                             |
| --------------------------------------- | ------------------------------------------------------------ |
| Crystallizer (intent → program vector)  | No model can generate correct general-purpose programs from a single embedding. Current LLMs need step-by-step decoding. |
| ExecNet (general diffusion for code)    | Diffusion works for images/robotics, not arbitrary algorithms. Training data doesn't exist. |
| Latent space security                   | No known method to enforce hard constraints in learned latent spaces. |
| Manifold type checking                  | Early research stage.                                        |
| Hardware                                | No specialized accelerators for diffusion-based execution.   |

Symphony requires **AGI-level synthesis**, a **foundational model of execution**, and **new hardware** — none of which exist today.

---

## 🌌 Why This Exists

We're stuck in "AI generates text that humans can read." Symphony asks:

> **What if we freed AI from the constraints of human-readable text and let it program directly in its native medium — continuous vector spaces?**

This design is a **north star** for where programming languages could go once AI becomes the primary author of software.

---

## 📖 Read the Full Design

The complete conceptual design is in **[Symphony.md](./Symphony.md)** — including detailed sections on execution, security, typing, programming workflow, and related work.

---

## 💡 Getting Involved

Symphony is a question, not a product. If you have ideas on how to inch closer to this vision:

- **Discussions** — Open a [GitHub Discussion](https://github.com/Myoucai/Symphony/discussions) to share thoughts.
- **Issues** — Report conceptual bugs, suggest extensions, or propose research directions.
- **PRs** — Improvements to the design document are welcome.

---

## 📄 License

This project is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).  
Feel free to discuss, extend, or borrow ideas.

---

*Symphony is not a product. It is a question.*
