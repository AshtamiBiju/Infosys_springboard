# TEXTMORPH – Advanced Text Summarization & Paraphrasing

## About the Project
**TEXTMORPH** is a Python-based tool that makes reading, understanding, and rewriting text easier. It can take long articles or passages and turn them into short summaries, and it can also rephrase sentences so they sound clearer or match a different tone — all while keeping the meaning intact.  

---

## What It Does
- **Summarize**: Condenses long texts into concise, meaningful summaries.  
- **Paraphrase**: Rewrites sentences to improve clarity, flow, or style.  
- **Compare**: Checks similarity between original and processed text to make sure nothing important is lost.  

Used pre-trained models like T5,PEGASUS,BART from Hugging Face  

---

## Models Used

### 🔹 Summarization
| Model | Type | Description |
|--------|------|-------------|
| **T5** | Abstractive | Converts any NLP task into text-to-text form; concise but may lose context. |
| **BART** | Abstractive | Produces fluent, context-rich summaries. |
| **PEGASUS** | Abstractive | Designed specifically for summarization tasks with superior coherence. |

### 🔹 Paraphrasing
| Model | Description |
|--------|-------------|
| **PEGASUS Paraphrase (tuner007)** | Creates grammatically rich, diverse paraphrases. |
| **T5 Paraphrase (Vamsi/T5_Paraphrase_Paws)** | Generates meaning-preserving paraphrases. |
| **BART Paraphrase (eugenesiow)** | Produces smooth, natural-sounding rewordings. |

### 🔹 Similarity
| Model | Description |
|--------|-------------|
| **all-MiniLM-L6-v2** | Generates embeddings to calculate semantic similarity between texts. |

---

## Methodology

### 1. **Text Loading**
Two large texts are fetched from **Project Gutenberg**, cleaned, and truncated.  
Validation ensures each text is long enough for meaningful summarization.

### 2. **Summarization**
Each model generates a summary for the same text.  
The summaries are then compared based on length, quality, and semantic similarity to the original.

### 3. **Paraphrasing**
Each paraphrasing model rewrites selected sentences into new forms while preserving meaning.  
Results are analyzed for linguistic variation and similarity.

### 4. **Similarity Analysis**
Cosine similarity is computed using **Sentence-BERT** to assess how close each summary or paraphrase is to the source text.

### 5. **Visualization**
Using **Seaborn** and **Matplotlib**, the notebook visualizes:
- Summary length vs. similarity  
- Paraphrase length vs. similarity  
- Word frequency and bigram patterns across texts  

---

## Observations
1. **PEGASUS** consistently produces focused, coherent summaries.  
2. **BART** gives more detailed summaries but may be using words than necessary.  
3. **T5** tends to compress heavily, sometimes skipping subtle context.  
4. For paraphrasing, **T5 Paraphrase** maintains meaning most faithfully.  
5. **Similarity scores** show paraphrased texts retain higher semantic closeness than summaries.  
6. Bigram visualizations reveal writing style and recurring topic patterns within the texts.

---

## Evaluation Metrics
| Metric | Description |
|---------|-------------|
| **Word Count** | Measures compression ratio. |
| **Cosine Similarity** | Evaluates semantic closeness between model outputs and the original text. |
| **Inter-Model Similarity** | Compares stylistic overlap between models. |

