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

## Milestone 1
Here’s what we’ve done so far:  
- Loaded and cleaned text from external sources.  
- Built summarization pipelines using **T5, BART, and PEGASUS**.  
- Built paraphrasing pipelines using **T5, BART, and PEGASUS**.  
- Added **reference texts** for similarity checks.  
- Visualized text data: word frequencies, bigrams, and summary metrics.  

---

## Changes i made for Milestone 1
- Updated the text URLs to **new public text files** for variety.  
- Added **print statements** to confirm text loaded and character counts.  
- Improved **readability** with inline comments.  
- Added **error handling** (warnings).

---

## My Observations
- For Summarization Bart did the best job. It was the most similar to original in both.
- For Paraphrasing Pegasus and also bart did a great job
- Overall i would say T5 was lacking behind
