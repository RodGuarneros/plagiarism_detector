# Plagiarism Detector

## By Rodrigo Guarneros

## Objective
Based on supervised learning methods, this model is aimed to detect plagiarism.

## Dataset of learning
The model is trained using the dataset: Clough, P. and Stevenson, M. Developing A Corpus of Plagiarised Short Answers, Language Resources and Evaluation: Special Issue on Plagiarism and Authorship Analysis, available at: https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html.

The data structure includes 100 text files, a list with the most important characteristics of every text files (.csv file) categorized as:

1. Plagiarized categories: cut, light, and heavy. These categories represent different levels of plagiarized answer texts. cut answers copy directly from a source text, light answers are based on the source text but include some light rephrasing, and heavy answers are based on the source text, but heavily rephrased (and will likely be the most challenging kind of plagiarism to detect).

2. Non-plagiarized category: non. Indicates that an answer is not plagiarized; the Wikipedia source text is not used to create this answer.

3. Special, source text category: orig. This is a specific category for the original, Wikipedia source text. We will use these files only for comparison purposes.

This dataset is quite small, especially with respect to examples of varying plagiarism levels, however its a great **starting point**, you can train this model to detect specific sort of texts.

## Pre-processing the data

This step is particularly important previously the training model.

1. Convert categorical variables in numerical.
2. Split our data set in train and test. The stratified random sampling is the method of sampling used to split the dataset so as to get a fairly distributed accross task and plagiarism combinations.
3. Longest common subsequence. This technique is really useful to detect **cut and paste plagiarism**. 
4. Building the model based on Scikit-learn: (i) classification model LinearLearner; (ii) define the estimator; (iii) train the estimator; (iv) deploy the model, and (v) test the model. 

## The cloud service is Amazon Web Services

- In this project we use Amazon Web Service to optimize the procedure base on scalability.
- SageMaker service
- The processing instance used was ml.m4.xlarge
