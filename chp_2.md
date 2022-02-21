# Design a ML System

<img src='./assets/2_1.png'></img>

# Goal of ML System Design

1. Reliability
2. Scalability
3. Maintainability
4. Adaptability

<img src='./assets/2_2.png'></img>

## Reliability

<img src='./assets/2_3.png'></img>

The chanllenge : What does "correct" means for ML system

when there are no ground truth labels?

<img src='./assets/2_4.png'></img>

翻譯說 : 嚴禁吃地板(正確意思應該為，嚴禁吃東西，會弄髒地板)

## Scalability

<img src='./assets/2_5.png'></img>

<img src='./assets/2_6.png'></img>

## Maintainability

<img src='./assets/2_7.png'></img>

### Subject matter expert

they helps a lot

<img src='./assets/2_8.png'></img>

<img src='./assets/2_9.png'></img>

no code ML helps this? (this is an intresting question!)

## Adaptability

<img src='./assets/2_10.png'></img>

the feature discovery, and auto updating.

# Different type of ML systems

1. batch prediction vs online prediction
2. cloud computing vs edge computing
3. offline learning vs online online

## Batch prediction vs online prediction

<img src='./assets/2_11.png'></img>

<img src='./assets/2_12.png'></img>

misnomer : 誤稱(n.)

<img src='./assets/2_13.png'></img>

There is a hybird approach.

<img src='./assets/2_14.png'></img>

## cloud computing vs edge computing

<img src='./assets/2_15.png'></img>

<img src='./assets/2_16.png'></img>

caveat (v./n.) 警告

edge computing is more easier to access more user data!

<img src='./assets/2_17.png'></img>

There is also a hybird approach =)

<img src='./assets/2_18.png'></img>

### The future ML system

<img src='./assets/2_19.png'></img>

## Offline learning vs online learning

<img src='./assets/2_20.png'></img>

<img src='./assets/2_21.png'></img>

<img src='./assets/2_22.png'></img>

# Iterative Process

<img src='./assets/2_23.png'></img>

So true!!! It's ... just expectation.

<img src='./assets/2_24.png'></img>

So ture!!! The reality hit me EVERYTIMES!

<img src='./assets/2_25.png'></img>

<img src='./assets/2_26.png'></img>

Actually, your work and your team may occupy a pieces. The other team stand the other pieces. So the strategy is communication and be prepared!

## Project Scoping

<img src='./assets/2_27.png'></img>

One of the most important things is, 

in a company doesn't konw ML/DL well, force them to communicate with you about project scope at the first time may be useless. You need prove the ML functionality and value first(means you need to do all of the things at the first time.)

## Data Management

<img src='./assets/2_28.png'></img>

data comsumer?

## Model development

<img src='./assets/2_29.png'></img>

## Deployment

<img src='./assets/2_30.png'></img>

## Monitoring and maintenace

<img src='./assets/2_31.png'></img>

## Business Analysis

<img src='./assets/2_31.png'></img>

This part can be pre-design and post evaluation.

# Details and case study of every stage of iterative process

# Project scoping

<img src='./assets/2_32.png'></img>

<img src='./assets/2_33.png'></img>

Still some exceptions(例外情況)

<img src='./assets/2_34.png'></img>

There is a lot of options to do that.

<img src='./assets/2_35.png'></img>

<img src='./assets/2_36.png'></img>

Side effects:

Extreme and hatful political content will be a big part when we tring maximizing engagement.

facebook, youtube also part of it.

## from goal to objective (modeling)

Goals -> Objective (more psecific)

start here

<img src='./assets/2_37.png'></img>

<img src='./assets/2_38.png'></img>

Not Safe For Work(MSFW) - sex content, job content maybe

<img src='./assets/2_39.png'></img>

filter fake news and rank them by quality, finally, CTR.

<img src='./assets/2_40.png'></img>

<img src='./assets/2_41.png'></img>

<img src='./assets/2_42.png'></img>

<img src='./assets/2_43.png'></img>

