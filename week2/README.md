Introduction/Business Problem

In today's world many people can't imagine their lives without a car. Cars have become an integral part of modern humans, making it easier not only to perform everyday activities but also to travel long distance. Nonetheless, road vehicles are also the most unsafe of all available to humans. Traffic collisions are in first place in terms of the number of deaths and injuries. According to these parameters, cars significantly overtake railway, aviation and water transport.
Unfortunately, car accidents occur for many reasons, including both technological and human factors. An accident can happen due to the fault of a tired driver, due to icing of the road surface or a malfunction of the brake system. However, the risk of getting into an accident is often influenced by external factors, such as the day of the week, weather conditions and the quality of the road itself.
Many car companies are working on fully autonomous cars, which could potentially reduce the amount of car accidents. Until then regular cars will remain popular. Therefore, it would be great to have a mechanism that could warn you, given the weather and the road conditions, about the possibility of you getting into a car accident and how severe it would be, so that you would drive more carefully or even change your travel if you are able to. 
Thus, the goal of this project is:
1.	to identify the factors that significantly affect the risk of traffic collisions, and
2.	to create a model that will predict the severity of car accidents.
The findings may be useful for improving road safety or for insurance companies planning to introduce life and health insurance programs for drivers and passengers. 

Data section
Describe the data that you will be using to solve the problem or execute your idea. So make sure that you provide adequate explanation and discussion, with examples, of the data that you will be using.

For this project I will be using a shared dataframe called "Collisions" that is provided by the IBM (the original dataset by the City of Seattle is available here). The data in the dataset is labeled, which will allow me to use a supervised machine-learning model. 

The data is about “accident severity”. The dataset includes all types of collisions for the timeframe from 2004 to 2018. The dataset has an extensive amount of observations - more than 190,000. The total amount of attributes in the dataframe is 37. However, not all attributes will be useful for this project. Also, some attributes include missing data.

In order to meet the goals of this project, the following attributes were chosen:

•	'SEVERITYCODE' - Target variable, which is used to measure the severity of an accident from 0 to 4 within the dataset;
•	'ADDRTYPE' - Collision address type (Alley, Block, Intersection);
•	'PERSONCOUNT' - The number of pedestrians involved in the collision;
•	'VEHCOUNT' - The number of vehicles involved in the collision;
•	'INCDATE' - The date of the incident;
•	'WEATHER' - A description of the weather conditions during the time of the collision;
•	'ROADCOND' - The condition of the road during the collision;
•	'LIGHTCOND' - The light conditions during the collision;

Note: initially the attribute “SPEEDING” was also included in the selection. However, it has more than 185,000 missing values, which can create a biased ML model. Therefore, this attribute was eventually dropped.

Finally, rows with missing values from the attributes "ADDRTYPE","WEATHER","ROADCOND","LIGHTCOND" were also dropped.  The final size of the dataframe includes 187524 entries and 8 attributes.
