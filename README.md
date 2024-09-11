# Plausibly Problematic Questions in Multiple-Choice Benchmarks for Commonsense Reasoning
This repository contains the data collected in the paper: Plausibly Problematic Questions in Multiple-Choice Benchmarks for Commonsense Reasoning. 

## Introduction
The data contains plausibility ratings for individual question answer tuples and the votes received when all the answer choices were shown to the annotators. We collect data for 125 questions each from Social IQA and CommonsenseQA. 

Overall, we collect 5000 plausibility ratings in total for both datasets and 1530 full question annoataions. Please refer to our paper for more details.

## Data
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
This project is licensed under the CC-BY-4.0 License.
## Citation
If you use this dataset, please cite the following paper: