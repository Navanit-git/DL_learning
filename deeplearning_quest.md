# 🎮 Deep Learning Quest: LSTM → RNN → Transformer → LLMs

**Quest Type:** Solo Campaign  
**Difficulty:** Progressive (Easy → Legendary)  
**Total XP Available:** 10,000  
**Current Level:** 0

---

## 🗺️ World Map

```
[FOUNDATIONS] → [LSTM REALM] → [RNN VALLEY] → [TRANSFORMER EMPIRE] → [LLM ENDGAME]
     ⭐              ⭐⭐            ⭐⭐⭐              ⭐⭐⭐⭐                ⭐⭐⭐⭐⭐
```

---

## 🏰 LEVEL 0: FOUNDATIONS CAMP

**Objective:** Build your starter kit  
**XP Reward:** 500  
**Status:** 🔓 Unlocked

### Checkpoint 0.1: Math Arsenal ✅
**Skills to Learn:**
- Vector/matrix operations
- Derivatives and chain rule
- Softmax function
- Cross-entropy loss

**Verify You Can:**
- [ ] Compute dot product by hand (3x1 · 3x1)
- [ ] Derive d/dx of sigmoid(x)
- [ ] Explain chain rule with f(g(x))
- [ ] Code softmax from scratch (numpy)
- [ ] Calculate cross-entropy loss manually

**Resources:**
- 3Blue1Brown: Neural Networks playlist
- udlbook Chapter 1-3

**Boss Check:** Code gradient descent for y = wx + b (5 iterations, plot loss)

---

### Checkpoint 0.2: PyTorch Basics ✅
**Skills to Learn:**
- Tensors (creation, indexing, operations)
- Autograd and .backward()
- nn.Module, nn.Linear, nn.MSELoss
- Optimizers (SGD, Adam)

**Verify You Can:**
- [ ] Create tensor, reshape, slice it
- [ ] Set requires_grad=True and compute gradients
- [ ] Build a class inheriting nn.Module
- [ ] Write training loop with optimizer.step()

**Mini Quest:**
```python
# Code this from scratch
class TinyNet(nn.Module):
    # 2-layer MLP
    # Train on XOR problem
    # Achieve <0.1 loss
```

**Resources:**
- PyTorch 60-min blitz tutorial
- udlbook Chapter 4-5

---

### 🎯 BOSS BATTLE 0: MNIST Conqueror
**Challenge:** Train MLP on MNIST, achieve >95% accuracy

**Requirements:**
- [ ] Load data with DataLoader
- [ ] Build 2-3 layer MLP
- [ ] Use ReLU activation
- [ ] Track train/val loss
- [ ] Plot learning curves
- [ ] Test on holdout set

**XP:** 200  
**Unlocks:** LSTM Realm

---

## 🏰 LEVEL 1: LSTM REALM

**Objective:** Master long-term memory  
**XP Reward:** 1,500  
**Status:** 🔒 Locked (Complete Level 0)

### Checkpoint 1.1: LSTM Theory ✅
**Skills to Learn:**
- Forget gate, input gate, output gate
- Cell state vs hidden state
- Why LSTM > vanilla RNN for long sequences

**Verify You Can:**
- [ ] Draw LSTM cell diagram from memory
- [ ] Explain each gate's purpose (in 1 sentence each)
- [ ] Write LSTM equations (all 4: f, i, o, c)
- [ ] Explain vanishing gradient problem

**Resources:**
- colah's blog: Understanding LSTMs
- udlbook Chapter 7

**Side Quest:** ⭐ Implement single LSTM cell forward pass (numpy, no training)

---

### Checkpoint 1.2: Sequence Data Handling ✅
**Skills to Learn:**
- Padding and masking
- Batch-first vs time-first
- Teacher forcing
- Next-token prediction loss

**Verify You Can:**
- [ ] Pad sequences to same length
- [ ] Create attention masks
- [ ] Explain teacher forcing vs free-running
- [ ] Code data loader for text sequences

**Mini Quest:**
```python
# Create dataset class for:
sequences = ["hello", "world", "deep learning"]
# Output: padded tensors + masks
```

---

### Checkpoint 1.3: PyTorch LSTM ✅
**Skills to Learn:**
- nn.LSTM parameters
- Input shape: (batch, seq, features)
- Hidden/cell state initialization
- Many-to-one vs many-to-many

**Verify You Can:**
- [ ] Initialize nn.LSTM with correct args
- [ ] Feed sequences through LSTM
- [ ] Extract final hidden state
- [ ] Use output for classification/generation

**Mini Quest:**
```python
# Sentiment classifier
# IMDB reviews → positive/negative
# LSTM → Linear → sigmoid
```

