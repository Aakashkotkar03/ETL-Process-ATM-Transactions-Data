Problem Statement
In this segment, you will get to know more about the problem statement for the ETL project, which you will be going through in this project. 

In the next video, our expert will walk you through the detailed problem statement for the ETL project.

As discussed in the video, banks have to refill the ATMs when the money goes below a specific threshold limit. 

 

This depends on the activity and the area where a particular ATM is located as well as the weather, day of the week, etc.

 

In our project, Spar Nord Bank is trying to observe the withdrawal behavior and the corresponding dependent factors to optimally manage the refill frequency. Apart from this, other insights also have to be drawn from the data.

 

Coming to the analysis part, you will be tasked to carry out the calculations to perform the following analytical queries:

Top 10 ATMs where most transactions are in the ’inactive’ state

Number of ATM failures corresponding to the different weather conditions recorded at the time of the transactions

Top 10 ATMs with the most number of transactions throughout the year

Number of overall ATM transactions going inactive per month for each month

Top 10 ATMs with the highest total amount withdrawn throughout the year

Number of failed ATM transactions across various card types

Top 10 records with the number of transactions ordered by the ATM_number, ATM_manufacturer, location, weekend_flag and then total_transaction_count, on weekdays and on weekends throughout the year

Most active day in each ATMs from location "Vejgaard"

 

Your overall task in this project will be to build a batch ETL pipeline to read transactional data from RDS, transform and load it into target dimensions and facts on Redshift Data Mart(Schema).


Please note that the source data and target schema details are provided to better understand the source and targets, which would help design the ETL pipeline. Once the data is loaded into Redshift, you would have to write the analytical queries discussed above.

 

We have data from more than 100 ATMs across Denmark. Data is captured for every transaction including, card type, location, date, time, ATM type, etc.

 

Also, the transaction amount field in the data set was added separately using a random function for the analysis purpose. 

 

Spar Nord Bank has also built a dimensional model datastore (ATM Data Mart) on this ATM transaction data to understand the ATM usage pattern. This exact schema(target schema) of this Data Mart will be provided to you for the sake of this project. Basically, this will be the schema according to which you will be creating tables in Redshift. 

 

Broadly you will be performing the following task-

Extracting the transactional data from a given MySQL RDS server to HDFS(EC2) instance using Sqoop.

Transforming the transactional data according to the given target schema using PySpark. 

This transformed data is to be loaded to an S3 bucket.

Creating the Redshift tables according to the given schema.

Loading the data from Amazon S3 to Redshift tables.

Performing the analysis queries.


In the next segment, you will learn more about the data set, which you will be dealing with in this project.


Additional Content
If you want to get clarity on the concepts of Dimension Model and Data Mart, you can refer to the relevant segments in the Data Warehousing and ETL module. Anyways the Dimensional Model(target schema) to be used in this project will be provided to you.
Data Marts - A data mart is a simple form of a data warehouse that is focused on a single subject (or functional area), such as Sales or Finance or Marketing.

Dimensional modelling - Dimensional modelling includes a set of methods, techniques and concepts for use in data warehouse design.


Dataset Description
Now, in this segment, you will get to know about the data set that you are dealing with in this project. Our expert Ganesh will walk you through the details of the data set in the next video.

This dataset comprises around 2.5 million records of withdrawal data along with weather information at the time of the transactions from around 113 ATMs from the year 2017.

This data set contains various types of transactional data as well as the weather data at the time of the transaction, such as:

Transaction Date and Time: Year, month, day, weekday, hour

Status of the ATM: Active or inactive

Details of the ATM: ATM ID, manufacturer name along with location details such as longitude, latitude, street name, street number and zip code

The weather of the area near the ATM during the transaction: Location of measurement such as longitude, latitude, city name along with the type of weather, temperature, pressure, wind speed, cloud and so on

Transaction details: Card type, currency, transaction/service type, transaction amount and error message (if any)