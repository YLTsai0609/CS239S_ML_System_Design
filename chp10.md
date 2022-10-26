# Ref

docx : https://docs.google.com/document/d/14uX2m9q7BUn_mgnM3h6if-s-r0MZrvDb-ZHNjgA1Uyo/edit#heading=h.2p8lce0bcck

pptx : https://docs.google.com/presentation/d/1tuCIbk9Pye-RK1xqiiZXPzT8lIgDUL6CqBkFSYZXkbY/edit#slide=id.g112c1e99806_0_529


# ML Failure Diagnosis

## Natural lavels

Label 和斯斯一樣分 3 種，手標標籤(hand label)、自然標籤(natural label)、透過程式碼所產生的標籤(programmic label)

<img src='./assets/10_1.png'></img>

<img src='./assets/10_2.png'></img>

<img src='./assets/10_3.png'></img>

## Delayed when we collecting natural labels

<img src='./assets/10_4.png'></img>

<img src='./assets/10_5.png'></img>

## Dirty labels in nature labels

<img src='./assets/10_6.png'></img>

<img src='./assets/10_7.png'></img>

# ML failure

<img src='./assets/10_8.png'></img>

<img src='./assets/10_9.png'></img>

<img src='./assets/10_10.png'></img>

<img src='./assets/10_11.png'></img>

<img src='./assets/10_12.png'></img>

<img src='./assets/10_13.png'></img>

<img src='./assets/10_14.png'></img>

## Edge Case

<img src='./assets/10_15.png'></img>

<img src='./assets/10_16.png'></img>

## Degenerate feedback loops

<img src='./assets/10_17.png'></img>

<img src='./assets/10_18.png'></img>

* the model prediction becmoe more homogenous.

<img src='./assets/10_19.png'></img>

Not only the recommendation system.

If you use nautral labels, degenerated feedback loops might happend.

<img src='./assets/10_20.png'></img>

if a feature importance become more important over time, it will be a suspecious feature.

<img src='./assets/10_21.png'></img>

## Detect degenerated feedback loops

<img src='./assets/10_22.png'></img>

### Randomization

<img src='./assets/10_23.png'></img>

<img src='./assets/10_24.png'></img>

* since feedback is biased (user only give feedback when the item is recommend to them)
* Tiktok push popular items(but not in prediction) to get unbiased feedback.
  * tradeoff by user experience.
  * [some math trick to avoid it - Recommendations as Treatments: Debiasing Learning and Evaluation 2016, citation 306](https://arxiv.org/pdf/1602.05352.pdf)

### Positional features

<img src='./assets/10_25.png'></img>

User click the item due to good recommendation or just position?

#### Naive Approach
ans : 

training : data with positional features (e.g. is_first)

inference : set all testing set (is_first = False)

might not be enough to combat degenerate feedback loops.

#### 2 models approach


<img src='./assets/10_26.png'></img>

design a model only predict the prob when **user saw the items**

### Data Distribution Drift

source dist : data the model trained

target dist : data the model run inference

concept from transfer learning.


<img src='./assets/10_27.png'></img>

* Notations
* $X$ for features, $Y$ for targets
* $P(X, Y)$ - joint distribution of features and targets (聯合機率，表達 features, targets 同時發生的機率分佈)
* $P(Y|X)$ - conditional distribution(條件機率) of targets when features are seen
  * the modeling distribution which ML models.
* training data : sampling from joint distribution

e.g. Is an email spam given the content
* $P(X)$ - email content
* $P(Y)$ - is the email spam

We can decompse $P(X, Y)$ in two ways

$P(X, Y) = P(Y|X)P(X)$ 

$P(X, Y) = P(X|Y)P(Y)$

<img src='./assets/10_28.png'></img>

### Covariate shift 

* Covariate - 協變量，也就是 X

<img src='./assets/10_29.png'></img>

<img src='./assets/10_30.png'></img>

<img src='./assets/10_35.png'></img>

Case I - Cancer detection

* **特徵集的分布變了，但特徵和 Target 的關係沒變**
* **most widely studied forms of data distribution shift**
* cancer prediction
  * you have a bias data (person who dosn't have a cancer won't see the doctor - which you collect your data)
  * production 容易誤判年紀大於 40 時，癌症風險高估
* Strategy?
  * 對齊 Source dist, Target dist
  * Source dist 不要隨機抽，要照著 Target dist 來抽



Case II - Potential VIP user detection

<img src='./assets/10_31.png'></img>

* New marketing campaign attracting users from with higher income
* P(income) changed (if we have such this data)
* P(convert to paid user | free user) remains the same.
* We have a biased data (income is higher)
* Strategy?

<img src='./assets/10_36.png'></img>


<img src='./assets/10_32.png'></img>

fix it by importance weighting

```
Importance weighting consists of two steps: estimate the density ratio between the real-world input distribution and the training input distribution, then weight the training data according to this ratio, and train an ML model on this weighted data
```

importance weighting : 

[paper - Rethinking Importance Weighting for Deep
Learning under Distribution Shift 2020](https://arxiv.org/pdf/2006.04662.pdf)

[github, 16 stars](https://github.com/TongtongFANG/DIW)

### Label shift

<img src='./assets/10_34.png'></img>

<img src='./assets/10_33.png'></img>


* Target 改變了，但影響 Target, Features 之間的機制並沒有改變
* **$P(x)$ changes usually leads $P(Y)$ changed, since $P(Y|X)$ ususally remains the same**

### Concept Drift

* Target 和 features 之間的機制改變了
* features 沒改變

<img src='./assets/10_37.png'></img>

<img src='./assets/10_38.png'></img>

# During Operation

<img src='./assets/10_39.png'></img>

<img src='./assets/10_40.png'></img>

## Detecting shifts

<img src='./assets/10_41.png'></img>

<img src='./assets/10_42.png'></img>

<img src='./assets/10_43.png'></img>

<img src='./assets/10_44.png'></img>

[alibi-detect](https://github.com/SeldonIO/alibi-detect)

## Type of shifts

<img src='./assets/10_45.png'></img>

<img src='./assets/10_46.png'></img>

<img src='./assets/10_47.png'></img>


# Retraining Policy to against shifts

<img src='./assets/10_48.png'></img>

<img src='./assets/10_49.png'></img>


# Monitoring

<img src='./assets/10_50.png'></img>

<img src='./assets/10_51.png'></img>

<img src='./assets/10_52.png'></img>

<img src='./assets/10_53.png'></img>

<img src='./assets/10_54.png'></img>

<img src='./assets/10_55.png'></img>

<img src='./assets/10_56.png'></img>

<img src='./assets/10_57.png'></img>

<img src='./assets/10_58.png'></img>

* [pandas-profiling](https://github.com/ydataai/pandas-profiling)
* [facets](https://github.com/PAIR-code/facets)
* [great_expectations](https://github.com/great-expectations/great_expectations)
* pydantic or attrs

# Problems when monitoring features

<img src='./assets/10_59.png'></img>

<img src='./assets/10_60.png'></img>

<img src='./assets/10_61.png'></img>


# Monitoring --> Continual Learning

<img src='./assets/10_62.png'></img>