---

### 🎯 BOSS BATTLE 1A: Character-Level Text Generator
**Challenge:** Generate text in the style of a book/author

**Requirements:**
- [ ] Char-level tokenization (vocab size ~50-100)
- [ ] LSTM with embedding layer
- [ ] Train with next-char prediction
- [ ] Sample with temperature
- [ ] Generate 200+ coherent chars

**Dataset:** tiny-shakespeare.txt or any .txt file  
**XP:** 300

---

### 🎯 BOSS BATTLE 1B: Time Series Prophet
**Challenge:** Forecast temperature/stock-like data

**Requirements:**
- [ ] Sliding window data prep
- [ ] LSTM for regression
- [ ] Multi-step forecasting
- [ ] Plot predictions vs actual
- [ ] Compute MAE/RMSE

**Dataset:** Synthetic sine wave + noise OR air quality dataset  
**XP:** 300

---

### 🏆 ACHIEVEMENT UNLOCKED: "LSTM Master"
- Complete both boss battles
- Code LSTM from scratch (forward only)
- **Bonus XP:** 200  
- **Unlocks:** RNN Valley

---

## 🏰 LEVEL 2: RNN VALLEY

**Objective:** Understand the OG recurrent network  
**XP Reward:** 1,200  
**Status:** 🔒 Locked (Complete Level 1)

### Checkpoint 2.1: Vanilla RNN ✅
**Skills to Learn:**
- Single recurrence equation
- Unrolling through time
- Tanh activation role
- Why gradients vanish/explode

**Verify You Can:**
- [ ] Write RNN equation: h_t = tanh(W_hh * h_{t-1} + W_xh * x_t)
- [ ] Unroll RNN for 5 timesteps on paper
- [ ] Explain gradient flow problem
- [ ] Compare RNN cell vs LSTM cell size

**Resources:**
- Karpathy: Unreasonable Effectiveness of RNNs
- CS231n RNN lecture notes

---

### Checkpoint 2.2: Backpropagation Through Time ✅
**Skills to Learn:**
- BPTT algorithm
- Truncated BPTT
- Gradient clipping (why + how)

**Verify You Can:**
- [ ] Derive gradient for simple 2-step RNN
- [ ] Explain truncation trade-off
- [ ] Implement gradient clipping (torch.nn.utils.clip_grad_norm_)
- [ ] Show exploding gradient in practice

**Mini Quest:**
```python
# Train RNN without clipping → watch gradients explode
# Add clipping → see stabilization
# Log gradient norms over time
```

---

### Checkpoint 2.3: GRU (The Middle Child) ✅
**Skills to Learn:**
- Reset gate and update gate
- GRU vs LSTM (fewer params)

**Verify You Can:**
- [ ] Draw GRU cell diagram
- [ ] List GRU equations (3 gates)
- [ ] Compare param count: GRU vs LSTM

**Side Quest:** ⭐ Swap LSTM for GRU in Boss Battle 1A, compare performance

---

### 🎯 BOSS BATTLE 2: RNN From Scratch
**Challenge:** Code vanilla RNN forward + backward (BPTT)

**Requirements:**
- [ ] Numpy only (no PyTorch autograd)
- [ ] Forward pass for sequence
- [ ] BPTT for 10 timesteps
- [ ] Train on tiny task (copy sequence)
- [ ] Verify gradients with finite differences

**XP:** 400  
**Difficulty:** ⭐⭐⭐

---

### 🎯 BOSS BATTLE 2B: Architecture Deathmatch
**Challenge:** Compare RNN vs LSTM vs GRU on same task

**Requirements:**
- [ ] Same dataset (pick from Level 1)
- [ ] Same hyperparams (hidden size, LR, epochs)
- [ ] Track: loss curves, training time, final accuracy
- [ ] Plot all 3 on same graph
- [ ] Write 1-paragraph conclusion

**XP:** 300

---

### 🏆 ACHIEVEMENT: "Recurrence Archaeologist"
- Beat both battles
- Explain vanishing gradients to a friend
- **Unlocks:** Transformer Empire

---

## 🏰 LEVEL 3: TRANSFORMER EMPIRE

**Objective:** Master attention mechanisms  
**XP Reward:** 2,500  
**Status:** 🔒 Locked (Complete Level 2)

### Checkpoint 3.1: Attention Fundamentals ✅
**Skills to Learn:**
- Query, Key, Value concept
- Scaled dot-product attention
- Softmax for alignment scores
- Why "attention is all you need"

**Verify You Can:**
- [ ] Compute attention scores by hand (2x2 example)
- [ ] Explain Q, K, V in 1 sentence each
- [ ] Code attention function (no batching)
- [ ] Visualize attention weights

