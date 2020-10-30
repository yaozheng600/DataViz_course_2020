[click here to see the protoptype]( https://yaozheng600.github.io/DataViz_course_2020/)

# Project Documentation
## 1. Concepts of our work      

## 2. Data sources
## 3. design decisions
### 3.1 Domain problem characterization        
The target users are stock market investors and people who interested in the economy during the COVID-19 period. The domains of interest are the stock market and the epidemic. The questions are how to invest during the epidemic, and to explore the state of the world economy through the stock market. The data related to the problem is divided into two aspects. One is the data regarding to the epidemic situation in each country, including new cases, national policies, medical conditions, and aging degree etc. The second is the price changes at different levels of the stock market, including national stocks, stock sectors, and company stocks. 
### 3.2 Abstraction    
Based on the problem domain, we are concerning about the price changes of all levels of the stock market (countries, sectors, companies) over time in the context of the epidemic. And find the correlation between the epidemic and the stock market. From this we can roughly determine the object of data abstraction: 1. The changes in the stock market at three levels. 2. The severity of the epidemic and the factors affecting the development of the epidemic in various countries. 3. Describing information about different aspects of a company.   
#### 3.2.1 Data abstraction
We use the change rate of the stock market's price relative to the price at start time to express the change in the stock market. The start time is February 19, 2020, which is the start of the global pandemic of COVID-19. We calculate it as the fomular:     
![](https://latex.codecogs.com/gif.latex?growth_t=\\frac{Price_t}{Price_{19.Feb.2020}}-1)      
We use the positive rate to express the severity of the epidemic, and the way to aggregate data is to take the average of the products. In addition, the factors affecting the development of the epidemic are GDP, the stringency of policies, the average age of the population, and the number of hospital beds per thousand people， which can be quantified numerically.      
We use information such as the number of employees, the enterprise value, and the profit margin to describe a company. This information can also be obtained directly.      
#### 3.2.2 Task abstraction
The abstraction of tasks is still divided into three levels to discuss. At the national level, firstly, our task is to find how each country's stock market changes over time. And it can be compared between different countries. Here we design two filters to filter different continents and different countries to focus on countries of interest. Secondly, in order to find the correlation between the stock market and the epidemic, we selected several representative countries as a comparison, and explore the correlation between the stock market change rate and various epidemic-related factors.      
At the sector level, our task is to find the composition of 11 stock sectors in a specific country and their changes during the epidemic.       
At the company level, our task is to find out what kind of companies performed well during the epidemic. We need to find the correlation between the rate of change of the stock market and the description information of each company, and perform cluster analysis according to the country to find the overall performance of the company within this country.
### 3.3 Visual encoding / interaction design     
According to task abstraction, we extracted the following tasks:
1. The changes in the stock market of each country over time, and the horizontal comparison between countries.
2. the correlation between the stock market and the epidemic
3. composition of 11 stock sectors in one country and their changes.
4. the correlation between the stock market and companies.
## 4. possible improvements
