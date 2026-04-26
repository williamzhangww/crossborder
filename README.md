# Big Data Pipeline: U.S. Border Crossing Analysis

## Project Overview
This project analyzes U.S. border crossing data using a Big Data pipeline built with **Apache Spark** and **MongoDB**.

The dataset contains over **273,000 records** of monthly crossings at U.S. ports of entry. The goal is to process large-scale data, perform analysis, and extract meaningful insights about transportation patterns and trends.

---

## Team Members
**Group 35 – CrossBorder**

- Muhamed Aniss Lotfy  
- Jie Xu  
- Mu Zhao  
- Weiwei Zhang  

---

## Dataset
- **Name:** U.S. Border Crossing Entry Data  
- **Size:** 273,391 rows, 10 columns  

### Main Features
- Port Name  
- State  
- Border (US-Canada / US-Mexico)  
- Date  
- Measure (transport type)  
- Value (number of crossings)  

This dataset is suitable for Big Data analysis because it spans multiple years and contains a large number of records.

---

## Problem Statement
This project investigates how border crossing patterns have changed over time.

### Key Questions
- Which border has the highest traffic?  
- Which transportation types dominate?  
- How did COVID-19 affect crossings?  
- Which ports grew or declined between 2019 and 2024?  

---

## Project Objectives
- Process large datasets using Apache Spark  
- Store and query data efficiently using MongoDB  
- Perform analytical queries using Spark and MongoDB  
- Compare performance across different approaches  
- Generate insights through analysis and visualization  

---

## Methodology

### Data Processing Pipeline
CSV Dataset  
→ Spark DataFrame  
→ Data Cleaning  
→ Feature Engineering  
→ Spark Analysis (DataFrame + SQL)  
→ MongoDB Storage  
→ MongoDB Aggregation  
→ Visualization & Insights  

### Preprocessing Steps
- Selected relevant columns  
- Removed missing values  
- Converted date format  
- Extracted **Year** and **Month**  

---

## Implementation

### Apache Spark
- Loaded dataset into Spark DataFrame  
- Performed transformations and aggregations  
- Used both DataFrame API and Spark SQL  

### MongoDB
- Stored processed data as documents  
- Schema includes:
  - Border  
  - Port Name  
  - State  
  - Date  
  - Measure  
  - Value  

- Implemented indexing for performance  
- Demonstrated sharding for scalability  

### Queries Performed
- Total crossings by border  
- Total crossings by measure  
- Total crossings by year  
- Top ports by activity  

---

## Results and Insights
- The **U.S.-Mexico border** has significantly higher traffic than the U.S.-Canada border  
- **Personal vehicles** dominate crossings  
- **COVID-19 caused a major drop** in crossings during 2020–2021  
- Some ports showed strong growth, while others declined  

---

## Performance Evaluation

| Method | Execution Time |
|--------|--------------|
| Spark DataFrame | ~0.29 s |
| Spark SQL | ~0.23 s |
| MongoDB Aggregation | ~0.11 s |

### Observations
- MongoDB is fastest for aggregation queries  
- Spark SQL is slightly faster than the DataFrame API  
- Caching had limited impact due to dataset size  

---

## Optimization Techniques
- Spark caching  
- Execution plan analysis  
- MongoDB indexing  

---

## Visualizations
The project includes:
- COVID-19 impact analysis  
- Peak month analysis  
- Port growth and decline charts  
- Transportation pattern trends  

These visualizations help identify trends and support conclusions.

---

## Challenges
- Data cleaning and preprocessing  
- Performance tuning  
- Integration between Spark and MongoDB  

---

## Future Work
- Real-time processing using Spark Streaming  
- Machine learning predictions  
- Integration with external datasets  

---

## How to Run the Project

### Requirements
- Python 3  
- PySpark  
- MongoDB (running locally)

### Steps
1. Start MongoDB  
2. Open the Jupyter Notebook  
3. Run all cells in order:
   - Data loading  
   - Data processing  
   - MongoDB insertion  
   - Analysis  

---

## Project Structure
- `Border_Crossing_Analysis.ipynb`  
- `Border_Crossing_Entry_Data.csv`  
- `README.md`  
- `presentation.pdf`  

---

## Conclusion
This project demonstrates a complete Big Data pipeline using Apache Spark and MongoDB. It shows how large datasets can be processed, analyzed, and optimized to generate meaningful insights about real-world patterns.
