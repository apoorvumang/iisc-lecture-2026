# IISc DS 207 — Guest Lectures (April 2026)

Guest lecturer: **Apoorv Saxena**, Inception AI
Course: DS 207 — Introduction to NLP, IISc Bangalore
Instructor: Danish Pruthi

---

## Lecture 1 — Decoding in Autoregressive LLMs (April 2, 2026)

**Slides:** [Google Slides](https://docs.google.com/presentation/d/1MA1TJSrTo31cBc--ex6lIlyj5akOfGCVIffL_8Kn_y4/edit)
**Notebook:** `lecture1_decoding.ipynb`

### Topics covered
- What is a language model? Autoregressive generation
- Greedy decoding · Temperature scaling
- Top-k · Top-p (nucleus) · Min-p sampling
- The autoregressive speed bottleneck
- Prompt Lookup Decoding (PLD) — speedup without a second model

### Running the notebook

```bash
uv venv
source .venv/bin/activate
uv pip install torch torchvision transformers jupyterlab matplotlib numpy
jupyter lab lecture1_decoding.ipynb
```

GPT-2 (~500 MB) downloads automatically on first run.

---

## Lecture 2 — Discrete Diffusion Language Models (April 7, 2026)

*Coming soon.*
