# Generative-AI-with-large-languge-models-LLMs----Curated-notes
This repository have the notes that I have made while doing the course of GAI with LLM by deeplearning.ai

--


| Metric  | ROUGE (Recall-Oriented Understudy for Gisting Evaluation) | BLEU (Bilingual Evaluation Understudy) |
|---------|----------------------------------------------------------|--------------------------------------|
| Type    | Recall-based metric                                      | Precision and recall-based metric   |
| Purpose | Measures the quality of summaries or machine-generated text by comparing overlap of n-grams (usually unigrams, bigrams, and trigrams) between the generated text and reference (human-written) text. | Measures the quality of machine-generated translations by comparing n-grams in the generated translation with reference translations. |
| Components | ROUGE-N: Measures n-gram overlap (unigrams, bigrams, trigrams, etc.). ROUGE-L: Longest Common Subsequence (LCS) based. ROUGE-W: Weighted ROUGE, giving more importance to longer n-grams. | BLEU-1: Unigram precision. BLEU-2: Bigram precision. BLEU-3: Trigram precision. BLEU-4: Cumulative 4-gram precision. Also computes a brevity penalty to account for shorter translations. |
| Calculation | ROUGE calculates recall by dividing the count of overlapping n-grams in the generated text and reference text by the total count of n-grams in the reference text. | BLEU calculates precision for each n-gram order and then combines them using a geometric mean. It also includes a brevity penalty to adjust for shorter translations. |
| Range   | ROUGE scores range from 0 to 1, with 1 indicating perfect overlap between generated and reference text. | BLEU scores also range from 0 to 1, with 1 indicating perfect match with reference translations. Higher scores are generally better. |
| Limitations | ROUGE doesn't penalize for additional words in the generated text that are not present in the reference text, potentially leading to overly verbose summaries. | BLEU may favor shorter translations due to its brevity penalty, which could be problematic for languages with different syntactic structures. |
| Widely Used | Commonly used for evaluating text summarization tasks. | Widely used for evaluating machine translation tasks. |
| Domain Dependence | Can be domain-specific. | Can be domain-specific. |
