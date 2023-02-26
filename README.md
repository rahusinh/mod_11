# Module 11

Module 11: What Drives the Price of a Car?
Jupyter Notebook: https://github.com/rahusinh/mod_11/blob/main/prompt_II.ipynb

## Overview
In this application, we explored a dataset from kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. Our goal was to understand what factors make a car more or less expensive. As a result of our analysis, we should provide clear recommendations to our client -- a used car dealership -- as to what consumers value in a used car.

## CRISP-DM
This framework, which is a standard process, was followed to provide a foundation for our steps and analysis. 


### Business Understanding

From a business perspective, we are tasked with identifying key drivers for used car prices.  In the CRISP-DM overview, we are asked to convert this business framing to a data problem definition.  Using a few sentences, reframe the task as a data task with the appropriate technical vocabulary. 


#### Determine Business Objectives
a. **Background:** We have a dataset containing features on 426k used cars and their prices.

b. **Business Objectives:** The goal is to understand what features make a car more or less expensive so we can eventually give advice to our client on what drivers value.

c. **Business Success Criteria:** The final model should provide recommendations to the client on what features consumers value in a car. The model would do this by predicting the price through a given feature set. 

#### Assess Situation

a. **Inventory of Resources:** Previous lectures, notebooks, and assignements. Search engines like Google.

b. **Requirements, Assumptions, and Constraints:** Dealing with a subset of the total data to avoid hardware resource roadblocks. Assuming the given data is correct.

c. **Risks and Contingencies Terminology:** Our model might be detrimental to our client if it's over fitted or just plain inaccurate.  

d. **Costs and Benefits:** The potential benefits of this model are that our clients will be able to enhance their sales by only targeting sales of cars that are most appealing to customers. This could be used in companies across the country.

#### Determine Data Mining Goals

a. **Data Mining Goals:** The good news is we are provided with the dataset. The next part would be to perform exploratory data analysis and data processing to prepare our data for training.

b. **Data Mining Success Criteria:** The success criteria would be having enough data to find relationships between features and targets. Having clean enough data to be able to draw conclusions out of both categorical and coninutious features. 

#### Produce Project Plan

a. **Project Plan:** Follow the CRISP-DM framework, explore the data, prep the data, find relationships, narrow the features, explore different regression models, evaluate them, choose the best one.

b. **Initial Assessment of Tools and Techniques:** Will be using the scikit learn, numpy, pandas, and seaborn libraries for data exploration and modeling.

## Findings

### Data Exploration
- id was a useless feature
- kept the following features: **manufacturer, year, cylinders, fuel, odometer, transmission, state**
- removed the following features because of too many missing variables or not enough correlation: **paint color, VIN, and size**

### Final Findings
Looking at the coefficients above, we can conclude the following features should be taken into consideration:
    - **Year**, the newer (higher) it is, the higher price
    - The **less mileage** on the car, the higher the price
    - The **better the condition**, the higher the price
    - The better the title status and the condition, the higher the price
    
Year was the most positively correlated to the price.

Based on our findings, the factors that affect the price the most are the following:
**Year made, mileage, condition, title status, and the fuel.**

From the analysis we can see odometer, year, condition, fuel would be the most important factors.
The model should provide clear recommendations which cars consumers will value more than others.

Further analysis could have narrowed it down to less features. These methods and models could obviously be refined. Which would have potentially made the model better. We could have also used different types of models (random forests, neural nets, etc). We could also go and search for more potential features which might not have been collected as part of the original dataset. Talk to more domain experts and gain more knowledge on where to go next.
