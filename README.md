# Get Started with Data Engineering: Part 1
## Objectives:
1. Being able to exchange with Data Engineers
2. Figure out if you're interested to learn more about Data Engineering
------------------------
### Chapter 1: [What is Data Engineering](#Chapter-1)
1. [Data Engineering](#11-Data-Engineering) and [Big Data](#Big-Data)
2. [Data Engineers vs. Data Scientists](#12-Data-Engineers-vs-Data-Scientists)
3. [Data Pipelines](#13-Data-Pipelines)
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
### Spotflix:

A fictional music streaming compnany

-----------------

# Chapter 1

----------------
## Data Workflow:
![](https://github.com/Harsha2409/data-engineering-part1-blog/blob/main/workflow.PNG)
--------------------
# 1.1 Data Engineering

**Data Engineers** are responsible for the first step of the Data Workflow process - ingesting collected data and storing it. They have a great responsibility as they lay the ground work for data analysts, data scientists and machine learning engineers.

If the data is scattered around, corrupted, and difficult to access, there's not much to prepare, explore, or experiment with. And that's exactly why you need a Data engineer: their job is to deliver the correct data, in the right form, to the right people, as efficiently as possible.

They ingest data from different sources, optimize the databases for analysis, and manage data corruption. Data engineers develop, construct, test, and maintain architectures such as databases and large-scale processing systems to process and handle massive amounts of data.

If you're not sure what this all means, that's okay! The article will unpack all this jargon and explain the what, why, and how.

# Big Data
Big data can be defined as data so large you have to think about how to deal with its size, because it's difficult to process using traditional data management methods.

![](https://github.com/Harsha2409/data-engineering-part1-blog/blob/main/big-data-graph.PNG)

This graph helps make sense of the growth of big data.In order of volume, big data is mainly composed of:
1. sensors and devices data
2. social media data
3. enterprise data and VoIP data.

## The five Vs
Big data is commonly characterized by five Vs:
1. Volume (the quantity of data points)
2. Variety (type and nature of the data: text, image, video, audio)
3. Velocity (how fast the data is generated and processed)
4. Veracity (how trustworthy the sources are)
5. Value (how actionable the data is).

## Data engineers need to take all of this into consideration.

----------------------

# 1.2 Data Engineers vs. Data Scientists

Now that you know how data flows through an organization, let's quickly prevent the confusion and assumptions that comes with the *Data Scientists* and *Data Engineers*.

We already know the responsibilities of Data Engineers - first step of [Data Workflow](#Data-Workflow)

**Data Scientists** interevene on the rest of the worflow. They prepare the data according to their analysis' needs, explore it and build insightful visualizations. They run experiments and/or build predictive models.

**Data Engineers** lay the ground work that makes Data Science activity possible. Let's see how.

Introducing ***Ava***, a Data Engineer  and ***Katie***, a Data Scientist at [Spotflix](#Spotflix)

|Ava|Katie|
|:---:|:---:|
|Ingest and Store Data|Exploit Data|
|Set up Databases|Access Databases|
|Build Data Pipelines|Use Pipeline outputs|
|Strong Software Skills|Strong Analytical Skills|

---------------------

# 1.3 Data Pipelines

You might have heard **'Data is the new Oil'** as first coined by the Economists. Let's follow this idea.

1. We extract Crude Oil from an oil field.
2. We move the Crude Oil to a distillation unit where we separate the oil into several products (gasoline, naphtha, kerosene, diesel, heavy oil, resideu etc)
3. Some products are sent directly to their final users. Eg: Some pipes go to Airport to deliver Kerosene.
4. Some are sent to storage facilities and stored in big tanks before being distributed to Gas stations. Eg: Gasoline.
5. Some products undergo several chemical transformations to create synthetic polymers. Eg: Naphtha is transformed to a polymer which is used to manufacture CDs. (CDs - yeah, so last century!!)

So, we have many pipelines tying the entire process together.

#### *Ava* follows a similar procedure to manage data for *Spotflix*. She creates and maintains **pipelines** to automate flow from one station to the next so that *Data Scientists* can use up-to-date, accurate and relevant data. Obviously, this isn't an easy task.

At *Spotflix*, we have multiple sources of data.
1. Users' actions and listening history from the mobile application, desktop application and the website.
2. Internal website used by HR at *Spotflix* for Payroll, hiring etc.

All this data is ingested in a [data lake.](#) We have our first **three pipelines.**
1. Mobile app -> Data lake
2. Desktop app -> Data lake
3. Website -> Data lake

Now, we will organize it into different [databases.](#)
1. Artists: Name, Number_of_followers
2. Albums: Label, Producer, Year_of_Release
3. Tracks: Name, Length, Featured_artists, number_of_listens
4. Playlists: Name, songs, date_of_creation
5. Customers: Name, account_open_date, subscription_tier (free, premium (monthly, yearly))
6. Employees: Name, Department, Salary, manager
7. many many more..!

So, we have atleast **six new pipelines** now - from data lake to each database.

Now, let's think of this in terms of oil.

1. What can be saved directly? hmm... album photos! - all images in another database. No processing Required. **One more pipeline.**
2. Do we need to segregate anything? Employees database in different [tables](#) - by department (sales, engineering, support etc) - **Three more pipelines**
    * We can also split these department tables by office - US, Belgium, UK etc **Three more pipelines**. 
    * Okay, where will this be used? If *Data Scientists* had to investigate Employee Turnover, this is the data they would use.
3. Tracks database (Transformation)  -> Is the format correct? Is it readable (lyrics/transcripts)? Video? **One more pipeline** for transformation i.e. data processing. Then a new clean tracks database will be stored. **One more pipeline**. This can be used by *Data Scientists* to develop Content-based/Similarity Recommendation Engine.

