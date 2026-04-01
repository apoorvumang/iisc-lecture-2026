# Guest Lecture Plan: From Decoding to Diffusion LLMs

**Course:** DS 207 — Introduction to NLP (Jan–May 2026)
**Guest Lecturer:** Apoorv Saxena, Inception AI
**Dates:** April 2 & April 7, 2026 (1–1.5 hrs each)

---

## Lecture 1 (Apr 2): Decoding in Autoregressive LLMs

Since decoding hasn't been covered yet in the course, this lecture builds up from fundamentals to modern inference-time techniques.

**Foundations & Basic Decoding (~30 min, with notebook)**
Autoregressive generation setup, logits → softmax → probabilities, greedy decoding and its failure modes, sampling with temperature, top-k, top-p (nucleus sampling), and min-p. Interactive notebook using GPT-2 where students see real probability distributions and implement basic decoding from scratch.

**Speculative & Prompt Lookup Decoding (~25 min)**
The autoregressive speed bottleneck (sequential dependency, uniform cost per token). Speculative decoding: draft-then-verify paradigm and parallel verification. Prompt Lookup Decoding: generating draft tokens from the prompt itself without a separate model, with code walkthrough and benchmarks.

**Bridge to Lecture 2 (~5 min)**
All these methods accept the autoregressive constraint and try to work around it. What if we could generate all tokens in parallel through iterative refinement instead?

---

## Lecture 2 (Apr 7): Discrete Diffusion Language Models

**Motivation (~8 min)**
Limitations of autoregressive generation: sequential bottleneck, left-to-right constraint, no native infilling. What would ideal generation look like?

**Diffusion Intuition + Discrete Diffusion Theory (~20 min)**
Brief visual intuition from image diffusion, then focus entirely on discrete/masked diffusion for text. Forward process: progressively mask tokens according to a noise schedule. Training objective: predict masked tokens at varying noise levels — connecting BERT's MLM (fixed 15% masking) to diffusion (MLM across all noise levels). Generation: iterative unmasking with confidence-based token selection. Brief mention of SEDD as an alternative formulation.

**Notebook Demo (~20 min)**
Three-step progression using the dLLM library: (1) naive autoregressive generation with BERT — doesn't work well; (2) iterative unmasking with vanilla BERT — better but hacky; (3) ModernBERT-chat trained with a proper diffusion objective — actually works. Step-by-step visualization of the denoising process.

**Results, Capabilities & Open Problems (~10 min)**
Key models: MDLM, LLaDA, SEDD. Quality comparisons with autoregressive models. Unique capabilities: infilling, parallel generation, controllable compute. Open problems: scaling, long sequences, alignment for diffusion models.

---

**Jupyter notebooks** will accompany both lectures for hands-on demonstration.
