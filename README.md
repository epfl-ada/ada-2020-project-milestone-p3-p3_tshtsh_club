# Project P3 milestone

## 1. Title : Born with a silver spoon? / Food (and money) for thought


## 2. Abstract
[comment]: <> (A 150 word description of the project idea, goals, datasets used. What's the motivation behind your project? How do you propose to extend the analysis from the paper? What story would you like to tell, and why?)
Keeping a good and balanced diet is fundamental to having a healthy life as it helps avoiding food-related illnesses such as diabetes, obesity and cardiovascular diseases. However, the price of the food products influences greatly the decisions of individuals in purchasing them or not. There is a strong belief amongst consumers that more expensive products are healthier than cheaper ones, even this is not always true. Thus, we ask ourselves: do people have an equal chance in maintaining a nutritious diet and thus a healthy life? We explore the link between the economic situations of households and their food purchases in the boroughs of Greater London, Britain. To measure the level of wealth in each area, we study the economic factors such as incomes, employment rates and children poverty per borough provided by the London Datastore. We compare them to the nutritional properties of each borough’s typical product given in the Tesco Grocery 1.0 dataset. 


## 3. Research Questions
Some research questions you would like to address during the project:
- How does each borough's typical product evolves over a whole year?
- What is the proportion of food related expenditure in each borough?
- How does a healthy diet relates to the borough's economic situation?


## 4. Proposed dataset
List the dataset(s) you want to use, and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you've read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible given the datasets at hand.

Datasets that we want to use:
- [Grocery purchases, Borough](https://figshare.com/articles/dataset/Area-level_grocery_purchases/7796666?backTo=/collections/Tesco_Grocery_1_0/4769354) from the Tesco Grocery 1.0 dataset presented in the paper:  aggregated information on food purchases, enriched with information coming from the census at the level of boroughs.
- [Earnings by Place of Residence, Borough](https://data.london.gov.uk/dataset/earnings-place-residence-borough): gross earnings of employees by place of residence. We only consider the resident based median earnings weekly, averaged between full-time and part-time, in 2015.
- [Children poverty, Borough](https://data.london.gov.uk/dataset/children-poverty-borough): numbers and percentages of children in poverty for Borough and London Wards (at 31 August each year). We only take into accout the percentage of children in low-income families in 2015.
- [London Consumer Expenditure Estimates - Detailed Borough Base](https://data.london.gov.uk/dataset/london-consumer-expenditure-estimates-2011-2036): consumer expenditure data to 2036 broken down by London borough. We will transform the data concerning food in percentages of the total expenditure over the year 2015.

## 5. Methods
- We will compute the Spearman Rank correlation between entropy of nutrients and the earnings of employees, the percentage of children in poverty and the percentage of food expenditures. 
- We will then run a linear regression to predict the entropy of nutrients from the highest correlated factors and other control variables accounting for demographics and store penetration. If a high goodness of fit is obtained regarding the $R^2$ coefficient, it will indicate that these economic factors are representative of the food diet. 


## 6. Proposed timeline


## 7. Organization within the team
A list of internal milestones up until project milestone P4. Add here a sketch of your planning for the next project milestone.


## 8. Questions for TAs (optional)
Add here any questions you have for us related to the proposed project.
