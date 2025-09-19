# Course 4 - Group Employer Project for the Bank of England (Final Grade: High Distinction)

Project Details: This final 6 week project for the LSE course gave myself and 5 students the opportunity to work together in a collaborative project aimed at providing strategic insights to The Bank of England. It served as a quasi internship as there was frequent contact and presentations to The Bank itself. The focus was on speech data sentiment scores and any potential correlation to economic indicators. 

Project Scenario: Part of the job of the Bank of England is to provide reassurance and stability to financial markets. One way this is achieved is through representatives of the Bank delivering speeches at various public events. As an organisation, the Bank of England is interested in how the trends in these speeches correlate with observed events and economic indicators, as well as how the sentiment of these speeches can be used to predict market behaviour. This analysis will inform our understanding of the impact of the Bank’s communications on the economy, as well as the predictive power of using this data set.

This analysis considered the following business questions:

**1. Has the sentiment of central bank speeches changed over time? If so, how has it changed?**

**2. How does the sentiment of the Bank of England’s speeches correlate with key Events?**

**3. How does the sentiment of speeches correlate with key economic indicators of the UK?**

**4. Do these speeches have any predictive power to assist in predicting market behaviour?**

**5. Are there other insights or findings from the analysis that may be of interest to the organisation?**

**6. What are the potential reasons for any of the correlations discovered above? How have you drawn these conclusions?**


I was part of a strong team of analysts, who all brought unique skills and ideas to the project. The team consisted of:

Chris Buck (CB): team lead, spearheading all aspects of the project and instrumental in collating, cleaning, and merging economic-indicator data

Germán de la Fuente (GF): conducted web scraping to update the data set with the most recent BoE speeches, ran predictive models including scenario analysis using external volatility data

Harshdeep Kohli (HK): Implemented several sentiment models, applied an advanced Gradient Boosting regression that demonstrated the predictive power of speech sentiment

Kelvin Dhondee (KD): Compiled economic-research primers for the team to enhance our collective domain knowledge, ran an advanced time-series forecasting model (SARIMAX) that demonstrated how sentiment could enhance economic predictions

Victoria Pogonyaylova (VP): Played a large part in initial cleaning and EDA, used advanced techniques to customise a highly specialised sentiment model (CentralBankRoBERTa) to suit our needs.


**Personal Analytical Approach Highlights:**

Role: My role in the group project was defined as 'data visualiser', using my attention to detail, designer like thinking and skills in storytelling to develop visualisations in Python using libraries such as Seaborn and Matplotlib. Whilst other members of the team were also developing visualisations, I contributed with constructive feedback to enable the visuals to be more effective. My personal involvement was specifically in the exploratory sentiment data analysis and predictive modelling (Gradient Boosting Regression)

Exploratory sentiment analysis: I researched and implemented four different NLP models to explore potential sentiment scores; TextBlob, Vader, Loughran McDonald and FinBERT. This included the pre-processing of speech data across the time period and using descriptive statistics, visualisations and proactive discussion to evaluate which model would best capture the relationship between BoE speech sentiment and economic indicators. We ultimately recommended that BoE incoporate the specialised CentralBankRoBERTa sentiment model, which was researched and implemented solely by Victoria Pogonyaylova.

Predictive modelling: My primary objective was to model the relationship between speech sentiment and CPI rates to predict future inflation. Due to the complex relationship between speech sentiment and CPI rates, a gradient boosting regression model was recommended by our project supervisor which led me to implement a lagged version of the gradient boosting regressor using the scikit-learn python library. I aggregated sentiment scores to monthly averages to mitigate noise from individual speeches. I created 1, 2, and 3-month lags for each sentiment indicator, which allowed me to check if sentiment from previous months influenced current economic conditions. I chose a 1-month lag for inflation because the most recent past value of a time series is usually its strongest predictor. Standard Scaler was applied to features for consistency. I set ‘shuffle=False’ during the train/test split to preserve the chronological order of the data. I visualised feature importance bar graphs to highlight which features are the
most influential in making predictions. This allowed me to directly quantify which sentiment features contribute most to predicting inflation

**Personal Key Insights and Recommendations:**
1. The agent-specific lagged CBRoBERTa score ‘households’, with a 2-month delay (Importance: 0.012) and a 1-month delay (Importance: 0.007), turned out to be the most influential. These insights show that the Bank's tone on households significantly contributes to predicting future inflation. As anticipated, the previous month's value of CPI was its strongest predictor. This underscores the inherent persistence and auto-correlation in inflation time series.
2. The model shows that past speech sentiment can indeed help explain and predict the direction of future economic indicators.  Our model predicts Inflation rates well, explaining 57% of its variation, with a mean sqaured error of 3.73. Because financial markets strongly consider inflation, this forecasting ability gives market analysts valuable clues into its direction
   
Feature importance for predicting CPI rates
<img width="1038" height="582" alt="image" src="https://github.com/user-attachments/assets/c6cf5c64-e42c-447a-b426-658a70167678" />

Actual vs Predicted CPI rate using gradient boosting regressor
<img width="1050" height="602" alt="image" src="https://github.com/user-attachments/assets/82016333-ea56-4675-90f3-404575ba0bbc" />

**Recommendations**

Implement a Proactive Sentiment Intelligence System:
Establish a dedicated, real-time sentiment monitoring dashboard within the Bank. This system should track not only overall sentiment but also granular sentiment towards key economic topics (e.g., 'financial sector', 'households', 'inflation outlook').Integrate these NLP-derived sentiment metrics directly into the Bank's economic analysis tools and dashboards, with a specific focus on incorporating the lagged sentiment indicators (e.g., sentiment 1-3 months prior) that our models identified as having significant predictive power. This provides a leading indicator for upcoming economic data releases.

Optimize Communication for Lagged Impact:
Policymakers should strategize speech content and tone with an explicit understanding that the full economic noise of their words may not be immediate, but rather unfold over several months. For specific policy objectives, craft messages with identified sentiment facets in mind (e.g., focusing on a consistently positive 'financial sector' tone to subtly bolster exchange rates or investment confidence over the next 2-3 months).


**Team Presentation** - (insert link here)

**Professional Development and Impact:**
This project showcased my intepersonal communication skills through working with a group of people I have never previously worked with. I was also able to take on a predictive modelling task (Gradient Boosting Regression),  aswell as as a bespoke financial sentiment model which was not covered in the programme. Finally, a genuine passion for predictive analytics was cemented in the exploration of the business questions, a passion which I would love to be able to explore further.