**Mini Quest:**
```python
def scaled_dot_product_attention(Q, K, V):
    # Implement this
    # Test on random 3x3 matrices
    pass
```

**Resources:**
- Illustrated Transformer (Jay Alammar)
- Attention is All You Need paper (skip experiments first)

---

### Checkpoint 3.2: Multi-Head Attention ✅
**Skills to Learn:**
- Why split into multiple heads
- Parallel attention computations
- Concatenation and projection

**Verify You Can:**
- [ ] Explain multi-head benefit
- [ ] Code MultiHeadAttention class
- [ ] Verify output shape (batch, seq, d_model)

**Side Quest:** ⭐ Visualize what different heads learn (attention heatmaps)

---

### Checkpoint 3.3: Positional Encoding ✅
**Skills to Learn:**
- Sin/cos encoding formula
- Why transformers need positions
- Learned vs fixed encodings

**Verify You Can:**
- [ ] Code sinusoidal PE function
- [ ] Plot PE for 100 positions
- [ ] Add PE to embeddings

---

### Checkpoint 3.4: Encoder Block ✅
**Skills to Learn:**
- Multi-head attention
- Feed-forward network (2-layer MLP)
- Add & Norm (residual + LayerNorm)

**Verify You Can:**
- [ ] Build EncoderLayer class
- [ ] Stack N encoder layers
- [ ] Explain residual connection benefit

---

### Checkpoint 3.5: Decoder Block ✅
**Skills to Learn:**
- Masked self-attention (causal mask)
- Cross-attention to encoder
- Autoregressive generation

**Verify You Can:**
- [ ] Create causal mask (upper triangular)
- [ ] Build DecoderLayer with 2 attention modules
- [ ] Explain decoder vs encoder differences

---

### Checkpoint 3.6: Full Transformer ✅
**Skills to Learn:**
- Encoder-decoder architecture
- Final linear + softmax layer
- Loss computation (cross-entropy over vocab)

**Verify You Can:**
- [ ] Combine encoder + decoder
- [ ] Add embedding and output layers
- [ ] Forward pass on dummy batch

---

### 🎯 BOSS BATTLE 3A: Copy Task Overfit
**Challenge:** Make transformer copy input sequence perfectly

**Requirements:**
- [ ] Input: random sequences (vocab=10, len=20)
- [ ] Output: exact copy
- [ ] Overfit on 100 examples to 100% accuracy
- [ ] Proves architecture works

**XP:** 200  
**Difficulty:** ⭐⭐

---

### Checkpoint 3.7: Tokenization ✅
**Skills to Learn:**
- BPE (Byte-Pair Encoding)
- WordPiece vs SentencePiece
- Vocab building

**Verify You Can:**
- [ ] Use tiktoken or tokenizers library
- [ ] Build BPE vocab from corpus
- [ ] Encode/decode text

**Resources:**
- HuggingFace tokenizers tutorial

---

### Checkpoint 3.8: Training Loop Tricks ✅
**Skills to Learn:**
- Learning rate warmup
- Label smoothing
- Batching by sequence length
- Gradient accumulation

**Verify You Can:**
- [ ] Implement LR schedule (warmup + decay)
- [ ] Add label smoothing to loss
- [ ] Group similar-length sequences
- [ ] Accumulate gradients over mini-batches

---

### 🎯 BOSS BATTLE 3B: Machine Translation
**Challenge:** Train transformer for EN→DE translation

**Requirements:**
- [ ] Dataset: IWSLT14 or Multi30k
- [ ] Full encoder-decoder transformer
- [ ] Train for 20+ epochs
- [ ] Implement greedy decoding
- [ ] Calculate BLEU score >10

**XP:** 500  
**Difficulty:** ⭐⭐⭐⭐

---

### Checkpoint 3.9: Inference Techniques ✅
**Skills to Learn:**
- Greedy vs beam search
- Top-k and top-p sampling
- KV caching for speed

**Verify You Can:**
- [ ] Implement greedy decoding
- [ ] Code beam search (beam_size=5)
- [ ] Add KV cache to decoder
- [ ] Compare speed with/without cache

**Mini Quest:**
```python
# Generate 50 tokens
# Time it without cache
# Time it with cache
# Report speedup
```

---

### 🎯 BOSS BATTLE 3C: Inference Optimizer
**Challenge:** Maximize generation speed

**Requirements:**
- [ ] Implement all 3: greedy, beam, top-p
- [ ] Add KV caching
- [ ] Batch inference (multiple prompts)
- [ ] Benchmark tokens/second
- [ ] Compare quality vs speed

