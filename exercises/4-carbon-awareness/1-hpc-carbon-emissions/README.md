template: titleslide
# Carbon Awareness
## Carbon Emissions from HPC Systems
### Exercise 4.1



---
# <span style="color:red">Exercise:</span> Carbon emissions from HPC systems

One estimate of the power draw of the ARCHER2 HPC system is 3.1 MW <br>(this includes overheads due to power and cooling).

The mean carbon intensity (CI) varies across the UK regions. <br>In 2024, three CI regions were identified.

|   Type |||| Carbon Intensity [gCO<sub>2</sub>e/kWh] |
| ---:   |||| ---:                         |
|    low ||||  30                          |
| medium |||| 120                          |
|   high |||| 250                          |
  
What would the carbon emissions be from the electricity use required for 1 year of ARCHER2 operations in the three different emission regions?



---
# <span style="color:green">Solution:</span> Carbon emissions from HPC systems

First we need to estimate the amount of energy consumed by ARCHER2 in kWh for 1 year from the power draw estimate.

3,100 kW × 365 days × 24 hours = 27,156,000 kWh

Next, we multiply this energy use by the quoted carbon intensity values to get the estimated emissions from a year of ARCHER2
operation in the three different regions.

|   Type |||| Carbon Emissions [kgCO<sub>2</sub>e] |
| ---:   |||| ---:                      |
|    low ||||   815,000                 |
| medium |||| 3,260,720                 |
|   high |||| 6,790,000                 |

Hosting ARCHER2 in a high CI region instead of the low CI region would lead to an additional 5,980,000 kgCO<sub>2</sub>e of emissions per year,
a more than eightfold increase.