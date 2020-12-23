# Get Started with Data Engineering: Part 1
## Objectives:
1. Being able to exchange with Data Engineers
2. Figure out if you're interested to learn more about Data Engineering
------------------------
### Chapter 1: What is Data Engineering
1. [Data Engineering](#Data-Engineering) and [Big Data](#Big-Data)
2. [Data Engineers vs. Data Scientists]
3. Data Pipelines
### Chapter 2: How Data Storage Works
1. Structure vs. Unstructured Data
2. SQL
3. Storage Solutions: Data warehouse and Data lakes
### Chapter 3: How to move and process the data?
1. Processing
2. Scheduling
3. Cloud Computing
4. Parallel Computing
----------------------
#### Spotflix: A fictional music streaming compnany
-----------------
### Data Workflow:
![](https://github.com/Harsha2409/data-engineering-part1-blog/blob/main/workflow.PNG)
--------------------
### Data Engineering

**Data Engineers** are responsible for the first step of the Data Workflow process - ingesting collected data and storing it. They have a great responsibility as they lay the ground work for data analysts, data scientists and machine learning engineers.

If the data is scattered around, corrupted, and difficult to access, there's not much to prepare, explore, or experiment with. And that's exactly why you need a Data engineer: their job is to deliver the correct data, in the right form, to the right people, as efficiently as possible.

They ingest data from different sources, optimize the databases for analysis, and manage data corruption. Data engineers develop, construct, test, and maintain architectures such as databases and large-scale processing systems to process and handle massive amounts of data.

If you're not sure what this all means, that's okay! The article will unpack all this jargon and explain the what, why, and how.

### Big Data
Big data can be defined as data so large you have to think about how to deal with its size, because it's difficult to process using traditional data management methods.

![](https://github.com/Harsha2409/data-engineering-part1-blog/blob/main/big-data-graph.PNG)

This graph helps make sense of the growth of big data.In order of volume, big data is mainly composed of:
1. sensors and devices data
2. social media data
3. enterprise data and VoIP data.

#### The five Vs
Big data is commonly characterized by five Vs:
1. Volume (the quantity of data points)
2. Variety (type and nature of the data: text, image, video, audio)
3. Velocity (how fast the data is generated and processed)
4. Veracity (how trustworthy the sources are)
5. Value (how actionable the data is).

####Data engineers need to take all of this into consideration.

----------------------

### Data Engineers vs. Data Scientists

Now that you know how data flows through an organization, let's quickly prevent the confusion and assumptions that comes with the *Data Scientists* and *Data Engineers*.

We already know the responsibilities of Data Engineers - first step of [Data Workflow](#Data-Workflow)

