# HebNLI - change log


## Summary
This document reflects the changes made to the dataset throughout its releases.
HebNLI was released on three different occasions:
19/03/24 - Oldest version which included the dataset in its entierty in one file.
18/06/24 - An interim version which included a small gold set extracted from HebNLI, verified by human taggers.
23/07/24 - The latest version which includes HebNLI split to 3 sets: train, validation (sampled from HebNLI) and test (formerly the gold set).



## Past releases - what changed?
Detailed below are the changes made in each of the 3 versions:

1. The initial release contained 303,383 pairs of sentences in a single file.
2. The interim release contained 302,150 pairs of sentences in the HebNL dataset and 1,011 pairs of sentences in the gold set (which were discarded from the HebNLI dataset along with other data cleanups).
3. The latest version contains: 300,150 pairs of sentences in the train set 
                                2000 pairs in the val test (sampled from the large HebNLI)
                                884 pairs in the test set (formerly the gold set).

4. The initial release of HebNLI contained the following keys:
"annotator_labels"
"genre"
"gold_label"
"pairID"
"promptID"
"sentence1"
"translation1"
"sentence2"
"translation2"

In the interim release the keys remained unchaged, but in the latest release two keys received a name change for convenience purposes:
"annotator_labels" was renamed to "original_annotator_labels" to reflect the fact that these are the labels given by the original English taggers.
"gold_label" was renamed to "original_label" to reflect the fact that this is the final label assigned to the pair of sentences in accordance with the majority decision of the original English taggers.

5. The interim release contained a gold set file alongside HebNLI which contained the following keys:
"hebrew_annotator_labels" (a list containing the labels assigned by the Hebrew taggers - this would eventually be discarded and superseded by a different key for convenience).
"genre"
"English_label"
"pairID"
"promptID"
"sentence1"
"translation1"
"sentence2"
"translation2"

In the latest release the gold set is used as the test set and its keys were renamed to match the keys in the training and evaluation sets, with the addition of the "hebrew_label" key which contains the labels manually assigned by the Hebrew taggers:
"original_annotator_labels"
"genre"
"original_label"
"pairID"
"promptID"
"sentence1"
"translation1"
"sentence2"
"translation2"
"hebrew_label" (supersedes the previous list key "hebrew_annotator_labels").


## Dataset Statistics in each release

Initial release:                                     Interim release:                                                

| Genre/Source     |  HebNLI Corpus   |              | Genre/Source     |  HebNLI Corpus   |                
|------------------|------------------|              |------------------|------------------|
| Nine eleven      |   1878           |              | Nine eleven      |   1869           |
| Government       |   76953          |              | Government       |   76709          |
| Letters          |   1974           |              | Letters          |   1966           |
| OUP              |   1986           |              | OUP              |   1979           |
| Slate            |   71082          |              | Slate            |   70755          |
| Travel           |   75776          |              | Travel           |   75526          |
| Fiction          |   73734          |              | Fiction          |   73346          |

Total # of sentences = 303,383.                      Total # of sentences = 302,150
________________________________________________________________________________________________


Latest release:

train set:                                  val set:                                    test set (formerly the gold set):

| Genre/Source     |  HebNLI Corpus   |     | Genre/Source     |  HebNLI Corpus   |     | Genre/Source     |  HebNLI Corpus   |                
|------------------|------------------|     |------------------|------------------|     |------------------|------------------|
| Nine eleven      |   1852           |     | Nine eleven      |   17             |     | Nine eleven      |   6              |
| Government       |   76183          |     | Government       |   526            |     | Government       |   206            |
| Letters          |   1953           |     | Letters          |   13             |     | Letters          |   7              |
| OUP              |   1965           |     | OUP              |   14             |     | OUP              |   4              |
| Slate            |   70306          |     | Slate            |   449            |     | Slate            |   215            |
| Travel           |   75030          |     | Travel           |   496            |     | Travel           |   223            |
| Fiction          |   72861          |     | Fiction          |   485            |     | Fiction          |   223            |

Total # of sentences = 300,150              Total # of sentences = 2,000                Total # of sentences = 884
