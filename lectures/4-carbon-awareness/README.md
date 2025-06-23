template: titleslide

# Green HPC
## Michael Bareford, EPCC
## m.bareford@epcc.ed.ac.uk



---
template: titleslide
# Carbon Awareness



---
# Carbon awareness

- Electricity is generated from various sources.
  - Some sources emit no (or little) carbon, e.g., renewables.
  - Other sources emit substantial quantities of carbon, e.g., fossil fuels.
    - The ratio of carbon emitted for coal:oil:gas is 100:70:50.

- The energy mix are the proportions of electricty contributed by each energy source.
  - The actual proportions vary by place and by time.

- Carbon awareness is about doing more work when electricity is being generated from <br>low carbon sources and less when it is not.


---
# Carbon intensity

- Carbon intensity (CI) measures how much carbon is emitted per kilowatt-hour (kWh) of electricity consumed.
  - Units are gCO<sub>2</sub>e / kWh , grams of carbon dioxide equivalent per kilowatt-hour.

- If your computer is directly plugged into a wind farm, the electricity required to run the computer would have zero carbon intensity.

- In actual fact, a computer (or HPC system) is plugged into a national grid that is supplied with electricity from various sources.
  - How much electricity is provided by each source is outside of the customer's control.


---
# Carbon intensity varies by location

- Some UK regions have an energy mix containing more "clean" energy sources than others.

| Type        ||| Carbon Intensity ||| UK Region |
| ---:        ||| ---:             ||| :--- |
| Low         ||| 22-48            ||| Scotland, N. England |
| Low Medium  ||| 77               ||| N. Wales |
| Medium      ||| 108-135          ||| Yorkshire, London, W. Midlands, E. & SE. England |
| High Medium ||| 186-203          ||| E. Midlands, S. England |
| High        ||| 242-255          ||| S. Wales, SE. England |

- Carbon intensities in units of gCO<sub>2</sub>e / kWh over the year 2024.
  - See [electricityinfo.org regional carbon intensity history](https://electricityinfo.org/region-archive/).


---
# Carbon intensity varies by location

| Carbon Intensity ||| Country ||| Change |
| ---: ||| ---: ||| ---: |
| 959  ||| Kosovo ||| -3%
| 636  ||| Taiwan ||| 0%
| 560  ||| China ||| -29%
| 552  ||| Australia ||| -32%
| 470  ||| Russia ||| -4%
| 384  ||| United States ||| -37%
| 344  ||| Germany ||| -40%
| 211  ||| UK ||| -60%
| 31   ||| Norway ||| +19%

- *Per capita* carbon intensities in units of gCO<sub>2</sub>e / kWh over the year 2024 and the percentage change between 2000 and 2024.
  - Worldwide per capita carbon intensity has fallen by 10% over the last 24 years, <br> See [Our World in Data](https://ourworldindata.org/grapher/carbon-intensity-electricity?tab=table) for further info.



---
# Carbon intensity varies over time

- Carbon intensity increases when the wind is not blowing or when it is cloudly.

.center[![:scale_img 80%](carbon_intensity_temporal_variability.png)]



---
# Brownouts and blackouts

- The electricity grid must be run such that the demand and the supply are in balance.
  - This is the responsibiity of the grid operator.

- A brownout occurs when the demand exceeds supply.

- A blackout occurs when the supply exceeds demand.
  - Ciruit breakers must be activated to avoid damaging infrastructure.



---
# Dispatchability and curtailment

- For fossil fuels and nuclear power, the amount of electricty produced can be controlled.
  - These sources of power have high dispatchability.

- Some renewable sources of energy, such as solar and wind, have low dispatchability.
  - And so, if the energy provided by those power sources exceeds demand, the electricity must be "thrown away",
  aka, curtailment.



---
# Marginal carbon intensity

- The marginal power plant usually runs on a power source that has high dispatchability.
  - In other words, it can meet a sudden increase in demand.

- Marginal carbon intensity is simply the carbon intensity of a marginal power plant.

- This is high for fossil-fueled power plants, which typically have a minimum functioning threshold.
  - Such plants provide an always-on baseload to the grid.



---
# Zero marginal carbon intensity

There is a scenario when the marginal carbon intensity is zero.

.center[![:scale_img 80%](renewable_marginal_carbon_intensity.png)]

This can happen if renewable sources are available to meet demand fluctuations via curtailment.


---
# Energy markets

- Energy prices fluctuate with demand; in general, the market can respond as follows.

- When demand **drops** buy less energy from...
  1. fossil fuel plants
  2. renewable sources

- When demand **rises** buy more energy from...
  1. renewable sources that are currently being curtailed
  2. fossil fuel plants



---
# Energy markets

- Energy prices fluctuate with demand; in general, the market can respond as follows.

- When demand **drops** buy less energy from...
  1. fossil fuel plants
  2. renewable sources

- When demand **rises** buy more energy from...
  1. renewable sources that are currently being curtailed
  2. fossil fuel plants

- The above picture is a simplification, in reality, it is much more complex.

- Market regulations are set so as to make fossil fuels expensive compared to renewables.
  - Investment should therefore flow from fossil fuels to renewables.



---
# How to be more carbon aware

Use more electricity when it can be generated by carbon neutral sources of power.

.center[![:scale_img 80%](carbon_aware_transition.png)]