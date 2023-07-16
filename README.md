# EDA Global Terrorism Analysis

# Project Summary: 
The Global Terrorism Database (GTD) is a publicly available database that provides details about acts of terrorism worldwide spanning from 1970 to 2017. It offers comprehensive data on both domestic and international terrorist incidents that have taken place during this duration, encompassing over 180,000 attacks. The database is managed by a team of researchers at the National Consortium for the Study of Terrorism and Responses to Terrorism (START), which is based at the University of Maryland. Engage with the data to uncover significant insights related to terrorist activities.

# Problem Statement: 
Try to identify the terrorist hotspots as a security/defense analyst. What security issues and insights can EDA provide?

# Import Libraries:
This section imports the necessary libraries for data manipulation, visualization, and model training. The imported libraries include:
- `pandas`: Used for data manipulation and aggregation.
- `numpy`: Used for computationally efficient operations.
- `matplotlib.pyplot` and `seaborn`: Used for data visualization.

# Dataset Loading :
load a data set from a Google Drive location using Google Colab. It mounts Google Drive and then reads the CSV file named "Global Terrorism Data.csv
” using pd.read_csv() from the pandas library.

.head is used to display the topmost rows.

Data.shape is used to display the no of rows and col.The dataset contains 181691 rows and 135 columns.

# Dataset Information: 
data.info() provides a summary of the DataFrame, including the number of non-null values and data types of each column. It gives an overview of the data structure and helps in identifying missing or inconsistent data.

# Missing Values/Null Values:
The table shows the number of missing values (null values) in each column of the dataset. We can see 

Visualizing the missing values : it creates a heatmap visualization of missing values.The missing values are represented by a distinct color, allowing to identify the presence of missing values in the dataset visually.

# What did you know about your dataset?
The dataset provided is managed by researchers from the National Consortium for the Study of Terrorism and Responses to Terrorism (START), located at the University of Maryland. The objective is to comprehend and implement measures to mitigate the continued propagation of terrorism and promote peace.
Our dataset consists of 181691 rows and 135 columns. The data encompasses a total of 135 columns, encompassing both numerical and textual information. There are instances of missing values within our dataset.

# Understanding Variable name
Data.columns display the coln name
data.describe(include='all') it is a describe method which is used to generate descriptive statistics of the data within the DataFrame.
For numerical columns, additional statistics are provided, such as mean, std (standard deviation), min, 25%, 50% (median), 75%, and max.
For categorical columns, only the count, unique, top, and freq values are displayed.

# Check Unique Values for each variable.
This loop will iterate over each column in data.columns.tolist() and print a statement indicating the number of unique values in that column.
Data Wrangling: This section focuses on several data transformations and preparations are performed to make the dataset analysis-ready
Using the rename function and a dictionary, rename the column name.
I chose only a few columns that will be useful for our analysis.

# What all manipulations have you done and insights you found?
To ensure better comprehension of terminologies, I initially renamed the variables relevant for analysis. Subsequently, I filtered the dataset, retaining only those variables necessary for further analysis. As a result, I obtained a curated dataframe with a shape of (181691, 16). The data reveals the presence of missing values in certain variables such as state, city, latitude, longitude, killed, wounded, and target.
To address this, I first removed the missing values from the state, city, latitude, longitude, and target variables. Then, for the variables killed and wounded, I replaced the missing values with the respective column averages. By applying these actions, we successfully eliminated all missing values in our dataset. Consequently, we now have a clean dataframe ready for data analysis, featuring a shape of (175708, 16).
With the removal of all NaN values, we can proceed with insightful plot visualizations to analyze the data.

# Data Vizualization
# Chart - 1 : 

Why this chart : 
An area plot visually represents quantitative data.And aided me in analysing terrorist activities by region and year.

insights :
The frequency of terrorist activities has experienced a significant surge since 2010 worldwide. 
The regions of the Middle East and North Africa have consistently been the site of major attacks over the years.

