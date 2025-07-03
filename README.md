<p align="center">
  <img src="https://github.com/user-attachments/assets/d982466c-adab-48f2-b889-3130a128d788" width="90%">
</p>
<h1> 📊 How to analyze User Retention with Python and Machine Learning</h1>
Author: Phuong Dasen<br>
Tool: Python and Machine Learning<br>

## 📌 Table of Contents
- [📌 Background & Overview](#-background--overview)
- [📁 Dataset Description & Data Structure](#-dataset-description--data-structure)
- [🧠 Design Thinking Process](#-design-thinking-process)
- [📊 Key Insights & Visualizations](#-key-insights--visualizations)
- [🔍 Final Conclusion & Recommendations](#-final-conclusion--recommendations) 
  
## [📌 Background & Overview](#-background--overview)

<h2>1. About Cohort Analysis</h2>
  <b>What is cohort and cohort analysis?</b>
  <ul>
    <li> A cohort is a group of users who share a common characteristic, and cohort analysis is a tool to measure their engagement over time. </li>
    <li>Cohort analysis helps to differentiate between actual improvements in user engagement and those that may be driven by growth, while vanity indicators do not provide the same level of insight.</li>
  </ul>
  <h3>Three major types of Cohort</h3>
  <ul>
    <li>Time cohorts: customers who signed up for a product or service during a particular time frame.</li>
    <li>Behavior cohorts: customers who purchased a product or subscribed to a service in the past.</li>
    <li>Size cohorts: refer to the various sizes of customers who purchase the company's products or services.</li>
  </ul>
  <h3> Which tpye of cohort is for this project?</h3>
  <ul>
    <li>I will focus on performing Cohort Analysis based on Time (Time cohorts)</li>
    <li>Customers will be divided into acquisition cohorts depending on the month of their first purchase.</li>
    <li>The cohort index would then be assigned to each of the customer's purchases, which will represent the number of months since the first transaction.</li>
    </ul>
<h2>2. Business Questions</h2>
<ul>
  <li>One ecommerce company has a project on predicting churned users in order to offer potential
promotions.</li>
  <li>Using Python to analyze transaction data from KPMG and creating a cohort that allows stakeholders to assess user engagement starting from their first transaction.</li>
</ul>

## [📁 Dataset Description & Data Structure](#📁-dataset-description--data-structure)  

### 📌 Data Source
- Source: KPMG Dataset
- - Format: .csv
## ⚒️Main Process 
🔍 Import libraries<br>


📤 Load KPMG dataset <br>
<img width="700" alt="Screenshot 2025-07-03 at 3 05 00 PM" src="https://github.com/user-attachments/assets/38b0684f-1910-4188-92f4-1318a8d644dc" /><br>

🔍 Filtering oders_status is approved<br>
<img width="700" alt="Screenshot 2025-07-03 at 3 04 53 PM" src="https://github.com/user-attachments/assets/8977273f-685a-438e-8511-3a6c13240f8e" /><br>


📤 Create a function to get month from transaction_date <br>
<img width="700" alt="Screenshot 2025-07-03 at 3 09 31 PM" src="https://github.com/user-attachments/assets/a0140e9f-a019-4f93-8616-8aa497c46e5e" />


🔍 Convert transaction date data type: from string to datetime<br>
<img width="700" alt="Screenshot 2025-07-03 at 3 09 37 PM" src="https://github.com/user-attachments/assets/5c9934e7-a4e6-4f4a-b821-c17e11aeb85a" />

📤 Create tarnsaction_date column based on month and store in TransactionMonth



📤 Query Output <br>
<img width="700" alt="Screenshot 2025-07-02 at 10 49 46 AM" src="https://github.com/user-attachments/assets/2be72812-1e12-439f-8229-c3da1e06ed7f" /><br>

🔍Average number of pageviews by purchaser type (purchasers vs non-purchasers) in June, July 2017<br>

<img width="700" alt="Screenshot 2025-07-02 at 10 50 13 AM" src="https://github.com/user-attachments/assets/025c3b49-1eae-4243-8282-c88b2914ac68" /><br>
📤 Query Output <br>
<img width="700" alt="Screenshot 2025-07-02 at 10 50 39 AM" src="https://github.com/user-attachments/assets/58efd013-c7c7-4969-92ae-056fa72e5936" /><br>

🔍 Average number of transactions per user that made a purchase in July 2017<br>

<img width="700" alt="Screenshot 2025-07-02 at 11 15 23 AM" src="https://github.com/user-attachments/assets/e11d0b9d-ba4d-4a9f-b0f2-0dd5f2d34384" /><br>
📤 Query Output <br>
<img width="700" alt="Screenshot 2025-07-02 at 10 50 39 AM" src="https://github.com/user-attachments/assets/58efd013-c7c7-4969-92ae-056fa72e5936" /><br>

🔍 Average amount of money spent per session. Only include purchaser data in July 2017<br>

<img width="700" alt="Screenshot 2025-07-02 at 11 15 42 AM" src="https://github.com/user-attachments/assets/7282c299-b9c6-4f9d-af98-3be893990af8" /><br>
📤 Query Output <br>
<img width="700" alt="Screenshot 2025-07-02 at 11 15 54 AM" src="https://github.com/user-attachments/assets/e6d781cb-5165-4c37-bfc0-ef5d8eb045f6" /><br>

🔍 Other products purchased by customers who purchased product "YouTube Men's Vintage Henley" in July 2017. Output should show product name and the quantity was ordered<br>

<img width="700" alt="Screenshot 2025-07-02 at 11 16 11 AM" src="https://github.com/user-attachments/assets/33e22dc9-4180-4b18-ac4f-a0f3e4ce6638" /><br>
📤 Query Output <br>
<img width="700" alt="Screenshot 2025-07-02 at 11 16 26 AM" src="https://github.com/user-attachments/assets/3859b8d9-df0d-4cf5-a00e-755e4047f25a" /><br>

🔍Calculate cohort map from product view to addtocart to purchase in Jan, Feb and March 2017<br>

<img width="1000" alt="Screenshot 2025-07-02 at 11 17 10 AM" src="https://github.com/user-attachments/assets/2cf99014-34d5-47ac-bf88-ba0055109a4a" /><br>
📤 Query Output <br>
<img width="900" alt="Screenshot 2025-07-02 at 11 17 21 AM" src="https://github.com/user-attachments/assets/f1ed82f2-8b1d-47e8-a580-c8209f0d4351" />

## 🔎 Final Conclusion & Recommendations






<h1>II. Data Visualization with Python</h1>
- MoM Retention Rate for Customer Transaction Data <br>
<img width="829" alt="Screenshot 2025-05-12 at 09 35 44" src="https://github.com/user-attachments/assets/0472e084-7b7c-41b0-a584-d3158f6265fa" />
<h1>III. Insights</h1>
<ul>
  <li>Customers who register and place their first order in July 2017 have a high retention rate (up to 48.1%) after 5 months of operation. </li>
  <li>Customers who register and place their first order in April 2047 have a stable and relatively high retention rate: 45.1% (4th month), 42.1% (5th month), and 42.7% (7th month).</li>
  <li>Customers who register and place their first order in May 2017 also have a fairly high and stable retention rate: 40.4%, 39% and 41.3% in the 2nd, 3 rd and 4th month activities.</li>
  <li>Looking at the above insights, we can see that customers who start ordering from mid-year 4, 5, 6, 7, 8 tend to order statble, and relatively higher than the rest months of the year.</li>
  <li>Customer who place orders at the beginning of January and February only show stablility, nothing special.</li>
  <li>KPMG's year-to-date retention rate is quite good, all 30% or more (except 11st month at 25.5%)</li>
</ul>
<h1>Recommendations</h1>
<ul>
  <li>There should be attractive preferential policies for customers in the first months of the year to increase teh order rate (retention) over the months.</li>
  <li>The Mid-year months have higher retention rates than other months -> need to dive into why (with relevant data, and visualizatin of other data) to apply to other months of the year.</li>
</ul>
