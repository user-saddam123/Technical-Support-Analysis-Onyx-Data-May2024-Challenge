# Technical Support Analysis Onyx Data May2024 Challenge

## Created & Analyzed by Saddam Ansari @Aspiring Data Analyst [Linkedin](https://www.linkedin.com/in/saddam-ansari-dataanalyst/)

### Live Dashboard at Novypro [Live_link_Novypro](https://project.novypro.com/Lj7DNu)
#



## Objective:

The objective of this project is to analyze the performance of a **Technical Support Centre** by examining ticket volumes, resolution times, and customer satisfaction rates. 

The analysis will identify **peak ticket creation times**, compare response and resolution times against **Service Level Agreements (SLAs)**, and explore customer satisfaction across various categories. 

Additionally, the project will evaluate **daily, weekly, and monthly ticket trends**, assess differences between workday and weekend volumes, analyze ticket topics and support channels, and evaluate agent performance in adhering to SLAs. 

This comprehensive analysis aims to provide actionable insights to improve the efficiency and effectiveness of the Technical Support Centre.



## Dataset Overview:

The provided dataset consists of **2,330 rows of technical support data**, capturing a comprehensive range of information related to support tickets. Each row in the dataset represents a unique support ticket with the following columns:

### Key Attributes Included:

| Column name | Description |
|--|--|
|Status:| Indicates the current state of the ticket (e.g., Closed, In progress, Resolved).|
|Ticket ID:| A unique identifier for each support ticket.|
|Priority:| The priority level of the ticket (e.g., Low, Medium, High).|
|Source: |The medium through which the ticket was created (e.g., Email, Phone, Chat).|
|Topic:| The main subject or issue of the support request (e.g., Feature request, Product setup, Purchasing and invoicing).|
|Agent Group: |The support team or line handling the ticket (e.g., 1st line support, 2nd line support).|
|Agent Name:| The name of the support agent handling the ticket.|
|Created time:| The timestamp when the ticket was created.|
|Expected SLA to resolve:| The expected Service Level Agreement (SLA) time to resolve the ticket.|
|Expected SLA to first response:| The expected SLA time for the first response.|
|First response time: |The actual timestamp when the first response was made.|
|SLA for first response:| Indicates whether the first response was within the SLA.|
|Resolution time: |The actual time taken to resolve the ticket.|
|SLA for resolution:| Indicates whether the resolution was within the SLA.|
|Close time:| The timestamp when the ticket was closed.|
|Agent interactions:| The number of interactions the agent had with the ticket.|
|Survey results: |Customer satisfaction survey results associated with the ticket.|
|Product group:| The category of the product involved in the support request (e.g., Custom software development, Ready to use Software).|
|Support Level:| The tier level of the support provided (e.g., Tier 1, Tier 2).|
|Country:| The country from which the ticket was submitted.|
|Latitude:| The latitude coordinate of the ticket's origin.|
|Longitude:| The longitude coordinate of the ticket's origin.|

This dataset offers a rich source of information for analyzing various aspects of technical support performance. 
#

## Data Preparation and Cleaning Steps
During the project, several data preparation and cleaning steps were performed after loading the dataset into Power BI to ensure accurate analysis. These steps included correcting data types, handling blank values, and creating new columns for more detailed insights:

### 1. Correcting Data Types:
Upon loading the dataset into Power BI, it was observed that many columns had incorrect data types. These were systematically corrected to ensure proper analysis. For example, date and time fields were converted to DateTime data types, numerical fields were corrected to appropriate numerical types, and categorical fields were converted to text.

### 2. Handling Blank Values:
Some columns contained blank values. These blanks were left as they were, either because they were not critical for the analysis or because imputing them might have introduced bias or inaccuracies.

### 3. Creating New Columns:
   * **Time Difference in Minutes:** A new column was created to calculate the time difference in minutes between the ticket creation time and the first response time. This column helps in evaluating the responsiveness of the support team.
   * **Time Difference in Hours:** Another new column was created to calculate the time difference in hours between the ticket creation time and the resolution time. This metric is essential for understanding how long it takes to resolve issues.
   * **Weekday or Weekend:** A column was added to differentiate between weekdays and weekends. Saturdays and Sundays were marked as weekends, while the remaining days were marked as weekdays. This distinction helps in analyzing ticket volume and performance variations across different days of the week.
   * **Working Hours Indicator:** A column named "Working Hours" was created to indicate whether the ticket creation time fell within standard working hours (9 AM to 5 PM). Tickets created between 9 AM and 5 PM were marked as "Working Hours," while those created outside this timeframe were marked as "After Working Hours." This helps in assessing the support team's performance during and outside of regular business hours.