business impact:
Positive Impact of Insights = Data analysis can enhance the strategic deployment of peacekeeping forces.

 Negative Impact of Insights = Data analysis has the potential to hinder business activities in impacted regions.
 
# Chart - 2 : 

Why Subplots  : 
The Subplots method allows you to plot multiple plots on a single figure.

Insight : 
The frequency of attacks peaked in 2014, followed by a similar pattern in 2015. In comparison to the attacks occurring from 1970 onwards, the past six years witnessed the highest number of incidents. However, since 2014, there has been a gradual decline in the overall count.

Business Impact: 
The data analysis presented above is sure to increase motivation, given the declining trends in terrorist activities.
# Chart - 3 : 

Why count plot: 
The countplot is an appropriate option for illustrating the distribution of categorical data, like the occurrence of terrorist attacks based on different regions. It displays the bar chart representing the frequency of each region.

Insight:
The Middle East & North Africa takes the top spot among all regions, followed by South Asia in second place.

Business Impact: 
The regions of the Middle East, North Africa, and South Asia possess a wealth of human resources that hold immense potential for enhanced business opportunities.

# Chart - 4 : 

Why count plot: 
the countplot is a concise and effective way to visualize the distribution of attacks by country

Insight:
Iraq is the most prominent among all countries, experiencing the highest number of attacks, closely followed by Pakistan, Afghanistan, and India..

Business Impact:
The governments of these countries should enhance safety protocols.

# Chart - 5 :

Why bar plot: 
the bar plot provides a straightforward and visually appealing way to present the 
data on the highest number of attacks in different cities.

Insight: 
The data analysis indicates that Baghdad city is the most impacted by terrorism. Following Baghdad, Karachi and Lima are also notable for their high levels of terrorism.

Business impact:
Cities of significant cultural importance, such as Baghdad and Karachi, possess vast untapped potential that can be harnessed for the purpose of fostering inclusive urban development.

# Chart - 6 : 

Why Count plot: 
A countplot is a type of visualization commonly used to display the count or frequency of categorical data. In this case, it seems that you are using a countplot to visualize the frequency of different terrorist groups.

Insight:
Here we can observe the leading 15 terrorist organizations, with the exception of the most unidentified one. Based on the analysis provided, it is evident that the Taliban stands as the most ruthless terrorist group, responsible for approximately 7500 acts of terrorism.

Business impact:
Compiling a list of the most dangerous terrorist organizations will aid in monitoring their activities. Such heightened awareness will ultimately curb their malevolent actions.

# Chart - 7 : 

Why Count plot:
A countplot is a type of bar plot that shows the frequency of different categories in a dataset. It is particularly useful when you want to visualize the distribution or frequency of a categorical variable.

Insight:
As it has been evident, bombing remains the preferred approach for carrying out attacks, with explosives being the primary weapon of choice. Terrorist activities predominantly rely on the utilization of explosives and firearms.

Business impact:
The aforementioned observations will prove valuable in ensuring effective surveillance of the cross-border transportation of weapons such as explosives and firearms. Affected nations' governments can collaborate by exchanging border-related information, thereby enhancing border security measures.

# Chart - 8 : 

Why countplot :
the countplot is a useful visualization for understanding the distribution and relative frequencies of different target types in the dataset.

Insight:
we can observe that private citizens and Military personals are the primary targets of terrorism. The most common targets consist of private citizens and property, military personals, police personals, government(general) officers.. 
Those responsible for maintaining law and order often bear the brunt of terrorism. Even ordinary citizens are not exempt and tend to be significantly impacted. To enhance the safeguarding of lives and property, it is essential to ensure that security personnel are adequately equipped with all the necessary weaponry.

Business impact:
Insightful information will prove beneficial for the successful deployment of security forces.

# Chart - 9 

Why count plot:
It visualizes the data through graphical representations.
It simplifies the data analysis process.
We can readily compare data with different variables.

