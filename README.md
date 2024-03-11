## Abstract

This project is about patient notes that medical students write during their clinical skills assessment. Those notes include long sentences that professional doctors analyze later to score them, and due to the large number of notes with very long sentences, this can be a very time and effort exhaustive task for the medical practitioners.

utilizing natural language processing, we propose a solution using BERT Trasnformer to make these notes more interpretable and ease the development and administration of such assessments by extracting the most important words of the text for the doctors to analyze.

This keywords extraction problem is described as a special case of Named Entity Recognition, which involves identifying and classifying specific entities in text into predefined categories.

The used dataset (patient notes) are provided from the USMLE® Step 2 Clinical Skills examination, a medical licensure exam. This exam measures a trainee's ability to recognize pertinent clinical facts during encounters with standardized patients.

Full report of the project:  https://docs.google.com/document/d/1T7o6p91TjP0m0ToWpX_P7Hytt_aQlIToeCN1ynGUbQE/edit?usp=sharing

## Table of Contents

- [Used Libraries](#Libraries)
- [Data Visualization](#Visualization)
- [Preprocessing](#Preprocessing)
- [Fine Tuning BERT and Results](#Fine_Tuning_BERT_and_Results)





## Libraries

Here are the imports of the used libraries

![libs](https://github.com/Mo-Moustafa/Scoring-Patient-Notes/assets/81877648/c5a52f4e-3e2e-4c9f-beca-9cf537a38b77)


## Visualization

Here we explore and visualize the data

![data](https://github.com/Mo-Moustafa/Scoring-Patient-Notes/assets/81877648/60966911-75a3-43da-9c48-f56dd7d14ece)
![data 2](https://github.com/Mo-Moustafa/Scoring-Patient-Notes/assets/81877648/85201707-a743-4104-8a0a-2706fd3cd97e)

The dataset contains a huge number of notes without labels (annotations).


## Preprocessing

Original Data

![data before](https://github.com/Mo-Moustafa/Scoring-Patient-Notes/assets/81877648/b063acb1-51b7-4ca9-ac14-26d509fb2dcd)

After Preprocessing, Tokenization, removing notes without annotations, and converting annotations into labels

![data after](https://github.com/Mo-Moustafa/Scoring-Patient-Notes/assets/81877648/4019284d-47fd-4129-a9d2-fce25c4adab2)


## Fine_Tuning_BERT_and_Results

We used Distillbert-base-uncased model and fine-tuned it on the available data with the Masking method. We kept trying different hyperparameters until we reached the best results using a Learning rate of 1e-3, a batch_size of 16, and training the model for 15 epochs and 5 folds.

We reached a precision of 0.85 as our final result 







