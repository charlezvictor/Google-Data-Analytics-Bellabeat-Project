# Google-Data-Analytics-Bellabeat-Project
Case study on Bellabeat
The case study followed the six steps involved in a data analysis process:

Ask

Prepare

Process

Analyze

Share

Act

**Scenario**

Since it was founded in 2013, Bellabeat has grown rapidly and quickly positioned itself as a tech-driven wellness company for women. The company has 5 focus products: bellabeat app, leaf, time, spring and bellabeat membership. Bellabeat is a successful small company, but they have the potential to become a larger player in the global smart device market. **Our team have been asked to analyze smart device data to gain insight into how consumers are using their smart devices. The insights we discover will then help guide marketing strategy for the company.**

As a junior data analyst working on the marketing analyst team at Bellabeat, a high-tech manufacturer of health-focused
products for women. Bellabeat is a successful small company, but they have the potential to become a larger player in the
global smart device market. Urška Sršen, cofounder and Chief Creative Officer of Bellabeat, believes that analyzing smart
device fitness data could help unlock new growth opportunities for the company. I have been asked to focus on one of
Bellabeat’s products and **analyze smart device data to gain insight into how consumers are using their smart devices. The
insights you discover will then help guide marketing strategy for the company.**

1. **ASK**

Analyze Fitbit data to gain insight required to help improve Belleabeat's marketing strategy and gain an edge in the competitve market space

Primary stakeholders: Urška Sršen and Sando Mur, executive team members.
Secondary stakeholders: Bellabeat marketing analytics team.

2. **PREPARE**

Data Source: 30 participants FitBit Fitness Tracker Data from Mobius: https://www.kaggle.com/arashnic/fitbit

The dataset contains 18 CSV files. The data also follow a ROCCC approach:
The dataset is
- Reliability 
- Original
- Comprehensive
- Current 
- Cited

The dataset has its own shortcomings:

Just 30 user data was made available. For accurate and pricise analysis, more data is required.  
Certain parameters needed to a more comprehensive analysis were not in the dataset. Prameters like age, nature of job, lifestyle.

3   **PROCESS**
    
Used Excel and R Studio was used to complete this analysis because of the many packages and data visualization features available to explore the data with.
    
Used Excel to verify and remove all duplicate data

Used the dailyActivity_merged csv file because it contians all the required data about each users daily activity merged into one csv file
Installed and loaded all the required libraries, then imported the files needed for analysis
    
Verified that the number of rows of the csv merged into the dailyActivtiy file was the same number of rows available with that of the dailyActvity_merged file.
    
 
4   **ANALYSIS**


Viewing dataframes
           
           head(daily_activity)

![Head daily Activity](https://user-images.githubusercontent.com/87811793/171422296-b0133ddc-a5c2-4e41-ba41-adfbd0a73788.png)
           
Sumarizing dataframe
          
           summary(daily_activity)
          
![Screenshot (440)](https://user-images.githubusercontent.com/87811793/171422789-ade4ec1c-4fd6-42d3-acf3-4d1818193b68.png)

Checked for the relationship between Very Active Distances and the amount of calories burned

             ggplot(data=daily_activity, aes(x=VeryActiveDistance, y=Calories)) + geom_point() + geom_smooth(lm) + labs(title= "Relationship between Very Active Distance and Calories Burned")

![Screenshot (441)](https://user-images.githubusercontent.com/87811793/171425056-6154445e-2e07-497a-a4e2-ebe1ffefc9fa.png)


Checked for the reationship between Total Distance and the amount of calories burned
              
               ggplot(data=daily_activity, aes(x=TotalSteps, y=Calories)) + geom_point() + geom_smooth(method=lm) + labs(title= "Relationship between Very Active Distance and Calories Burned")
![Screenshot (442)](https://user-images.githubusercontent.com/87811793/171425354-2206db3f-f797-457a-bfb0-f2e4fd21123a.png)

Also factored in the amount of sedemenatry time that were involved for calories burned and total steps taken

                 ggplot(data=daily_activity, aes(x=TotalSteps, y = Calories, color=SedentaryMinutes))+ 
                  +   geom_point()+ 
                  +   stat_smooth(method=lm)+
                  +   scale_color_gradient(low="steelblue", high="orange")

![Screenshot (439)](https://user-images.githubusercontent.com/87811793/171425906-ec2b085f-a48d-4767-818b-3839a5ab39fe.png)







  
    
  
