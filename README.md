# Team 11 Project Part 1
Our international research health company is focused on developing methods and practices to help prevent suicide. The analytical department has been tasked with predicting trends and analyzing the correlation between economic factors, demographic variables (such as age and sex), and the number of suicide cases.

We hypothesize that economic factors significantly impact suicide rates, particularly among middle-aged and younger populations. By analyzing predictor correlations and the lag between declining economic indicators and rising suicide cases, we can forecast critical periods and identify target groups for anti-suicide campaigns. This will allow us to time interventions more effectively and tailor our strategies to those most at risk, thereby adding substantial business value by enhancing our ability to prevent suicide through data-driven decision-making.


# Data set
Data set for reserch "Suicide Rates Overview (1985 to 2021)"
https://www.kaggle.com/datasets/omkargowda/suicide-rates-overview-1985-to-2021/data
# Columns desription
1. country - the name of the country where the data was collected.
2. year - the year in which the data was recorded.
3. sex - the gender of the individuals in the data.
4. age - the age range of the individuals in the data.
5. suicides_no - the total number of suicide cases reported in the given year and country for the specified age and sex group.
6. population - the total population of the specified age and sex group in the given country and year.
7. suicides/100k pop - the number of suicides per 100,000 individuals in the specified age and sex group.
8. country-year - a concatenated field combining the country and year for easy reference.
9. HDI for year - the Human Development Index (HDI) for the country in the given year. This is a composite statistic of life expectancy, education, and per capita income indicators.
10. gdp_for_year ($) - the Gross Domestic Product (GDP) of the country in current US dollars for the given year.
11. gdp_per_capita ($) - the GDP per capita, which is the GDP divided by the population of the country for the given year, in current US dollars.
12. generation - The generational cohort of the individuals in the data. This can reflect the cultural or historical context influencing the individuals based on their birth period.

# Scope of analysis
1. How the number of suicides varies depending on gender and age.
2. How GDP per capita affects the number of suicides.

# Team's Rules of Engagement
* Tackle problems, not people.
* Everyone participates, no one dominates.
* State views and ask genuine questions. 
* Share all relevant information.
* Explain reasoning and intent.
* Focus on interests, not positions. 
* Test assumptions and inferences. 
* Discuss undiscussable issues. 
* Be the crew, not the passenger

# Solution approches  
1. Data preparation: import and clean data from Kaggle by handling missing values and standardizing data
2. Exploratory data analysis: visualize relationship between suicide rates (response variable) and GDP per capita (predictor variable) using scatter plots 
3. Hypothesis testing: compare suicide rates across genders and age groups by categorizing demographic variables
4. Regression analysis: train-test split to separate data for model training and evaluation, fit multiple linear regression to predict suicide rates. We also performed simple linear regression on HDI vs. suicide rates. 
5. Model evaluation: calculate evaluation metrics such as root mean squared error and generate a Q-Q plot to check if data follows a normal distribution. 

# Results and recommendations
Studying and understanding suicide rates from a public health perspective is crucial. In this project, we utilized global suicide statistics to investigate how economic factors and demographic variables correlate with suicide rates.

1. Gender is a strong predictor as our analysis show that males have significantly higher suicide rates (5.12 more suicide cases per 100,000 population, p<0.001) compared to females. 
2. Suicide rates vary across different age groups with higher age groups showing highest rates - age 75 + years has a coefficient of 2.22 (p<0.001) 
3. Higher GDP per capita is associated with slightly higher suicide rates (coefficient: 1.04, p <<0.001). Moreover, the effect of GDP per capita on suicide rates may vary by gender - the relationship may be stronger for males compared to females (interaction term coefficient: 0.26, p<0.001). 
4. The Human Development Index (HDI), which incorporates health, education, and standard of living indicies in addition to economic output measured by GDP, is significantly associated with changes in suicide rates (coefficient: 11.37, p<0.001). As HDI increases, so do suicide rates. Of note, our analysis also identified country where the HDI has the highest positive correlation with suicide rates (Bosnia and Herzegovina). 

Suicide prevention requires multifaceted and coordinated approches, we made the following recommendations based on our analysis:
1. Target support programs: advocacy for developing and promoting mental health inititives and resources tailored to male's needs such as addressing stigma and encouraging help-seeking behavior. 
2. Mental health support for elderly (55+ years of age) population: as the elderly population has the highest suicide rates, resources should be invested in expanding access to geriatric mental health services and promoding social activities to reduce isolation and increase mental well-being among the eldly population. 
3. The positive correlation between GDP or HDI with suicide rates can stem from many socioeconomic, cultural, and psychological factors. Higher GDP/HDI may indicates greater levels of economic productivity and urbanization. However, individuals may be at higher risk for suicide due to increased economic stressors,  societal expectations, and social disconnect and isolation. Further studies investigating these predictor variables are necessary to pinpoint areas for mental health improvement.


# Limitations and considerations of the analysis
While our analysis reveals important insights into factors that influence suicide rates such as gender, age, and economic factors, it is important to discuss the limitations of our analysis. 

* The Q-Q plot showed skewness and outliers, suggesting that residuals may not be normally distributed. Presence of outlier suggests data points where model's predictions significantly deviate from observations. We removed some of the outliers by excluding data points where the suicide rate (case/100k population) to less than 60. As a result, we have effectively enhanced the prediction model, as evidenced by the decreased RMSE and MSLE values. 
* Our models assume linear relationships between predictor variables and response variable and did not address potential interactions between predictor variables (except for GDP& gender). Violation(s) of these assumptions leads to failure to capture more complex relationships and suboptimal interpretations and predictions. 
* Variable selection: our current selection of predictor values does not fully capture relevant factors influencing suicide rates.  Limited number of predictor variables may lead to oversimplification of models and biased estimates of predictor variable's effect on suicide rates. Suicide is a complex phenomenon influenced by a multitude of factors across individual, social, cultural, economic and environmental contexts. Understanding these factors on a population level using a data-driven approch is crucial for designing and implementing effective suicide prevention measures. 

# Link to individual videos
Ihor Kylymchuk:

Parva Thakker: https://youtu.be/zPPQr8p7lzI

Raghvendra Mishra: https://drive.google.com/file/d/1ThON_69vjB1kUukUc_4m8y4NKXrN3q3v/view?usp=share_link

Jia Xin (Janet) Jiang: https://drive.google.com/file/d/1BDpbBjPunKSY10ZufssWMvSAVZ6IDHT9/view?usp=drive_link


