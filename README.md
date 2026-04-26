Big Data Pipeline: U.S. Border Crossing Analysis

Project Overview
This project analyzes U.S. border crossing data using a complete Big Data pipeline built with Apache Spark and MongoDB. The dataset contains over 273,000 records of monthly crossings at U.S. ports of entry. The goal is to process large-scale data, perform analysis, and extract meaningful insights about transportation patterns and trends.

Team Members
Group 35 – CrossBorder
Muhamed Aniss Lotfy
Jie Xu
Mu Zhao
Weiwei Zhang

Dataset
Name: U.S. Border Crossing Entry Data
Size: 273,391 rows and 10 columns

The dataset contains monthly border crossing volumes, including attributes such as port name, state, border, date, transportation type, and crossing volume. It is suitable for Big Data analysis because it spans many years and includes a large number of records.

Problem Statement
This project investigates how border crossing patterns have changed over time. The main questions include identifying which border has the highest traffic, which transportation types dominate, how COVID-19 affected crossings, and which ports experienced growth or decline between 2019 and 2024.

Project Objectives
The main goals of the project are to process large datasets using Apache Spark, store and query data efficiently using MongoDB, perform analytical queries using Spark and MongoDB, compare performance across different methods, and generate insights through analysis and visualization.

Methodology
The project follows a structured pipeline. The dataset is first loaded into a Spark DataFrame. Data cleaning and preprocessing are performed, including removing missing values and extracting new features such as year and month. The processed data is then analyzed using both Spark DataFrame operations and Spark SQL queries. After processing, the data is stored in MongoDB, where additional queries and aggregations are performed. Finally, results are visualized and interpreted.

Implementation
Apache Spark is used to load and transform the dataset. Aggregations are performed to compute totals by border, transportation type, and year. Both the DataFrame API and Spark SQL are used to ensure correctness and flexibility.

MongoDB is used as the storage layer. The data is stored as documents, where each record contains fields such as border, port name, date, measure, and value. Indexes are created on important fields to improve query performance, and sharding is demonstrated to show scalability.

Queries performed in the project include total crossings by border, total crossings by transportation type, yearly trends, and identification of top ports by activity.

Results and Insights
The analysis shows that the U.S.-Mexico border has significantly higher crossing volumes than the U.S.-Canada border. Personal vehicles and personal vehicle passengers are the dominant transportation types. The impact of COVID-19 is clearly visible, with a sharp decrease in crossings during 2020 and 2021, followed by partial recovery. Some ports experienced strong growth between 2019 and 2024, while others showed decline, indicating changes in cross-border traffic patterns.

Performance Evaluation
The project compares execution times between Spark DataFrame operations, Spark SQL queries, and MongoDB aggregation. MongoDB performs fastest for simple aggregations, while Spark SQL is slightly faster than the DataFrame API. Spark caching is tested, but it provides limited improvement due to the relatively small dataset size.

Optimization Techniques
Several optimization techniques are applied, including Spark caching, analysis of execution plans, and MongoDB indexing. These techniques demonstrate how performance can be improved in larger-scale scenarios.

Visualizations
The project includes visualizations such as COVID-19 impact analysis, peak month analysis for top ports, and charts showing port growth and decline. These visualizations help identify trends and support the conclusions drawn from the data.

Challenges
The main challenges include handling data cleaning and preprocessing, optimizing query performance, and integrating Spark with MongoDB. Ensuring consistency across different processing methods was also an important aspect.

Future Work
Future improvements could include real-time data processing using Spark Streaming, applying machine learning models for prediction, and integrating additional external datasets to enrich the analysis.

How to Run the Project
The project is implemented in a Jupyter Notebook. To run it, ensure that Python, PySpark, and MongoDB are installed. Start MongoDB locally, open the notebook file, and run all cells in order. This will load the data, process it, store it in MongoDB, and execute the analysis.

Project Structure
The repository contains the main notebook file for the analysis, the dataset file, the presentation, and this README file.

Conclusion
This project demonstrates a complete Big Data pipeline using Apache Spark and MongoDB. It shows how large datasets can be processed, analyzed, and optimized to generate meaningful insights about real-world patterns.
