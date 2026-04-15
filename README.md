[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/FxAEmrI0)
# Actuarial Theory and Practice A

#SOA Case Study Report
> By Leo Lee and Maxwell Wu

---

### Report

#Part 1
Our product design for Galaxy General Insurance Company (GGIC) consists of a structured premium framework governed by actuarial risk modelling with tailored design features. The premium was based on a frequency-severity approach where expected aggregate losses were calculated along with additional loadings to capture expenses, capital cost, tail risk and target profitability. 

The following equation was used: 
[]
Additional product design features included deductibles and claim limitations to address the distinct risk profiles of each hazard type and solar system. Here, insurers are capable of restricting the loss distribution and placing a ceiling on extreme losses which is especially effective for volatile environments. 

This integrated approach is detailed in Q2, aligning with the GGIC’s risk management framework. The premium calculation effectively identifies and quantifies risk profiles where claim frequency and severity that is characteristic of the solar system is accounted for. Risk exposure is then managed through deductibles and price ceilings which are calculated based on environmental characteristics to ensure that variable costs are controlled. From a capital management perspective, monetary initiatives against extreme losses were accounted for by pre-emptively offsetting capital allocation through the premium calculation. To support the deployment of the product, scenario analysis for evolving conditions such as solar flares and extreme heat have been provided, ensuring that the ERM framework is adaptable and dynamic against a broad range of situations. 

#Part 2
Our insurance policies have an overall structure comprising a deductible equivalent to 50% of the average claim severity for each solar system, and a ceiling equal to the 90th percentile of the claim severities for that system, which ensures that they are representative of their respective solar systems. Any claims over the ceiling in magnitude will only incur a payout of this ceiling value, while any claims under the deductible threshold will not be paid out by the insurer, but are instead paid out by the policy holder. If in between, the payout is equivalent to the claim amount, less the deductible, which the policy holder covers. The average loss per policyholder was found by dividing the mean aggregate loss by the number of unique policyholders in each solar system, with the results shown in appendix. 

Each risk scenario was assigned a weight, based on their likelihood. The baseline scenario was assigned a weight of  98%, while extreme heat was 1.5%, and solar flares were given a weighting of 0.5%. The annual premium for each policy was determined by adding the expected losses, capital expense, risk loading factors and required profit margin (equivalent to 10% of capital expenses). It was then applied to a 10-year annuity, with interest and inflation rates being found by averaging the last 5 years of provided rates

---

> Be creative! You can embed or link your [data](player_data_salaries_2020.csv), [code](sample-data-clean.ipynb), and [images](ACC.png) here.

More information on GitHub Pages can be found [here](https://pages.github.com/).

![](Actuarial.gif)
