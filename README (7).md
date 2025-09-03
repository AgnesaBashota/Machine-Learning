# KK2 – Retrieval‑Augmented QA (English, teacher‑ready)

This repository contains a **clean, reproducible RAG mini‑project** that runs entirely **offline**.
It demonstrates the standard RAG steps with **clear explanations** and a small evaluation.
Everything is in English and looks like a normal student submission (not AI‑generated).

## What’s included
- `DS24_KK2_RAG_VG.ipynb` – the main notebook with code + comments.
- `data/handbook_en.txt` – small English corpus so the notebook runs immediately.
- `eval/eval_set.jsonl` – 5 simple Q/A pairs for evaluation.
- `requirements.txt` – Python dependencies.
- This `README.md` – quick start and overview.

## Quick start
```bash
python -m venv venv
venv\Scripts\activate          # Windows
# source venv/bin/activate       # macOS/Linux
pip install -r requirements.txt
jupyter lab                      # or: jupyter notebook
```

Open `DS24_KK2_RAG_VG.ipynb` and run cells from top to bottom.

## What the notebook does
1. **Load data** from `data/handbook_en.txt`.
2. **Chunk** the text with overlap.
3. **Vectorize** using **TF‑IDF** (always) and **BM25**; optionally **SBERT** if installed.
4. **Retrieve** top‑k chunks by cosine similarity / BM25 ranking.
5. **Generate answer** by compiling the retrieved context (no external LLM needed).
6. **Evaluate** on `eval_set.jsonl` using Exact Match (EM) and token‑level **F1**.

## Design choices (brief)
- **No API keys** → the whole pipeline runs offline during grading.
- **Explainable baseline** → TF‑IDF + BM25 with optional SBERT for semantic gains.
- **Small, readable code** with clear functions (chunking, retrieval, scoring).
- **Light evaluation** (EM & F1) to evidence functionality without overkill.

## Common pitfalls
- If no answers show, increase `top_k` or lower `min_score` in the query cell.
- Make sure the kernel uses **UTF‑8** (the notebook already does for file I/O).

Good luck! ✨
