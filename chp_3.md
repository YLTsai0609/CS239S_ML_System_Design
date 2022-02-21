# Data Engineering / Data Management

<img src='./assets/3_1.png'></img>

# Mind vs Data

<img src='./assets/3_2.png'></img>

profoundly : 深刻地 adv.

<img src='./assets/3_3.png'></img>

<img src='./assets/3_4.png'></img>

debate : 辯論 n.

# AI Needs

<img src='./assets/3_5.png'></img>

<img src='./assets/3_6.png'></img>

The Moore's Law in AI computation.

<img src='./assets/3_7.png'></img>

# Data Engineering 101

<img src='./assets/3_8.png'></img>

## Data source

<img src='./assets/3_9.png'></img>

<img src='./assets/3_10.png'></img>

https://www.onaudience.com/audience-data

## format to store

<img src='./assets/3_11.png'></img>

<img src='./assets/3_12.png'></img>

Serialization! 

[Intro to parquet I](https://codertw.com/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80/406598/)

[Intro to parquet II](https://www.itread01.com/content/1520454216.html)

<img src='./assets/3_13.png'></img>

## Column-Based

<img src='./assets/3_13.png'></img>

<img src='./assets/3_14.png'></img>

## Row-Based

<img src='./assets/3_15.png'></img>

## OLTP & OLAP

<img src='./assets/3_16.png'></img>

<img src='./assets/3_17.png'></img>

<img src='./assets/3_18.png'></img>

## ETL

<img src='./assets/3_19.png'></img>

<img src='./assets/3_20.png'></img>

from OLTP to OLAP.

<img src='./assets/3_21.png'></img>

from Source data to semi-sort out data.(data warehouse, data mart, database, ...)

### Data Lake vs Data Warehouse(Unstructure vs Structure)

<img src='./assets/3_22.png'></img>

<img src='./assets/3_23.png'></img>

## Batch Processing vs Online Processing

<img src='./assets/3_24.png'></img>

### Case Study : Fraud Detection in ride sharing

<img src='./assets/3_25.png'></img>

<img src='./assets/3_26.png'></img>

<img src='./assets/3_27.png'></img>

<img src='./assets/3_28.png'></img>

<img src='./assets/3_29.png'></img>

<img src='./assets/3_30.png'></img>

<img src='./assets/3_31.png'></img>

[Machine learning with Flink in Weibo - Qian Yu, 2020](https://www.youtube.com/watch?v=WQ520rWgd9A&ab_channel=FlinkForward)

[flink - open source stream processing framework with powerful stream- and batch-processing capabilities.](https://github.com/apache/flink)

<img src='./assets/3_32.png'></img>

Can we make them from 2 pipeline to 1 ? - Yes, use flink

## Microservice vs REST APIs

<img src='./assets/3_33.png'></img>

<img src='./assets/3_34.gif'></img>

<img src='./assets/3_35.png'></img>

If we need price optimization

incentivize : 激勵(v.)

### Problem of Request-Driven

<img src='./assets/3_36.png'></img>

### Event-driven

<img src='./assets/3_37.png'></img>

### Barrier to Streamming Processing

<img src='./assets/3_38.png'></img>

<img src='./assets/3_39.png'></img>

### Case Study - Uber’s Big Data Platform: 100+ Petabytes with Minute Latency

<img src='./assets/3_40.png'></img>

100 + PB data, processing in minutes(data engineering part)

<img src='./assets/3_41.png'></img>

# Creating Training Dataset

**Creating training data with clean ground truth is the bottleneck, not algorithm!**

<img src='./assets/3_42.png'></img>

Realword data is a monster!

## Split data

### General thought

<img src='./assets/3_43.png'></img>

<img src='./assets/3_44.png'></img>

<img src='./assets/3_45.png'></img>

### A better way to deal with dynamics dataset

<img src='./assets/3_46.png'></img>

### Data : The more the better?

<img src='./assets/3_47.png'></img>

<img src='./assets/3_48.png'></img>

<img src='./assets/3_49.png'></img>

1. Rule of thumb, how many data should we use as training data? 10%, enought diversity will be a good start, [from Practical Lessons from Predicting Clicks on Ads at Facebook](http://quinonero.net/Publications/predicting-clicks-facebook.pdf)
2. Clean feature and correlation to the target is important! check    [risk_bound_for_interpolated_models](https://github.com/YLTsai0609/DataScience_Note/blob/master/risk_bound_for_interpolated_models.md)

### Label multiplicity

<img src='./assets/3_50.png'></img>

<img src='./assets/3_51.png'></img>

We need domain expert!!!!!

But too much expert, slow down the labelling task.

How to make this easier?

<img src='./assets/3_51.png'></img>

lineage : 血統(n.)

<img src='./assets/3_52.png'></img>

1. Clear problem definition.
2. Annotation training(train your labeller)
3. data lineage(track the data come from)
4. do some math trick on algorithm to make our algorithm know where label is correct(hard, less efficient)

### Programmatic labeling

<img src='./assets/3_53.png'></img>

commoditized : 商品化的(adj.)

<img src='./assets/3_54.png'></img>

<img src='./assets/3_55.png'></img>

<img src='./assets/3_56.png'></img>

<img src='./assets/3_57.png'></img>

A conmmunication dictionary!

SME : subject matter experts

LFs : label functions!

<img src='./assets/3_58.png'></img>

<img src='./assets/3_59.png'></img>

<img src='./assets/3_60.png'></img>

<img src='./assets/3_61.png'></img>

<img src='./assets/3_62.png'></img>

Use some math to help the poor grandson, he cannot get the money from grandma!

<img src='./assets/3_63.png'></img>

total agreement and disaggrement to solve this.

consistent : 一致的

[details - Accelerating Machine Learning with Training Data Management Alex Ratner 2019](https://www.datacouncil.ai/hubfs/DataEngConf/Data%20Council/Slides%20SF%2019/Accelerating%20Machine%20Learning%20with%20Training%20Data%20Management.pdf)

<img src='./assets/3_64.png'></img>

<img src='./assets/3_65.png'></img>

### Weak Supervision and more

supervision : 監督(v.)

<img src='./assets/3_66.png'></img>

[Weak Supervision: A New Programming Paradigm for Machine Learning Stanford AI Lab Blog](https://ai.stanford.edu/blog/weak-supervision/)

#### Semi Supervised

<img src='./assets/3_67.png'></img>

hashtag provide a similar story!

#### Weakly Supervised

<img src='./assets/3_68.png'></img>

Like the money in the email, poor grandson.

#### Active learning

<img src='./assets/3_69.png'></img>

help our system to find more valueable data point.

#### Transfer learning

<img src='./assets/3_70.png'></img>
