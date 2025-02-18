
# BCG X : AI-POWERED FINANCIAL CHATBOT DEVELOPMENT

## BCG GenAI Job Simulation on Forage


## Project Overview

This project aims to develop an AI-powered chatbot that analyzes financial documents, specifically 10-K and 10-Q reports, to provide insights into corporate financial performance. The chatbot is designed to help users easily access and understand complex financial data through an interactive, user-friendly interface.

## Context

This project is undertaken as part of the GenAI Consulting team at Boston Consulting Group (BCG). The team has been approached by Global Finance Corp. (GFC), a leading financial institution, seeking a cutting-edge solution to enhance financial analysis capabilities. The goal is to create an AI-driven chatbot that can extract, analyze, and communicate key financial insights effectively.

## Objectives :

- Extracting financial data from ***10-K*** and ***10-Q*** documents.
- Conducting basic analysis to identify significant financial trends and indicators.
- Preparing and preprocessing data for integration into an AI model.
- Developing an AI-powered chatbot that provides interactive financial insights.

---

## Project Structure

The project is organized into two main tasks:

### Task 1: Extracting and Analyzing Financial Data

#### Objectives:
- Extract meaningful financial data from 10-K documents.
- Conduct a basic analysis to identify significant financial trends.
- Prepare and clean the data for AI model integration.

