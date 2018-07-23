# Analysis_of_Smart_meter_readings_in_London
<p> The goal of this analysis is to understand energy consumption pattern in London. The dataset consisted of 5,566 London households and their energy consumption between November 2011 and February 2014. The readings for each household were taken every half hour. Households in UK have been allocated to CACI ACORN(Classification of Residential Neighborhoods) categories, which is a geo-demographic segmentation of UK's population. There are 6 such categories. Each of these 6 categories are further divided into 3 groups, making a total of 18 groups. For this analysis, households belonging to 'Affluent Achievers', 'Comfortable Communities' and 'Urban Adversity' categories were only considered. More information about ACORN groups can be found <a href="https://acorn.caci.co.uk/what-is-acorn">here</a>.</p>
	
<p>UK's energy tariff plans are categorized into two groups: Dynamic Time of Use and Standard. The Dynamic Time of Use plan is set up in such a way that each household is informed in advance of the specific times when their electricity tariff would be higher or lower than normal price– High (67.20p/kWh), Low (3.99p/kWh) or normal (11.76p/kWh). The Standard plan has a constant flat rate(14.228p/kWh) throughout the day. </p>

<p>This dataset was used to understand energy consumption patterns across different ACORN groups. Initial analysis consisted of understanding the different ACORN groups and the difference between them. The next steps of analysis consisted of a deep dive into the dataset which contains the records of household energy consumption (monitored every half hour) to try to establish different consumption patterns based on tariff plans and the ACORN groups. Analysis of weather impacts on energy consumption across groups was also conducted. The resulting output comprised of visualizations of various parameters which exhibit energy consumption trends  within and across ACORN groups.</p>

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
<p>Datasets can be found<a href="https://www.kaggle.com/jeanmidev/smart-meters-in-london"> here.</a></p> 
<p>Tariff dataset can be found<a href="https://data.london.gov.uk/dataset/smartmeter-energy-use-data-in-london-households">here.</a></p>
<ol type="decimal">
<li>Informations_households.xls : It contains all the information on the households including their ACORN group classification and type of tariff plan to which they are subscribed.</li>

<li>Halfhourly_dataset.zip : This zip file contains the block files with the half-hourly smart meter measurement. For this analysis, only a few blocks representing each ACORN group( Affluent/ Comfortable/ Adversity) were used.
Blocks used : Block_0, Block_2, Block_4, Block_62, Block_78, Block_79, Block_80, Block_95, Block_96, Block_105</li>

<li>Acorn_details.xls : It contains detail on acorn groups and profile of individuals in each group based on social, demographic, economic and other differentiating aspects.The first three columns are the attributes studied, the ACORN-* is the index of the attribute for each acorn group. At a national scale, the index is 100. If for one column the value is 150, it means that there are 1.5 times more people with this attribute in the ACORN group than at the national scale. You can find an explanation on the <a href="https://acorn.caci.co.uk/what-is-acorn">CACI website </a>.</li>

<li>Weather_hourly_darksky.csv : It contains hourly data from darksky api. It consists of hourly weather information across UK including minimum-maximum temperature and wind data.</li>

<li>Tariff:It contains half hourly tariff rates(High, Normal, Low) for the households subscribed to Dynamic Time of Use plan for the year 2013.</li>
</ol>

## Table Of Contents:


#### <a href="http://nbviewer.jupyter.org/github/Sunanda1/Analysis_of_Smart_meter_London/blob/master/Jupyter_notebooks/Smart_meter_london_data_preparation.ipynb">Data preparation</a>

#### <a href="http://nbviewer.jupyter.org/github/Sunanda1/Analysis_of_Smart_meter_London/blob/master/Jupyter_notebooks/Smart_meters_london_visualizations.ipynb">Exploratory data analysis and visualizations</a>

#### [Inline Visualization](#viz-anchor)
#### [Summary](#summary-anchor)
#### [Next steps](#next-anchor)



### <a id='viz-anchor'></a>Visualizations

![image8](https://user-images.githubusercontent.com/31700068/42986122-3ce88126-8ba9-11e8-8c00-633acaef8c0f.png)

<p>Energy usage was very high during evening hours, less during day time and mean energy usage dips down to the lowest during late night hours. This pattern remains same irrespective of their tariff rates (high, normal, low). Also, it is seen that less energy is consumed when high rates are charged.</p>


![image_7](https://user-images.githubusercontent.com/31700068/43030868-9d36188e-8c4b-11e8-9549-9126e762d26e.png)

<p>Energy consumption was high from December to March. The average temperature for the same period was below 5°C and thus, this explains higher energy consumption during this period as heating systems would have been used extensively. Thus, temperature change plays a major role in energy consumption irrespective of different ACORN groups.</p>

<p><b>Note:</b> For complete work, please click <a href="http://nbviewer.jupyter.org/github/Sunanda1/Analysis_of_Smart_meter_London/blob/master/Jupyter_notebooks/Smart_meters_london_visualizations.ipynb">here.</a></p>



### <a id='summary-anchor'></a>Summary

<p> To summarize, energy consumption varies depends upon:
<ul><li> Temperature</li>
    <li> Applied tariff rates</li>
    <li> Different tariff plans(Std./DToU)</li>
    <li> ACORN classification</li></ul>	    
</p>

### <a id='next-anchor'></a>Next steps

<p> Few more ideas to explore: 
<ul><li> Energy consumption pattern during weekdays v/s weekends</li>
    <li> Energy consumption during holiday season</li>
    <li> Forecasting energy consumption for each household</li>	
</p>
