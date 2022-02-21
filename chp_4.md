# Model development and training

<img src='./assets/4_1.png'></img>

<img src='./assets/4_2.png'></img>

brain stroming : 

QA :

1. 10M x 0.01 = 100K misinformation tweets.

    sampling 1 : 1 true info vs misinformation, 50k, 50k.

2. Do stratified sampling by each annotater, misinformation/true information

   100K / 20 = 5k per labeller, each labeller we stratified sampling, each section we sample 1000 instances.(statistically coverage)

   so I'll sampling (1000+1000) x 20 = 40k instances. to estimate the quality.

3. no idea.

# Sampling

<img src='./assets/4_8.png'></img>

## Non-Probabilistic Sampling

<img src='./assets/4_3.png'></img>

[probabilistic sampling vs non-probabilistic sampiling](https://www.cuhk.edu.hk/soc/lsonline/ies/ies2009/2/electure2_4.htm)

The big problem in ML community!

<img src='./assets/4_4.png'></img> - Lots of bias in data!

# Probabilistic Sampling(Random Sampling)

<img src='./assets/4_5.png'></img>

<img src='./assets/4_6.png'></img>

If you just do random sampling, there is a black swam.

<img src='./assets/4_7.png'></img>

<img src='./assets/4_10.png'></img>

<img src='./assets/4_11.png'></img>

<img src='./assets/4_12.png'></img>

<img src='./assets/4_13.png'></img>

When sampling from original population is infeasible, try sampling from correlated population, then do some math.

[重要性採樣](https://zh.wikipedia.org/zh-tw/%E9%87%8D%E8%A6%81%E6%80%A7%E9%87%87%E6%A0%B7)

<img src='./assets/4_14.png'></img>

reservior : 水庫(n.)

[水塘抽樣](https://zh.wikipedia.org/zh-tw/%E6%B0%B4%E5%A1%98%E6%8A%BD%E6%A8%A3)

<img src='./assets/4_15.png'></img>

<img src='./assets/4_16.png'></img>

* with replacement - approximate true population, also no covariance between two chosen sample - bagging
* a.k.a. random-forest
* why we train nn without replacement? any experiements compare the two of them?
  + **Because empirically it's converged faster**

<img src='./assets/4_17.png'></img>

<img src='./assets/4_18.png'></img>

## Sampling SOP

<img src='./assets/4_9.png'></img>

[A Data Scientist’s Guide to 8 Types of Sampling Techniques](https://www.analyticsvidhya.com/blog/2019/09/data-scientists-guide-8-types-of-sampling-techniques/)

# Class Imblance

<img src='./assets/4_19.png'></img>

[Andrew Ng: Bridging AI's Proof-of-Concept to Production Gap](https://www.youtube.com/watch?v=tsPuVAMaADY&ab_channel=StanfordHAI)

<img src='./assets/4_20.png'></img>

<img src='./assets/4_21.png'></img>

<img src='./assets/4_22.png'></img>

<img src='./assets/4_23.png'></img>

<img src='./assets/4_24.png'></img>

## Solution

<img src='./assets/4_25.png'></img>

## Resampling

<img src='./assets/4_26.png'></img>

<img src='./assets/4_27.png'></img>

<img src='./assets/4_28.png'></img>

<img src='./assets/4_29.png'></img>

They basically doesn't work well on high dimentional data.

## Weight Balancing

<img src='./assets/4_30.png'></img>

incentivize 激勵(v.) - Give more weight to rare classes - then you incentivize the model to learn to classify them better.

<img src='./assets/4_31.png'></img>

[Focal Loss for Dense Object Detection](https://arxiv.org/pdf/1708.02002.pdf)

[機器/深度學習: 損失函數(loss function)- Huber Loss和 Focal loss](https://chih-sheng-huang821.medium.com/%E6%A9%9F%E5%99%A8-%E6%B7%B1%E5%BA%A6%E5%AD%B8%E7%BF%92-%E6%90%8D%E5%A4%B1%E5%87%BD%E6%95%B8-loss-function-huber-loss%E5%92%8C-focal-loss-bb757494f85e)

[損失函數的設計(Loss Function)](https://medium.com/@CinnamonAITaiwan/cnn%E6%A8%A1%E5%9E%8B-%E6%90%8D%E5%A4%B1%E5%87%BD%E6%95%B8-loss-function-647e13956c50)

## Algorithms

<img src='./assets/4_32.png'></img>

sampling minorty samples and same numbers of majority, then boostraping - bagging

<img src='./assets/4_33.png'></img>

boosting

# Data Augmentation

<img src='./assets/4_34.png'></img>

<img src='./assets/4_35.png'></img>

<img src='./assets/4_36.png'></img>

<img src='./assets/4_37.png'></img>

## mixup and random erease idea work well on different domain

<img src='./assets/4_38.png'></img>

<img src='./assets/4_39.png'></img>

<img src='./assets/4_40.png'></img>

think more about data augmentation, you'll get good result on your problem.

# Feature Engineering

<img src='./assets/4_41.png'></img>

<img src='./assets/4_42.png'></img>

<img src='./assets/4_43.png'></img>

<img src='./assets/4_44.png'></img>

# Data Leakage

<img src='./assets/4_45.png'></img>

<img src='./assets/4_46.png'></img>

<img src='./assets/4_47.png'></img>

<img src='./assets/4_48.png'></img>

<img src='./assets/4_49.png'></img>

Type of leakage is important!

<img src='./assets/4_50.png'></img>

How to avoid leakage is also important.

# Feature Engineering also caused overfitting, and cost

<img src='./assets/4_51.png'></img>

Maintining / develop cost : additional feature, make sure they work properly.

How to manage the features?

<img src='./assets/4_52.png'></img>

# Model Selection and Training

<img src='./assets/4_53.png'></img>

<img src='./assets/4_54.png'></img>

<img src='./assets/4_55.png'></img>

<img src='./assets/4_56.png'></img>

<img src='./assets/4_57.png'></img>

<img src='./assets/4_58.png'></img>

https://slideslive.com/38923183/deep-learning-with-bayesian-principles

<img src='./assets/4_59.png'></img>

<img src='./assets/4_60.png'></img>

<img src='./assets/4_61.png'></img>

Model evaluation.

<img src='./assets/4_62.png'></img>