[A Neural Algorithm of Artistic Style](https://arxiv.org/pdf/1508.06576.pdf)

Custom loss is widely used, just need more experiemnts to make sure how to make it work. But it is not good for ML System design.

<img src='./assets/2_44.png'></img>

<img src='./assets/2_45.png'></img>

Just like a stacked model.

A simple logistic regression based on two model input, give $\alpha, \beta$, then we don't need to retrain whole 2 model when we wanna optimized a better $\alpha, \beta$, Or just a human control value!

## decouple helps a lot

<img src='./assets/2_46.png'></img>

1. easier training - multi-objective -> two stage single objective
2. easier to tweak your system(dynamic tweak with the busniess subject.)
3. easier for maintenance - different objectives might need difference maintenance schedules.

## Constraint of project

<img src='./assets/2_47.png'></img>

<img src='./assets/2_48.png'></img>

<img src='./assets/2_49.png'></img>

<img src='./assets/2_50.png'></img>

<img src='./assets/2_51.png'></img>

legacy code will be a contraint.

## Evaluation

<img src='./assets/2_54.png'></img>

## When to use ML?

<img src='./assets/2_55.png'></img>

<img src='./assets/2_56.png'></img>

<img src='./assets/2_57.png'></img>

<img src='./assets/2_58.png'></img>

<img src='./assets/2_59.png'></img>

<img src='./assets/2_60.png'></img>

<img src='./assets/2_61.png'></img>

## When NOT to use ML?

1. It's unehical.
2. Simple solution to do this trick.
3. It's impossible to get the right data.
4. One single prediction error can cause devastating consequences.
5. Every single decision the system makes must be exaplainable.
6. It's not cost effective.(maybe now it's not, but it'll be in the further.)

## It can be part of system

<img src='./assets/2_62.png'></img>

# Four Phase of ML Adaption

1. heuristic. - high cp!
2. Simplest ML model - validate hypothesis, validate pipeline.
3. Optimizing simple models - different objective func, feature engineering, more data, ensembling.
4. Complex model. 

<img src='./assets/2_63.png'></img>
<img src='./assets/2_64.png'></img>
<img src='./assets/2_65.png'></img>
<!-- <img src='./assets/2_66.png'></img> -->

# If I wanna pick a most important one from this chapter

Case study : 

ML goal breakdown into objective and constraint.

Building a ranking system of news feed.

pick a goal 

1. minimize the spread of misinformation.
2. maximize revenue from sponsered content.
3. maximize engagement. (we pick this for better user experience and longer app usage time)

Side effect : extreme and hateful political content will be a big part when we tring maximizing engagement.

To avoid side effect.

E.g. Ranking system for **wholesome** newsfeed.

| Goal                         | Objective                                     |
|------------------------------|-----------------------------------------------|
| General purpose of a project | Specific steps on how to realize that purpose |
| Maximize user's engagement   | 1. Filter out spam <br> 2. Filter out Not Safe For Work(NSFW) <br> 3. Filter out misinformation <br> 4. Rank post by quality. <br> 5. Rank post by how likely user will click on it                                         |

Decouple Multiple Objective Optimization.

$L_{total} = \alpha L_{quality} + \beta L_{engagement}$

Style transfer do this work!

But we can just combine two single model with coefficient.

Why?

1. Easier for training - only one object for each model.

2. Easier for tweak your system. ($\alpha$ % model optimized for quality + $\beta$ % model optmized for engagement)
3. easier for maintance - different objective might need different maintance schedules.

   * **Spamming technique evolve faster** than rhe way post quality ia perceived.
   * **Spamming filtering system** needs update more frequently than quality ranking system.

Constraint : 

1. Time
2. Buget
3. Performance
4. Privacy
5. Competitors
6. Legacy System

<img src='./assets/2_47.png'></img>

<img src='./assets/2_49.png'></img>

<img src='./assets/2_50.png'></img>

<img src='./assets/2_51.png'></img>
