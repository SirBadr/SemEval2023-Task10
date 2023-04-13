# Lexicools at SemEval-2023 Task 10: Sexism Lexicon Construction via XAI

This repo is our work on [the SemEval-2023 Task 10 Explainable Detection of Online Sexism (EDOS)](https://github.com/rewire-online/edos) 

The main idea is to develop lexicon-based models for sexism classifier as we prioritize explanability over performance.

Our approach consists of three main steps: 
1. Lexicon Construction: based on Pointwise Mutual Information (PMI) and Shapley value
2. Augmentation: by utilising an unannotated corpus, BERTweet and GPT-J
3. Incorporating Lexicons: for bag-of-word logistic regression and fine-tuning LLMs.

Our results demonstrate that our Shapley approach effectively produces a high-quality lexicon. We also show that simply counting the presence of certain words in our lexicons and comparing the count can outperform a BoW logistic regression in task B/C and fine-tuning BERT in task C. In the end, our classifier achieved F1-scores of 53.34% and 27.31% on the official blind test sets for tasks B and C, respectively.


## Project Structure

Please follow these steps to re-run our experiments.

1. Find-tune a model in Task A
* `TaskA Fine-tuning BERT.ipynb`
* `TaskA Fine-tuning BERTweet.ipynb`
* `TaskA Fine-tuning TwHINBERT.ipynb`

2. Contruct the lexicons: 
* `TaskB Lexicon Construciton [PMI].ipynb`
* `TaskB Lexicon Construciton [Shapley].ipynb`

3. Generate more data with GPT-J: 
* `Generate data w: GPT-J.ipynb`

4. Augment the lexicons: 
* `TaskB Augmentation w_ XAI.ipynb`
* `TaskB Augmentation with BERTTweets.ipynb`
* `TaskB Augmentation with GPT-J.ipynb`

5. Incorperate the lexicons: 
* `TaskB Incorporate BERT.ipynb`
* `TaskB Logistic Regression.ipynb`


See our resulting lexicons in `Lexicons`

## Authors

* [Pakawat Nakwijit](https://wp.curve.in.th/): <p.nakwijit@qmul.ac.uk>
* [Mahmoud Samir](): <mahmoudbadr9199@gmail.com>
* [Matthew Purver](): <m.purver@qmul.ac.uk>


## Citation

If you use our lexicon or accompanying materials, please cite:

```
@inproceedings{nakwijit-samir-semeval-2023,
    title = "Lexicools at SemEval-2023 Task 10: Sexism Lexicon Construction via XAI",
    author = "Nakwijit, Pakawat and
              Samir, Mahmoud and
              Purver, Matthew",
    booktitle = "Proceedings of the 16th International Workshop on Semantic Evaluation (SemEval-2022)",
    month = july,
    year = "2022",
    address = "Seattle",
    publisher = "Association for Computational Linguistics"
}
```

## More information about the task and data

Plese visit [Explainable Detection of Online Sexism (EDOS)
](https://github.com/rewire-online/edos)
