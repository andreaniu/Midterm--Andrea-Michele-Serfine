# The Impact of Baltimore County Education Systems on Voter Turnout
By Andrea Niu, Michele Lan, and Serfine Okeyo

Trump’s unexpected 2016 election victory revealed what a crucial role voter turnout plays in shaping the democratic future of the United States. Many wondered how we could improve voter turnout among younger voters. Multiple studies ([source](http://ftp.iza.org/dp6539.pdf)) have established that education positively impacts voter turnout, so it is vital to investigate:
* **what aspect(s) of Baltimore County's education systems we should target to improve voter turnout**, and
* **which school districts in Baltimore require the most resources to increase voter turnout**, so that we can prioritize resources for them. 

Our findings showed that:
* **voter turnout increased as chronic absence and dropout rates decreased** and,
* **areas with similar characteristics to Patterson Park N&E require the most resources to increase turnout**. 


In the future, these findings will allow us to:
* **prioritize funding allocation for specific school districts in Baltimore**, and 
* **predict voting trends based on absence and dropout rates**.

# Why is this a Challenge/Problem?
What do you remember when you think of the 2016 election? For many, shock was the predominant emotion they felt in the wake of Trump’s election. Many expected that Clinton would inevitably win, but poor voter turnout in key states may have helped Trump win the election. Consequently, we are interested in investigating the factors that influence voter turnout. Hence, this business question is an important issue to consider because *if high numbers of young voters do not show up to vote, the elected representatives of the Baltimore area and the entire U.S. will poorly reflect the wants and needs of its younger residents*. 

Voter turnout in the United States is consistently lower than other developed nations, ranking at about 26 out of 32 OECD nations ([source](https://www.pewresearch.org/fact-tank/2018/05/21/u-s-voter-turnout-trails-most-developed-countries/)). Almost 92 million eligible Americans did not vote in the 2016 presidential elections, which represents almost an entire third of the total US population ([source](https://www.americanprogress.org/issues/democracy/reports/2018/07/11/453319/increasing-voter-participation-america/)). Furthermore, for young people aged 18-24, the 2018 midterm elections only had a turnout of 35.8% ([source](https://www.fairvote.org/voter_turnout#voter_turnout_101)).
Young people are an important but generally underrepresented demographic in elections. Furthermore, young voters represent a demographic that is **more diverse in terms of race, sexual orientation, religion, and gender** than older generations. Consequently, neglecting to encourage young voter participation may result in the election of representatives who fail to support the interests of young voters, and enables the passage of **exclusive government policies that further systemic inequities.**

Hence, encouraging young people's participation in the United States democracy through elections is essential. Since education has been proven to correlate with increased civic engagement ([source](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1540-5907.2009.00400.x)), we will examine what educational metrics we can target to promote higher voter turnout.

# Business Questions
* Which education system metrics should we target to increase voter turnout?
* Which Baltimore County areas should we prioritize our efforts towards? 

**Datasets Used:**
[Civic engagement](https://data.baltimorecity.gov/Neighborhoods/Neighborhood-Action-Sense-of-Community-2010/ipje-efsv)
 vs. [the education metrics of Baltimore County students (HS only)](https://data.baltimorecity.gov/Neighborhoods/Education-and-Youth-2010-2013-/f9ua-ivaj)

*Note: We used 2010 data for voter turnout and compared it with the 2010 education metrics for high schools (including suspension/expulsion rate, chronic absence rate, rate of passing US Govt. class, dropout rate, and completion rate).*

# Our Solution

Our data analysis indicates the following conclusions to our business questions:
* High **chronic absence rates and dropout rates** *may* result in lower voter turnout rates.
* Areas with similar rates of voter turnout, chronic absences, and dropout rates as **Patterson Park N&E** need the most support when it comes to improving education metrics to increase voter participation.

Some possible business explanations these conclusions include that:
* Schools/CSAs with high dropout or chronic absence rates may result in students missing key explanations on why civic engagement is important.
* Systemic inequities in these CSAs (socioeconomic / demographic) may be responsible for both high absence and dropout rates and low voter participation.


The impact of these findings is that since we know what measurable aspects of the education systems are most closely related to voter turnout and which areas have the most severe situations, we can 1) predict voter turnout based on school absence and dropout metrics, 2) target those metrics to improve voter turnout, and 3) prioritize funding towards the schools that need the most support to increase voter turnout. 

A limitation to our analysis is that, despite identifying the metrics associated with voter turnout, we do not know the relationship between them (i.e. correlation vs. causation), and we did not identify what factors might be responsible for  higher absence and dropouts, and whether those factors are also responsible for reduced voter turnout.


To achieve our solution, we performed the following types of data analysis:
* *Multivariable Regression*: we examined a variety of education metrics to identify how significantly correlated each one is with voter turnout. The regression indicated that, of all the education metrics examined, only **chronic absence rates and dropout rates** were significantly correlated with voter turnout. The multivariable regression model indicated that for each 10% increase in chronic absences, a district's voter turnout would decrease by 5%. Also, for each 10% increase in dropout rates, a district's voter turnout would drop by 16%. 

![alt_text](https://github.com/jhu-business-analytics/Midterm--Andrea-Michele-Serfine/blob/master/Multivariable%20Table.png "Multivariable Table")

   The multivariable regression model also predicted that in an ideal district with no chronic absences or dropouts, the **best voting turnout could be 68.8%**. This model can **account for 60% of the Baltimore areas** analyzed, so we have reasonable confidence in its ability to estimate voter turnout based on education metrics.

* *Simple linear regression*: To better visualize the relationship between voter turnout and dropout rates, we performed simple linear regressions against chronic absence rates and dropout rates and plotted them.

   **Chronic Absence**  
     
   The linear regression of chronic absence rates compared to voter turnout revealed a **negative relationship** between the two and predicted with about **53% confidence** that **voter turnout would decrease by 6% given a 10% increase in absence rates**.  


   ![alt text](https://github.com/jhu-business-analytics/Midterm--Andrea-Michele-Serfine/blob/master/Annotation%202019-10-25%20151518.png "Voter Turnout vs HS Chronic Absence rates")  
   Takeaway: Each 10% increase in chronic absence rates is correlated with a 6% decrease in voter turnout.  


   **Dropout Rates**  
     
   The linear regression of dropout rates compared to voter turnout predicted with **31% confidence** that **voter turnout would decrease by 32% given a 10% increase in dropout rates**. 
![alt text](https://github.com/jhu-business-analytics/Midterm--Andrea-Michele-Serfine/blob/master/Annotation%202019-10-25%20151452.png "Voter Turnout vs HS Dropout rates")  
   Takeaway: Each 10% increase in dropout rates is correlated with a 32% decrease in voter turnout.


* *Cluster Analysis*: In order to identify the areas with the worst voter turnout and the greatest need for changes in the education system, we analyzed how to best sort the districts into 3 groups based on the following characteristics: suspension/expulsion rate, US Govt. pass rate, chronic absence rate, HS completion rate, dropout rate, and voter turnout.

   We identified three 'representative' areas for each cluster, and described their traits below:
![alt text](https://github.com/jhu-business-analytics/Midterm--Andrea-Michele-Serfine/blob/master/Annotation%202019-10-25%20152422.png "Cluster Analysis Results")

   Since **Patterson Park N & E** was characterized by the **lowest voter turnout and highest chronic absence rate**, (as well as high suspension/expulsion, and lowest US Govt. pass rate), it is a representative area for the Baltimore districts that require the most attention and support for education system reform to promote voter turnout. Districts that share similar characteristics to Patterson Park N & E include Greenmount East, Cherry Hill, Oldtown/Middle East, and others. These areas should be prioritized when allocating resources or funding to increase young voter turnout.

# Future Suggestions

We should focus on reducing rates of chronic absenteeism and dropouts to boost voter turnout, and also prioritize areas with high absences and low voter turnout similar to Patterson Park N & E.

What steps can we take to achieve this? 
To Teachers and School Administrators: help kids stay in school! Actions that schools can take include:
* Tracking attendance to identify students at risk of becoming chronically absent, then **meeting/calling their guardians** to discuss the importance of consistent attendance. This plan can be implemented relatively quickly, and could also be a way to hear from guardians about factors such as home life, socioeconomic situations, or transportation, which may be the cause of chronic absences or dropping out.
* Setting **milestones towards graduation** to discourage dropping out and **partnering with college-readiness nonprofits** to offer students counseling or resources that will support their journey to graduation,
* For high priority schools/CSAs, **interview students** to investigate factors resulting in dropouts or chronic absences. This action can be implemented quickly (within 6 months), and can help each school decide what actions to take to reduce these rates.

To legislators and Board of Education members: 
* Policy Changes: **Set goals for school districts** to reduce their absence and dropout rates to a certain level. This may be a longer term goal that takes multiple years for schools to achieve, but defining a target goal in the first place is an important step to take. 
* **Prioritize funding and resources** for schools with the highest dropout and absence rates. Generally, annual Board of Education budgets allocate a certain sum of money towards strategic initiatives aimed at improving the quality of the education system, which allows schools to try out riskier pilot programs without having to take money out from the funding for their normal operating expenses. Setting 'chronic absence and dropout reduction' as one possible strategic initiative and including it in the budget is one way to incentivize schools to work towards that goal.

Following through with these actions will motivate schools to understand what situations may lead to chronic absence or dropout rates. As schools become more engaged and communicative with students and families about the importance of attendance, there may be a reduction in dropout and absence rates, which will increase the exposure students get to civic education and politically engaged peers/teachers, thus positively influencing voter turnout. In turn, this may result in better representation of young voters in Baltimore County and the election of representatives whose policies align with the younger population, and consequently increase their sense of political agency and civic satisfaction.