**XP:** 400

---

### 🏆 ACHIEVEMENT: "Attention Grandmaster"
- Complete all 3 boss battles
- Code transformer from scratch (no copy-paste)
- **Bonus XP:** 500  
- **Unlocks:** LLM Endgame

---

## 🏰 LEVEL 4: LLM ENDGAME

**Objective:** Build and train your own language model  
**XP Reward:** 4,000  
**Status:** 🔒 Locked (Complete Level 3)

### Checkpoint 4.1: Decoder-Only Architecture ✅
**Skills to Learn:**
- GPT-style causal transformer
- Remove encoder, keep decoder blocks
- Autoregressive LM objective

**Verify You Can:**
- [ ] Build GPT-like model (decoder-only)
- [ ] Verify causal masking works
- [ ] Explain why no encoder needed for LM

**Resources:**
- nanoGPT (Karpathy) - study the architecture

---

### Checkpoint 4.2: Data Pipeline ✅
**Skills to Learn:**
- Web scraping / dataset curation
- Deduplication
- Quality filtering
- Data mixing ratios

**Verify You Can:**
- [ ] Download OpenWebText or C4 sample
- [ ] Remove near-duplicates (MinHash)
- [ ] Filter by quality metrics
- [ ] Tokenize with BPE

**Side Quest:** ⭐ Build custom dataset (Reddit threads, Wikipedia, books)

---

### Checkpoint 4.3: Pretraining Setup ✅
**Skills to Learn:**
- Next-token prediction loss
- Batch construction for LM
- Learning rate schedules (cosine decay)
- Checkpointing

**Verify You Can:**
- [ ] Create DataLoader for pretraining
- [ ] Implement cosine LR schedule with warmup
- [ ] Save/load checkpoints with optimizer state
- [ ] Resume training from checkpoint

---

### 🎯 BOSS BATTLE 4A: TinyLM from Scratch
**Challenge:** Pretrain a small GPT on limited data

**Requirements:**
- [ ] Model: 6 layers, 384 dim, 6 heads (~30M params)
- [ ] Dataset: 10M tokens (tiny-stories, openwebtext subset)
- [ ] Train until loss <3.0
- [ ] Generate coherent 100-token samples
- [ ] Track perplexity

**Hardware:** 1 GPU or Colab free tier  
**XP:** 800  
**Difficulty:** ⭐⭐⭐⭐

---

### Checkpoint 4.4: Scaling Laws ✅
**Skills to Learn:**
- Compute-optimal training (Chinchilla)
- Model size vs dataset size trade-off
- Power law scaling

**Verify You Can:**
- [ ] Read Chinchilla paper (focus on key results)
- [ ] Explain "overtrained" vs "undertrained"
- [ ] Estimate compute for your model

**Resources:**
- Scaling Laws paper (Kaplan et al.)
- Chinchilla paper (Hoffmann et al.)

---

### Checkpoint 4.5: Distributed Training Basics ✅
**Skills to Learn:**
- Data parallelism (DDP)
- Tensor parallelism concept
- Pipeline parallelism concept
- Gradient checkpointing

**Verify You Can:**
- [ ] Wrap model in DDP
- [ ] Train on 2+ GPUs (or simulate)
- [ ] Explain when to use each parallelism type

**Resources:**
- PyTorch DDP tutorial
- Megatron-LM paper (for advanced)

---

### 🎯 BOSS BATTLE 4B: Multi-GPU Training
**Challenge:** Train model on 2+ GPUs with DDP

**Requirements:**
- [ ] Same TinyLM architecture
- [ ] Use DistributedDataParallel
- [ ] Achieve 1.5x+ speedup
- [ ] Verify identical results to single GPU

**XP:** 400  
**Difficulty:** ⭐⭐⭐

---

### Checkpoint 4.6: Instruction Tuning ✅
**Skills to Learn:**
- SFT (Supervised Fine-Tuning)
- Instruction dataset format
- Few-shot prompting
- Evaluation metrics (helpfulness, accuracy)

**Verify You Can:**
- [ ] Format data as (instruction, response) pairs
- [ ] Fine-tune pretrained model
- [ ] Evaluate on held-out instructions
- [ ] Compare pre/post tuning samples

**Dataset:** Dolly, Alpaca, or OpenAssistant subset

---

### 🎯 BOSS BATTLE 4C: Instruction Tuned Assistant
**Challenge:** Create helpful chatbot from your pretrained LM

**Requirements:**
- [ ] Fine-tune TinyLM on instruction data
- [ ] Evaluate on 20+ diverse prompts
- [ ] Show improvement over base model
- [ ] Implement chat interface (CLI or Gradio)

