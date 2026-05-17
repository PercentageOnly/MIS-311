# Case Study For Student Exam Performance Analysis
The rise of the digital era and the fourth industrial revolution have made data one of the most core strategic resources for every organization, business, and even large-scale educational institutions. In this context, Business Analytics has emerged as a scientific lens, providing methodologies and mathematical toolsets to transform raw data into actionable insights. In order to meet the rigorous requirements of this business process—specifically guided through the program framework of the MIS 311 module .This report presents a comprehensive process system, covering from Exploratory Data Analysis to the application of descriptive statistical models for extraction strategic information.

<h2 align="center"><img width="240" height="240" alt="image" src="https://github.com/user-attachments/assets/1c6bc7c3-9346-4d98-8bb6-3de88a185881"/>

*This project aims to mine data (EDA), analyze and determine which external factors and lifestyle behaviors affect students' final exam scores the most such as learning environment, sleep time, and Internet access.*

## 1. Data Overview
**Description & Context:** The selected dataset is the "Student Exam Performance" dataset. It simulates student academic performance based on study behavior, engagement, and lifestyle factors. It is designed to help analysts explore how elements like sleep, study environment, and socio-economic background influence a student's final exam score.

**Source:** The dataset was sourced from Kaggle, uploaded by the user 'ssssws'.

**Dataset Size:** The dataset contains a substantial *10,000 rows* (representing individual students) and 23 columns (features and target variables).

## 2. Data Cleaning
**To ensure the accuracy of the analysis, the data was cleaned using the following steps:**
**Identify and handle missing values:** During the initial data inspection using Excel's Filter tool, missing values (blanks) were identified in critical numerical columns such as *study_hours_per_day* and *sleep_hours*. To address this, Mean Imputation was applied, replacing the blank cells with the calculated average of their respective columns to preserve the overall data distribution.
**Identify and remove duplicate rows:** The dataset was checked for duplicates using the 'Remove Duplicates' function based on the primary key *student_id*. The check confirmed that there were no duplicate rows in the dataset, ensuring the integrity of all 10,000 unique records.
# 3: Descriptive Statistics
Descriptive statistics is the art of condensing thousands of raw data points into representative numbers that have narrative power. Using the Analysis ToolPak in Excel, the 10,000-line data block of column final_exam_score (Final Exam Score) was fed into the analysis model.

<img width="325" height="445" alt="image" src="https://github.com/user-attachments/assets/25536f90-0222-4ac6-a747-47e29a5b5eb3" />

**Statistical Results Core Description:**
1.	Count: 10,000 students.
2.	Average Score: 49.68
3.	Median (Median Score): 49.55
4.	Mode: 45.40
5.	Standard Deviation (Độ lệch chuẩn): 12.15
6.	Range: 93.4 (From Minimum is 4.4 to Maximum is 97.8)
Statistical Insight Explanation: The  average score of the whole course hovered near 50 points (49.68), with the median almost exactly matching (49.55). This convergence proves that the test scores have an extremely symmetrical standard distribution pattern (bell-shaped curve). A standard deviation of 12.15 indicates that student scores are moderately dispersed around the mean; However, the huge gap from the lowest (4.4 points) to the highest (97.8 points) exposes a large inequalities in performance, requiring us to explore the impact variables later.
## 4: Extracting Data Analysis Insights using Pivot Tables
Here are 3 excellent insights extracted from the dataset through the Pivot Table tool, demonstrating how external and lifestyle factors affect academic outcomes.

**Insight 1: How does the learning environment affect grades?**

<img width="1189" height="463" alt="image" src="https://github.com/user-attachments/assets/ef14673a-dd55-4862-a2b9-8ebaff85c5ac" />

Comparing the study_environment variable  with the average value of the final_exam_score gives quite surprising results:
1.	Noisy Environment: 49.88 points
2.	Quiet Environment: 49.69 points
3.	Moderate: 49.57 points
Insight takeaway: The data picture shows that the difference in scores between environments is very tenuous (both fluctuate around 49.5 - 49.9). Intuitively, the group of students in the "Noisy" environment had a slightly higher GPA. This suggests that, within the framework of this dataset, the physical environment is not the biggest "bottleneck" that determines success or failure, or that students in noisy environments have developed higher concentration resilience skills. (Recommended chart: Clustered Column Chart).

**Insight 2: The Connection Between Sleep Time and Scores**

<img width="1194" height="442" alt="image" src="https://github.com/user-attachments/assets/249fd1ca-a8a1-4ecf-ac90-0dfe0e2208a0" />

Using Feature Engineering in Excel (using the function =IF(J2<6, "Low sleep", IF(J2<=8, "Enough sleep", "Too much sleep"))), the sleep_group variable  has been decayed to evaluate performance:
1.	Too much sleep (over 8 hours): 50.17 points
2.	Enough sleep (6 to 8 hours): 49.66 points
3.	Low sleep (less than 6 hours): 49.25 points
*Insight taken: The  Pivot Table reveals a clear biological law: Low sleep directly impairs cognitive capacity, pushing the average score to the lowest level (49.25). Surprisingly, the group of students who slept too much performed the highest (50.17). Management conclusion: Plowing and hoeing all night is ineffective; Ensuring adequate rest plays an essential role in strengthening memory and passing exams. (Recommended chart: Bar Chart).*

**Insight 3: The Impact of the Internet on Pass/Fail Rates**

<img width="1294" height="432" alt="image" src="https://github.com/user-attachments/assets/4f7ea07c-e1f8-4283-b10c-83f321d8ce08" />

By analyzing the percentage weight (% of Row Total) between the internet_access and the variable pass_fail:
1.	Group with Internet (Yes): Pass Rate is 48.89% (Slippage 51.11%)
2.	Group No Internet (No): Pass Rate is 45.86% (Slippage 54.14%)
Insight takeaway: The  presence of the Internet created a clear push, improving students' pass rates by about 3% (from 45.86% to 48.89%). In the era of digital education, Internet resources serve as a huge virtual library to help students fill knowledge gaps. This 3% gap is a testament to the "digital divide," a systemic barrier that policymakers need to level. (Recommended chart: 100% Stacked Column Chart).
# REFERENCE:

Ahmed, W., Wani, M. A., Plawiak, P., Meshoul, S., Mahmoud, A., & Hammad, M. (2025). Machine learning-based academic performance prediction with explainability for enhanced decision-making in educational institutions. Scientific Reports, 15(1), 26879. https://doi.org/10.1038/s41598-025-12353-4

Checking your browser - reCAPTCHA. (n.d.). https://www.kaggle.com/datasets/ssssws/student-exam-performance-dataset
