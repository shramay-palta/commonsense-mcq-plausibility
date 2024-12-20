# Plausibly Problematic Questions in Multiple-Choice Benchmarks for Commonsense Reasoning
This repository contains the data collected in the paper: [Plausibly Problematic Questions in Multiple-Choice Benchmarks for Commonsense Reasoning](https://aclanthology.org/2024.findings-emnlp.198/) presented at the [The 2024 Conference on Empirical Methods in Natural Language Processing (EMNLP 2024)](https://2024.emnlp.org)

## Introduction
The data contains plausibility ratings for individual question answer tuples and the votes received when all the answer choices were shown to the annotators. We collect data for 125 questions each from [Social IQA](https://aclanthology.org/D19-1454/) and [CommonsenseQA](https://aclanthology.org/N19-1421/). 

Overall, we collect 5000 plausibility ratings in total for both datasets and 1530 full question annotations. Please refer to our paper for more details.

## Data
The data is organized as follows:
```
└── data
    └── ind
        ├── siqa_ind.jsonl
        ├── siqa_ind.csv
        ├── cqa_ind.jsonl
        ├── cqa_ind.csv
    └── full
        ├── siqa_full.jsonl
        ├── siqa_full.csv
        ├── cqa_full.jsonl
        ├── cqa_full.csv  
```
We release our data as ``jsonl`` and ``csv`` files.
1. Files with the suffix ``ind`` in the file name contain the plausibility ratings of individual question answer tuples. The ``ind`` files are structured as follows:
    ```json
    {
    "id": "A unique identifier for the dataset entry",
    "context": "The context text",
    "question": "The question text",
    "answerA": "The answer text for option A",
    "answerA_ratings": "List of plausibility ratings for option A",
    "answerA_stats": "Mean, variance, standard deviation and median of the plausibility ratings for option A",
    "feedback_answerA": "Optional feedback provided by the annotators for option A",
    "answerB": "The answer text for option B",
    "answerB_ratings": "List of plausibility ratings for option B",
    "answerB_stats": "Mean, variance, standard deviation and median of the plausibility ratings for option B",
    "feedback_answerB": "Optional feedback provided by the annotators for option B",
    "answerC": "The answer text for option C",
    "answerC_ratings": "List of plausibility ratings for option C",
    "answerC_stats": "Mean, variance, standard deviation and median of the plausibility ratings for option C",
    "feedback_answerC": "Optional feedback provided by the annotators for option C",
    "gold_label": "The original gold label from the dataset",
    "gold_label_rating": "The mean plausibility rating of the gold label"
    }
2. Files with the suffix ``full`` in the file name contain the votes received when all the answer choices were shown to the annotators. The ``full`` files are structured as follows:
    ```json
    {
    "id": "A unique identifier for the dataset entry",
    "context": "The context text",
    "question": "The question text",
    "answer_picked": "List of the answer choices picked by the annotators",
    "feedback": "Optional feedback provided by the annotators",
    "original_gold_label": "The original gold label from the dataset",
    "votes_distribution": "Annotator vote distribution for the answer choices for the question"
    }


The above are structures of an example based on Social IQA. Please note that CommonsenseQA does not have a ``context`` field and has 5 answer options for each question.
## License
This project is licensed under the MIT License.
## Citation
If you use this dataset, please cite the following paper:

```
@inproceedings{palta-etal-2024-plausibly,
    title = "Plausibly Problematic Questions in Multiple-Choice Benchmarks for Commonsense Reasoning",
    author = "Palta, Shramay  and
      Balepur, Nishant  and
      Rankel, Peter A.  and
      Wiegreffe, Sarah  and
      Carpuat, Marine  and
      Rudinger, Rachel",
    editor = "Al-Onaizan, Yaser  and
      Bansal, Mohit  and
      Chen, Yun-Nung",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2024",
    month = nov,
    year = "2024",
    address = "Miami, Florida, USA",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.findings-emnlp.198",
    pages = "3451--3473",
}
```

Please also cite the original dataset papers:

```
@inproceedings{sap-etal-2019-social,
    title = "Social {IQ}a: Commonsense Reasoning about Social Interactions",
    author = "Sap, Maarten  and
      Rashkin, Hannah  and
      Chen, Derek  and
      Le Bras, Ronan  and
      Choi, Yejin",
    editor = "Inui, Kentaro  and
      Jiang, Jing  and
      Ng, Vincent  and
      Wan, Xiaojun",
    booktitle = "Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP)",
    month = nov,
    year = "2019",
    address = "Hong Kong, China",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/D19-1454",
    doi = "10.18653/v1/D19-1454",
    pages = "4463--4473"
}
```


```
@inproceedings{talmor-etal-2019-commonsenseqa,
    title = "{C}ommonsense{QA}: A Question Answering Challenge Targeting Commonsense Knowledge",
    author = "Talmor, Alon  and
      Herzig, Jonathan  and
      Lourie, Nicholas  and
      Berant, Jonathan",
    editor = "Burstein, Jill  and
      Doran, Christy  and
      Solorio, Thamar",
    booktitle = "Proceedings of the 2019 Conference of the North {A}merican Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long and Short Papers)",
    month = jun,
    year = "2019",
    address = "Minneapolis, Minnesota",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/N19-1421",
    doi = "10.18653/v1/N19-1421",
    pages = "4149--4158"
}
```
