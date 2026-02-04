# 🎮 Deep Learning Quest - Complete Reference Guide

This document provides curated resources (YouTube videos, blog posts, papers, tutorials) for every checkpoint in the Deep Learning Quest roadmap.

---

## 📚 LEVEL 0: FOUNDATIONS CAMP

### Checkpoint 0.1: Math Arsenal

**Vectors & Matrices:**
- 📺 [3Blue1Brown: Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) - Visual intuition for linear algebra
- 📄 [The Matrix Calculus You Need For Deep Learning](https://explained.ai/matrix-calculus/) - Comprehensive guide to matrix derivatives
- 📄 [What Is a Gradient in Machine Learning?](https://machinelearningmastery.com/gradient-in-machine-learning/) - Clear explanation of gradients

**Chain Rule & Derivatives:**
- 📺 [3Blue1Brown: Neural Networks Chapter 2 - Gradient Descent](https://www.3blue1brown.com/lessons/gradient-descent)
- 📄 [Computing Neural Network Gradients (Stanford)](https://web.stanford.edu/class/cs224n/readings/gradient-notes.pdf)
- 📄 [Sebastian Raschka: Backprop with Arbitrary Functions](https://sebastianraschka.com/faq/docs/backprop-arbitrary.html)

**Softmax & Cross-Entropy:**
- 📄 [CS231n: Backpropagation and Gradients](https://cs231n.stanford.edu/slides/2018/cs231n_2018_ds02.pdf)
- 📄 [Peter Roelants: Neural Network Implementation Part 1](https://peterroelants.github.io/posts/neural-network-implementation-part01/)

**Comprehensive Neural Network Math:**
- 📖 [Neural Networks and Deep Learning (Michael Nielsen)](http://neuralnetworksanddeeplearning.com/chap2.html) - Chapter 2 on backpropagation
- 📄 [Understanding Higher Order Gradient Computation](https://danieltakeshi.github.io/2017/01/21/understanding-higher-order-local-gradient-computation-for-backpropagation-in-deep-neural-networks/)
- 📄 [Medium: Explaining Neural Networks - Gradient Descent](https://medium.com/data-science-engineering/explaining-neural-network-as-simple-as-possible-gradient-descent-00b213cba5a9)

---

### Checkpoint 0.2: PyTorch Basics

**Tensors & Autograd:**
- 📄 [PyTorch Official: Autograd Tutorial](https://docs.pytorch.org/tutorials/beginner/blitz/autograd_tutorial.html)
- 📄 [PyTorch: Automatic Differentiation](https://docs.pytorch.org/tutorials/beginner/basics/autogradqs_tutorial.html)
- 📄 [PyTorch: Fundamentals of Autograd](https://docs.pytorch.org/tutorials/beginner/introyt/autogradyt_tutorial.html)
- 📄 [PyTorch: Autograd Mechanics](https://docs.pytorch.org/docs/stable/notes/autograd.html)

**PyTorch nn.Module:**
- 📄 [Learning PyTorch with Examples](https://docs.pytorch.org/tutorials/beginner/pytorch_with_examples.html)
- 📄 [PyTorch: Tensors and Autograd Example](https://docs.pytorch.org/tutorials/beginner/examples_autograd/polynomial_autograd.html)

**Comprehensive Guides:**
- 📄 [Medium: Understanding PyTorch AutoGrad - Complete Guide](https://medium.com/@piyushkashyap045/understanding-pytorch-autograd-a-complete-guide-for-deep-learning-practitioners-f5dd1f43b417)
- 📄 [Neuromatch Academy: Tutorial on Gradient Descent and AutoGrad](https://deeplearning.neuromatch.io/tutorials/W1D2_LinearDeepLearning/student/W1D2_Tutorial1.html)

**Advanced:**
- 📄 [PyTorch: Hooks for Autograd Saved Tensors](https://docs.pytorch.org/tutorials/intermediate/autograd_saved_tensors_hooks_tutorial.html)
- 📄 [PyTorch Automatic Differentiation Package Documentation](https://docs.pytorch.org/docs/stable/autograd.html)

---

### Boss Battle 0: MNIST Conqueror

**MNIST Tutorials:**
- 📺 [3Blue1Brown: But what is a neural network?](https://www.3blue1brown.com/topics/neural-networks)
- 📄 [PyTorch MNIST Tutorial](https://docs.pytorch.org/tutorials/beginner/basics/quickstart_tutorial.html)
- 📖 [Deep Learning Book Chapter 1-3](https://udlbook.github.io/udlbook/) - Understanding Deep Learning

---

## 📚 LEVEL 1: LSTM REALM

### Checkpoint 1.1: LSTM Theory

**Primary Resources:**
- 📄 [Understanding LSTM Networks (colah's blog)](https://colah.github.io/posts/2015-08-Understanding-LSTMs/) - **THE definitive LSTM explanation**
- 📺 [Stanford CS224n: LSTM and GRU](https://web.stanford.edu/class/cs224n/)
- 📄 [Medium: Introduction to LSTM](https://medium.com/analytics-vidhya/introduction-to-long-short-term-memory-lstm-a8052cd0d4cd)

**Supplementary:**
- 📄 [Medium: Guide to LSTMs for Beginners](https://medium.com/analytics-vidhya/guide-to-lstms-for-beginners-ac9d1fc86176)
- 📄 [IITK: Understanding LSTM Networks Slides](https://www.cse.iitk.ac.in/users/sigml/lec/Slides/LSTM.pdf)
- 📖 [Understanding Deep Learning Book Chapter 7](https://udlbook.github.io/udlbook/)

**Papers:**
- 📜 [Original LSTM Paper (Hochreiter & Schmidhuber, 1997)](http://www.bioinf.jku.at/publications/older/2604.pdf)

---

### Checkpoint 1.2: Sequence Data Handling

**Tutorials:**
- 📄 [PyTorch: Sequence Models and LSTM](https://pytorch.org/tutorials/beginner/nlp/sequence_models_tutorial.html)
- 📄 [Practical PyTorch: Classifying Names with RNN](https://github.com/spro/practical-pytorch)

**Teacher Forcing:**
- 📄 [Machine Learning Mastery: Teacher Forcing for RNNs](https://machinelearningmastery.com/teacher-forcing-for-recurrent-neural-networks/)

---

### Checkpoint 1.3: PyTorch LSTM

**Official Documentation:**
- 📄 [PyTorch nn.LSTM Documentation](https://pytorch.org/docs/stable/generated/torch.nn.LSTM.html)
- 📄 [PyTorch LSTM Tutorial](https://pytorch.org/tutorials/beginner/nlp/sequence_models_tutorial.html)

**Practical Examples:**
- 📄 [PyTorch Forums: LSTM Discussions](https://discuss.pytorch.org/c/nlp/6)

---

### Boss Battle 1A: Character-Level Text Generator

**Primary Resource:**
- 📄 [The Unreasonable Effectiveness of Recurrent Neural Networks (Karpathy)](https://karpathy.github.io/2015/05/21/rnn-effectiveness/) - **MUST READ**
- 💻 [karpathy/char-rnn GitHub](https://github.com/karpathy/char-rnn)

**Implementations:**
- 📄 [PyTorch Forums: Char-RNN Discussions](https://discuss.pytorch.org/t/char-rnn-it-trains-but-doesnt-sample/192651)
- 📄 [Minimal Char RNN in PyTorch](https://discuss.pytorch.org/t/minimal-char-rnn-in-pytorch/38019)

**Additional Reading:**
- 📄 [Revisiting Karpathy's Unreasonable Effectiveness](https://www.gilesthomas.com/2025/10/revisiting-karpathy-unreasonable-effectiveness-rnns)
- 📄 [Medium: Unreasonable Effectiveness Explained](https://medium.com/@nitishj_57176/unreasonable-effectiveness-of-recurrent-neural-networks-f5b64fdb097e)

**Dataset:**
- 📂 [tiny-shakespeare.txt](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt)

---

### Boss Battle 1B: Time Series Prophet

**Resources:**
- 📄 [Machine Learning Mastery: Time Series with LSTM](https://machinelearningmastery.com/time-series-prediction-lstm-recurrent-neural-networks-python-keras/)
- 📄 [PyTorch Time Series Tutorial](https://pytorch.org/tutorials/beginner/timeseries_tutorial.html)

**Datasets:**
- 📂 [Air Quality UCI Dataset](https://archive.ics.uci.edu/ml/datasets/Air+Quality)

---

## 📚 LEVEL 2: RNN VALLEY

### Checkpoint 2.1: Vanilla RNN

**Blog Posts:**
- 📄 [Karpathy: Unreasonable Effectiveness of RNNs](https://karpathy.github.io/2015/05/21/rnn-effectiveness/)
- 📄 [Understanding RNNs (Stanford)](https://web.stanford.edu/class/cs224n/)

**Theory:**
- 📺 [MIT 6.S191: RNNs](https://www.youtube.com/live/alfdI7S6wCY)
- 📖 [Deep Learning Book Chapter on RNNs](https://www.deeplearningbook.org/)

---

### Checkpoint 2.2: Backpropagation Through Time

**Resources:**
- 📄 [CS231n: RNN Lecture Notes](https://cs231n.github.io/rnn/)
- 📺 [Stanford CS231n: RNN Video Lecture](https://www.youtube.com/watch?v=6niqTuYFZLQ)

**Gradient Problems:**
- 📄 [Understanding Vanishing Gradient Problem](https://towardsdatascience.com/the-vanishing-gradient-problem-69bf08b15484)

---

### Checkpoint 2.3: GRU

**Resources:**
- 📄 [Illustrated Guide to LSTM and GRU](https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21)
- 📄 [colah's blog section on GRU](https://colah.github.io/posts/2015-08-Understanding-LSTMs/)

---

## 📚 LEVEL 3: TRANSFORMER EMPIRE

### Checkpoint 3.1: Attention Fundamentals

**Visual Guides:**
- 📄 [The Illustrated Transformer (Jay Alammar)](https://jalammar.github.io/illustrated-transformer/) - **ESSENTIAL**
- 📄 [Attention? Attention! (Lilian Weng)](https://lilianweng.github.io/posts/2018-06-24-attention/)

**Video Tutorials:**
- 📺 [StatQuest: Attention for Neural Networks](https://www.youtube.com/watch?v=PSs6nxngL6k)
- 📺 [Stanford CS224n: Attention Mechanisms](https://web.stanford.edu/class/cs224n/)

---

### Checkpoint 3.2-3.6: Building Transformers

**Comprehensive Guide:**
- 📄 [The Annotated Transformer (Harvard NLP)](https://nlp.seas.harvard.edu/annotated-transformer/) - **Implementation walkthrough**
- 📺 [Andrej Karpathy: Let's build GPT from scratch](https://www.youtube.com/watch?v=kCc8FmEb1nY)

**Papers:**
- 📜 [Attention Is All You Need (Vaswani et al., 2017)](https://arxiv.org/abs/1706.03762) - **THE transformer paper**

---

### Checkpoint 3.7: Tokenization

**Resources:**
- 📄 [HuggingFace Tokenizers Tutorial](https://huggingface.co/docs/tokenizers/)
- 📄 [Let's build the GPT Tokenizer (Karpathy)](https://www.youtube.com/watch?v=zduSFxRajkE)

**BPE Explained:**
- 📄 [Neural Machine Translation of Rare Words with Subword Units](https://arxiv.org/abs/1508.07909)

---

### Boss Battle 3B: Machine Translation

**Datasets:**
- 📂 [IWSLT14 Dataset](https://wit3.fbk.eu/2014-01)
- 📂 [Multi30k Dataset](https://github.com/multi30k/dataset)

**Tutorials:**
- 📄 [PyTorch Seq2Seq Tutorial](https://pytorch.org/tutorials/intermediate/seq2seq_translation_tutorial.html)

---

### Checkpoint 3.9: Inference Techniques

**KV Caching:**
- 📄 [Transformer Inference Optimization](https://lilianweng.github.io/posts/2023-01-10-inference-optimization/)

**Beam Search:**
- 📄 [HuggingFace: How to Generate Text](https://huggingface.co/blog/how-to-generate)

---

## 📚 LEVEL 4: LLM ENDGAME

### Checkpoint 4.1: Decoder-Only Architecture

**Resources:**
- 💻 [nanoGPT (Karpathy)](https://github.com/karpathy/nanoGPT) - **Clean GPT implementation**
- 📺 [Let's build GPT from scratch (Karpathy)](https://www.youtube.com/watch?v=kCc8FmEb1nY)

---

### Checkpoint 4.2: Data Pipeline

**Resources:**
- 📄 [The RefinedWeb Dataset](https://arxiv.org/abs/2306.01116)
- 📄 [Data Curation for LLMs](https://lilianweng.github.io/posts/2023-03-15-prompt-engineering/)

**Deduplication:**
- 📜 [Deduplicating Training Data (Google)](https://arxiv.org/abs/2107.06499)

---

### Boss Battle 4A: TinyLM from Scratch

**Implementation Guides:**
- 💻 [nanoGPT](https://github.com/karpathy/nanoGPT)
- 📺 [Karpathy: Build GPT from Scratch](https://www.youtube.com/watch?v=kCc8FmEb1nY)

**Datasets:**
- 📂 [TinyStories Dataset](https://huggingface.co/datasets/roneneldan/TinyStories)
- 📂 [OpenWebText](https://huggingface.co/datasets/Skylion007/openwebtext)

---

### Checkpoint 4.4: Scaling Laws

**Papers:**
- 📜 [Scaling Laws for Neural Language Models (Kaplan et al.)](https://arxiv.org/abs/2001.08361)
- 📜 [Training Compute-Optimal LLMs (Chinchilla)](https://arxiv.org/abs/2203.15556)

---

### Checkpoint 4.5: Distributed Training

**PyTorch DDP:**
- 📄 [PyTorch Distributed Tutorial](https://pytorch.org/tutorials/intermediate/ddp_tutorial.html)
- 📄 [Getting Started with DDP](https://pytorch.org/tutorials/beginner/ddp_series_intro.html)

**Advanced:**
- 📜 [Megatron-LM Paper](https://arxiv.org/abs/1909.08053)

---

### Checkpoint 4.6: Instruction Tuning

**Datasets:**
- 📂 [Dolly 15k](https://huggingface.co/datasets/databricks/databricks-dolly-15k)
- 📂 [Alpaca](https://github.com/tatsu-lab/stanford_alpaca)
- 📂 [OpenAssistant](https://huggingface.co/datasets/OpenAssistant/oasst1)

**Papers:**
- 📜 [FLAN: Finetuned Language Models are Zero-Shot Learners](https://arxiv.org/abs/2109.01652)

---

### Checkpoint 4.7: Alignment

**RLHF:**
- 📜 [InstructGPT Paper](https://arxiv.org/abs/2203.02155)
- 📄 [Illustrating RLHF (HuggingFace)](https://huggingface.co/blog/rlhf)

**DPO:**
- 📜 [Direct Preference Optimization](https://arxiv.org/abs/2305.18290)

---

### Checkpoint 4.8: Evaluation

**Tools:**
- 💻 [lm-evaluation-harness (EleutherAI)](https://github.com/EleutherAI/lm-evaluation-harness)

**Benchmarks:**
- 📄 [MMLU Paper](https://arxiv.org/abs/2009.03300)
- 📄 [HellaSwag Paper](https://arxiv.org/abs/1905.07830)

---

## 📜 ESSENTIAL PAPERS BY LEVEL

### Level 1-2: RNNs & LSTMs
- Long Short-Term Memory (Hochreiter & Schmidhuber, 1997)
- Learning Phrase Representations using RNN Encoder-Decoder (Cho et al., 2014)

### Level 3: Transformers
- **Attention Is All You Need (Vaswani et al., 2017)** - Must read
- BERT: Pre-training of Deep Bidirectional Transformers (Devlin et al., 2018)

### Level 4: LLMs
- **GPT-3: Language Models are Few-Shot Learners** (Brown et al., 2020)
- **LLaMA: Open and Efficient Foundation LMs** (Touvron et al., 2023)
- **Scaling Laws for Neural Language Models** (Kaplan et al., 2020)
- **Training Compute-Optimal LLMs (Chinchilla)** (Hoffmann et al., 2022)
- InstructGPT (Ouyang et al., 2022)
- Direct Preference Optimization (Rafailov et al., 2023)

---

## 🎥 YOUTUBE CHANNELS TO FOLLOW

- **3Blue1Brown** - Visual math intuitions
- **Andrej Karpathy** - Implementation-focused deep learning
- **StatQuest with Josh Starmer** - Clear explanations
- **Stanford Online (CS224n, CS231n)** - Full courses
- **MIT OpenCourseWare (6.S191)** - Intro to DL course
- **Yannic Kilcher** - Paper reviews

---

## 📖 BOOKS

1. **Understanding Deep Learning** by Simon J.D. Prince - https://udlbook.github.io/udlbook/
2. **Neural Networks and Deep Learning** by Michael Nielsen - http://neuralnetworksanddeeplearning.com/
3. **Deep Learning** by Goodfellow, Bengio, Courville - https://www.deeplearningbook.org/
4. **Dive into Deep Learning** - https://d2l.ai/

---

## 💻 CODE REPOSITORIES

- [karpathy/nanoGPT](https://github.com/karpathy/nanoGPT) - Minimal GPT
- [karpathy/char-rnn](https://github.com/karpathy/char-rnn) - Character RNN
- [pytorch/examples](https://github.com/pytorch/examples) - Official PyTorch examples
- [huggingface/transformers](https://github.com/huggingface/transformers) - Reference (not for training from scratch)

---

## 🌐 COURSE WEBSITES

- [Stanford CS224n: NLP with Deep Learning](https://web.stanford.edu/class/cs224n/)
- [Stanford CS231n: CNNs for Visual Recognition](https://cs231n.stanford.edu/)
- [MIT 6.S191: Intro to Deep Learning](http://introtodeeplearning.com/)
- [Fast.ai](https://www.fast.ai/) - Practical deep learning

---

## 🔧 TOOLS & LIBRARIES

**Essential:**
- PyTorch 2.0+ - https://pytorch.org/
- Weights & Biases - https://wandb.ai/
- Jupyter - https://jupyter.org/

**Advanced:**
- tiktoken (tokenization) - https://github.com/openai/tiktoken
- lm-evaluation-harness - https://github.com/EleutherAI/lm-evaluation-harness
- vLLM (inference) - https://github.com/vllm-project/vllm

---

**Last Updated:** February 2026
**Maintained for:** Deep Learning Quest Roadmap