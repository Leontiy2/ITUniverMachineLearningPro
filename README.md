# ITUniverMachineLearningPro

30.05.2026


```markdown
# NLP Evaluation Metrics Notebook

This notebook demonstrates the calculation of three common Natural Language Processing (NLP) evaluation metrics: BLEU, ROUGE, and Perplexity. These metrics are crucial for assessing the quality of machine-generated text, such as in machine translation, summarization, or language modeling.

## Table of Contents

1.  [BLEU (Bilingual Evaluation Understudy)](#bleu)
2.  [ROUGE (Recall-Oriented Understudy for Gisting Evaluation)](#rouge)
3.  [Perplexity](#perplexity)

## 1. BLEU (Bilingual Evaluation Understudy)

**Purpose**: BLEU is primarily used to evaluate the quality of machine-translated text against human-translated references. It measures the precision of n-grams (sequences of words) in the candidate text compared to the reference text.

**How it works**: The BLEU score ranges from 0 to 1 (or 0 to 100). Higher scores indicate better quality translations that are closer to human reference translations. It considers precision for unigrams, bigrams, trigrams, and quadrigrams, and includes a brevity penalty to penalize overly short translations.

**Usage in Notebook**: 
- Installs `nltk` library.
- Downloads necessary NLTK data (`punkt`).
- Demonstrates `sentence_bleu` from `nltk.translate.bleu_score` to compare a candidate sentence against a reference, using a smoothing function to handle zero-count n-grams.

## 2. ROUGE (Recall-Oriented Understudy for Gisting Evaluation)

**Purpose**: ROUGE is widely used for evaluating automatic summarization and machine translation tasks. Unlike BLEU, which focuses on precision, ROUGE emphasizes recall, measuring how many n-grams from the reference text appear in the candidate text.

**How it works**: This notebook demonstrates ROUGE-1 (unigram overlap), ROUGE-2 (bigram overlap), and ROUGE-L (Longest Common Subsequence). For each, it calculates precision, recall, and f-measure.

**Usage in Notebook**: 
- Installs `rouge_score` library.
- Demonstrates `rouge_scorer` to evaluate multiple candidate texts against a single reference. It prints precision, recall, and f-measure for ROUGE-1, ROUGE-2, and ROUGE-L.

## 3. Perplexity

**Purpose**: Perplexity is a metric used to evaluate language models. It quantifies how well a probability distribution or language model predicts a sample. A lower perplexity score indicates a better language model.

**How it works**: Perplexity essentially measures the

```markdown
'surprise'  of the model when encountering a given text. If a model perfectly predicts the next word every time, its perplexity would be 1.

**Usage in Notebook**: 
- Installs `transformers` and `torch` libraries.
- Loads a pre-trained `gpt2` model and tokenizer from the Hugging Face Transformers library.
- Defines a `calculate_perplaxity` function that tokenizes input text, feeds it to the GPT-2 model, computes the loss, and then calculates perplexity as the exponent of the loss.
- Demonstrates the function with several examples, showing how perplexity changes for grammatically correct, strange, and nonsensical sentences.

## How to Use This Notebook

1.  **Run all cells**: Execute each cell sequentially from top to bottom.
2.  **Examine outputs**: Observe the BLEU, ROUGE, and Perplexity scores for the provided examples.
3.  **Modify examples**: Feel free to change the `reference` and `candidate` texts in the BLEU and ROUGE sections, or the input texts for the Perplexity calculation, to experiment with different scenarios and understand how the metrics respond.
```
