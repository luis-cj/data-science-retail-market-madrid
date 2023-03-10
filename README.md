# Data science project: retail market analysis of Madrid using Airbnb data
Data science project analysing Airbnb data of Madrid to help a retail business make strategic decisions.

This is a **discovery project**, where the main goal is to explore the data sources, check hypotheses and find out new patterns and insights relevant for the business without requiring any machine learning algorithm.

## Context
A retail business is dedicated to make great investments in important touristic cities where they can buy properties and eventually rent them as tourist apartments. 

The business managers have recently decided to invest in Madrid. The data science team has been required to analyse the Airbnb public data to find those properties that can lead to the greatest revenue for the business.

<p align="center">
  <img width="460" height="300" src="https://github.com/luis-cj/data-science-retail-market-madrid/blob/main/images/madrid.gif">
</p>


As the main requirement, they expect to know what type of property they should be looking for among the existent properties and the main neighbourhoods or districts they should focus on.

## Methodology

### 1. Objective
Find the property profile that maximise the potential revenue in the renting retail market and the main neighbourhoods where these are situated.

### 2. Levers (metrics)
After talking with the business team we are informed that those levers (this is, metrics we can analyse) that have the greatest revenue impact are the following:

- **Renting price**: the greater the renting price the greater the revenue.
- **Availability**: generally the more days the property is occupied for renting the greater the revenue (more demand).
- **Property price**: the cheaper the property the greater the revenue.

### 3. KPIs
- The renting price will be measured by the price for one night in euros according to Airbnb.
- The availaibility will be measured as the total number of days the property can be rented.
- The property price will be measured as the product between the total surface of the property and its average price per m<sup>2</sup>. Then, a 25% discount will be applied to the final price assuming the business can negotiate and lower the purchase price thanks to the purchase team.

### 4. Entities and data
The relevant entities we can retrieve data from in order to accomplish our objective are the following:

- Airbnb dataset of Madrid
- Price per m<sup>2</sup> in the city of Madrid by district

Some web scrapping is necessary to obtain all the data. 

### 5. Seed questions
These are the first questions we need to start finding relevant insights. Different questions apply to each lever.

About renting price:

- What is the average price? What about the price range? What is the variation among the different districts?
- What is the average renting price ranking for the different districts and neighbourhoods?
- What are the most important factors that determine the renting price?
- What is the relationship between the property size and the renting price?
- How does the amount of properties per district affect the renting price?
- What are the prices variation for each type of property? (the whole flat, a private room, a shared room)

About availability:

- What is the mean availability? What is the variation among the different districts?
- What is the average availability ranking for the different districts and neighbourhoods?
- What are the most important factors that determine the availability?
- How does the amount of properties per district affect the availability?

About property price:

- What is the property price ranking by m<sup>2</sup> by district?
- What is the relationship between the property price and the renting price by district?
- What is the relationship between the property price and the availability by district?


### 6. Analysis and insights
All the analysis is carried out in the following Jupyter Notebooks (Python):

[Retail market analysis in Madrid - Python script (PART 1 - DATA ACQUISITION)](https://github.com/luis-cj/data-science-retail-market-madrid/blob/main/retail_market_madrid_part_1.ipynb)

[Retail market analysis in Madrid - Python script (PART 2 - CREATE DATA MART)](https://github.com/luis-cj/data-science-retail-market-madrid/blob/main/retail_market_madrid_part_2.ipynb)

[Retail market analysis in Madrid - Python script (PART 3 - DATA PREPARATION)](https://github.com/luis-cj/data-science-retail-market-madrid/blob/main/retail_market_madrid_part_3.ipynb)

[Retail market analysis in Madrid - Python script (PART 4 - ANALYSIS AND INSIGHTS)](https://github.com/luis-cj/data-science-retail-market-madrid/blob/main/retail_market_madrid_part_4.ipynb)

Here is a summary of the steps taken throughout the analysis process:

- Gathering the data from the internet and create a database using SQLite
- Selecting what data is useful for the project
- Cleaning the data
- Create and transform relevant variables for the project
- Analyse the data by answering the seed questions from Section 5.

### 7. Communication
For this project a report was generated, communicating all the analysis and found insights.
The report can be checked in the following file:

[Retail market analysis in Madrid - Report](https://github.com/luis-cj/data-science-retail-market-madrid/blob/main/report.md)

## BONUS: Lessons learnt

- Cleaning data is not so straightforward. That's why analysing data is an iterative process, because normally some data quality problems are only found at later stages during data analysis processes rather than during the cleaning process.

- It is very difficult to have all the data. Many assumptions are made during the process due to lacking information. Then, the more data (and more relevant) we can have the better is the approach to any problem.

- Business knowledge is very helpful. Making the correct questions is key when looking for data insights. Sometimes an analytical mindset is enough, but business knowledge about the project topic can accelerate the analysis process.
