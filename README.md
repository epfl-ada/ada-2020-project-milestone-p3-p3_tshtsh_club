# Project P3 milestone

## 1. Title : Born with a silver spoon? / Food (and money) for thought


## 2. Abstract
Keeping a good and balanced diet is fundamental to having a healthy life as it helps avoiding food-related illnesses such as diabetes, obesity and cardiovascular diseases. However, the price of the food products influences greatly the decisions of individuals in purchasing them or not. There is a strong belief amongst consumers that more expensive products are healthier than cheaper ones, even this is not always true. Thus, we ask ourselves: do people have an equal chance in maintaining a nutritious diet and thus a healthy life?

Our goal is to provide insight on the food consumption discrepancies between different boroughs of Greater London. We explore the link between the economic situations of households and their food purchases. To measure the level of wealth in each area, we study the income and children poverty per borough provided by the London Datastore. We compare them to the nutritional properties of each borough’s typical product given in the Tesco Grocery 1.0 dataset. 


## 3. Research Questions
- What constitutes a healthy diet?
- What is the proportion of food related expenditure in each borough? How does it relate to its economic situation?
- How does a healthy diet relates to the borough's economic situation? Is this connection area-dependent?

## 4. Proposed datasets
- [Grocery purchases, Borough](https://figshare.com/articles/dataset/Area-level_grocery_purchases/7796666?backTo=/collections/Tesco_Grocery_1_0/4769354) from the Tesco Grocery 1.0 dataset presented in the paper:  aggregated information on food purchases, enriched with information coming from the census at the level of boroughs.
- [Earnings by Place of Residence, Borough](https://data.london.gov.uk/dataset/earnings-place-residence-borough): gross earnings of employees by place of residence. We will only consider the median weekly earnings per borough in 2015, averaged between full-time and part-time.
- [Children poverty, Borough](https://data.london.gov.uk/dataset/children-poverty-borough): numbers and percentages of children in poverty for Borough and London Wards (at 31 August each year). We will only take into accout the percentage of children in low-income families per borough in 2015.
- [London Consumer Expenditure Estimates - Detailed Borough Base](https://data.london.gov.uk/dataset/london-consumer-expenditure-estimates-2011-2036): consumer expenditure data to 2036 broken down by London borough. We will transform the data concerning food expenditure in percentages of the total expenditure over the year 2015.
- [Statistical GIS Boundary Files for London](https://data.london.gov.uk/dataset/statistical-gis-boundary-files-london): geolocalization of London's areas. We will use the boundaries of the boroughs as at 2011 for visualization purposes.

## 5. Methods
- Visualize the wealth differences between areas based on gross earnings and child poverty.
- Visualize the proportion of food related expenditure in each borough.
- Compute the Spearman rank correlation between the proportion of food related expenditure and the wealth across areas.
- Compute a healthy diet score based on the nutritional properties of each borough’s typical product.
- Visualize the healthy diet score differences between areas.
- Compute the Spearman rank correlation between the food health score and the earnings of employees, the percentage of children in poverty and the percentage of food expenditures. 
- Run a linear regression to predict the food health score from the highest correlated factors and other control variables accounting for demographics and store penetration. If a high goodness of fit is obtained regarding the <i>R<sup>2</sup></i> coefficient, it will indicate that these economic factors are representative of the food diet quality. 


## 6. Proposed timeline
- 27th of November - 4th of December:  creative extension analysis notebook
- 4th of December - 11th of December: creative extension data story/report and video pitch
- 11th of December - 18th of December: individual update of the replication notebook 


## 7. Organization within the team
- Marie: wrangling the data, computing the health diet score + data story/report
- Sofia: computing the correlations and fitting the linear regressions + video pitch
- Héloïse: map visualization, plotting the results + data story/report


## 8. Questions for TAs 
We thought of several ways to compute the healthy diet score:
- only take into account the energy from carbs (<i>energy-carbs</i>) and the entropy of nutrients (<i>H<sub>energy-nutrients</sub></i>), the two-highest correlated factors with the prevalence of diabetes, as seen in the paper.
- use the recommendations from the [World Health Organization](https://www.who.int/news-room/fact-sheets/detail/healthy-diet): we compute n criterias that make a diet healthy and that are either 0 or 1 depending on if they are fulfilled or not: fat criteria (< 30% of total energy intake), saturated fat criteria fulfilled or not (< 10% of total energy intake), sugars criteria (< 10% of total energy intake), etc... We obtain a final score between 0 and n, out of n.
- compute the score with a weighted sum of all the nutrients' energy. We choose those weights as the correlation coefficients with diabetes that are found in the Tesco paper. 

The problem is: how can we validate that the computed healthy diet score is representative of the people health in an unbiased manner? Do you think it is possible?
