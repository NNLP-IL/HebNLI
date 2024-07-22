# HebNLI - A Natural Language Inference Dataset in Hebrew

## Summary
HebNLI is a Hebrew dataset for natural language inference (NLI) tasks.

## Introduction
This dataset is the first of its kind in the Hebrew language and aims to serve as training data for NLI tasks.
HebNLI is based on MultiNLI, a large crowd-sourced corpus of sentences from varied genres and writing styles in the English language.
MultiNLI was originally built by collecting hundreds of thousands of base sentences from which different taggers derived follow-up sentences that stand in one of 3 logical relations to the base sentences: entailment, contradiction or neutral.
Different taggers were then given paired sentences - base sentence and a derived sentence. The logical relation between them was determined by the majority vote, and each pair of sentences was labled according to the determined logical relation.
In HebNLI we used machine translation (Google Gemini) to translate the English corpus to Hebrew, such that each base sentence and its compiled derivative sentences appear in Hebrew.

## Genres/Sources in HebNLI
HebNLI comprises 7 of the original 10 genres/sources that appeared in MultiNLI:
1. Nine eleven - Written protocols from a commitee investigating the events of 9/11.
2. Government - Reports, speeches and press releases published on U.S.A government websites.
3. Letters - A database of letters written in the late 90's and early 2000's.
4. OUP (Oxford University Press) - Publications about the textile industry and about child development.
5. Slate - Pop-culture articles published in Slate magazine.
6. Travel - Travel guides by Berlitz press.
7. Fiction - Texts extracted from modern works of literature.

The remaining three sources were found to either be too English-oriented to be properly translated to Hebrew by machine translation ("Verbatim" magazine source), or included too many broken sentences and filler-words to be properly translated to Hebrew by machine translation (face-to-face conversations and telephone conversations sources). 

## Dataset Statistics (Updated for HebNLI ver2.0)
The table below shows the distribution of each source corpus within HebNLI (how many setences exist in the dataset from each source).

| Genre/Source     |  HebNLI Corpus   |
|------------------|------------------|
| Nine eleven      |   1869           |
| Government       |   76709          |
| Letters          |   1966           |
| OUP              |   1979           |
| Slate            |   70755          |
| Travel           |   75526          |
| Fiction          |   73346          |

Total # of sentences = 302,150.

## HebNLI Gold set
Additionally, we have created a Gold set for HebNLI which contains 883 pairs of sentences. These sentences were randomlly chosen from HebNLI, and were omitted from it such that sentence pairs appearing in the Gold set no longer appear in HebNLI's ver 2.0. The translations for the sentences in the Gold set were manually verfied by two taggers who are linguists - in cases where the automatic translation provided by Google Gemini was deemed good it was left as is, while in cases where the auto-translations were false or not natural/idiomatic enough to a Hebrew speaker they were retranslated manually by the tagger. The 883 sentences in the Gold set were also manually tagged for their logical relation (Entailment, Neutral, Contradiction) by both linguists.
The percantage of agreement between the two Hebrew taggers for the Hebrew sentences was 87.44% (on originally 1010 pairs of sentences), which gave rise to the final 883 pairs of sentences in the final version of the Gold set which contains a single Hebrew label agreed upon by both Hebrew taggers.

## Dataset Details
Below is a description of the data found in the HebNLI and the Gold set files:

1. **original_annotator_labels** = All the original labels assigned by the English taggers in the original English dataset (MultiNLI) presented as a list.

2. **genre** = The genre (source) to which the pair of sentence belong (Government, Letters, Slate Magazine, Travel, Fiction etc.)

3. **original_label** = The final English label assigned to the pairs of sentences by the English taggers (either by consensus or by majority).

4. **pairID** and **promptID** = unique identifiers for each pair of sentences

5. **sentence1** = The first sentence of the English pair of sentences.

6. **translation1** = The Hebrew translation of English "sentence1".

7. **sentence2** = The second sentence of the English pair of sentences.

8. **translation2** = The Hebrew translation of English "sentence2".

9. **hebrew_label** (found only in the Gold set) = The label assigned manually by the Hebrew taggers.



## Literature

### HebNLI Post
https://www.facebook.com/groups/MDLI1/posts/2675912835906081/

### HebNLI PDF
You can find a detailed PDF file summarizing the work done on HebNLI in the repository's file section.

### Original MultiNLI Paper
https://cims.nyu.edu/~sbowman/multinli/paper.pdf

## Contributors
HebNLI was translated and checked for quality by Webiks for MAFAT, as part of the National Natural Language Processing Plan of Israel. 

Contributors: Hilla Merhav Fine (Webiks), Yaniv Maylik (Webiks), Carinne Cherf (Webiks), Tal Geva (MAFAT).

## Acknowledgments
We would like to express our gratitude to Adina Williams, Nikita Nangia and Samuel R. Bowman, the creators of [the original NLI dataset MultiNLI](https://huggingface.co/datasets/nyu-mll/multi_nli).