#### Key terms:
1. **10-K and 10-Q reports:** Annual and quarterly financial reports filed by publicly traded companies containing detailed information about financial performance. Here is an example of a 10-k repport from [Apple](https://d18rn0p25nwr6d.cloudfront.net/CIK-0000320193/c87043b9-5d89-4717-9f49-c4f9663d0061.pdf) for the last three years. The inofrmations we seek to find are can all be found at 
***Item 8. Financial Statements and Supplementary Data***
2. **GenAI:** A branch of AI focusing on generating new content, including text and data analysis, which is crucial for the chatbot's ability to interpret and communicate financial data.
#### Key Sections to Focus On:
1. **Income Statement**:
   - **Key Data Points:** Total revenue, cost of goods sold (COGS), operating expenses, net income.
   - **Extraction:** Identify year-over-year changes and trends.

2. **Balance Sheet**:
   - **Key Data Points:** Current assets, long-term assets, current liabilities, long-term liabilities, shareholders’ equity.
   - **Extraction:** Compare assets against liabilities to assess financial health.

3. **Cash Flow Statement**:
   - **Key Data Points:** Cash from operating activities, investing activities, and financing activities.
   - **Extraction:** Analyze cash generation and expenditure patterns to understand liquidity.

### Steps :

**Step 1: Data Extraction**
- Navigate to the SEC's EDGAR database:
    - [Microsoft](https://www.sec.gov/edgar/searchedgar/companysearch.html)
    - [Tesla](https://www.sec.gov/edgar/searchedgar/companysearch.html)
    - [Apple](https://www.sec.gov/edgar/searchedgar/companysearch.html)

- For each company, find the 10-K filings for the last three fiscal years. (2024-2023-2022)
- Extract the following financial figures:  
  - Total Revenue  
  - Net Income  
  - Total Assets  
  - Total Liabilities  
  - Cash Flow from Operating Activities  

**Step 2: Organize the Data**
- Compile the extracted data into an Excel spreadsheet for easy reference during your Python analysis.

**Step 3: Analyzing trends with pandas**

- Use pandas to calculate year-over-year changes for each financial metric. 
- We can do this by creating new columns in your DataFrame that represent the percentage change from one year to the next.
---


### Task 2: Developing an AI-Powered Financial Chatbot

#### Objectives:
- Develop an AI chatbot capable of analyzing financial data and providing insights.
- Integrate the extracted and analyzed data into the chatbot system.
- Test the chatbot for effective communication of financial insights and comparisons.

#### 2.1 Techniques for integrating financial data with chatbot functionalities :


Integrating financial data into the chatbot is about making static data dynamic and interactive. The aim is to transform the previously analyzed financial data into insightful responses that the chatbot can provide when prompted by user queries.

- **Data structuring:** Before integrating, we have to ensure that our financial data is structured in a way that allows the chatbot to access and interpret it easily. Using formats such as JSON or CSV can be helpful, so that we can map data points to specific queries.

- **Retrieval methods:** Implement simple retrieval methods that allow our chatbot to fetch the right piece of data based on the user's query. For instance, if a user asks about a company's net income, the chatbot should know how to find and present that specific data point.

- **Predefined data points:** Since we're focusing on predefined queries, associate each query with specific data points in our data set. This direct mapping simplifies the process of fetching and presenting data in response to user inputs.

#### 2.2 Communicating complex financial insights : 

The ultimate goal of your chatbot is to communicate complex financial insights in a way that's accessible and engaging. This involves presenting data in a manner that's informative and easy to understand.

- **Simplification and summarization:** Simplifying and summarizing financial insights. The use of clear, jargon-free language to explain financial concepts or data points. Remember, the user might not have a financial background.

- **Interactive dialogue design:** Design our chatbot's dialogue to be interactive. Encourage users to explore different queries by suggesting related topics or asking follow-up questions. This can improve user engagement and make the interaction more informative.

- **Visual aids:** While our focus is on text-based interaction, we have to consider describing how data visualization aids such as charts or graphs could be referenced or described by the chatbot to aid in understanding complex data.

#### Key Features:
- **Natural Language Processing (NLP)**: Enables the chatbot to understand and respond to user queries in natural language.
- **Financial Insights**: Provides in-depth analysis and comparisons of financial performance.
- **User-Friendly Interface**: Interactive platform designed for ease of use and accessibility.


---

## Data Sources

The project utilizes 10-K financial reports from the following companies:
1. **Microsoft (2024)**: [Link](https://microsoft.gcs-web.com/node/32871/html#item_8_financial_statements_and_supplem)
2. **Tesla (2024)**: [Link](https://www.sec.gov/Archives/edgar/data/1318605/000162828025003063/tsla-20241231.htm#ie9fbbc0a99a6483f9fc1594c1ef72807_1148)
3. **Apple (2024)**: [Link](https://d18rn0p25nwr6d.cloudfront.net/CIK-0000320193/c87043b9-5d89-4717-9f49-c4f9663d0061.pdf)

---

## Key Takeaways

- **Contextualizing AI in Finance**: Understand how AI transforms financial data into insightful analytics.
- **Identifying Financial Indicators**: Learn to recognize significant financial metrics crucial for AI analysis.
- **Preparing Data for AI**: Ensures clean, consistent, and structured data for accurate model predictions.
- **Chatbot Development**: Apply NLP and AI techniques to develop an interactive financial chatbot.

---

## 🛠 Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn)
- **Jupyter Notebook** for structured analysis and visualization
- **Excel** To save the information we get from the 10-K reports and use it as a spreadsheet for easy reference during your Python analysis.

## 📂 Project Structure
```
📦 BCG_GenAI_Financial_Chatbot  
┣ 📜 Task_One.ipynb   # Jupyter Notebook for Task One  
┣ 📜 Task_Two.ipynb   # Jupyter Notebook for Task Two  
┣ 📜 10K_Financial_Data.xlsx    # Excel Spreadsheet with the 10-K reports information  
┣ 📜 10K_Financial_Data.csv    # CSV version of the 10-K reports data for easier handling in Python  
┣ 📜 10K_Financial_Data_Enhanced.csv    # Enhanced CSV with calculated metrics and growth percentages  
┣ 📜 Certificate.pdf    # Certificate of completion or participation  
┣ 📜 README.md    # Documentation and overview of the project  


```

---

## Future Improvements

- Enhance NLP capabilities for more accurate financial interpretations.
- Integrate additional financial documents for comprehensive analysis.
- Implement advanced AI models for predictive financial analytics.

---


### 🏆 Author: Nassim BENCHIKH

---
