[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/FxAEmrI0)
# Actuarial Theory and Practice A

#SOA Case Study Report
> By Leo Lee and Maxwell Wu

---

### Report

#Question 1
Our product design for Galaxy General Insurance Company (GGIC) consists of a structured premium framework governed by actuarial risk modelling with tailored design features. The premium was based on a frequency-severity approach where expected aggregate losses were calculated along with additional loadings to capture expenses, capital cost, tail risk and target profitability. 

The following equation was used: 
[images](Premium_formula.png)
Additional product design features included deductibles and claim limitations to address the distinct risk profiles of each hazard type and solar system. Here, insurers are capable of restricting the loss distribution and placing a ceiling on extreme losses which is especially effective for volatile environments. 

This integrated approach is detailed in Q2, aligning with the GGIC’s risk management framework. The premium calculation effectively identifies and quantifies risk profiles where claim frequency and severity that is characteristic of the solar system is accounted for. Risk exposure is then managed through deductibles and price ceilings which are calculated based on environmental characteristics to ensure that variable costs are controlled. From a capital management perspective, monetary initiatives against extreme losses were accounted for by pre-emptively offsetting capital allocation through the premium calculation. To support the deployment of the product, scenario analysis for evolving conditions such as solar flares and extreme heat have been provided, ensuring that the ERM framework is adaptable and dynamic against a broad range of situations. 

#Question 2
Our insurance policies have an overall structure comprising a deductible equivalent to 50% of the average claim severity for each solar system, and a ceiling equal to the 90th percentile of the claim severities for that system, which ensures that they are representative of their respective solar systems. Any claims over the ceiling in magnitude will only incur a payout of this ceiling value, while any claims under the deductible threshold will not be paid out by the insurer, but are instead paid out by the policy holder. If in between, the payout is equivalent to the claim amount, less the deductible, which the policy holder covers. The average loss per policyholder was found by dividing the mean aggregate loss by the number of unique policyholders in each solar system, with the results shown in appendix. 

Each risk scenario was assigned a weight, based on their likelihood. The baseline scenario was assigned a weight of  98%, while extreme heat was 1.5%, and solar flares were given a weighting of 0.5%. The annual premium for each policy was determined by adding the expected losses, capital expense, risk loading factors and required profit margin (equivalent to 10% of capital expenses). It was then applied to a 10-year annuity, with interest and inflation rates being found by averaging the last 5 years of provided rates, using the following formula: 
[images](revenue_simulation.png)

#Question 3

#Question 4
Scenario testing was undertaken by constructing models for both claim frequency and severity. A Poisson model was chosen for frequency, and a Gamma model was chosen for severity. A vector of parameters was obtained for each model by creating predictions using frequency data, as it had a more comprehensive account of all policies in place. 100 simulations were then run, with the Poisson model using rPois to generate a claim count, which was then used by the Gamma model to generate a series of claim severities, contributing to the total aggregate loss. The mathematical reasoning behind this workflow can be seen in. 

The multipliers in the table above were applied separately to  in the Poisson model, and  in the Gamma model, to mimic the effects of extraordinary environmental variables on aggregate loss. For example, the Helionis cluster did not experience any volatile solar activity, and was therefore given the lowest multipliers for solar flares, as it meant that solar flares would be unlikely to affect business operations.

For a baseline scenario, no multipliers were used, to mimic a system where there were no accidents. Solar flare activity was deemed to be the highest risk scenario due to the potential damage it could cause within the different hazard areas, along with its strong presence in all 3 systems. The middle risk scenario was extreme heat, which holds less immediate danger than solar flares, but is still capable of accentuating hazard areas and causing complications. 

#Question 5 - Assumptions
The distribution of claim counts was assumed to follow a Poisson distribution, while claim severity was assumed to follow a Gamma distribution. This was done to make data simulation possible, in order to explore the ramifications of each risk scenario, but this assumption did not always hold up, and alternate distributions had to be used to fit the data.
The effects of different risk scenarios on loss within solar systems were quantified through the usage of multipliers, which were determined through the analysis of the online encyclopaedia, to determine the effect of certain scenarios on frequency and severity in a solar system
Due to the lack of future interest and inflation rates, an assumed rate was devised by taking the average of the past 5 rates, to create a stable estimate
Obtaining formulae for capital costs, risk loading and operational expenses required careful consideration with regards to choosing a coefficient that would prevent the variable from having an excessive impact on the premium, while being feasible in real life
The profit margin of 10% was attained through external research using a vehicle insurance provider (greenslips.com.au), which provided real world evidence of a 10% profit margin being a reasonable and fair aim. 

#Question 6 - Data Limitations
A significant limitation of the data was the existence of poor quality variable names and values. For example, some claim counts in the business interruption dataset were negative, which made modelling using Poisson and Gamma GLMs impossible. These values had to be removed before any work or modelling started. Additionally, there was the existence of variable names with ‘garbage’ values, such as ‘Zeta?????_’, that would show up as extra factor levels in GLM models, warping the coefficients and creating difficult, lengthy summary sheets. These values were dealt with by preprocessing the data to only include variable values that had full names, uniform names. 

Additionally, there was a constant presence of statistical outliers in claim_count and claim_amount that created problems with GLM models converging. This was rectified by imposing artificial ‘caps’ on data, to remove some outliers that were having an enormous impact on the data. A similar problem was seen when using these GLMs to form predictions on data, and was handled the same way. 

AI was utilised to support the validation of modelling approaches (Poisson, Gamma, e.t.c), where assumptions and outputs were cross checked with industrial actuarial practices. This included assessing the consistency of model outputs and the reasonableness of our product design including premium levels, ensuring that proposed pricing structures aligned with realistic offerings within the market. 

---

> Be creative! You can embed or link your [data](player_data_salaries_2020.csv), [code](sample-data-clean.ipynb), and [images](ACC.png) here.

More information on GitHub Pages can be found [here](https://pages.github.com/).

![](Actuarial.gif)
