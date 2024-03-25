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

## Dataset Statistics
The table below shows the distribution of each source corpus within HebNLI (how many setences exist in the dataset from each source).

| Genre/Source     |  HebNLI Corpus   |
|------------------|------------------|
| Nine eleven      |   1878           |
| Government       |   76953          |
| Letters          |   1974           |
| OUP              |   1986           |
| Slate            |   71082          |
| Travel           |   75776          |
| Fiction          |   73734          |

Total # of sentences = 303,383.

### HebNLI Blog Post
XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

### HebNLI PDF
You can find a detailed PDF file summarizing the work done on HebNLI in the repository's file section.

### Original MultiNLI Paper
https://cims.nyu.edu/~sbowman/multinli/paper.pdf

## Contributors
HebNLI was translated and checked for quality by Webiks for MAFAT, as part of the National Natural Language Processing Plan of Israel. 

Contributors: Hilla Merhav Fine (Webiks), Yaniv Maylik (Webiks), Carrine Cherf (Webiks), Tal Geva (MAFAT).

## Acknowledgments
We would like to express our gratitude to Adina Williams, Nikita Nangia and Samuel R. Bowman, the creators of [the original NLI dataset MultiNLI](https://huggingface.co/datasets/nyu-mll/multi_nli).
