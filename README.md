# Plausibly Problematic Questions in Multiple-Choice Benchmarks for Commonsense Reasoning
This repository contains the data collected in the paper: Plausibly Problematic Questions in Multiple-Choice Benchmarks for Commonsense Reasoning. 

## Data
We release our data as ``jsonl`` and ``csv`` files.
1. Files with the suffix ``ind`` in the file name contain the plausibility ratings of individual question answer tuples. The ``ind`` files are structured as follows:
    ```json
    This is the structure of an example based on Social IQA. Please note that CommonsenseQA does not have a ``context`` field and has 5 options for each question.
    {
    "id": "a unique identifier for the dataset entry",
    "context": "the context text",
    "question": "the question text",
    "answerA": "the answer text for option A",
    "answerA_ratings": "list of plausibility ratings for option A",
    "answerA_stats": "mean, variance, standard deviation and median of the plausibility ratings for option A",
    "feedback_answerA": "Optional feedback provided by the annotators for option A",
    "answerB": "the answer text for option B",
    "answerB_ratings": "list of plausibility ratings for option B",
    "answerB_stats": "mean, variance, standard deviation and median of the plausibility ratings for option B",
    "feedback_answerB": "Optional feedback provided by the annotators for option B",
    "answerC": "the answer text for option C",
    "answerC_ratings": "list of plausibility ratings for option C",
    "answerC_stats": "mean, variance, standard deviation and median of the plausibility ratings for option C",
    "feedback_answerC": "Optional feedback provided by the annotators for option C",
    "gold_label": "The original gold label from the dataset",
    "gold_label_rating": "The mean plausibility rating of the gold label"
    }
2. Files with the suffix ``full`` in the file name contain the votes received when all the answer choices were shown to the annotators. The ``full`` files are structured as follows:
    ```json
    This is the structure of an example based on Social IQA. Please note that CommonsenseQA does not have a ``context`` field and has 5 options for each question.
    {
    "id": "a unique identifier for the dataset entry",
    "context": "the context text",
    "question": "the question text",
    "answer_picked": "list of the answer choices picked by the annotators",
    "feedback": "Optional feedback provided by the annotators",
    "original_gold_label": "The original gold label from the dataset",
    "votes_distribution": "Annotator vote distribution for the answer choices for the question."
    }
## License
This project is licensed under the CC-BY-4.0 License.
## Citation
If you use this dataset, please cite the following paper: