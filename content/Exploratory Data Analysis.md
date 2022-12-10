Description:
The datasets of interest are housed within a collection of datasets titled “Compiled Datasets for CDP Analytics Competition.” The dataset was published to Kaggle by user “seraphimstreets.” and features data collected and cited from several reputable organizations, such as Organization for Economic Co-operation Development, The Institute for Health metrics and Evaluation, and The World Resource Institute.

The first dataset in question is titled “Percent of Energy Consumption by Country”. The dataset is a CSV file containing 11 columns of data. The first three columns include the country and year the data in each row was obtained from, as well as the corresponding country codes. The next eight columns list the percentages of each industry’s energy consumption within each country in a given year. The industries recorded include coal, gas, oil, hydroelectric, nuclear, solar, wind, and biomass.

The second dataset in question is titled “CO2 Emissions by Country.” The dataset is also a CSV file containing 4 columns of data. The first three columns again include the country and year the data in each row was obtained from, as well as the corresponding country codes. The last column lists the CO2 emissions from each country in a given year.

Prior to directly analyzing any data, our group first decided to generate overarching questions about the nature of our data, the relationships we could identify between variables, and how these relationships reinforce our project goals. The following four questions were generated:
	Is there a strong correlation between energy consumption and CO2 emissions? If so, what energy industries are responsible for the most CO2 emissions?
	How have energy consumption and CO2 emissions changed since 1965? Have there any significant increases or decreases, or have these variables remained generally stagnant?
	How do changes in energy consumption and CO2 emissions over the years differ between countries? Have some countries made greater efforts to reduce their energy consumption and CO2 emissions? Have any countries increased these variables?
While these questions do not necessarily account for all potential trends within our data, we believe they comprise the most important features of our data and cover our general project goals.

To have a better understanding of the dataset, I have to organize and clean datasets. Initially, the biggest problem of these datasets is the problem of the unit. Some sorts of energy consumption categories are listed by Terawatt-hour(TWh), while others are listed by Exajoul(EJ). So, clarifying and transferring the unit of energy is beneficial for data analysis and comparison. 

Secondly, since this dataset is about energy consumption during 1965-2018, there are several data missed because some countries/regions didn’t begin investigating the consumption of energy level at a very early age. These missing data will significantly disturb the calculation of the dataset and cause an error during code running. To solve this problem, I used “replace” function to change all missing data to 0.

Thirdly, these datasets contain several data representing a massive region like South Africa or Mid East. These data caused duplication problems when I tried to get the total energy consumption per year. To get a straightforward and convenient dataset, I only collected the data from a specific country or region like the United States or China.


![p1](images/Fig1(1).jpg)
![p2](images/Fig%201(2%EF%BC%89.png)
Fig 1. Organize and Clean the datasets

After Organizing and cleaning the datasets, I eventually can preliminary analyze the data. From Fig2, energy consumption in the whole world has been rising gradually during the last 50 years. Oil, Coal, and Gas are the three main categories that increased the fastest. From 2000 to 2010, it’s been a tremendous improvement in the consumption of Coal. 
![p3](images/Fig2.png)
Fig 2. Different Types of Energy Consumption Per Year

Depends on whether the source of energy is reproducible, we can divide Oil, Coal, and Gas into non-renewable resource, and divide Geo biomass, Hydro, Nuclear, Solar, Wind into renewable resources. Based on the classification, the trend of different type of consumed energy can be plot.
![p4](images/Fig3.png)
Fig 3. Trend of Different type of Consumed Energy

From CO2 emission data, I can get CO2 emission quantity in each country/region and receive a ranking list.
![p5](images/Fig4.jpg)
Fig 4. Top 5 CO2 Emission Countries

My next plan for data analysis is to meticulously analysis energy consumption construction and CO2 emission change in these five countries.

Predictive Modeling:
I will use energy consumption construction in different countries as the independent variable, use CO2 emission data as the dependent variable, and building a model. Through training by the dataset, I can get a model which can predict CO2 emission in the future, which can play a guiding role in environmental protection work.