By performing these data preparation and cleaning steps, the dataset was refined to support a more accurate and insightful analysis of the Technical Support Centre's performance. 
#

## Dashboard Overview
Based on the project requirements, I have created a single-page Power BI report-type dashboard. While it is somewhat lengthy, with a height of approximately 3950 pixels and a width of 1280 pixels, it comprehensively covers and presents all the insights needed by stakeholders. 
#

# Detailed Insights Explanation:

## Section_1: Ticket Volume Trends:
This section presents ticket volume trends from various perspectives. Let's dive into the insights:
#

### Ticket Volume and Status Distribution:

![Screenshot 2024-05-23 083027](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/d43f2dd3-e7b3-4edc-a8d7-4abc0e722bff)

During the period from January 2, 2023, to December 31, 2023, a **total of 2,330 tickets were created**. These tickets represent customer service requests.

#### Distribution by Status:
 * **Closed:** 50.3% of the total tickets, amounting to 1,173 tickets, have been closed.
 * **Resolved:** 31.7% of the total tickets, which equals 739 tickets, have been resolved.
 * **In Progress:** 17.2% of the total tickets, translating to 400 tickets, are still in progress.
 * **Open:** 0.8% of the total tickets, or 18 tickets, remain open.
#

![Screenshot 2024-05-23 083930](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/4c96e1da-28d8-4a6a-b6b5-f5df0eee3c97)

### Ticket Volume by Day Type:
Using a doughnut chart, we can easily see that:

 * **84.94%** of the total requests, amounting to **1,979 tickets**, were generated on **workdays**.
 * **15.06%**, which equals 351 tickets, were created on **weekends**.

📝 **Note:** For this analysis, weekends are considered to be Saturday and Sunday, while all other days are classified as workdays.
#

### Ticket Volume by Work Hours:
Another doughnut chart reveals that:

 * **67.21%** of the total tickets, amounting to **1,566 tickets**, were generated **after work hours**.
 * **32.79%**, or 764 tickets, were created during work hours.

📝 **Note:** In this context, "after work hours" refers to any time after 5 PM and before 9 AM. These insights provide a clear understanding of when support requests are most frequently made, aiding in better resource planning and allocation.
#

### Monthly Ticket Volume Trend
![Screenshot 2024-05-23 084914](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/af8ce89b-b172-4fa7-9e08-fb6ecc98ea24)

A line chart was utilized to visualize the trend in ticket volumes over the months, revealing the following insights:
 * The **highest ticket volume occurred in January**, with a total of **224 tickets**, representing **9.6% of the total**.
 * The **second-highest month was May**, with **219 tickets**, followed by **November with 213 tickets**.
 * The **lowest ticket volume was observed in February**, with **159 tickets**, accounting for** 6.8% of the total**.

These observations provide valuable insights into monthly variations in support ticket volumes, aiding in resource planning and performance evaluation.
#

### Total Tickets by Week Number
A line chart was utilized to visualize the total ticket volumes across different weeks. Here are the key insights:

![Screenshot 2024-05-23 084926](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/f86902f3-b8b0-4a1e-9c14-1ea69cbef0fb)

 * **Week 3** had the **highest number of tickets, totaling 61**.
 * Following closely, **Week 18 recorded 58 tickets**, indicating the second-highest volume.
 * Conversely, **Week 52** experienced the **lowest ticket volume**, with **only 24 tickets** recorded.

These observations shed light on weekly fluctuations in ticket volumes, providing valuable insights for resource management and operational planning.
#

### Creation Time by Day and Time
The purpose of this analysis is to identify peak creation times and peak creation days. Here are the key insights:

📝 **Note:** Before interpreting this visualization, it's important to note that darker shades of blue indicate high ticket creation, while lighter shades represent low ticket creation.

![Screenshot 2024-05-23 084945](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/476a7758-cf8f-44ff-80df-19b41ccb971a)

 * **Peak Creation Time:** Analysis reveals that, excluding weekends, **ticket creation peaks around 3 PM on almost every day**.
 * **Peak Creation Day:** **Wednesday** emerges as the day with the **highest ticket generation**, totaling **439 tickets**. Following closely, **Monday sees 410 tickets**, making it the second-highest day. Friday ranks third with a notable ticket count.

These insights provide valuable information for scheduling support staff and optimizing resource allocation to address peak demand periods effectively.
#