Insight:
The majority of the attacks involve bombing or explosions due to their extensive reach, coupled with significant destructive capabilities.

Business impact:
The data provided above will prove valuable in comprehending the intentions and methods employed by terrorist groups in carrying out their activities.

# Chart - 10 : 

Why plot:
One significant advantage of using the crosstab function is its capability to standardize the output dataframe, presenting values expressed as percentages.

Insight:
Based on the figure provided, it is evident that bombing and explosion have been the most frequently employed techniques for carrying out terrorist attacks throughout the years, closely followed by armed assault. The analysis above also reveals a notable surge in incidents involving bombings and explosions, particularly since 2010.

Business impact:
The aforementioned data will provide valuable insights into comprehending the intentions and methods employed by terrorist organizations in carrying out their activities.

# Chart - 11 : 

Why countplot : 
Code complexity has been decreased. 
Shifting the reference frame of the bar chart has become significantly simpler.

Insight:
Based on the chart provided, it is evident that the highest fatality rates were recorded in the categories of Armed Assualt, Assassination, and Bombing/Explosion.

Business impact:
The data presented will offer guidance in comprehending the potential factors contributing to fatalities in a terrorist attack.

# Chart - 12 : 

Why plot: 
Condense a vast collection of data into visual representations; effortlessly compare two or three sets of data; enhance the understanding of patterns more effectively than tables; swiftly assess essential values.

Insight:
Based on the chart provided, it is evident that Bombing/Explosion caused the most significant injuries to individuals.

Business impact:
Based on the aforementioned analysis, it is evident that a significant number of individuals have been injured as a result of bombings and explosions.
Therefore, it is crucial for government agencies to take appropriate measures to enhance the monitoring and detection of explosive devices.

# Chart - 13 : 
Why bar plot : 
Plotting our data is a straightforward task. By utilizing this library, we can effectively visualize our data without concerning ourselves with the intricacies of its internal workings. All we need to do is provide our dataset as input.

Insight:
Based on the data analysis provided, it can be concluded that the Taliban exhibits the highest level of activity among terrorist organizations, with ISIL and SL following closely behind.

Business impact:
Having access to data on the most active terrorist organizations can prove valuable in limiting their financial assistance. 
This information plays a crucial role in our ongoing efforts to combat terrorism and serves as an efficient method for reducing support towards terrorist activities.

# Chart - 14 - Correlation Heatmap

Why heatmap:
The heatmap-style correlation matrix proves highly effective when utilized correctly. It empowers users to pinpoint variables with strong correlations, enabling them to streamline the process of selecting relevant features.

Insight:
The data analysis above indicates a significant correlation between the data on individuals wounded and those killed in terrorist attacks.

# Chart - 15 - Pair Plot

Why pair plot:
The Seaborn Pairplot enables us to visualize the relationships between variables in a dataset. This results in an aesthetically pleasing representation and aids in comprehending the data by condensing a substantial amount of information into a single graph.

Insight: 
The plot above indicates that the majority of the killings occurred during the middle of the month, with fewer killings at the end of the month. 
There are noticeable variations in latitude and longitude, as most of the killings are concentrated in the middle latitudes. 
The data reveals an increase in killings from 2000 to 2013, followed by a decrease. 
Throughout this pair plot, the significance of the area code can be observed, and the number of churn in relation to various features provides valuable insights. 
Additional insights can be inferred from the aforementioned graph.

# Solution to Business Objective

Steps to Take in Order to Mitigate Terrorism
Regulate the availability of hazardous weaponry Enhance governmental security measures across nations



# Conclusion

Iraq experiences the highest number of attacks.
The regions of the Middle East and North Africa are the most targeted.
The majority of attacks involve bombing and explosions.
Private citizens and property bear the brunt of the highest number of attacks.
Based on the above analysis, the following actions are recommended:
Enhance border security measures.
Implement government initiatives to address the rise in immigration and more.

# THANK YOU
