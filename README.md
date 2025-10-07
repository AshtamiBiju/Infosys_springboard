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

### Summarization
| Model | Type | Description |
|--------|------|-------------|
| **T5** | Abstractive | Converts any NLP task into text-to-text form; concise but may lose context. |
| **BART** | Abstractive | Produces fluent, context-rich summaries. |
| **PEGASUS** | Abstractive | Designed specifically for summarization tasks with superior coherence. |

### Paraphrasing
| Model | Description |
|--------|-------------|
| **PEGASUS Paraphrase** | Creates grammatically rich, diverse paraphrases. |
| **T5 Paraphrase** | Generates meaning-preserving paraphrases. |
| **BART Paraphrase** | Produces smooth, natural-sounding rewordings. |

### Similarity
| Model | Description |
|--------|-------------|
| **Sentence-BERT** | Generates embeddings to calculate semantic similarity between texts. |

---

## Methodology

### 1. **Text Loading**
Two long texts are taken from **Project Gutenberg**, cleaned up, and shortened to a workable size.  
We check that each text is long enough for proper testing.

### 2. **Summarization**
Each model creates a summary of the same text.  
We then compare the summaries based on how long they are, how well they capture the main ideas, and how close they stay to the original meaning.

### 3. **Paraphrasing**
Different models rewrite selected sentences in new ways while keeping the same meaning.  
We look at how creative, natural, and accurate these rewrites are.

### 4. **Similarity Analysis**
Using **Sentence-BERT**, we calculate **cosine similarity** to measure how similar each summary or paraphrase is to the original text.

### 5. **Visualization**
With **Seaborn** and **Matplotlib**, we create graphs that show:
- How summary length relates to similarity  
- How paraphrase length relates to similarity  
- Common words and phrase patterns in the texts  

---

## Observations
1. **PEGASUS** gives short, clean, and well-focused summaries.  
2. **BART** adds more detail but can get wordy.  
3. **T5** makes very short summaries and sometimes misses small details.  
4. For paraphrasing, **T5 Paraphrase** keeps the original meaning best.  
5. **Similarity scores** show that paraphrases stay closer in meaning to the original text than summaries do.  

---

## Evaluation Metrics
| Metric | What It Shows |
|---------|----------------|
| **Word Count** | How much shorter the summary is compared to the original. |
| **Cosine Similarity** | How close the meaning is to the original text. |
| **Inter-Model Similarity** | How similar the outputs of different models are to each other. |