## Section_2: Ticket Content and Resolution:
In this section, we will explore ticket distribution based on content and insights related to ticket resolution time. Let's delve into the insights:
#

### Ticket Volume by Topic
The analysis reveals the distribution of tickets across different topics:

![Screenshot 2024-05-23 091219](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/f42e3934-ec22-4c5e-816f-6258eff66331)

 * **Product Setup**: This group has the **highest ticket volume**, comprising** 630 tickets**, which accounts for** 27% of the total**. It indicates a significant number of support requests related to setting up products.
 * **Training Request:** Conversely, this topic has the **lowest ticket volume**, suggesting fewer support requests related to training.

📝 **Note:** Furthermore, users can drill down into the ticket distribution based on specific product groups, enabling a more detailed analysis of support needs within each product category.

This breakdown provides valuable insights into the areas where customers require the most assistance, facilitating targeted support strategies and resource allocation to address prevalent issues effectively.
#

### Ticket Volume by Source

📝 **Note:** Before proceeding, it's important to note that the "Source" indicates the channel through which customers connect for help.

![Screenshot 2024-05-23 091235](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/173613fb-7896-49ca-97df-668bdf3e17c0)

#### The analysis reveals:

 * The majority of tickets, totaling **1,234 and representing 52% of the total**, were generated via **email**.
 * **Chat accounted for 850 tickets**, making up a significant portion of the total.
 * **Phone calls** resulted in the **lowest ticket** volume, with only **246 tickets generated**, representing **10.56% of the total**.

These insights provide valuable information about the preferred channels through which customers seek support, aiding in resource allocation and service optimization to enhance customer satisfaction.
#

### Ticket Volume by Support Level

📝 **Note:** Before proceeding, it's important to note that the "Support Level" indicates the difficulty level of tickets.

![Screenshot 2024-05-23 091249](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/cb2b17ec-c8e7-4963-8bf3-d6b393d86da1)

#### The analysis reveals:
📝 **Note:** Before proceeding, it's important to note that the Support-Level Indicate Ticket dificultie level.

 * A significant majority of tickets, totaling **1,770 and representing 75.97%** of the total, were generated at **Tier 1 support level**.
 * **Tier 2 support level** accounted for **560 tickets**, comprising **24.03% of the total**.

These insights provide an understanding of the distribution of support requests based on difficulty levels, aiding in resource allocation and staffing decisions to ensure efficient handling of tickets across different support tiers.
#


### Ticket Volume by Priority
📝 **Note:** Before proceeding, it's important to note that "Priority" indicates the urgency of a ticket, reflecting how urgently a customer requires service.

![Screenshot 2024-05-23 091302](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/34d22fab-be2a-4c58-b0ad-882c6f8de04c)

#### The analysis reveals:

 * **Low Priority:** The **majority of tickets**, **totaling 1,192** and representing **51.2%** of the total, were categorized as **low priority**.
 * **Medium Priority:** **Medium priorit**y tickets accounted for **722 tickets**, comprising **31.0%** of the total.
 * **High Priority:** Tickets categorized as **high priority** totaled** 416**, making up** 17.9% of the total**.

These insights provide an understanding of the urgency levels of support requests, enabling appropriate prioritization and allocation of resources to ensure timely resolution of customer issues.
#

### Before diving into SLA-based insights, it's important to understand the following key concepts:
![Screenshot 2024-05-23 092100](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/93a82a10-b509-410b-aa8d-0d3614d1e21e)
#



# Investigation of First Response Time

## The average first response time is observed to be 26.07 minutes.
![Screenshot 2024-05-23 094036](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/e2a63aa1-dc66-440f-a0d5-e69a1e61127c)

### Average First Response Time against SLA:
For a detailed analysis, a table has been prepared to illustrate the average first response time in minutes based on SLA:

![image](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/ee324203-7f43-4b1f-8cd3-17a34fea5343)

 * **SLA Violated:** The average **first response time for tickets where SLA was violated is 93.42 minutes**, involving a total of **311 tickets**.
 * **Within SLA:** **Tickets resolved within SLA have an average first response time of 16.30 minutes**, encompassing a total of **2,019 tickets**.

These findings provide valuable insights into the adherence to SLA targets and the efficiency of the support team in responding to customer queries promptly.
#

Additionally, when analyzing 

![Screenshot 2024-05-23 094356](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/2c96368b-f878-4865-beeb-f213c13bf82e)

