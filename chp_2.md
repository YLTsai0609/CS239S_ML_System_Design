# Design a ML System

<img src='./asserts/2_1.png'></img>

# Goal of ML System Design

1. Reliability
2. Scalability
3. Maintainability
4. Adaptability

<img src='./asserts/2_2.png'></img>

## Reliability

<img src='./asserts/2_3.png'></img>

The chanllenge : What does "correct" means for ML system

when there are no ground truth labels?

<img src='./asserts/2_4.png'></img>

翻譯說 : 嚴禁吃地板(正確意思應該為，嚴禁吃東西，會弄髒地板)

## Scalability

<img src='./asserts/2_5.png'></img>

<img src='./asserts/2_6.png'></img>

## Maintainability

<img src='./asserts/2_7.png'></img>

### Subject matter expert

they helps a lot

<img src='./asserts/2_8.png'></img>

<img src='./asserts/2_9.png'></img>

no code ML helps this? (this is an intresting question!)

## Adaptability

<img src='./asserts/2_10.png'></img>

the feature discovery, and auto updating.

# Different type of ML systems

1. batch prediction vs online prediction
2. cloud computing vs edge computing
3. offline learning vs online online

## Batch prediction vs online prediction

<img src='./asserts/2_11.png'></img>

<img src='./asserts/2_12.png'></img>

misnomer : 誤稱(n.)

<img src='./asserts/2_13.png'></img>

There is a hybird approach.

<img src='./asserts/2_14.png'></img>

## cloud computing vs edge computing

<img src='./asserts/2_15.png'></img>

<img src='./asserts/2_16.png'></img>

caveat (v./n.) 警告

edge computing is more easier to access more user data!

<img src='./asserts/2_17.png'></img>

There is also a hybird approach =)

<img src='./asserts/2_18.png'></img>

### The future ML system

<img src='./asserts/2_19.png'></img>

## Offline learning vs online learning

<img src='./asserts/2_20.png'></img>

<img src='./asserts/2_21.png'></img>

<img src='./asserts/2_22.png'></img>

# Iterative Process

<img src='./asserts/2_23.png'></img>

So true!!! It's ... just expectation.

<img src='./asserts/2_24.png'></img>

So ture!!! The reality hit me EVERYTIMES!

<img src='./asserts/2_25.png'></img>

<img src='./asserts/2_26.png'></img>

Actually, your work and your team may occupy a pieces. The other team stand the other pieces. So the strategy is communication and be prepared!

## Project Scoping

<img src='./asserts/2_27.png'></img>

One of the most important things is, 

in a company doesn't konw ML/DL well, force them to communicate with you about project scope at the first time may be useless. You need prove the ML functionality and value first(means you need to do all of the things at the first time.)

## Data Management

<img src='./asserts/2_28.png'></img>

data comsumer?

## Model development

<img src='./asserts/2_29.png'></img>

## Deployment

<img src='./asserts/2_30.png'></img>

## Monitoring and maintenace

<img src='./asserts/2_31.png'></img>

## Business Analysis

<img src='./asserts/2_31.png'></img>

This part can be pre-design and post evaluation.

# Details and case study of every stage of iterative process

# Project scoping

<img src='./asserts/2_32.png'></img>

<img src='./asserts/2_33.png'></img>

Still some exceptions(例外情況)

<img src='./asserts/2_34.png'></img>

There is a lot of options to do that.

<img src='./asserts/2_35.png'></img>

<img src='./asserts/2_36.png'></img>

Side effects:

Extreme and hatful political content will be a big part when we tring maximizing engagement.

facebook, youtube also part of it.

## from goal to objective (modeling)

Goals -> Objective (more psecific)

start here

<img src='./asserts/2_37.png'></img>

<img src='./asserts/2_38.png'></img>

Not Safe For Work(MSFW) - sex content, job content maybe

<img src='./asserts/2_39.png'></img>

filter fake news and rank them by quality, finally, CTR.

<img src='./asserts/2_40.png'></img>

<img src='./asserts/2_41.png'></img>

<img src='./asserts/2_42.png'></img>

<img src='./asserts/2_43.png'></img>

[A Neural Algorithm of Artistic Style](https://arxiv.org/pdf/1508.06576.pdf)

Custom loss is widely used, just need more experiemnts to make sure how to make it work. But it is not good for ML System design.

<img src='./asserts/2_44.png'></img>

<img src='./asserts/2_45.png'></img>

Just like a stacked model.

A simple logistic regression based on two model input, give $\alpha, \beta$, then we don't need to retrain whole 2 model when we wanna optimized a better $\alpha, \beta$

## decouple helps a lot

<img src='./asserts/2_46.png'></img>

1. easier training - multi-objective -> two stage single objective
2. easier to tweak your system(dynamic tweak with the busniess subject.)
3. easier for maintenance - different objectives might need difference maintenance schedules.

## Constraint of project

<img src='./asserts/2_47.png'></img>

<img src='./asserts/2_48.png'></img>

<img src='./asserts/2_49.png'></img>

<img src='./asserts/2_50.png'></img>

<img src='./asserts/2_51.png'></img>

legacy code will be a contraint.

## Evaluation

<img src='./asserts/2_52.png'></img>
