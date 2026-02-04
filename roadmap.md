# Deep Learning Roadmap (LSTM → RNN → Transformer → LLMs)

This roadmap follows your requested order. Note: LSTM is a type of RNN, so after LSTM we’ll revisit “vanilla” RNNs to deepen intuition and see why LSTMs were introduced.

## Phase 0 — Foundations (quick but essential)
- Math: vectors, matrices, gradients, chain rule, softmax, cross-entropy
- Core DL: backprop, SGD/Adam, overfitting, regularization, train/val/test
- Tools: Python + PyTorch basics (tensors, autograd, modules, optimizers)

Mini project
- Train a simple MLP on MNIST or a small tabular dataset

## Phase 1 — LSTM First (your starting point)
Goals
- Understand LSTM gates, cell state, and why they help long-term dependencies
- Implement LSTM from scratch, then use PyTorch LSTM

Learn
- LSTM equations and gating intuition
- Sequence data: padding, masking, batching, teacher forcing
- Loss for sequence prediction (next-token prediction)

Mini projects
- Character-level text generation with LSTM
- Time series forecasting with LSTM (e.g., temperature or stock-like synthetic data)

## Phase 2 — RNN (vanilla, GRU, BPTT)
Goals
- Understand vanilla RNNs and the vanishing/exploding gradient problem
- Compare vanilla RNN, GRU, and LSTM

Learn
- RNN recurrence and unrolling
- Backpropagation Through Time (BPTT)
- Gradient clipping

Mini projects
- Implement vanilla RNN forward + BPTT from scratch (small toy sequence)
- Compare training stability: RNN vs LSTM vs GRU on same task

## Phase 3 — Transformer (full training, then inference)
Goals
- Understand attention, multi-head attention, positional encodings
- Implement a full encoder-decoder transformer
- Train on a small translation dataset
- Implement inference with greedy + beam search and KV caching

Learn
- Self-attention, scaling, masking
- Encoder-decoder vs decoder-only
- Tokenization and subword vocab (BPE)
- Training loop: LR warmup, label smoothing, batching by length
- Inference: autoregressive decoding, cache past keys/values

Mini projects
- Build a toy transformer and overfit a copy task
- Train on IWSLT14 (or smaller parallel dataset) for translation
- Write a clean inference script with greedy + beam search + caching

## Phase 4 — LLM Training & Methods
Goals
- Understand pretraining objectives and scaling behavior
- Learn data pipelines, tokenization, distributed training basics
- Understand instruction tuning and alignment methods

Learn
- Causal LM objective (next-token prediction)
- Data pipeline: dedup, filtering, mixing, tokenization
- Scaling laws + compute-optimal training
- Distributed training: data parallel, tensor parallel, pipeline parallel
- Fine-tuning: SFT, instruction tuning
- Alignment: RLHF, DPO (conceptual understanding)

Mini projects
- Pretrain a small decoder-only model on an open dataset (tiny scale)
- Instruction-tune on a small curated dataset
- Evaluate with perplexity + simple downstream tasks

---

# Recommended Resources (Blogs, YouTube, Courses, Papers)

## Blogs / Articles
- Understanding LSTMs (colah): https://colah.github.io/posts/2015-08-Understanding-LSTMs/
- The Unreasonable Effectiveness of RNNs (Karpathy): https://karpathy.github.io/2015/05/21/rnn-effectiveness/
- The Illustrated Transformer (Jay Alammar): https://jalammar.github.io/illustrated-transformer/
- The Annotated Transformer (Harvard NLP): https://nlp.seas.harvard.edu/annotated-transformer/

## YouTube / Lectures
- MIT 6.S191 Introduction to Deep Learning (MIT Deep Learning): https://www.youtube.com/live/alfdI7S6wCY
- Stanford CS224n: NLP with Deep Learning (Stanford Online playlist + course site)
  - Course site: https://web.stanford.edu/class/cs224n/index.html

## Core Papers (LLM & Transformers)
- Attention Is All You Need: https://arxiv.org/abs/1706.03762
- GPT-3: Language Models are Few-Shot Learners: https://arxiv.org/abs/2005.14165
- Scaling Laws for Neural Language Models: https://arxiv.org/abs/2001.08361
- Training Compute-Optimal LLMs (Chinchilla): https://arxiv.org/abs/2203.15556
- LLaMA: Open and Efficient Foundation Language Models: https://arxiv.org/abs/2302.13971

---

# Suggested Pace (optional)
- If you can study ~6–8 hours/week:
  - Phase 0: 1–2 weeks
  - Phase 1: 3–4 weeks
  - Phase 2: 2–3 weeks
  - Phase 3: 4–6 weeks
  - Phase 4: ongoing, 6+ weeks

