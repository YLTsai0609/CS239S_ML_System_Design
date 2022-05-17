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

* push new items to users (new items have no clicks, not possible to be recommend)

### Positional features

<img src='./assets/10_25.png'></img>

User click the item due to good recommendation or just position?

ans : training your data with positional features

<img src='./assets/10_26.png'></img>

design a model only predict the prob when **user saw the items**

### How might degenerate feedback loops occur?
