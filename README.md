# SQL-Witch-Trial-Analysis

# Witchcraft Database SQL Exploration  

## Project Overview  
This project is focused on practicing SQL queries and extracting insights from the **Witchcraft** database.  

I have always been interested in the history of witch trials, and I believe it's important to recognize the many parallels that exist between historic witch trials and ongoing issues of marginalized groups becoming targets of legal and societal punishment. By analyzing this dataset, I hope to understand trends in witchcraft accusations and how they might reflect larger historical forces.  

## Files in This Repo  
- `witchcraft_analysis.ipynb` – Jupyter Notebook with SQL queries and findings.  
- `witchcraft_analysis.html` – HTML version for quick viewing.  

## Dataset / Database Info  
The **Witchcraft database** is hosted on a MySQL server and contains records of individuals accused of witchcraft, certain demographic characteristics, trial outcomes, evidence, etc. 

## SQL Concepts Practiced  
Throughout this project, I explored several key SQL techniques, including:  

- **Filtering & Aggregation**: Used `WHERE`, `GROUP BY`, and `FROM` to analyze trends on select data.  
- **Joins**: Combined tables to examine relationships between different variables.  
- **Subqueries**: Extracted specific subsets of data for clearer insights.  
- **Counting & Ranking**: Used `ORDER BY` and `COUNT` to identify key patterns.  

## Key Findings  
Some of my interesting findings:

- **Gender Disparities**: The majority of accused individuals were women, but the majority of accusers were male. There was a maximum of 48 male accusers in one single trial.
- **Trial Outcomes**: The most common sentencing outcome was execution, but the second most common sentencing type was the accused being released. Some were banished or excommunicated. On average, trials that resulted in a 'guilty' verdict involved about 1.3 more accusers than those resulting in a 'not guilty' verdict.
- **Torture and Confessions**: Less than 25% of the trials actually involved a confession from the accused. There was a confession in 63.5% of torture trials even though the confession rate for all trials overall was only 23.5%. So it looks like torture played a crucial role in forcing confessions out of the accused when torture was involved.

## How to Run  
If you want to explore this dataset yourself, you'll need:  

1. **A Python Environment** with Jupyter Notebook and the `%load_ext sql` magic command.  
2. **Access to the Witchcraft Database** (this project assumes a MySQL server setup).  

Once set up, you can execute the queries within a Jupyter Notebook or any SQL environment.  

### Example Query  
To determine the proportion of female accused, you can run:  

```sql
num_female = %sql SELECT COUNT(*) FROM accused WHERE sex = 'Female'
num_total = %sql SELECT COUNT(*) FROM accused
proportion_female = num_female[0][0] / num_total[0][0]
print(f"Propotion of accused that ar female: {proportion_female}")
