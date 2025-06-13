# California House Prices

**California House prices** is a comprehensive data analysis tool designed to provide analysis of housing prices across California based on demographic and population features.

This [dashboard](https://app.powerbi.com/groups/me/reports/9464cf40-a039-4bec-a77e-9d3a2507faf7/1848ffc4ffbbd5254249?experience=power-bi) 
is for streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.


<img src="https://storage.googleapis.com/kaggle-datasets-images/1446091/2391843/2b2935fb8f7e9cf17349d6dd4ec36570/dataset-cover.jpg?t=2021-07-03-15-46-44" width=150 height=100>


## Dataset Content
* The Dataset was taken from the [Kaggel California Housing Prices link](https://www.kaggle.com/datasets/camnugent/california-housing-prices/data).
The data contains information from the 1990 California housing prices census. Although it may not help with predicting current housing prices but it does provide an accessible dataset to learn Data Analysis and machine learning.

* The dataset has 20640 rows and 10 columns. The size of housing.csv file is 135mb.
* The dataset is not clean and have outliers too.
* Datase has 9 numerical columns and 1 categorical column
* The following are the columns in dataset, and little description what do they represent.
* 1.longitude: A measure of how far west a house is; a higher value is farther west

2. latitude: A measure of how far north a house is; a higher value is farther north

3. housing_median_age: Median age of a house within a block; a lower number is a newer building

4. total_rooms: Total number of rooms within a block

5. total_bedrooms: Total number of bedrooms within a block

6. population: Total number of people residing within a block

7. households: Total number of households, a group of people residing within a home unit, for a block

8. median_income: Median income for households within a block of houses (measured in tens of thousands of US Dollars)

9. median_house_value: Median house value for households within a block (measured in US Dollars)

10. ocean_proximity: Location of the house w.r.t ocean/sea

## Business Requirements
* This was my capstone project in data analysis and AI course. I was asked to create an Interactive dashboard and maschine learning model for analyis and predicting house prices in california.
The following are the business requirements and investigation questions and their answers.


#### 1) What factors are most strongly associated with housing prices?
- Q: How does median income, total rooms, or total bedrooms influence house prices?
-  A: There are two scatter plots on descriptive_and_gen_stats1 page in dashboard, one with median income vs median house value, and the other one is rooms per household vs median house value. Both scatter plots are showing upper trends, which means income and rooms per household affect the house prices to higher.

- Q: Which features have the strongest correlation with median house value?
- A: The strongest correlation of median house value is with median income and ocean proximity which is a location.. There is a barplot with income category on page descriptive_and_gen_stats1 and heatmap on descriptive_and_gen_stats4 page in dashboard

#### 2) How does house value vary by geographic location?
- Q: Are houses located closer to the coast more expensive?
- A: I constructed a box plot in Jupyter Notebook. named california_house_prices, Which clearly shows that when you go towards the ocean, the house prices become higher. So if you live close to the ocean, the house prices become higher. There is also a pie chart on main dashboard which clearly shows that when you live close to the ocean, the house price goes higher.

- Q: Which latitude/longitude regions exhibit the highest and lowest house values?
- A: I created the whole table which lists the latitudes and longitudes values for lowest and highest house prices. The table is on a dashboard page descriptive_and_gen_stats1. The farther you go west in longitude region and farther you go south region in latitude , the house values go higher and for lowest house values you have to go farther in east the longitude and farther in north in latitude, the houses become cheaper. Meaning the higher the negative value of longitude the house is near ocean and it is more expensive. Similarly in regions opposite direction the houses are cheaper.
#### 3) What is the relationship between income and housing value?
- Q: Is there a linear relationship between income and house price? 
- A: There is a LM plot in Jupyter notebook california_house_prices and there is a scatter plot in descriptive_and_gen_stats1 page on dashboard, which shows the exact linear relationshipbetween median income and house value

- Q: Are there income thresholds that show sudden jumps in value?
- A: Yes there are sudden jumps. There is a bar plot on descriptive_and_gen_stats1 page in dashboard between income category and the house value which shows sudden jumps from high income to very high and from medium to very high.

#### 4) What demographic patterns exist in high- and low-priced areas?
- Q: Do wealthier regions have higher or lower population densities?
- A: The wealthier regions have lower population densities. This can also be seen in a scatter plot between median house value and population in Jupyter Notebook and on page descriptive_and_gen_stats2 in Dashboard.

- Q: How does household size correlate with house prices?  
- A: The correlation is negative and there is a scatterplot on page descriptive_and_gen_stats2 in dashboard which shows a downward trend. The scatterplot is between population per household and median house value.

#### 5) How do housing characteristics impact house value?
- Q: Do older houses tend to be cheaper or more expensive?
- A: Yes, the older houses tend to be a little cheaper than newer houses. The newer houses are a little bit more expensive. There's also a bar plot and a scatter plot on page descriptive_and_gen_stats2 in dashboard between house age and median house value that shows upward trend with newer houses

- Q: Is there a significant relationship between rooms per 
household and price?
- A: Yes, there is an upward trend when the rooms or bedrooms per household  increase, the house value increases as well.

#### 6) How evenly is housing distributed across income and population?
-Q: Are expensive homes concentrated in specific demographic or geographic clusters?
- A: I have created a full matrix on descriptive_and_gen_stats3 in dashboard with income_category and population bins which shows a clear imbalance in how housing is distributed — income has a stronger influence than population in determining housing value. There is clear demographic and geographic concentration of expensive homes among high-income groups. Expensive homes are concentrated in the Very High income category across almost all population levels. Geopgraphically in west and south there are more expensive homes.
There is also a scatter plot on page Gen_stats in dashboard which shows the house values by longitude, lattitude and ocean proximity to confirm the findings above.


- Q: Is there evidence of inequality in housing access?
- A: Yes, there's significant inequality in housing access. Income level is a strong determinant of housing value, and lower-income groups are systematically limited to lower-value housing — even in similar population densities.


#### 7) Can we build a predictive model for house value?
- Q: What is the performance of a regression model (e.g., RMSE, R^2)?
- A: The Best result came out of RandomForestRegressor. The following are the scores:
R2 Score: 0.977
Mean Absolute Error: 11239.313
Mean Squared Error: 308991989.666
Root Mean Squared Error: 17578.168




* Test Set
R2 Score: 0.819
Mean Absolute Error: 30536.628
Mean Squared Error: 2403574885.83
Root Mean Squared Error: 49026.267


- Q: Which features contribute most to the model's accuracy?
- A: The most important features were median income, followed by longitude, latitude, and ocean proximity.



## Hypothesis and how to validate?
* List here your project hypothesis(es) and how you envision validating it (them) 

#### Hypothesis 1: 
- “Higher income households tend to own more expensive homes.”

   - How to Validate: 
   - There is a scatter plot and bar plot to validate this. Plots are  between median house income versus median house value and income category with the median house value. It shows a clear upward trend on page descriptive_and_gen_stats1 in dashboard
  

#### Hypothesis 2: “Larger households are associated with lower house values due to crowding.”

   - How to Validate:
   - There is a scatterplot on page descriptive_and_gen_stats2 between population per household and house value to validate this, and early shows a downward trend that Larger households are associated with lower house values

#### Hypothesis 3: “Houses closer to the coast (‘ocean_proximity’) are more expensive.”

- How to Validate:
- I created a bar plot on page descriptive_and_gen_stats4 in dashboard between Ocean Proximity and House Value which clearly shows houses closer to the coast are more expensive

#### Hypothesis 4: “Newer homes are more expensive than older ones.”

- How to Validate: 
- There is a scatter plot and barplot in dashboard on page descriptive_and_gen_stats4, which clearly shows upward trend with housing age, the house value increases   

#### Hypothesis 5: “Areas with more rooms per household tend to have higher income levels.”

- How to Validate:
- I created a scatter plot in dashboard on page descriptive_and_gen_stats4, between rooms per houshold with median income which clearly supports this with upward trend that areas with more rooms per household tend to have higher income levels.”


#### Null Hypothesis: “Median income has no effect on median house value.”
- How to validate:
    - There is a scatter plot and bar plot reject this hypothese. Plots are  between median house income versus median house value and income category with the median house value. It shows a clear upward trend on page descriptive_and_gen_stats1 in dashboard


## Project Plan
* Outline the high-level steps taken for the analysis.

   - I started with ETL in Jupyter notebook file california_house_price, use Ydata profiling for initial exploration of data, ceated a report a exported the report in html with name Ydata_EDA_report in output/datasets/cleaned diretory.
   Then maunauly did some EDA to confirm the report.
   -    The data was not cleaned, total_bedrooms had 287 missing values, so filled them with median values. 
   There were also some outiers. I removed the 2 outliers from population as these data points were quite from other data points in a dataset of 20,640 rows. 

   - Did some visualtions to see distribution and descriptive stastics of data. Created a QQ plot for skewness and kurtosis. Also created also a Correaltion Matrix and Heatmap of original dataset.

   - once the dataset was cleaned. I changed the name of 9 columns for readability purpose to be exported to POwerBi dashboard for a non technical person. The new column names were these now:  Longitude, Latitude, Housing Age                 
Total Rooms                 
Total Bedrooms              
Population                  
Households                  
Median Income               
Median House Value 
   
    - did Feature Engnieering, created 6 more columns from the columns came in original dataset, amd one column was created from newly created column, so now I had 16 columns total with 3 categorical columns and 13 numerical columns.
    The newly created columns were as follows: rooms_per_household        
bedrooms_per_room           
population_per_household    
price_per_room              
income_category             
pop_per_household_bins

   -   Then I did visualisations of all varaiables and created another heatmap with newly formed varaiables after cleaning to see correaltion coefficients of all variables.
Did further visualisations, created roughly 35 plots in total in california_house_price file. 6 were plotly plots and others are seaborne and matplotlib to understand the disttribution of all varaiables. 
  - The following are some of the plots in california_house_price  jupyter notebook. Scatter plot of Median House variable with all variables, creaated through using loop. Heatmaps, KDE plot, Box plots, lmplot, stacked Area plots, PLottly plots including mapbox, 3D scatter and Treemap. Treemap was save as html file in output/datasets/cleaned directory as california_housing_treemap.
  - Then I loaded the clean dataset df_clean in output/datasets/cleaned directors to exported to Power BI, to perform further interactive visualisations and dashboard in PowerBI.

  - In juypter notebbok created another file ML_notebook to create Maschine Learning model. Used original dataset instead of using cleaned dataset from previous notebook. Because I wanted to clean and encode categoricial variables in ML pipeline with original dataset.
  
  - Data set was not normalised, used log+1 transformation to normalise some of the varaiables. 
  - I wanted to test multiple ML algorthims in one go rather than testing algorithms seperately to find the best model. Therefore, I wrote a python class to be used for multiple multiple ML algorithms for GridsearchCV.
  - Created a pipeline for multiple models, with encoders, imputers, feature scaling and feature selection.

  - First perfomed the GridsearchCV on multiple models with default hyperparameters, in order to find models with best scores. Once  I found the models with best scores then used hyperparameters for best combinations.

  - Then I had the model with best scores, I plotted them and found the most important features that were playing a big role in this dataset.

  - Then created a wireframe for dashboard for PowerBI. Thinking user wants to have access to as much information as possible instead of scrolling through seperate pages. 

  -   In PowerBI created another new table apart from housing_clean table using DAX which would give us the list of all Longitude and Lattitude values for highest and lowest house prices.

  -  Also craeted 4 more measures for data analysis and visualisations, like converting income to income in avg inome in thousands of dollars. Created population bins, most common proximity, and Housing Age bins.

* How was the data managed throughout the collection, processing, analysis and interpretation steps?

    - The data was downloaded from kaggle and initially checked for datatypes, removed 2 outliers in population variable, checked for duplicates, created 6 more columns. Cleaned data was exported as housing_clean.csv to PowerBI for further analysis and interpretation.

* Why did you choose the research methodologies you used?

    - I choose correlation matrix, QQ plots for statistical analysis and understand the distribution of varaiables and corrleations to with each other. 
    - Used the RandomForestRegressor model as it gave the best score with hyperparameters of [200,300,400].
    - Intitally I used OrdinalEncode to encode categorical variable but the score with OrdinalEncoder was significanlty low but when OneHotEncoder used model score became significantly higher.

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations



#### 1) What factors are most strongly associated with housing prices?
- Q: How does median income, total rooms, or total bedrooms influence house prices?
-  A: There are two scatter plots on descriptive_and_gen_stats1 page in dashboard, one with median income vs median house value, and the other one is rooms per household vs median house value. Both scatter plots are showing upper trends, which means income and rooms per household affect the house prices to higher.

- Q: Which features have the strongest correlation with median house value?
- A: The strongest correlation of median house value is with median income and ocean proximity which is a location.. There is a barplot with income category on page descriptive_and_gen_stats1 and heatmap on descriptive_and_gen_stats4 page in dashboard

#### 2) How does house value vary by geographic location?
- Q: Are houses located closer to the coast more expensive?
- A: I constructed a box plot in Jupyter Notebook. named california_house_prices, Which clearly shows that when you go towards the ocean, the house prices become higher. So if you live close to the ocean, the house prices become higher. There is also a pie chart on main dashboard which clearly shows that when you live close to the ocean, the house price goes higher.

- Q: Which latitude/longitude regions exhibit the highest and lowest house values?
- A: I created the whole table which lists the latitudes and longitudes values for lowest and highest house prices. The table is on a dashboard page descriptive_and_gen_stats1. The farther you go west in longitude region and farther you go south region in latitude , the house values go higher and for lowest house values you have to go farther in east the longitude and farther in north in latitude, the houses become cheaper. Meaning the higher the negative value of longitude the house is near ocean and it is more expensive. Similarly in regions opposite direction the houses are cheaper.
#### 3) What is the relationship between income and housing value?
- Q: Is there a linear relationship between income and house price? 
- A: There is a LM plot in Jupyter notebook california_house_prices and there is a scatter plot in descriptive_and_gen_stats1 page on dashboard, which shows the exact linear relationshipbetween median income and house value

- Q: Are there income thresholds that show sudden jumps in value?
- A: Yes there are sudden jumps. There is a bar plot on descriptive_and_gen_stats1 page in dashboard between income category and the house value which shows sudden jumps from high income to very high and from medium to very high.

#### 4) What demographic patterns exist in high- and low-priced areas?
- Q: Do wealthier regions have higher or lower population densities?
- A: The wealthier regions have lower population densities. This can also be seen in a scatter plot between median house value and population in Jupyter Notebook and on page descriptive_and_gen_stats2 in Dashboard.

- Q: How does household size correlate with house prices?  
- A: The correlation is negative and there is a scatterplot on page descriptive_and_gen_stats2 in dashboard which shows a downward trend. The scatterplot is between population per household and median house value.

#### 5) How do housing characteristics impact house value?
- Q: Do older houses tend to be cheaper or more expensive?
- A: Yes, the older houses tend to be a little cheaper than newer houses. The newer houses are a little bit more expensive. There's also a bar plot and a scatter plot on page descriptive_and_gen_stats2 in dashboard between house age and median house value that shows upward trend with newer houses

- Q: Is there a significant relationship between rooms per 
household and price?
- A: Yes, there is an upward trend when the rooms or bedrooms per household  increase, the house value increases as well.

#### 6) How evenly is housing distributed across income and population?
-Q: Are expensive homes concentrated in specific demographic or geographic clusters?
- A: I have created a full matrix on descriptive_and_gen_stats3 in dashboard with income_category and population bins which shows a clear imbalance in how housing is distributed — income has a stronger influence than population in determining housing value. There is clear demographic and geographic concentration of expensive homes among high-income groups. Expensive homes are concentrated in the Very High income category across almost all population levels. Geopgraphically in west and south there are more expensive homes.
There is also a scatter plot on page Gen_stats in dashboard which shows the house values by longitude, lattitude and ocean proximity to confirm the findings above.


- Q: Is there evidence of inequality in housing access?
- A: Yes, there's significant inequality in housing access. Income level is a strong determinant of housing value, and lower-income groups are systematically limited to lower-value housing — even in similar population densities.


#### 7) Can we build a predictive model for house value?
- Q: What is the performance of a regression model (e.g., RMSE, R^2)?
- A: The Best result came out of RandomForestRegressor and those can be also be visualed in scatter plot for train and test scores in ML_notebook in the end. The following are the scores:
R2 Score: 0.977
Mean Absolute Error: 11239.313
Mean Squared Error: 308991989.666
Root Mean Squared Error: 17578.168




* Test Set
R2 Score: 0.819
Mean Absolute Error: 30536.628
Mean Squared Error: 2403574885.83
Root Mean Squared Error: 49026.267


- Q: Which features contribute most to the model's accuracy?
- A: There is a bar chart in ML_notebook which shows the most important features were median income, followed by longitude, latitude, and ocean proximity.


    - There is a donut chart, pie chart, scatterplot, bar chart on the main dashboard which exactly serve the purposes of the business requirements of the questions asked. On other pages, there are several other plots with variables against other variables which answer all the questions of business requirements. There is also a scatter plot of house value against all variables in Jupyter Notebook california_house_price which serves and describe the relationship and trend against all variables.

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.

    - To analyze the California housing dataset, I applied a combination of exploratory data analysis (EDA), Ydata profiling, correlation analysis, statistical summary techniques, and predictive modeling using machine learning.

       

    - EDA techniques:
        - Distribution plots (scatterplots, qqplots,histograms, boxplots) to understand skewness/outliers.
        - Scatter plots to visualize relationships (income and other variables vs. house price).
        - Heatmaps for feature correlation analysis.

    - Data preprocessing:
        - Missing value handling
        - Feature scaling/normalization
        - Outlier detection

    - ML modeling:

        - RandomForestRegressor

        - GridSearchCV for hyperparameter tuning

    
    - Limitation: The dataset does not include key variables like interest rates, employment data, or real-time housing demand.

    - Alternative: I used feature engineering (e.g., binning proximity to ocean or population categories) to enrich the dataset.

* How did you structure the data analysis techniques. Justify your response.

- I structured the analysis in the following pipeline:

    - Data Cleaning:
        - Filled null values, removed outliers, there were no duplicates or strange characters in dataset.

    - EDA:
        - Used seaborn, matplotlib and pandas-profiling for visualization.

    - Feature Engineering
        - once the dataset was cleaned. I changed the name of 9 columns for readability purpose to be exported to POwerBi dashboard for a non technical person. The new column names were these now:  Longitude, Latitude, Housing Age                 
Total Rooms                 
Total Bedrooms              
Population                  
Households                  
Median Income               
Median House Value 
   
        - Then created 6 more columns from the columns came in original dataset, amd one column was created from newly created column, so now I had 16 columns total with 3 categorical columns and 13 numerical columns.
    The newly created columns were as follows: rooms_per_household        
bedrooms_per_room           
population_per_household    
price_per_room              
income_category             
pop_per_household_bins


    - Model Training and Evaluation:
        - Created a pipeline to use for multiple algorithms to get best model with default values, using GridsearchCV and wrote a python class which will be used for multiple models. Once the best model was evaualted then used hyperparamter optimization again with values different values and RandomForestRegressor with [200,300,400] came out with best scores for RMSE, MAE.

    - Model Optimization
        - Applied cross-validation and GridSearchCV for parameter tuning.

    - Justification: This pipeline ensured the analysis was reproducible, scalable, and aligned with best ML practices.


* Did the data limit you, and did you use an alternative approach to meet these challenges?

- Yes there were limitations and tried to find a work around

    - Missing Features: No temporal trends or market sentiment in the dataset.

    - Workaround: Focused on spatial/geographic and demographic trends.

    - Categorical data limitations: Only a few categorical variables.

        - Workaround: Binned numerical variables to simulate categorical insights.

* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

- Yes constant use of ChatGPT, Gemini, Microsoft co pilot

    - Ideation: Used AI tools (ChatGPT, gemini, copilot) to explore feature engineering and visualization ideas.

    - Design Thinking: chatGPT helped clarify user needs for dashboard layout and storytelling.

    - Code Optimization: Constantly used Copilot for code optimization and fxing code in Jupyter Notebook and in Power Bi.
    - Coplot used to comment the cells in Jupyter Notebook. Also created some visualisations through Copilot.
    Also assisted in refactoring loops, cleaning data efficiently, and suggesting best-practice ML pipelines.

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?

- Data Privacy:

    - The dataset is anonymized and does not contain personally identifiable information (PII), which minimizes direct privacy concerns.

    - However, geographic information (like latitude/longitude) can sometimes raise re-identification risks if combined with other data sources.

- Bias and Fairness:

    - The dataset focuses only on California, which introduces geographic bias—findings cannot be generalized to other regions.

    - There may be societal biases embedded in the data (e.g., income disparities or historical housing segregation) that influence price predictions.

    - Features like median income can reflect socioeconomic inequality, which could be amplified if used uncritically in modeling.


* How did you overcome any legal or societal issues?

- Legal:

    - The dataset is publicly available on Kaggle and intended for educational/research use, so there are no direct licensing issues.

- Societal:

    - Aware of the risk that models predicting house prices could unintentionally reinforce existing inequalities (e.g., by favoring high-income areas), care was taken to:

    - Analyze and highlight such disparities in visualizations.

    - Avoid using the model for any real-world pricing or decision-making without further ethical review.

- Mitigations:

    - Included fairness-aware discussions in the analysis (e.g., how wealthier areas had lower population densities).

    - Did not use sensitive or proxy variables (e.g., race or neighborhood naming) in ML modeling.

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.

- User can navigate through 7 pages through front dashboard.

- First page Overview:

    - On the top left corner is photo of houses taken from google search pbblicly available, next to the photo is the name of dashboard in Headline California House Prices interactive DA tool. Next to the name is a logo of houses being built. Next to logo of houses, there are 3 crds showing Averge House value, Total Housholds and Average pop per houshold. 

    - On top left under the image of houses is a description of dashboard, next to it is a slider to select house values and next to it 2 cards showing Averge income and Most common  Proximity, next to them is a checkbox for ocean proximity.

    - Under the description on left there is a Donut chart of Average House values by income:category, next to it in middle is a scatter plot for house values by Avg income, count of household and ocean_proximity. Next to it is a tiled box for income category and then a check box for family size selection.

    - On the down left corner is a bar chart with average house value by income category and ocean proximity. Next to it in the middle is a pie chart with average house value by ocean proximity and next to it is a horizontal bar chart by average rooms per household and average population per household by income category.

    - And right at the bottom, in the middle, there is a conclusion text box.

- Second page Gen_Stats:

    - On this page, on the top left, we have a stacked column chart with average house value by income category and population per household. And next is horizontal bar chart with average room per household, average bedrooms, and average population per household. And on the down left is a scatter plot with average house value by ocean proximity, longitude, and latitude. And next to it is a column  chart with average income in US dollars by ocean proximity.  All 4 charts have description box under them.

- Third page descriptive_and_gen_stats1:

    - On this page, on the top left, we have a table showing the values of longitude and latitude for minimum and maximum house values. Next to it is a column chart with average house value by income category. On the down left, we have a scatter plot, medium income versus median house value. And the next to it is scatter plot and rooms per household and median house value. All 4 charts have description box under them.

- Fourth Page descriptive_and_gen_stats2

    - .On this page, we have on the top left is a column chart, average house value by housing age. Next to it is a scatter plot, average house value by housing age. On the down left, we have a scatter plot, population per household, and next to it median house value, and next to it is a scatter plot, medium income versus population. All 4 charts have description box under them.

- Fifth page descriptive_and_gen_stats3:

    - On this page, on top left, we have a matrix showing income category and the population bins, showing the values. Next to it is a scatter plot with rooms per household versus median house value. And under there, there's a whole description box about the matrix and it's explanation 

- Sixth page descriptive_and_gen_stats4:

    - On this page, on top left, we have a scatter plot with median income vs. rooms per household. And under there, there's a column chart, ocean proximity vs. average house value. And both of them have a text box under them. And next to it, on the top right, is a heat map. And under there is a full description of the heat map and its variables.

- Seventh page Tree Model:

    - On this page, we have a decomposition tree, analyzed by average house value explained by median income, ocean proximity, population per household, longitude, total bedrooms, name category, latitude and important variables

* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).

    - On the main dashboard, right bottom corner, there is a horizontal bar chart with average rooms per household and average population per household by income category. I would like to remove it and I put a simple scatter plot of Median Income vs roons per houshold

* How were data insights communicated to technical and non-technical audiences?

    - To Non-Technical Audiences (e.g., Business Stakeholders, General Users)
    - Power BI Dashboard:
        - Interactive visualizations made insights accessible without requiring data expertise.

        - Used clear titles, color coding, and slicers to let users explore house prices by income level, population, proximity to ocean, etc.

        - Included simple metrics (e.g., average price by category) and geospatial maps to make patterns intuitive.

        - Simplified Language:
        - Avoided technical jargon — instead of saying “correlation coefficient = 0.87,” explained it as “Income strongly influences house prices.”

        - Used storytelling: framed findings around real-world questions like “Where are the most affordable areas?” or “What drives up housing prices?”

    -  To Technical Audiences 
    - Code and Documentation:

        - Jupyter notebooks and Python scripts shared with clear comments and explanations.

        - Shared model evaluation metrics (e.g., RMSE, MAE) and hyperparameter tuning results.

    - Model Interpretation:

        - Included feature importance graphs to show what features most affected predictions.

        - Considered limitations and assumptions behind the ML model (e.g., data bias, lack of time-based data).

    - README / Report:

        - Provided structured analysis summaries with links to the model, visualizations, and data sources.

    
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

-  For Non-Technical Audiences 
    - Clear, clean layout:

    - Key metrics (average house price, income, population) placed at the top.

    - Descriptive titles and tooltips help explain charts without requiring technical knowledge.

    - Interactive visuals:

    - Used slicers and dropdowns to let users filter by family size, income category, proximity to the ocean.

    - Scatter plots and  bar charts made regional and demographic patterns easier to understand.

    - Minimal jargon:

    - Charts are labeled in plain language for user to understand

- For Technical Audiences:

    - Provided breakdowns of relationships between variables (e.g., scatter plots showing income vs. price).

    - Included visual summaries of modeling outcomes, such as feature importance and correlation heatmaps.

    - Data drill-down:

    - Users can explore specific combinations (e.g., high-income, low-population areas) to understand nuanced relationships.

    - Supports deeper analysis:

    - The dashboard complements notebooks anddocumentation, offering a visual overview to guide further exploration.



## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.

- I faced software glitches and limitations while using PowerBI desktop applications. The software requires more computing power
The Map visualisation was not working properly in PowerBI.

* Did you recognise gaps in your knowledge, and how did you address them?
    - I recognised gaps in knowledge which I addressed through constant research and use AI to ask complex questions and tried to understand complicated codes.
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

    - Once I have submitted it, I will recive the feedback and project is on GiHub

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?

    - I faced Data Volume & Processing Power. The dataset was large and Power BI became slow or unresponsive during filtering or visual rendering. I used aggregating and binning fields (e.g., population and income bins) to over come
    - Map visuals failed to display locations correctly using latitude/longitude. I used longitudes and lattitudes in scatter to plot these graphs.
* What new skills or tools do you plan to learn next based on your project experience? 
    - I would like to deepen skills in DAX (Data Analysis Expressions) for dynamic metrics.
    - I would also like to invest more time in Maschine Learning

## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.

    - Main Data Analysis Libraries were, Numpy, Seaborn, Plotly, Matplotlib, Pandas, Scipy.stats, sklearn, warnings

    - Here is an example of scatter plot in Plotly:
        - fig = px.scatter(
    df_clean,
    x="Median Income",
    y="Median House Value",
    color='ocean_proximity',
    title="Scatter Plot: Median Income vs Median House Value<br>by Ocean Proximity"
)
fig.update_layout(width=600, height=400)
fig.show()

## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
- code institute LMS material.
chatGPT, Perplexity AI, Copilot.Gemini
google searches, Power BI.

### Content 

-  The ETL, data  visualization and ML in jupyter notebook were taken from the code institute'LMS content.
The dashboard data visualisation was done in Power BI
Used chatGPT, perplexity AI, Copilot in VS Code and Power BI for some predictions.



### Media

- The photos used on the home and sign-up page are from This Open-Source site
- -  The images for the dashboard were taken from these sites.
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSQ-g62LOU6vpi5o44tvaSHtNOP6UC5kZSEUg&s
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRS9qffVTZlcnhyQW0ZAP9HPwqCWPUj4RC1pQ&s



## Acknowledgements (optional)
* I wish to thank my facilitator Vasi, technical head Niel, our data coach John for the support during the project developmen