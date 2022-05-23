# TrueSight ML Project Documentation
## Project Overview
This repository contains all ML related files. The Main ML model Created using IndoBERT as base model and use transfer learning to create News Credibility Prediction. You can access the notebook file that we use to train our model in this repository [[Train Model]News Prediction with indoBert-base-p1.ipynb](https://colab.research.google.com/drive/1SSiVNF4Cw7gVSxE_mvvWydD7L-RfmVDL?authuser=1#scrollTo=0e2f542a)

## News Credibility Prediction Model
### Training Recap
We've tried to build our model with or without transfer learning, and using different amount of datasets, at the early phase we could only gather around 4851 datasets and were able to use web-crawling to gather more data 7444 datasets, even with that amount of data transfer learning definitely helps our model to gain more accuracy as shown in this recap table.
| Transfer Learning | Train Accuracy |  Validation Accuracy  | Datasets | 
| --- | --- | --- | --- |
| None | 99.4 | 78.76 | 4821 Indonesia Dataset |
| indobenchmark/indobert-base-p1 | 98.78 | 83.89 | 4851 Indonesia Dataset |
| indobenchmark/indobert-base-p1 | 99.58 | 87.04 | 7444 Indonesia Dataset |

### API from this model
| Methods   | Endpoint API                              | Usage                                         |
|-----------|-------------------------------------------|-----------------------------------------------|
| GET       | /api/predict                              | Get prediction value from a sequence of text  |
