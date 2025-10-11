# TEXTMORPH – Advanced Text Summarization & Paraphrasing

---

## Milestone 1 – Project Foundation

### About the Project
TEXTMORPH is a Python-based tool that makes reading, understanding, and rewriting text easier.  
It can take long articles or passages and turn them into short summaries, and it can also rephrase sentences so they sound clearer or match a different tone — all while keeping the meaning intact.

---

### What It Does
- **Summarize:** Condenses long texts into concise, meaningful summaries.  
- **Paraphrase:** Rewrites sentences to improve clarity, flow, or style.  
- **Compare:** Checks similarity between original and processed text to ensure no information is lost.

Pre-trained models like **T5**, **PEGASUS**, and **BART** from Hugging Face were used to achieve this.

---

### Models Used

#### Summarization
| Model | Type | Description |
|--------|------|-------------|
| **T5** | Abstractive | Converts any NLP task into text-to-text form; concise but may lose context. |
| **BART** | Abstractive | Produces fluent, context-rich summaries. |
| **PEGASUS** | Abstractive | Designed specifically for summarization tasks with superior coherence. |

#### Paraphrasing
| Model | Description |
|--------|-------------|
| **PEGASUS Paraphrase** | Creates grammatically rich, diverse paraphrases. |
| **T5 Paraphrase** | Generates meaning-preserving paraphrases. |
| **BART Paraphrase** | Produces smooth, natural-sounding rewordings. |

#### Similarity
| Model | Description |
|--------|-------------|
| **Sentence-BERT** | Generates embeddings to calculate semantic similarity between texts. |

---

### Methodology

1. **Text Loading**  
   Two long texts were taken from **Project Gutenberg**, cleaned up, and shortened to a workable size.  
   Each text was verified for sufficient length to ensure quality summarization.

2. **Summarization**  
   Each model created summaries of the same text.  
   The outputs were compared based on summary length, key idea retention, and semantic closeness.

3. **Paraphrasing**  
   Sentences were rephrased by different models, focusing on fluency, accuracy, and creativity.

4. **Similarity Analysis**  
   Used **Sentence-BERT** embeddings to calculate cosine similarity between outputs and originals.

5. **Visualization**  
   Graphs (via Seaborn + Matplotlib) showed how:
   - Summary length relates to similarity  
   - Paraphrase length affects meaning retention  
   - Common words and phrases were distributed  

---

### Observations
1. **PEGASUS** gives short, clean, and focused summaries.  
2. **BART** adds more context but is verbose.  
3. **T5** makes short summaries, occasionally missing fine details.  
4. **T5 Paraphrase** retains meaning best during rewording.  
5. **Paraphrases** tend to stay semantically closer to the original than summaries.  

---

### Evaluation Metrics
| Metric | What It Shows |
|---------|----------------|
| **Word Count** | Compression achieved in summarization. |
| **Cosine Similarity** | Semantic preservation across transformations. |
| **Inter-Model Similarity** | Agreement across models. |

---

## Milestone 2 – Implementation & Advanced Evaluation

### Overview
This milestone expands TEXTMORPH into a complete multi-model NLP system with powerful evaluation and dataset integration.  
It implements advanced abstractive and extractive summarization, along with performance metrics and model comparison.

---

### Features
- **Abstractive Summarization Models:** TinyLlama, Phi, BART-Large-CNN, Gemma  
- **Extractive Summarization:** TextRank (sentence embeddings)  
- **Metrics:** ROUGE-1, ROUGE-2, Semantic Similarity, Readability, Compression  
- **Interactive UI:**  
  - Summarize with All Models  
  - Summarize with Specific Models (checkbox UI)  
- **Dataset Testing:** 10+ sample texts + support for external `.txt`/`.csv` files  
- **GPU Enabled:** Optimized for Google Colab GPU  

---

### Models in Milestone 2

| Type | Models Used |
|------|--------------|
| **Abstractive Summarization** | TinyLlama, Phi-2, BART-Large-CNN, Gemma-2B |
| **Extractive Summarization** | TextRank (Embeddings-based) |
| **Similarity Measurement** | Sentence-BERT |

---

### Evaluation Metrics
| Metric | Description |
|---------|-------------|
| **ROUGE-1 / ROUGE-2** | Overlap between original and generated text. |
| **Cosine Similarity** | Semantic closeness using embeddings. |
| **Compression Ratio** | Degree of text shortening. |
| **Readability (Flesch)** | How easy the text is to read. |
| **Inter-Model Similarity** | Consistency among different models’ outputs. |

---

### Observations & Insights
1. **Gemma** gives the most factual and balanced summaries.  
2. **BART** generates context-rich but longer outputs.  
3. **Phi-2** and **TinyLlama** are lightweight and efficient with decent accuracy.  
4. **TextRank** performs well for extractive summarization but lacks abstract understanding.  
5. **Paraphrases** achieve higher similarity than summaries.  
6. **Visual comparisons** show model trade-offs between length, readability, and semantic retention.  

| **Word Count** | How much shorter the summary is compared to the original. |
riginal. |
| **Cosine Similarity** | How close the meaning is to the original text. |
| **Inter-Model Similarity** | How similar the outputs of different models are to each other. |
