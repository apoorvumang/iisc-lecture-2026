# IISc DS 207 — Guest Lectures (April 2026)

Guest lecturer: **Apoorv Saxena**, Inception AI
Course: DS 207 — Introduction to NLP, IISc Bangalore
Instructor: Danish Pruthi

---

## Lecture 1 — Decoding in Autoregressive LLMs (April 2, 2026)

**Slides:** [Google Slides](https://docs.google.com/presentation/d/1MA1TJSrTo31cBc--ex6lIlyj5akOfGCVIffL_8Kn_y4/edit) · `lecture1_decoding_final.pptx`
**Notebook:** `lecture1_decoding.ipynb`

### Topics covered
- What is a language model? Autoregressive generation
- Greedy decoding · Temperature scaling
- Top-k · Top-p (nucleus) · Min-p sampling
- The autoregressive speed bottleneck
- Prompt Lookup Decoding (PLD) — speedup without a second model

### Running the notebook

```bash
uv venv && source .venv/bin/activate
uv pip install -r requirements.txt
jupyter lab lecture1_decoding.ipynb
```

GPT-2 (~500 MB) downloads automatically on first run.

---

## Lecture 2 — Discrete Diffusion Language Models (April 7, 2026)

**Slides:** [Google Slides](https://docs.google.com/presentation/d/1Avb7RFp3tfQyzIxqn6Cb9z4_zT9lAZH1w6-0DRA8mMc/edit) · `lecture2_diffusion_final.pptx`
**Notebook:** `lecture2_diffusion.ipynb`

### Topics covered
- Recap: the autoregressive constraint and its limits
- Diffusion in images (Stable Diffusion / DALL-E) — how it maps to text
- BERT as a masked language model — filling blanks, AR generation, the key insight
- Discrete diffusion theory: forward process (progressive masking), training objective, inference
- Iterative unmasking algorithm — building it from scratch with BERT
- Infilling: something AR models can't do natively
- Real diffusion LLMs: MDLM, SEDD, LLaDA, Dream
- Open problems: scaling, alignment, efficiency

### Running the notebook

```bash
uv venv && source .venv/bin/activate
uv pip install -r requirements.txt
jupyter lab lecture2_diffusion.ipynb
```

BERT-base (~440 MB) downloads automatically on first run. The notebook runs fully on CPU (M-series Mac or any machine).

For the Dream diffusion LLM demo (Part 5), a GPU is needed — the relevant cells have a `USE_DREAM = False` flag with pre-computed example outputs shown below.
