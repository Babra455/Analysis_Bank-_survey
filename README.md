    Executive Summary
This project focused on analyzing a bank customer satisfaction survey collected from various African countries. The dataset contained responses in both English and French, requiring data translation, cleaning, integration, and analysis before meaningful insights could be extracted. 
The project simulates a real-world data analytics workflow, beginning from raw, inconsistent survey data to a final structured report that informs decision-making.The final deliverable includes cleaned data, pivot tables, statistical tests, and summarized insights in an Excel workbook.

The main goals of the project were to clean, merge, and standardize survey responses from bilingual datasets, ensuring consistency and accuracy. It involved transforming and summarizing the data to uncover patterns across country, gender, and group segments. Correlation analysis was conducted to identify significant relationships within the data. Additionally, the project aimed to build a structured and automated analysis pipeline to streamline future data processing. Finally, the findings were presented using pivot tables and summary reports in Excel for clear and actionable insights.
The dataset represents bank customers’ perceptions and experiences.The data shape (3263, 38) meaning dataset contains:

- 3263 rows → representing individual survey responses ,
- 38 columns → representing the different questions collected in the survey.

The cleaning process was done entirely in Python, using pandas and numpy, as these tools are highly efficient for data manipulation.
Loaded both the English and French datasets and used .info(), .head(), and .describe() to examine structure, data types, and missing values.
I focused on standardizing the column names and cleaning the bilingual entries in the dataset. I began by checking for duplicates to ensure data accuracy, and also reviewed the dataset for any missing columns. To handle the bilingual nature of the data, I displayed random examples containing both English and French text. From there, I extracted and retained only the English content from both the column headers and the cell values. As a result, the dataset is now fully standardized in English, with all French text removed—making it clean, consistent, and ready for further analysis.

 I cleaned and processed open-ended survey responses, removing inconsistencies and standardizing text. The cleaned dataset loaded with a shape of (3263, 27), with all columns translated to English and French content removed for clarity.

To understand the age distribution of respondents, I created custom age brackets, grouping the ages into:  
- Less than 17 years
- 18–24
- 25–29 
- 30–34  
- 35–39  
- 40–44  
- 45–54  
- 55–64  
- 65+

Each age group was then mapped to a corresponding numeric value to support analysis. Using value counts, I generated a bar chart showing how many respondents fall into each bracket. This provided a clear visualization of the most represented age group in the survey.

Lastly, I computed a correlation matrix, highlighting a strong positive correlation (0.587) between:  
- Overall satisfaction with the bank and  
- Likelihood to recommend the bank to friends/family

This suggests that satisfied customers are more likely to promote their bank, an insight valuable for customer experience strategies.

From the pivot tables, I observed that the majority of survey respondents identified as male (2225) compared to female (1038). When broken down by country, Cameroon, South Africa, and Nigeria had the highest number of responses. Gender distribution across countries revealed that males consistently outnumbered females in all participating countries.

Additionally, analyzing the average satisfaction scores per country showed that Ghana (3.77) and Nigeria (3.70) had the highest average satisfaction with banking services, while Côte d'Ivoire (2.94) recorded the lowest. This breakdown provided valuable insights into both demographic representation and customer satisfaction across regions.

Recommendations & Automation Plan
This dataset contains key recommendations to improve the survey data process, focusing on data quality, automation, visualization, and efficiency.
- Data Quality:  
  Implement validation checks at survey submission to reduce missing or inconsistent responses.

- Automation (Python):  
  Use a Python script with pandas and openpyxl to automatically clean, summarize, and export new survey data each cycle. Schedule it with Windows Task Scheduler or cron.

- Automation (Excel Macro):  
  Create a macro to remove duplicates, fill blanks with NA and refresh all pivot tables with a single button click.

- Visualization:  
  Use Excel charts or Power BI dashboards linked to this workbook for live updates.
- Efficiency:  
  Store the cleaning script on a shared folder so all analysts can reuse it when new survey data arrives.
