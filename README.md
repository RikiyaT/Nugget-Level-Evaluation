# Nugget-Level-Evaluation

Repository for the ACM SIGIR-AP 2023 Paper, [Open Domain Dialogue Quality Evaluation: Deriving Nugget-level Scores from Turn-level Scores](https://dl.acm.org/doi/10.1145/3624918.3625338). You can also access SIGIR-AP 2023 presentation slides [here](https://akihisa-watanabe.github.io/files/Slide_Open-Domain_Dialogue_Quality_Evaluation__Deriving_Nugget-level_Scores_from_Turn-level_Scores.pdf).

## Explanation

This is a repository showing the example code of how the Nugget-Level Evaluation can be calculated using a turn-level evaluation framework.

We implemented an example experiment to retrieve nugget-level engagingness scores using the EnDex framework (Xu et al., 2022)

The EnDex framework can be found here:
https://drive.google.com/file/d/1ph4P471n0LoM1vbsarj3wvEkpijhwCms/view?usp=sharing

---
We tested to calculate the nugget-level engagingness scores of each nugget in the following example system turn:

```
You are interested in SIGIR AP? According to the homepage, you should write a paper of 2-9 pages. I recommend that you review the Call for Papers to check the relevant topics. Good luck!
```

## Usage
The dataset file, and all the parameters (w_ø, w_diff, w_same, K, L) can be adjusted in config.py.

Make sure you have appropriate versions of pytorch and huggingface transformers installed

```
our version:
torch.__version__ == 2.0.1
transformers.__version__==4.33.2
```

## Test Results
The results we achieved in the case study is as folllows:

![test results](https://github.com/RikiyaT/Nugget-Level-Evaluation/blob/main/testresults.png)

For more information please refer to our paper.

## Bibtex
If you find our study useful in your research, please cite:
```
@inproceedings{10.1145/3624918.3625338,
author = {Takehi, Rikiya and Watanabe, Akihisa and Sakai, Tetsuya},
title = {Open-Domain Dialogue Quality Evaluation: Deriving Nugget-Level Scores from Turn-Level Scores},
year = {2023},
isbn = {9798400704086},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3624918.3625338},
doi = {10.1145/3624918.3625338},
abstract = {Existing dialogue quality evaluation systems can return a score for a given system turn from a particular viewpoint, e.g., engagingness. However, to improve dialogue systems by locating exactly where in a system turn potential problems lie, a more fine-grained evaluation may be necessary. We therefore propose an evaluation approach where a turn is decomposed into nuggets (i.e., expressions associated with a dialogue act), and nugget-level evaluation is enabled by leveraging an existing turn-level evaluation system. We demonstrate the potential effectiveness of our evaluation method through a case study.},
booktitle = {Annual International ACM SIGIR Conference on Research and Development in Information Retrieval in the Asia Pacific Region},
pages = {40–45},
numpages = {6},
keywords = {dialogue act, dialogue systems, evaluation},
location = {<conf-loc>, <city>Beijing</city>, <country>China</country>, </conf-loc>},
series = {SIGIR-AP '23}
}
```

### References
1. Guangxuan Xu, Ruibo Liu, Fabrice Harel-Canada, Nischal Reddy Chandra, and
Nanyun Peng. 2022. EnDex: Evaluation of Dialogue Engagingness at Scale. In
Findings of the Association for Computational Linguistics: EMNLP 2022. Association
for Computational Linguistics, Abu Dhabi, United Arab Emirates, 4884–4893. https://aclanthology.org/2022.findings-emnlp.359
