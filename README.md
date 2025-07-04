<p align="center">
  <img src="https://github.com/user-attachments/assets/d982466c-adab-48f2-b889-3130a128d788" width="90%">
</p>
<h1> 📊 How to analyze User Retention with Python and Machine Learning</h1>
Author: Phuong Dasen<br>
Tool: Python and Machine Learning<br>

## 📌 Table of Contents
- [📌 Background & Overview](#-background--overview)
- [📁 Dataset Description & Data Structure](#-dataset-description--data-structure)
- [⚒️ Main Process](#-main-Process)
- [📊 Visualizations](#-visualizations)
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
- Format: .csv
  
## [⚒️ Main Process](#-main-Process)

<img width="950" alt="Screenshot 2025-07-04 at 9 07 17 AM" src="https://github.com/user-attachments/assets/198c41e0-1753-4ed4-88bd-75669f76dc91" />
<img width="950" alt="Screenshot 2025-07-04 at 9 07 24 AM" src="https://github.com/user-attachments/assets/29442000-bee7-4815-84f6-141868980947" />
<img width="950" alt="Screenshot 2025-07-04 at 9 07 31 AM" src="https://github.com/user-attachments/assets/f33ab52e-b127-44e6-bd9a-40ffffc65577" />
<img width="950" alt="Screenshot 2025-07-04 at 9 07 38 AM" src="https://github.com/user-attachments/assets/77b77269-3a31-4c96-a52d-4d694f72cbb5" />
<img width="950" alt="Screenshot 2025-07-04 at 9 07 50 AM" src="https://github.com/user-attachments/assets/bd2783a4-3903-4fa7-9648-0bb19e69131d" />
<img width="950" alt="Screenshot 2025-07-04 at 9 07 56 AM" src="https://github.com/user-attachments/assets/98aff66d-2d5c-4fc9-ae1a-501ed7f62563" />
<img width="950" alt="Screenshot 2025-07-04 at 9 08 03 AM" src="https://github.com/user-attachments/assets/2eb48d52-0207-4d45-951d-7e5b82b7c107" />
<img width="950" alt="Screenshot 2025-07-04 at 9 08 11 AM" src="https://github.com/user-attachments/assets/303e05b8-44f2-47b8-9815-2f7ab5e115f8" />
<img width="950" alt="Screenshot 2025-07-04 at 9 08 23 AM" src="https://github.com/user-attachments/assets/e2ad0675-0251-49ec-a9fc-90465ffedd3c" />
<img width="950" alt="Screenshot 2025-07-04 at 9 08 29 AM" src="https://github.com/user-attachments/assets/56df3524-6974-402d-b3ec-dbefc9190caf" />
<img width="950" alt="Screenshot 2025-07-04 at 9 08 35 AM" src="https://github.com/user-attachments/assets/39013238-82f6-436b-bbf8-8e0eac54577a" />
<img width="950" alt="Screenshot 2025-07-04 at 9 08 47 AM" src="https://github.com/user-attachments/assets/0f0c5326-3568-425a-a327-6f5eb7954bed" />
<img width="950" alt="Screenshot 2025-07-04 at 9 08 55 AM" src="https://github.com/user-attachments/assets/7481d9bd-9714-45f6-800e-f8d787fd993b" />

## [📊 Visualizations](#-visualizations) 

- MoM Retention Rate for Customer Transaction Data <br>
<img width="950" alt="Screenshot 2025-05-12 at 09 35 44" src="https://github.com/user-attachments/assets/0472e084-7b7c-41b0-a584-d3158f6265fa" />

## [🔍 Final Conclusion & Recommendations](#-final-conclusion--recommendations) 
<h2>Final Conclusions</h2>
<ul>
  <li>Customers who register and place their first order in July 2017 have a high retention rate (up to 48.1%) after 5 months of operation. </li>
  <li>Customers who register and place their first order in April 2047 have a stable and relatively high retention rate: 45.1% (4th month), 42.1% (5th month), and 42.7% (7th month).</li>
  <li>Customers who register and place their first order in May 2017 also have a fairly high and stable retention rate: 40.4%, 39% and 41.3% in the 2nd, 3 rd and 4th month activities.</li>
  <li>Looking at the above insights, we can see that customers who start ordering from mid-year 4, 5, 6, 7, 8 tend to order statble, and relatively higher than the rest months of the year.</li>
  <li>Customer who place orders at the beginning of January and February only show stablility, nothing special.</li>
  <li>KPMG's year-to-date retention rate is quite good, all 30% or more (except 11st month at 25.5%)</li>
</ul>
<h2>Recommendations</h2>
<ul>
  <li>There should be attractive preferential policies for customers in the first months of the year to increase teh order rate (retention) over the months.</li>
  <li>The Mid-year months have higher retention rates than other months -> need to dive into why (with relevant data, and visualizatin of other data) to apply to other months of the year.</li>
</ul>
