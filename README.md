# Generative-AI-with-large-languge-models-LLMs----Curated-notes
This repository have the notes that I have made while doing the course of GAI with LLM by deeplearning.ai
---
# Table of contents 
- [ROUGE VS BLEU](#rouge-vs-bleu)




# ROUGE VS BLEU 


**ROUGE** (Recall-Oriented Understudy for Gisting Evaluation) and BLEU (Bilingual Evaluation Understudy) are both metrics used to evaluate the quality of machine-generated text, such as summaries or translations, by comparing them to reference (human-written) text. These metrics provide a quantitative measure of how well the generated text captures the content and style of the reference text.

ROUGE is a family of metrics that focus on recall, which measures the ability of the generated text to cover the content present in the reference text. It calculates the overlap of n-grams (sequences of words) between the generated and reference text. The most common variants of ROUGE are ROUGE-N (n-gram overlap), ROUGE-L (Longest Common Subsequence), and ROUGE-W (weighted ROUGE).

**BLEU**, on the other hand, emphasizes precision and recall. It compares n-grams in the generated text to those in the reference text, aiming to measure how well the generated text matches the reference. BLEU computes precision for different n-gram orders (usually up to 4-grams) and combines them using a geometric mean. Additionally, BLEU includes a brevity penalty to account for shorter translations.

Both ROUGE and BLEU have been widely used in natural language processing tasks:

ROUGE is often used in tasks like automatic text summarization, where the generated summary needs to capture the essence of a longer document. It's also used in other text generation tasks where maintaining content is crucial.

BLEU is commonly used for evaluating the quality of machine translation systems. It has been a standard metric for comparing the output of machine translation models against human translations.

While these metrics provide valuable insights into the quality of generated text, they do have limitations and might not capture all aspects of human judgment. Researchers and practitioners often use them in combination with other evaluation methods and conduct human evaluations to obtain a more comprehensive understanding of the quality of machine-generated text.

---

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

