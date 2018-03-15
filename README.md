### About

* Natural Language Processing Performance Metrics

* Average precision:
    * *Macro*: average of sentence scores
    * *Micro*: corpus (sums numerators and denominators for each hypothesis-reference(s) pairs before division)

### Machine Translation
1. **BLEU** (Bilingual Evaluation Understudy)
    * Papineni 2002
    * 'Measures how many words overlap in a given translation when compared to a reference translation, giving higher 
     scores to sequential words.' (recall)
    * Limitation: designed to be a corpus measure, so it has undesirable properties when used for single sentences.
    * See [paper](https://www.aclweb.org/anthology/P02-1040.pdf)
2. **GLEU** (Google-BLEU)
    * Wu et al. 2016
    * Minimum of BLEU recall and precision applied to 1, 2, 3 and 4grams
        * Recall: (number of matching n-grams) / (number of total n-grams in the target)
        * Precision: (number of matching n-grams) / (number of total n-grams in generated sequence)
3. **WER** (Word error rate)
    * Levenshtein distance for words
    * Range: greater than 0 (ref = hyp), no max range as ASR can insert an arbitrary number of words
    * Limitation: provides no details on the nature of translation errors
    * $ WER = \frac{S+D+I}{N} = \frac{S+D+I}{S+D+C} $
        * S: number of substitutions, D: number of deletions, I: number of insertions, C: number of the corrects,
            N: number of words in the reference (N=S+D+C)
    * WAcc (Word Accuracy) or Word Recognition Rate (WRR): $1 - WER$        
    * See [more info](https://martin-thoma.com/word-error-rate-calculation/)
4. **METEOR** (Metric for Evaluation of Translation with Explicit ORdering):
    * Banerjee 2005
    * About: "based on the harmonic mean of unigram precision and recall (weighted higher than precision)"
    * Includes: exact word, stem and synonym matching
    * Designed to fix some of the problems found in the BLEU metric, while also producing good correlation with human
        judgement at the sentence or segment level (unlike BLEU which seeks correlation at the corpus level).
5. **CIDEr**:     
    * About: 
    * Limitation:
6. **TER** (Translation Edit Rate)
    * About: 
    * Limitation:
    * **char-TER**: character level TER
7. **GTM** (General Text Matcher)
    * About: 
    * Limitation:


### Summarization
1. **ROUGE** (Recall-Oriented Understudy for Gisting Evaluation)
    * About: 
    * Limitation:
