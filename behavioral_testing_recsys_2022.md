# Ref

[ref](https://docs.google.com/presentation/d/e/2PACX-1vQZvsblf-15mwOs-f-UOxY9KoPcUaGS5Uof7i80Wyq1MQk5jUDkLIjLPWf5fFCf3DwxBsEx6QmsLjN0/pub?start=false&loop=false&delayms=3000&slide=id.g10a740b980a_1_1081)

[jacopotagliabue/reclist github star 178+](https://github.com/jacopotagliabue/reclist)

[paper - Beyond NDCG: behavioral testing of recommender systems with RecList, 2021](https://arxiv.org/pdf/2111.09963.pdf)


<img src='./assets/behaviorRec_1.png'></img>

# Model Evaluation

<img src='./assets/behaviorRec_2.png'></img>

Robustness of your system (at software engineering level)

<img src='./assets/behaviorRec_3.png'></img>

Nowdays, paper only care about **accuracy**

<img src='./assets/behaviorRec_4.png'></img>

<img src='./assets/behaviorRec_5.png'></img>

# Inspiration from behavior testing from nlp

<img src='./assets/behaviorRec_6.png'></img>

1. similar iteminfo (defined by item description or user click)
2. but not in the same price level

<img src='./assets/behaviorRec_7.png'></img>

# Behavior testing in recsys

<img src='./assets/behaviorRec_8.png'></img>

* sneakers - 運動鞋
* complementary item - 補充性物品(對應配件) (TV --> Cables)

<img src='./assets/behaviorRec_9.png'></img>


<img src='./assets/behaviorRec_10.png'></img>

1. similar - symmetric
2. complementary - asymmetric(there are levels)
3. some false positive impact more(fp for high LTV customer vs fp for low LTV customer)
   1. the prediction of data should be seperate by business impact

# Package - RecList

<img src='./assets/behaviorRec_11.png'></img>

<img src='./assets/behaviorRec_12.png'></img>

<img src='./assets/behaviorRec_13.png'></img>

<img src='./assets/behaviorRec_14.png'></img>

# E-commerce example

<img src='./assets/behaviorRec_15.png'></img>

<img src='./assets/behaviorRec_16.png'></img>

<img src='./assets/behaviorRec_17.png'></img>

<img src='./assets/behaviorRec_18.png'></img>

<img src='./assets/behaviorRec_19.png'></img>

<img src='./assets/behaviorRec_20.png'></img>

[colab](https://colab.research.google.com/drive/1Wn5mm0csEkyWqmBBDxNBkfGR6CNfWeH-?usp=sharing#scrollTo=JVVy-XhB8oVz)

* 看起來只是一個 framework，paper 中的知識吸收到即可，可以標註自己關心的 slice, 補充性配件等

