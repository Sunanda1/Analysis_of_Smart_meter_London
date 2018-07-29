# Analysis_of_Smart_meter_readings_in_London

## Overview:
<p> The goal of this analysis is to understand energy consumption pattern in London. The dataset consisted of 5,566 London households and their energy consumption between November 2011 and February 2014. The readings for each household were taken every half hour. Households in UK have been allocated to CACI ACORN(Classification of Residential Neighborhoods) categories, which is a geo-demographic segmentation of UK's population. There are 6 such categories. Each of these 6 categories are further divided into groups, making a total of 18 groups. More information about ACORN groups can be found <a href="https://acorn.caci.co.uk/what-is-acorn">here</a>.</p>
	
<p>UK's energy tariff plans are categorized into two groups: Dynamic Time of Use and Standard. The Dynamic Time of Use plan is set up in such a way that each household is informed in advance of the specific times when their electricity tariff would be higher or lower than normal price– High (67.20p/kWh), Low (3.99p/kWh) or normal (11.76p/kWh). The Standard plan has a constant flat rate(14.228p/kWh) throughout the day. </p>

<p>This dataset was used to understand energy consumption patterns across different ACORN groups. Initial analysis consisted of understanding the different ACORN groups and the difference between them. The next steps of analysis consisted of a deep dive into the dataset which contains the records of household energy consumption (monitored every half hour) to try to establish different consumption patterns based on tariff plans and the ACORN groups. Analysis of weather impacts on energy consumption across groups was also conducted. The resulting output comprised of visualizations of various parameters which exhibit energy consumption trends  within and across ACORN groups.</p>

![img8](https://user-images.githubusercontent.com/31700068/43369589-e63b121a-9325-11e8-8dfe-4d010fcad9a0.png)

<p>Different tariff plans were introduced in UK to reduce overall energy consumption. Dynamic Time of Use (DToU) plan provided users with different tariff rates(high/normal/low prices)so that subscribers could effectively plan their energy usage, thereby, reducing their overall consumption. Displayed in the chart above is the average energy consumption by different tariff plan subcribers for each ACORN classification over a span of roughly 2 years. It was seen that mean energy consumption for DToU subcribers were lower than the standard tariff plan subscribers in the case of Affluent and Adversity ACORN groups whereas for the comfortable ACORN group it was exactly opposite.</p>


![image8](https://user-images.githubusercontent.com/31700068/42986122-3ce88126-8ba9-11e8-8c00-633acaef8c0f.png)

<p>Energy usage was very high during evening hours, less during day time and mean energy usage dips down to the lowest during late night hours. This pattern remains same irrespective of their tariff rates (high, normal, low). Also, it is seen that less energy is consumed when high rates are charged.</p>


![img7](https://user-images.githubusercontent.com/31700068/43369608-17ce0b2a-9326-11e8-89d9-02c33923a2b4.png)

<p>Energy consumption was high from December to March. The average temperature for the same period was below 5°C and thus, this explains higher energy consumption during this period as heating systems would have been used extensively. Thus, temperature change plays a major role in energy consumption irrespective of different ACORN groups.</p>

### Summary
<p> To summarize, energy consumption varies depends upon:
<ul><li> Temperature</li>
    <li> Applied tariff rates</li>
    <li> Different tariff plans(Std./DToU)</li>
    <li> ACORN classification</li></ul>	    
</p>

### Dependencies:

#### Python Packages used:
<ol>
	<li>pandas</li>
	<li>numpy </li>
	<li>matplotlib</li>
	<li>seaborn </li>	
	<li>datetime </li>
	<li>plotly</li>
	<li>calendar</li>
</ol>

### Datasets used:
<p>https://www.kaggle.com/jeanmidev/smart-meters-in-london</p> 
<p>https://data.london.gov.uk/dataset/smartmeter-energy-use-data-in-london-households</p>

### Links to render on nbviewer:
#### <a href="http://nbviewer.jupyter.org/github/Sunanda1/Analysis_of_Smart_meter_London/blob/master/Jupyter_notebooks/Smart_meter_london_data_preparation1.ipynb">Data preparation</a>

#### <a href="http://nbviewer.jupyter.org/github/Sunanda1/Analysis_of_Smart_meter_London/blob/master/Jupyter_notebooks/Smart_meters_london_visualizations.ipynb">Exploratory data analysis and visualizations</a>

### Next steps:
<p> Few more ideas to explore: 
<ul><li> Energy consumption pattern during weekdays v/s weekends</li>
    <li> Energy consumption during holiday season</li>
    <li> Forecasting energy consumption for each household</li></ul>	
</p>