**XP:** 600  
**Difficulty:** ⭐⭐⭐⭐

---

### Checkpoint 4.7: Alignment Concepts ✅
**Skills to Learn:**
- RLHF overview (reward model + PPO)
- DPO (Direct Preference Optimization)
- Human feedback collection

**Verify You Can:**
- [ ] Explain RLHF pipeline (3 stages)
- [ ] Describe DPO vs RLHF trade-offs
- [ ] Read DPO paper (high-level understanding)

**Resources:**
- InstructGPT paper
- DPO paper

**Side Quest:** ⭐ Implement DPO on tiny preference dataset

---

### Checkpoint 4.8: Evaluation ✅
**Skills to Learn:**
- Perplexity
- MMLU, HellaSwag, TruthfulQA
- Human eval vs automatic metrics

**Verify You Can:**
- [ ] Compute perplexity on test set
- [ ] Run model on public benchmarks (lm-eval-harness)
- [ ] Interpret scores

**Resources:**
- EleutherAI lm-evaluation-harness

---

### 🎯 FINAL BOSS: Full LLM Pipeline
**Challenge:** Complete end-to-end LLM project

**Requirements:**
- [ ] **Pretrain:** 50M+ param model on 100M+ tokens
- [ ] **Evaluate:** Report perplexity + 2 benchmarks
- [ ] **Instruction Tune:** SFT on curated dataset
- [ ] **Deploy:** Inference API (FastAPI or Gradio)
- [ ] **Document:** Write README with results

**XP:** 1,200  
**Difficulty:** ⭐⭐⭐⭐⭐ LEGENDARY

---

### 🏆 FINAL ACHIEVEMENT: "LLM Architect"
**Requirements:**
- Complete Final Boss
- Code everything from scratch (no HuggingFace Trainer)
- Share project on GitHub
- **Reward:** QUEST COMPLETE 🎉

---

## 📊 XP Tracker

| Level | Name | XP | Status |
|-------|------|-----|--------|
| 0 | Foundations | 500 | 🔓 |
| 1 | LSTM Realm | 1,500 | 🔒 |
| 2 | RNN Valley | 1,200 | 🔒 |
| 3 | Transformer Empire | 2,500 | 🔒 |
| 4 | LLM Endgame | 4,000 | 🔒 |
| **TOTAL** | | **10,000** | |

---

## 🎯 Side Quest Catalog

**Optional Deep Dives:**
1. ⭐ Build Attention Visualizer (heatmaps for any model)
2. ⭐⭐ Implement Mixture of Experts (MoE) layer
3. ⭐⭐ Reproduce GPT-2 124M from scratch
4. ⭐⭐⭐ Add Flash Attention optimization
5. ⭐⭐⭐ Implement retrieval-augmented generation (RAG)

---

## 🛠️ Recommended Tools

**Essential:**
- PyTorch 2.0+
- Weights & Biases (experiment tracking)
- Jupyter notebooks
- VS Code + Python

**Advanced:**
- HuggingFace transformers (reference, not training)
- tiktoken (tokenization)
- lm-evaluation-harness
- vLLM (inference optimization)

---

## 📚 Boss Battle Datasets Quick Links

**Level 1:**
- [tiny-shakespeare.txt](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt)
- [Air Quality UCI](https://archive.ics.uci.edu/ml/datasets/Air+Quality)

**Level 3:**
- [Multi30k](https://github.com/multi30k/dataset)
- [IWSLT14](https://wit3.fbk.eu/2014-01)

**Level 4:**
- [TinyStories](https://huggingface.co/datasets/roneneldan/TinyStories)
- [OpenWebText](https://huggingface.co/datasets/Skylion007/openwebtext)
- [Dolly 15k](https://huggingface.co/datasets/databricks/databricks-dolly-15k)

---

## 🎮 How to Play

1. **Start at Level 0** - even if you think you know basics (refresh is good)
2. **Check each [ ] box** as you complete it (use GitHub or local markdown)
3. **Don't skip checkpoints** - they build on each other
4. **Boss battles are mandatory** - these prove mastery
5. **Side quests are optional** - do if curious or want bonus XP
6. **Go at your own pace** - this is your journey
7. **Share victories** - post GitHub repos, blog your wins

---

## 🏁 Victory Conditions

**You've mastered deep learning when you can:**
- [ ] Explain any architecture to a non-expert
- [ ] Debug training failures (vanishing grads, overfitting, etc.)
- [ ] Implement papers from scratch in <2 days
- [ ] Train models that actually work on real tasks
- [ ] Know when to use which architecture

**Now go build something amazing! 🚀**