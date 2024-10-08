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
