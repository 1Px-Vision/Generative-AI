# Lightweight Fine-Tuning Project 

## Project Overview
This project demonstrates how to fine-tune models in a simple and efficient manner. Lightweight fine-tuning is a crucial technique for adapting foundation models to specific tasks, as it enables customization without requiring significant computational resources.

## About the Project 
In this project, we will bring together all of the essential components of a PyTorch + Hugging Face training and inference process. Specifically, we will:

* Load a pre-trained model and evaluate its performance
* Perform parameter-efficient fine tuning using the pre-trained model
* Perform inference using the fine-tuned model and compare its performance to the original model

## Dataset Description
The dataset contains two columns:

* **tweet:** Each row contains the text of a tweet that originally included an emoji, but the emoji has been removed.
* **emoji:** Each row provides the name of the emoji that corresponds to the text in the tweet column.

## Overall Summary

| Metric               | GPT-2       | PEFT        |
|----------------------|-------------|-------------|
| Training Loss        | 1.5625      | 1.9241      |
| Validation Loss      | 1.5016      | 1.9065      |
| Accuracy             | 47.32%      | 33.87%      |
| F1 Score             | 46.14%      | 28.86%      |
| Precision            | 51.27%      | 40.97%      |
| Recall               | 47.32%      | 33.87%      |
| Training Duration    | 1 hr 33 min | 1 hr 25 min |
| Eval Runtime         | 3 min 28 sec| 3 min 39 sec|
| Samples per Second   | 108.258     | 102.473     |
| Steps per Second     | 1.696       | 1.605       |
| Epoch                | 1.0         | 1.0         |

## Conclusions

It's evident that the GPT-2 approach performed better for this particular task and dataset, indicating that fine-tuning does not always lead to higher accuracy. The dataset contained multiple labels, and if it had been structured for tasks like sentiment analysis (e.g., positive or negative), the hyperparameters might have been more effective and could have contributed to improving PEFT's accuracy. Additionally, increasing the number of epochs might have provided further insights or potentially enhanced accuracy.