### first response times within SLA by ticket priority,
there isn't a significant difference. The response times for high, medium, and low priority tickets are nearly the same. However, when **examining SLA violation, medium priority tickets exhibit a notably longer first response time of 131.22 minutes**.

Furthermore, we are interested in 

![Screenshot 2024-05-23 094407](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/c8ca7e91-aaf2-4f9b-8e0e-f5b7787d4336)

### investigating whether the First Response Time (minutes) is affected by Ticket Source.

In terms of First Response Time by Ticket Source within SLA, we observe that:

 * **Phone tickets have the shortest response tim**e, with an average of only **0.99 minutes**.
 * **Chat tickets** follow closely, with a response time of** 1.02 minutes within SLA**.
 * **Email tickets** experience a** slightly longer response time within SLA**, averaging at **30 minutes**.

 * On the other hand, **in cases of SLA violation**,** email tickets have the longest response time, averaging at 253 minutes**.

#

# Investigation of Ticket Resolution Time:
## The average ticket resolution time is observed to be 33.25 Hours.
![Screenshot 2024-05-23 094828](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/4bcf5c82-c6da-4ef6-9bca-4f98683c6fd4)
#


### The average ticket resolution time against SLA reveals the following:
![Screenshot 2024-05-23 094940](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/11868178-d0ad-4051-aca8-c599913d2f96)

 * **Within SLA**: The average ticket resolution time within the **SLA is 33.51 hours**.
 * **SLA Violated:** In cases where the **SLA was violated**, the **average ticket resolution time is 31.43 hours**.

These findings provide valuable insights into the efficiency of the support team in resolving tickets within the agreed upon SLA timeframe.
#

### When investigating the impact of Ticket Priority on ticket resolution time (hours), the following observations are made:
![Screenshot 2024-05-23 100615](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/e6ba8432-f7a9-4592-b8a8-63aa41d33728)

 * **Within SLA:** Upon examining resolution times within SLA by priority level, there isn't a significant difference. Medium priority tickets take slightly longer to resolve compared to high and low priority tickets.

 * **SLA Violated:** In terms of resolution time for tickets where the SLA was violated, the resolution times vary across different priority levels:

**SLA Violated:** **High priority** tickets have an average resolution time of **32.50 hours**.
**SLA Violated:** **Low priority** tickets have an average resolution time of **32.59 hours**.
**SLA Violated:** **Medium priorit**y tickets have a comparatively shorter average resolution time of **28.86 hours**.

These findings indicate that while there isn't a substantial difference in resolution times within SLA based on priority level, there is a notable variation in resolution times for tickets where the SLA was violated.
#

### The analysis of Ticket Resolution Time (hours) based on Ticket Source reveals the following insights:
![Screenshot 2024-05-23 100626](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/f12c5b5c-e2e8-4b34-893b-7f9db05bb172)

### Within SLA:
 * Tickets received via chat have an average resolution time of 27.51 hours.
 * Email-based tickets have a longer average resolution time of 36.35 hours.
 * Phone-based tickets exhibit the longest average resolution time of 39.45 hours.

### SLA Violated:
For tickets where the SLA was violated:
 * Chat-based tickets have an average resolution time of 28.62 hours.
 * Email-based tickets show an average resolution time of 32.75 hours.
 * Phone-based tickets have an average resolution time of 35.67 hours.
 * These findings indicate variations in resolution times based on the source of the ticket, with chat-based tickets generally having shorter resolution times compared to email and phone-based tickets, both within SLA and in cases where the SLA was violated.

#



## Distribution of Tickets by Country and Topic
The purpose of this analysis is to explore whether there is any relationship between specific topics and countries. Let's delve into our findings:
![Screenshot 2024-05-23 101804](https://github.com/user-saddam123/Technical-Support-Analysis-Onyx-Data-May2024-Challenge/assets/123800896/842c3c69-6667-4418-bfd2-b3698325cf5f)

#### Insights:
 * **Top Ticket-Generating Countries**: **Germany, Italy, Poland, and the United States** are the **countries** where the **highest number of tickets were generated**.
 * **Popular Topics in Top Countries:** In **these four countries**, the most common ticket topics are **Product Setup, Pricing and Licensing, and Feature Requests**.

#### Further Analysis:
 * **Drill-Down Analysis**: We can further investigate the distribution of tickets based on product group, priority, and ticket source to gain deeper insights into the support needs of specific countries and topics.

These findings provide valuable insights into the correlation between ticket topics and countries, guiding support teams in prioritizing and addressing customer needs effectively.


#

