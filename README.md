# SQL-Witch-Trial-Analysis

# Witchcraft Database SQL Exploration  

## Project Overview  
This project is focused on practicing SQL queries and extracting insights from the **Witchcraft** database.  

I’ve always been interested in historical patterns of social control, especially how certain groups—often marginalized ones—become targets of legal or societal punishment. By analyzing this dataset, I hope to understand trends in witchcraft accusations and how they might reflect larger historical forces.  

## Files in This Repo  
- `witchcraft_analysis.ipynb` – The Jupyter Notebook with SQL queries and findings.  
- `witchcraft_analysis.html` – The HTML version for quick viewing.  

## Dataset / Database Info  
The **Witchcraft database** is hosted on a MySQL server and contains records of individuals accused of witchcraft, their demographics, trial outcomes, and other contextual details. This dataset provides an opportunity to explore historical patterns and trends in accusations.  

## SQL Concepts Practiced  
Throughout this project, I explored several key SQL techniques, including:  

- **Filtering & Aggregation**: Used `WHERE`, `GROUP BY`, and `HAVING` to analyze trends.  
- **Joins**: Combined tables to examine relationships between different variables.  
- **Subqueries**: Extracted specific subsets of data for deeper insights.  
- **Sorting & Ranking**: Used `ORDER BY` and `LIMIT` to identify key patterns.  

## Key Findings  
Some of the interesting insights I found:  

- **Gender Disparity**: The majority of accused individuals were women, but the conviction rates varied by gender.  
- **Regional Trends**: Some areas had significantly higher accusation rates, potentially due to social or political factors.  
- **Trial Outcomes**: A surprising number of accused individuals were acquitted or received lesser punishments.  
- **Temporal Patterns**: Accusations seemed to spike in certain years, possibly linked to historical events.  

## How to Run  
If you want to explore this dataset yourself, you'll need:  

1. **A Python Environment** with Jupyter Notebook and the `%load_ext sql` magic command.  
2. **Access to the Witchcraft Database** (this project assumes a MySQL server setup).  
3. **A MySQL Connector** like `sqlalchemy` (if running queries outside Jupyter).  

Once set up, you can execute the queries within a Jupyter Notebook or any SQL environment.  

### Example Query  
To get a sense of the most common accusations, you can run:  

```sql
SELECT accusation_type, COUNT(*) AS count  
FROM accusations  
GROUP BY accusation_type  
ORDER BY count DESC;  
