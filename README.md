# B2W Reviews

The original dataset was published in the STIL 2019:
http://comissoes.sbc.org.br/ce-pln/stil2019/accepted.html

B2W-Reviews01: An open product reviews corpus - Livy Real (B2W Digital); Marcio Oshiro (B2W Digital); Alexandre Mafra (B2W Digital);

Real, L., Oshiro, M., Mafra, A.: B2w-reviews01: An open product reviews corpus. Proceedings of STIL - Symposium in Information and Human Language Technology (2019)

[GitHub Link](https://github.com/b2w-digital/b2w-reviews01)



Using the provided dataset three datasets were created. They are  `B2W-Polarity-Balanced`, `B2W-Rating-Balanced` and `B2W-Recommend-Balanced`.

## Description

The file `Dataset.zip` contains the dataset without separtion between Train and Test dataset. 

The file `Experiment_dataset.zip` contains the dataset with separation in Train and Test dataset. The Test dataset is composed of 500 reivews of each class of the dataset, while the Train dataset is the remaining reviews


Each file is in the format `<class>_<id>.txt`. Where `<class>` is the class of the document and `<id>` the document identifier. Details about the meaning of each class is described bellow.


## The three datasets

In this Section the creation process of each of the datasets is described.


### B2W-Polarity-Balanced

In this dataset, the categories 1 and 2 were grouped into the class Negative (0), the categories 4 and 5 were grouped int othe class Positive (1) and the category 3 was renamed to class Neutral (2).

| Rating | Count |
| ------ | ----- |
| 1      | 27369 |
| 2      | 8389  |
| 3      | 16315 |
| 4      | 32345 |
| 5      | 47955 |

The number of reviews are unbalanced across classes, as the following table shows:

| Class    | Count |
| -------- | ----- |
| Negative | 35758 |
| Neutral  | 16315 |
| Positive | 80300 |
|----------|-------|
| **TOTAL**|132373 |

In this dataset, classes Negative and Positive are reduced to be contain the same ammount of reviews as the Neutral class. The selection of the reviews are made randomly. Resulting in the dataset described by the following table:

| Class    | Count |
| -------- | ----- |
| Negative | 16315 |
| Neutral  | 16315 |
| Positive | 16315 |
|----------|-------|
| **TOTAL**| 48945 |


The test dataset is composes of 500 documents from each class.


### B2W-Rating-Balanced

In this dataset the rating of the reviews are the classes. The Rating 1 is the lowest rate while 5 is the best rate. In this dataset all classes contain the same number of reviews. The removal of reviews in the ratings 1, 3, 4 and 5 were made randomly.

| Rating    | Count   |
| --------- | ------- |
| 1         | 8389    |
| 2         | 8389    |
| 3         | 8389    |
| 4         | 8389    |
| 5         | 8389    |
| --------  | ------- |
| **TOTAL** | 41945   |

The test dataset is composes of 500 documents from each class.


### B2W-Recommend-Balanced

In this dataset there is 2 classes, the No (0) and Yes (1). The null values are removed from the dataset since it can't be set neither "Yes" nor "No". The original numbers are showed in the table below

| Recommend to a friend | Count |
| --------------------- | ----- |
| No                    | 35987 |
| Yes                   | 96368 |
| null                  | 18    |

Additionaly, the classes were balanced to contain the same number of reviews. Therefore, The "Yes" class lost some reviews randomly, leading to the following final dataset:

| Recommend to a friend | Count |
| --------------------- | ----- |
| No                    | 35987 |
| Yes                   | 35987 |
|-----------------------|-------|
| **TOTAL**             | 71974 |

The test dataset is composes of 500 documents from each class.



## Objectives

The following table specifies all datasets objectives and sizes

| Dataset                | Objective                                                   | Balanced | Dataset size | Number of classes | Train dataset size | Test dataset size |
| ---------------------- | ----------------------------------------------------------- | -------- | ------------ | ----------------- | ------------------ | ----------------- |
| B2W-Polarity-Balanced  | Classify polarity of the review                             | YES      | 48945        | 3                 | 47445              | 1500              |
| B2W-Rating-Balanced    | Classify rating of the review                               | YES      | 41945        | 5                 | 39445              | 2500              |
| B2W-Recommend-Balanced | Predict if a product is recommended or not                  | YES      | 71974        | 2                 | 70974              | 1000              |


## Dataset Statitiscs

The following table presents the statistics of the dataset concernig the number of words per review.


|                  METRIC                   | NUMERIC OBSERVATION |
|:-----------------------------------------:|:-------------------:|
|                   Mean                    | 24.296533280956087  |
|              Geometric Mean               |  18.47804203265341  |
|               Harmonic Mean               | 14.861573589133467  |
|                  Median                   |         16          |
|                   Mode                    |         10          |
|            Standard deviation             |  24.5049628883782   |
|                 Max Value                 |         796         |
|                 Min Value                 |          1          |
| Number of review with more than 75 words  |        4892         |
| Number of review with more than 150 words |         688         |
