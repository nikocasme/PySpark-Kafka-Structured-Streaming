# PySpark-Kafka-Structured-Streaming
This repository contains code for performing structured streaming operations with Apache Kafka in PySpark.

## Overview
In this project, we utilize structured streaming with Apache Kafka to perform real-time data processing on flight delay information. The goal is to calculate the average delay for each destination airport and continuously update this calculation as new data arrives.

## Functionality
The main functionality of this project includes:

* Defining a function retrasoMedio to calculate the average delay for each destination airport.
* Creating a streaming DataFrame to read from Kafka topic retrasos.
* Structuring the data to extract destination and delay fields from JSON messages.
* Applying the retrasoMedio function to the streaming DataFrame to calculate average delays in real-time.
* Displaying the results by querying the streaming DataFrame.

## File Structure
**retraso_medio.py:** Contains the implementation of the retrasoMedio function and the structured streaming operations.
**data_producer.py:** Python script to produce sample JSON messages to the Kafka topic retrasos.
**requirements.txt:** List of dependencies required to run the code.

# Usage
Ensure that you have Apache Kafka set up and running.
Install the required dependencies using pip install -r requirements.txt.
Run the data_producer.py script to produce sample JSON messages to the Kafka topic retrasos.
Execute the code in retraso_medio.py to perform the structured streaming operations.
Monitor the output by querying the temporary view retrasosAgg.

## Sample Data
Sample JSON messages to be sent to the Kafka topic retrasos:
{"dest": "GRX", "arr_delay": 2.6}
{"dest": "MAD", "arr_delay": 5.4}
{"dest": "GRX", "arr_delay": 1.5}
{"dest": "MAD", "arr_delay": 20.0}

## Requirements
Apache Spark
Apache Kafka
Python 3.x
PySpark
pyspark.sql module

## License
This project is licensed under the MIT License - see the LICENSE file for details.

# Author
**nikocasme**

# Acknowledgments
This project is inspired by the activities from the UNIR Master's in Big Data Analysis and Interpretation course.
