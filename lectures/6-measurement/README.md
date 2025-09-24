template: titleslide

# Measurement

---
# Introduction

The Greenhouse Gas (GHG) protocol is the most commonly-used method for organisations to measure their total carbon emissions.

Understanding GHG scopes and how to measure your software against industry standards will help you see to what extent you are reducing carbon emissions and how that fits with wider activities to reduce emissions.

The Software Carbon Intensity (SCI) specification complements the GHG protocol.

GHG is a more generic measurement suitable for many organisations, while SCI is specifically for measuring a rate of software emissions and designed to incentivise the elimination of those emissions.

---
# The GHG protocol

The [Greenhouse Gas protocol](https://ghgprotocol.org/) is the most widely used and internationally recognised greenhouse gas accounting standard.

[92%](https://ghgprotocol.org/about-us) of Fortune 500 companies use the GHG protocol when calculating and disclosing their carbon emissions.

Using the GHG protocol allows us to compare our emissions from use of HPC systems to other sources of emissions in a quantitative way.

---
# The GHG protocol

* The GHG protocol divides emissions into three scopes:
  * __Scope 1:__ direct emissions from operations owned or controlled by the reporting organisation, such as on-site fuel combustion or fleet vehicles.
  * __Scope 2:__  indirect emissions related to emission generation of purchased energy, such as heat and electricity.
  * __Scope 3:__  other indirect emissions from all of the other activities you are engaged in. Scope 3 emissions are typically split into two further categories.
    * __Upstream scope 3:__ includes all emissions from an organisation’s supply chain, e.g. emissions from manufacturing and shipping a product.
    * __Downstream scope 3:__ emissions resulting from the use of a product, e.g. the electricity customers may consume when using your product or waste output from the product.

---
# The GHG protocol

* Scope 3, sometimes referred to as value chain emissions, is often the most significant source of emissions, and the most complex to calculate.
* These encompass the full range of activities needed to create a product or a service, from conception to distribution.


---
# The GHG protocol

* <span style="color:gray"> Scope 3, sometimes referred to as value chain emissions, is often the most significant source of emissions, and the most complex to calculate. </span>
* <span style="color:gray"> These encompass the full range of activities needed to create a product or a service, from conception to distribution. </span>
* In the example of a laptop:
  * Every raw material used in its production emits carbon when being extracted and processed (part of upstream scope 3 emissions).
  * Emissions from the use of the laptop meaning emissions from the energy used to power the laptop after it has been sold to a customer (part of downstream scope 3 emissions).
* Through this approach it is possible to sum up all of the GHG emissions from every organisation and person in the world and reach a global total.

---
# <span style="color:red"> Exercise: </span> What scope for HPC emissions?

Throughout this lesson, we have spoken about emissions from two different sources associated with our use of HPC: emissions from the electricity used to run our models/simulations on HPC systems, and embodied emissions from the HPC system hardware.

Given the definitions of scope 1-3 emissions given above, which scope(s) do you think these two different sources of HPC system use emissions fall into?

---
# <span style="color:green"> Solution: </span> What scope for HPC emissions?

Emissions from the electricity used would be classified as scope 2 emissions.

Embodied emissions from HPC system hardware would be classified as upstream scope 3 emissions.

---
# HPC electricity

Whether the emissions from electricity use on HPC systems are downstream scope 3 or scope 2 really depends on who is computing the emissions, and for what purpose.

From the point of view of the hardware vendor who sells and manufactures the HPC system, the electricity use falls into downstream scope 3 emissions.

For the operators and users of the HPC system, the electricity use would be classified as scope 2 emissions.

As we are approaching this subject as buyers, operators, and users of HPC systems, we will always classify the emissions from our electricity use on HPC systems as scope 2.

---
# How to calculate your HPC emissions

It can be tempting to only include the use of HPC that produced useful output in our emissions calculations,  __this should be avoided__.

The true amount of emissions includes  __all__  of our HPC system use to get us to the results we use, and so failed jobs (due to errors) or calculations that did not produce useful output must be included.

On the positive side, one of the ways we can reduce our emissions from use of HPC systems is to be more careful and eliminate emissions arising from these types of non-productive jobs.

---
# How to calculate your HPC emissions

__1. Gather energy use__

Many HPC systems now provide energy use data for jobs run on the system.

If this is the case, you can use these as the starting point for calculating your energy use of the HPC system.

If this is not available you may need to estimate the energy use of the resources used from component power draw.

Even if energy use is available, this may only cover compute nodes (or just processors on compute nodes) so you typically have to do some estimation of power draw of other components.

If you’re very lucky, the HPC system staff will have done this calculation for you: this has been done for the UK National Supercomputing Service, [ARCHER2](https://docs.archer2.ac.uk/user-guide/energy/#scope-2-emissions).

---
# How to calculate your HPC emissions

__1. Gather energy use__

We will cover two different ways to estimate the power draw of the HPC system.

The methodologies outlined all assume the compute nodes are homogeneous.

If this is not the case (such as the case where some nodes have GPUs and others do not), you should try to treat each homogeneous partition as its own smaller HPC system to help calculate energy use.

---
# How to calculate your HPC emissions

__1. Gather energy use__


First method (a) – use the total power draw of the system

This is one of the simplest ways to estimate the energy use.

Use the total power draw of the HPC system and divide it by the number of components to get a mean power draw per component that can be used to estimate energy use.


---
# How to calculate your HPC emissions

__1. Gather energy use__


<span style="color:gray"> First method (a) – use the total power draw of the system. </span>

<span style="color:gray"> This is one of the simplest ways to estimate the energy use. >/span>

<span style="color:gray"> Use the total power draw of the HPC system and divide it by the number of components to get a mean power draw per component that can be used to estimate energy use. </span>

For example, if the total power draw is 250 kW, and there are 512 GPUs then the mean power draw per GPU is 250/512 = 0.488 kW/GPU.

Therefore, the energy used for 12 hours use of 2 GPUs is estimated by 12 hours * 2 GPUs * 0.488 kW/GPU = 11.7 kWh.

You should use the component that you measure resource use in to compute the mean power draw: if your usage is in GPUh then compute per GPU, if your usage is in nodeh, compute power draw per node.
---
# How to calculate your HPC emissions

__1. Gather energy use__


The second method (b) – using per-component power draws.

This approach requires more detailed information being available on the power draw of different component through measurement or from the vendors of the components.

If you get your energy use from counters on the compute nodes, as is sometimes possible on HPC systems, then this approach allows you to estimate additional energy overheads that need to be added on in addition to measured power draw.

The next slide illustrates this approach through estimates for the ARCHER2 HPC system.

---
# How to calculate your HPC emissions

__1. Gather energy use__

.center[![:scale_img 80%](measurement0.png)]

---
# How to calculate your HPC emissions

__1. Gather energy use__

In this case we have a mix of data measured on the system (power draw of the compute nodes and power draw of the interconnect switches), and estimates from the vendor (storage systems and CDU).

The total power draw is estimated at 2808 kW; there are 5860 compute nodes and the unit of resource is nodeh so we can calculate the mean per-node power draw (including all of the components in the table) in the same way as method (a).

This gives 2808 / 5860 = 0.480 kW/node, and then we can use this to compute energy consumption based on number of nodeh we use.

---
# How to calculate your HPC emissions

__1. Gather energy use__

However on ARCHER2 we also have the total compute node energy use available per job to users from the Slurm scheduler. The table shows compute nodes contribute around 85% of the total power draw of ARCHER2, so an alternative method to compute is to use the measurement from the scheduler and add an additional 15% to cover the energy from other components. In fact, this is the methodology used for computing per-job energy use on ARCHER2

As well as the energy used by the system itself, there is also energy used by the plant that supplies heating and cooling to the HPC system.

Different data centres have different overheads and this is given by PUE (Power Use Efficiency) from earlier in the lesson. A PUE of 1.25 indicates that an additional 25% energy use is added on top of the system energy use to account for the plant.

---
# How to calculate your HPC emissions

__1. Gather energy use__

The PUE will vary with outside weather conditions. For the ARCHER2 example, PUE is typically less than 10% so as a conservative estimate they add an additional 10% energy use to the total to account for plant overheads.

* For the ARCHER2 example, the process for computing your total energy use becomes:
  * Measure total compute node energy use from all jobs run via node counters
  * Add 15% extra energy to cover energy use from other components
  * Add another 10% energy use on top of this total so far to cover plant overheads

---
# How to calculate your HPC emissions

__2. Determine local carbon intensity__

Once you have your energy use, then you need to convert this to emissions using the carbon intensity for the electricity supply for the HPC system.

In most cases, HPC systems are powered by the energy grid and many energy grids provide details on the carbon intensity as a function of time.

For the UK, the carbon intensity is dependent on location and time. You can access the values through different web services; a commonly used one is the [Carbon Intensity API](https://carbonintensity.org.uk/).

Carbon intensity is reported every 30 minutes for every region. To estimate your emissions can either use the fine-grained intensity matched to the runtimes of your HPC system use, or use an aggregate value over a longer period.

The aggregate value is a simpler choice for a first estimate.

---
# How to calculate your HPC emissions

__2. Determine local carbon intensity__

The table below shows the approximate average carbon intensities for the different regions of the UK national grid for 2024 ordered from lowest to highest.

.center[![:scale_img 80%](measurement1.png)]

---
# How to calculate your HPC emissions

__3. Determine embodied emissions__

We are only considering upstream scope 3 emissions; the emissions from electricity use are captured in the scope 2 emissions estimates.

Calculating the embodied emissions can be more difficult than operational emissions due to problems getting information on embodied emissions associated with HPC system hardware.

You may be lucky, and the HPC system you are using could already provide estimates of the embodied emissions that you can then use!

---
# How to calculate your HPC emissions

__3. Determine embodied emissions__


* If you do need to estimate this yourself, the major contributors to embodied emissions are likely to be:
  * Compute nodes
  * Interconnect switches
  * Storage
* Bear in mind each HPC system is different so other components may need to be taken into account.
* You should start by finding out which components make up the majority of the system, by number of items.
* Additionally, complex components (such as nodes, storage, switches) are likely to have higher embodied emissions than simpler components (such as pumps, fans, cables).

---
# How to calculate your HPC emissions

__3. Determine embodied emissions__


As an example, here is how the embodied emissions for ARCHER2 have been estimated.

.center[![:scale_img 70%](measurement2.png)]

---
# How to calculate your HPC emissions

__3. Determine embodied emissions__

Note that there is a large amount of uncertainty for scope 3 emissions due to lack of high quality embodied emissions data.

The number used for the compute node emissions is at the high end of estimated values for a CPU-only compute node; the actual value could be up to 15% lower.

If the lower value is used it reduces the overall estimated embodied emissions but does not significantly change the fraction of emissions attributed to the compute nodes.

We have not included embodied emissions associated with the data centre buildings and plant in this analysis. The [IRISCAST report](https://zenodo.org/records/7692451) provides an evaluation of these values.

While the total embodied emissions can be high, their long lifespan means that their contribution during the lifetime of the HPC system is generally much less significant than that of the HPC system hardware itself.

---
# How to calculate your HPC emissions
__4. Compute your total HPC emissions__

Rather than computing total energy use, and then using an aggregate value for the carbon intensity, it may make more sense to compute the operational emissions (carbon emissions from the electricity required for your HPC use) on a per-job basis using the carbon intensity value at the job time.

This is the approach used in the tools available on ARCHER2 for estimating emissions\.

---
# <span style="color:red"> Exercise: </span> Computing total emissions from HPC system use

* You are using (or running) a GPU-based HPC service and a particular project has used the following amounts of resource over 3 months:
  * 1100 GPUh
  * 3,542,000 kWh
* The total embodied emissions for the service are 6,500,000 kgCO<sub>2</sub>e, the service lifetime is 7 years, and there are 1000 compute nodes each with 8 GPU. The service is hosted in a location with a carbon intensity of 40 gCO<sub>2</sub>e/kWh.
  * Compute the scope 2 emissions for the project use.
  * Compute the scope 3 emissions rate in kgCO<sub>2</sub>e/GPUh
  * Compute the scope 3 emissions for the project use
  * Compute the total emissions for the project use
  * Do scope 2 or scope 3 emissions dominate or are they evenly matched?

---
# <span style="color:green"> Solution: </span> Computing total emissions from HPC system use

1. The scope 2 emissions from energy use by the project are given by E * CI, the energy used multiplied by the carbon intensity of the electricity supply. In this case, this is given by 3,542,000 kWh x 0.040 kgCO<sub>2</sub>e/kWh = 141,700 kgCO<sub>2</sub>e.

2. The scope 3 emissions rate per GPUh is the total scope 3 emissions for the service divided by number of GPUh available over the lifetime of the service.
The total GPUh over the service lifetime is estimated by 7 years x 365 days x 24 hours x 1000 nodes x 8 GPU per node = 490,560,000 GPUh.
The scope 3 emissions rate is given by 6,500,000 kgCO<sub>2</sub>e / 490,560,000 GPUh = 0.013 kgCO<sub>2</sub>e/GPUh
3. The scope 3 emissions for the project use is the number of GPUh used multiplied by the scope 3 emissions per GPUh: 1,100 GPUh * 0.013 kgCO<sub>2</sub>e/GPUh = 14.3 kgCO<sub>2</sub>e

4. Total emissions are scope 2 + scope 3 emissions: 141,700 kgCO<sub>2</sub>e + 14.3 kgCO<sub>2</sub>e = 141,714 kgCO<sub>2</sub>e

5. Scope 2 emissions (from electricity use) heavily dominate the emissions in this example.

---
template: titleslide
# HPC Carbon Intensity

---
# HPC-CI specification

The definition, application, and calculation of the HPC Carbon Intensity (HPC-CI) is heavily inspired by the [Software Carbon Intensity (SCI)](https://sci.greensoftware.foundation/) from the Green Software Foundation.

HPC-CI is a methodology to calculate your emissions from HPC system use and to encourage action towards eliminating emissions.

This is not a replacement for the GHG protocol, but an additional metric to help you understand how your HPC system use can be measured in terms of carbon emissions, and thus help you make informed decisions.

---
# HPC-CI specification

<span style="color:gray"> The definition, application, and calculation of the HPC Carbon Intensity (HPC-CI) is heavily inspired by the Software Carbon Intensity (SCI) from the Green Software Foundation.</span>

<span style="color:gray"> HPC-CI is a methodology to calculate your emissions from HPC system use and to encourage action towards eliminating emissions.</span>

<span style="color:gray"> This is not a replacement for the GHG protocol, but an additional metric to help you understand how your HPC system use can be measured in terms of carbon emissions, and thus help you make informed decisions. </span>

The GHG protocol and the HPC-E calculate  __total emissions__, HPC-CI is for calculating the  __rate of emissions__.

In automotive terms: GHG/HPC-E is like total carbon footprint of a car manufacturer and all the cars they produce every year, while HPC-CI is like miles per gallon.

---
# HPC-CI specification

It is important to note that it is not possible to reduce your HPC-CI rate by purchasing offsets in the form of neutralisations, compensations, or by offsetting electricity in the form of renewable energy credits.

This means any HPC system use that makes no effort toward reducing emissions but spends money on carbon credits cannot reduce the associated HPC-CI rate.

Offsets are an essential component of any climate strategy; however offsets are not eliminations.

If you make your HPC use more  __energy efficient__,  __hardware efficient__, or  __carbon aware__, your HPC-CI rate will decrease. Investing time or resources into one of these three principles is the only way to reduce the HPC-CI rate.

---
# The HPC-CI equation

The HPC-CI is a rate rather than a total and measures the intensity of emissions according to the chosen functional unit.

The specification currently does not prescribe the functional unit; you are free to pick whichever suits the output from your use of HPC systems best.

For example, this could be a metric from the software you use (ns simulated, number of years simulated, iterations) or a metric tied to research progress (number of compounds modelled, data points analysed, papers published).

Imagine you are simulating the dynamics of a biomolecular system (using software such as GROMACS, Amber, or NAMD), then you might want to choose number of ns simulated as your unit.

You can use multiple functional units to have multiple HPC-CI values, each of which may be more useful than others in different contexts.

---
# The HPC-CI equation
__6. Calculate HPC-CI rate__

* Now you have both the total emissions for your use of HPC systems, and the number of functional units arising from the same use of HPC systems you can calculate HPC-CI by dividing the total emissions by the total number of functional units.
* Continuing the biomolecular simulation, let’s say the total emissions from our HPC system use is 1500 kgCO<sub>2</sub>e, and the total number of functional units are 950 ns simulated:
  * HPC-CI = 1500 / 950 = 1.58 kgCO<sub>2</sub>e/ns
* As well as a tool to help quantify HPC system use, HPC-CI can be used to project emissions from HPC system use for future or planned projects. Many funding bodies are starting to ask for emissions estimates as part of the submission process.

---
# <span style="color:red"> Exercise: </span> HPC-CI rate

* In the previous exercise we computed the total HPC system emissions for 3 months of project use to be 14,84 kgCO<span>2</span>e. The project was modelling the climate and managed to simulate 3,680 years of Earth’s climate during that 3 month period using 1100 GPUh of resource.
  * What is the HPC-CI in kgCO<sub>2</sub>e per simulated year?
  * What is the HPC-CI in kgCO<sub>2</sub>e per GPUh?

---
# <span style="color:green"> Solution: </span> HPC-CI rate

Given by 14,184 kgCO<sub>2</sub>e / 3680 simulated years = 3.85 kgCO<sub>2</sub>e / simulated year.

Given by 14,184 kgCO<sub>2</sub>e / 1100 GPUh = 12.89 kgCO<sub>2</sub>e/GPUh.

---
# Key Points

The GHG protocol is a metric for measuring an organisation’s total carbon emissions and is used by organisations all over the world.

The GHG protocol puts carbon emissions into three scopes. Scope 3, also known as value chain emissions, refers to the emissions from organisations that supply others in a chain. In this way, one organisation’s scope 1 and 2 will sum up into another organisation’s scope 3.

You can use the GHG protocol to estimate your emissions from HPC system use but it requires access to reasonable quality information from the HPC systems you are using.

The HPC-CI is a metric designed specifically to calculate emissions from HPC systems and is a rate rather than a total. This can be used to measure improvements in emissions efficiency and drive reductions in emissions.

---
# <span style="color:red">Next Lecture</span>

<br>
## [Reducing Emissions](../7-reducing-emissions/)
