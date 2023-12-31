# REMOTE WORK AND COVID-19
![](office_covid.jpg)
---
The purpose of this analysis is to assess the **productivity and morale implications of working remotely and outline an ideal policy for the post-pandemic future**. I used a survey results of 1,500 remote workers from the Australian state of New South Wales, taken in August-September 2020 and March-April 2021. You can access the survey results [here](https://app.mavenanalytics.io/datasets?page=3)

## Understanding Data
The data has two csv files. One is for 2020 which is the year COVID-19 was spreading rapidly and many countries had restrictions concerning public gatherings. It collected data about remote working before and during pandemic and expectations after the pandemic. The second one was for 2021 were restrictions are less tight. It collected data on the last month's of 2020, managers opinions on remote working and others. I can say data in both files were 80% categorical data.

Structure: 
* 2020 - 1507 records and 73 columns
* 2021 - 1512 records and 109 columns

<br/>
Questions that will help us to understand the productivity, morale of working remotely and a policy for post-pandemic future are as follows;

<br/>
<br/>

1.	How has the COVID-19 pandemic impacted the amount of work done remotely? What can be expected post-pandemic?

The impact of COVID-19 pandemic can be assesed by the amount of time spent working remotely before pandemic and during pandemic.

<br/>

![](impact_covid19.jpg)

<br/>
2.	Does working remotely positively impact productivity? Are there any other benefits?

<br/>
<br/>
<br/>

![](productivity.jpg)

<br/>

3.	How does an employees use of time differ when working remotely vs on-site?

<br/>

![](time_distribution.jpg)

Additional question, is the working hours truly the same between remote working and in-office. If is "YES" then we expect the number of working hours in remote working to be last worst experiences but it is among the top 5 worst experience remote workers face this is because they take regular breaks **in-between** working hours.

<br/>

4.	What are the biggest barriers to overcome if remote work becomes the norm in the future?
<br/>
One of the reasons for policies to be created/improved is to eradicate or minimize problems that are present in a particular environment. If after certain period of time the created/improved policies haven't solved problems then they should be re-constructed. So by using this perception we can check if the policies in remote working have changed/improved and solved the remote working problems.

 # 73% 
 of companies changed/improved their remote working policies

<br/>

![](policy.jpg)

<br/>

## Conclusion
From the analysis, employees don't prefer 100% remote working, their productivity when working remotely is the same to than in-office, remote workers have good work-life balance. So Hybrid working is the future (a flexible working model where employees work partly in physical workingplace and partly physical remotely). This will boost their morale, improve work-life balance and productivity

Companies that change/improve their policies in remote working, they should address the barriers faced in remote working and monitor closely the working hours to increase productivity

## Visualization
![](report_page1.jpg)
![](report_page2.jpg)

## Methodology
### 1. Data cleaning and Transformation

**Identifying errors and cleaning.**

<br/>
For 2020 data,
Columns M, T, U, AB, and AC had mixed data types that is percentage and general.  
Columns AI, AK, and AM had incorrect data. The 3 columns where asking the amount of time spent doing different activities when your remote working and on-site working. The columns had greater than 24 hours and less than 0 hours of working which is unrealistic. You can't spend 60 or -1 hours working.

For 2021 data, columns J, K, L,M, N, Q, R, and T had mixed data types that is percentage and general. 

All columns with mixed data types were all formated to have same data types using find and replace feature and Incorrect data, records with greater than 24 hours of working were deleted while with -1 was corrected to 1 hour.

**_find and replace_**
![](find_and_replace.jpg)

**Transformation**

The data needs to be changed its structure for easy analysis. Questions that were in multiple choice form they were transformed so as to get number of respondents that choose a certain category from the question. Power query was used to transform the data. Actions done during transformation are removing unwanted columns, unpivoting wanted columns, replace values, and renaming values.

|2020 power query|
|---|
|![](2020_power_query.jpg)|
---
|2021 power query|
|---|
|![](2021_power_query.jpg)|
---
Each transformation was purposely made for answering analytical questions. 
Columns transformed in 2020 data are;  
* _Compare remote working to working at your employer’s workplace. Select the best aspect of remote working for you - Managing my family responsibilities ; My working relationships ; Preparing for work and commuting ; The number of hours  I work ; My work-life balance ; My on-the-job learning opportunities_
* _Compare remote working to working at your employer’s workplace. Select the worst aspect of remote working for you - Managing my family responsibilities ; My working relationships ; Preparing for work and commuting ; The number of hours  I work ; My work-life balance ; My on-the-job learning opportunities_
* _From the following, please select the least significant barrier to doing your work remotely - Connectivity (internet connection) ; Feeling left out and/or isolated ; Poor management ; Cyber security ; Lack of motivation ; Lack of motivation_
* _From the following, please select the most significant barrier to doing your work remotely - Connectivity (internet connection) ; Feeling left out and/or isolated ; Poor management ; Cyber security ; Lack of motivation ; Lack of motivation_

Columns transformed in 2021 data are; **Column AX to Column BM**

#### 2020 workbook
#### Click the workbook image to interact

[![Iteract with 2020 workbook](2020_workbook.jpg)](https://1drv.ms/x/s!AkvFVdfC21wYhjE086F1jR-Mut2m)
---
#### 2021 workbook
#### Click the workbook image to interact

[![Iteract with 2021 workbook](2021_workbook.jpg)](https://1drv.ms/x/s!AkvFVdfC21wYhjOp59hTMcK67gKn)
---

### 2. Analysis
Two types of analysis were carried;

a) **Frequency distribution**. Used to determine the number of observations in each multiple choice. Pivot tables were used to summarise data and get insights

b) **Mode**. Which was used to determine which category appears most frequently in the data. Excel function was used

|Pivot tables|
|---|
|![](pivot_tables1.jpg)|
|![](pivot_tables2.jpg)|

Pivot tables show the following analysis
* (A) Analysis of time spent in remote working before pandemic
* (B) Analysis of time spent in remote working during pandemic
* (c) Analysis of the time employees would prefer to spend working remotely after pandemic
* (D) Comparison of productivity between remote working and on-site working
* (E) Worst experiences faced by employees when remote working
* (F) Barriers faced by remote workers
* (G) Satisfication of solutions taken on barriers
* (H) Analysis of working hours usage
* (I) Change of remote working policies after pandemic

The analysis for distribution of time usage in different activities when remote working and on-site working a function `=MODE('table'!$column1:$column1)` was used.

![](table.jpg)


