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

$P(Y|X) = \frac{P(X, Y)}{P(X)}$ --> $P(Y, X) = P(Y|X)P(X) = P(X|Y)P(Y)$

$P(X, Y)$ --> X, Y 同時發生

<img src='./assets/10_28.png'></img>

### Covariate shift

<img src='./assets/10_29.png'></img>

<img src='./assets/10_30.png'></img>

Case I - Cancer detection

* 特徵集的分布變了，但特徵和 Target 的關係沒變
* most widely studied forms of data distribution shift
* cancer prediction
  * you have a bias data (person who dosn't have a cancer won't see the doctor - which you collect your data)


Case II - Potential VIP user detection

<img src='./assets/10_31.png'></img>

* New marketing campaign attracting users from with higher income
* P(income) changed (if we have such this data)
* P(convert to paid user | free user) remains the same.
* We have a biased data (income is higher)
* Strategy?

<img src='./assets/10_32.png'></img>

fix it by importance weighting.

### Label shift

<img src='./assets/10_34.png'></img>

<img src='./assets/10_33.png'></img>

**$P(x)$ changes usually leads $P(Y)$ changed, since $P(Y|X)$ ususally remains the same**