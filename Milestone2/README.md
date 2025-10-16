# TEXTMORPH – Advanced Text Summarization & Paraphrasing

---

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
- **Dataset Testing:** 10 sample texts  
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
1. **BART** generates context-rich but longer outputs.  
2. **Phi-2** and **TinyLlama** are lightweight and efficient with decent accuracy.  
3. **TextRank** performs well for extractive summarization but lacks abstract understanding.  
4. **Paraphrases** achieve higher similarity than summaries.  
5. **Visual comparisons** show model trade-offs between length, readability, and semantic retention.

---

| Metric | Description |
|---------|-------------|
| **Word Count** | How much shorter the
