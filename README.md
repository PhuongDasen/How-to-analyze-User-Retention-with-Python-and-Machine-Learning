# [PYTHON] Cohort Analysis: How to analyze User Retention
<h1>I. Introduction</h1>
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
  <li>Using Python to analyze transaction data from KPMG and creating a cohort that allows stakeholders to assess user engagement starting from their first transaction.</li>
</ul>
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
