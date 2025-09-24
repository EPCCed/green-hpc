template: titleslide
# Carbon Reduction Methodologies

---
# Introduction

In recent years, many economic actors have sought to reach different climate goals by making various commitments to reducing carbon emissions.

The terms “net zero”, “carbon neutral”, “carbon negative”, and “climate neutral” have been used interchangeably with the primary objective to remove, reduce, and prevent carbon emissions.

As interest in these targets grows, it is essential to have a common understanding of what they mean and how to achieve them through the strategies and measurement procedures we have learnt.

---
# Carbon reduction methodologies

There are many ways to reduce emissions but it’s important to understand the exact mechanism of the reduction when thinking about reduction targets.

.center[![:scale_img 80%](carbon-reduction-methodologies0.png)]

---
# Abatement / Carbon Elimination

The [Science Based Targets initiative](https://sciencebasedtargets.org/) refers to a mechanism called [abatement](https://files.sciencebasedtargets.org/production/legacy/2020/09/foundations-for-net-zero-executive-summary.pdf), which means eliminating sources of CO<sub>2</sub> emissions associated with an organisation’s operations and [value chain](https://www.cisl.cam.ac.uk/education/graduate-study/pgcerts/value-chain-defs) so that they do not enter the atmosphere.

The value chain describes the full range of activities needed to create a product or service, from conception to distribution.

Abatement is not enough on its own; there will always be some emissions that cannot be eliminated due to technological or economic constraints, but it must from the core of every emissions reduction strategy.

To balance these residual emissions, we need to look at other mechanisms such as offsets, compensations, or neutralisations.

---
# <span style="color:red"> Exercise:</span> Strategies for abatement

Abatement is the critical component of carbon emissions reduction strategies. Pick one of the questions below (whichever is most relevant for your role) and write down some answers.

__Can you think of actions that individual users/researchers could take to implement abatement in their use of HPC systems?__

__Can you think of actions that a service operator could take to implement abatement in the operation of HPC systems?__

__Can you think of actions that an organisation procuring HPC systems could take to implement abatement when buying HPC systems?__

---
# <span style="color:green"> Solution: </span> Strategies for abatement

* Individual users:
  * Run fewer jobs; reduce wasted resources by having fewer job failures; run on systems that minimise emissions (spatial shifting); run when emissions from electricity are lower (temporal shifting).
* Service operators:
  * Build scheduler policies to eliminate emissions; provide tools and information that allow users to quantify their emissions and measure reductions; provide training on carbon emissions and abatement strategies.
* Service procurement:
  * Purchase the minimum amount of hardware possible for the service; build scoring on amount of embodied and operational emissions into the procurement process; site HPC systems at locations that have low carbon intensities; run services for as long as possible.

---
# Offsets

[Offsets](https://www.offsetguide.org/understanding-carbon-offsets/what-is-a-carbon-offset/) are direct investments in emission-reduction projects through the purchase of carbon credits on the voluntary carbon market (VCM).

The VCM is a decentralised market where private actors voluntarily buy and sell carbon credits that represent certified removals or reductions of greenhouse gases from the atmosphere.

To offset emissions you need to purchase the equivalent volume of carbon credits to compensate for those emitted, where one carbon credit corresponds to one tonne of CO<sub>2</sub> absorbed or reduced.

Various positive benefits can stem from these projects from ecosystem protection to empowering local communities.

To ensure these programs are implemented correctly, there are global standards that they must meet such as Verified Carbon Standard (VCS) and Gold Standard (GS).

---
# HPC-CI and Offsets

There are some limitations to carbon offsets and that is why they are not considered in an HPC-CI metric.

Imagine two projects, both running on an HPC service that is 100% carbon offset and matched 100% by renewable energy. Project A has invested significant time and resources into making sure it is using resources efficiently, whereas project B uses resources very inefficiently. For HPC-CI to be a useful metric, project A needs to score better than project B.

If HPC-CI considered offsets, both projects would score 0 due to the service they are using. This does not tell us about how efficiently they are using resources.


---
# HPC-CI and Offsets

<span style="color:gray"> There are some limitations to carbon offsets and that is why they are not considered in an HPC-CI metric. </span>

<span style="color:gray"> Imagine two projects, both running on an HPC service that is 100% carbon offset and matched 100% by renewable energy. Project A has invested significant time and resources into making sure it is using resources efficiently, whereas project B uses resources very inefficiently. For HPC-CI to be a useful metric, project A needs to score better than project B. </span>

<span style="color:gray"> If HPC-CI considered offsets, both projects would score 0 due to the service they are using. This does not tell us about how efficiently they are using resources. </span>

Although project B is emitting more carbon molecules into the atmosphere per unit of output, since its score is 0 and the lowest score is 0, why would it make further investments into improving its carbon efficiency?

HPC services and users need to have plans for how to both eliminate as well as neutralise emissions and the HPC-CI helps to drive the elimination of emissions due to use of HPC systems.


---
# Compensating / Carbon Avoidance

* [Compensations](https://abatable.com/blog/carbon-removal-vs-carbon-avoidance-projects/) are actions that organisations or individuals can take to help society avoid or reduce emissions. This is essentially investing in other organisations’ abatement projects.
* This includes actions such as:
  * __Conservation__ – credits are created based on carbon not released through protecting old trees.
  * __Community projects__  – these projects help communities worldwide, mainly developing ones, by introducing sustainable living methods.
  * __Waste to energy__  – these projects capture methane or landfill gas in smaller villages, human, or agricultural waste, and convert it into electricity.

---
# Neutralising / Carbon Removal

* [Neutralisations](https://abatable.com/blog/carbon-removal-vs-carbon-avoidance-projects/) are actions that organisations or individuals take to remove carbon from the atmosphere. Neutralisations refer to the removal and permanent storage of atmospheric carbon to counterbalance the effect of releasing CO<sub>2</sub> into the atmosphere.
* This includes actions such as:
  * __Enhancing natural carbon sinks__  that remove CO<sub>2</sub> from the atmosphere. For example\, forest restoration since photosynthesis removes CO<sub>2</sub> naturally. Forest expansion comes with challenges as it is essential not to impact the dynamics of farmland and food supply elsewhere. Modern farming methods can also prolong the length of time that carbon remains stored in soil.
  * __Direct air capture__  is the process of capturing CO<sub>2</sub> from the air and storing it permanently\, either underground or in long-lived products like concrete.

---
# Neutralising / Carbon Removal

* The effectiveness of these methods is typically measured based on whether they can deliver carbon removal at the scale and speed needed.
* In carbon removal projects, durability is a critical consideration; the durability of a project describes how long the carbon dioxide will be kept from the atmosphere.
* Short-term durability is up to 100 years, medium-term is 100 to 1,000 years, and long-term is more than 1,000 years.
  * Solutions that rely on Earth’s natural carbon cycle have short-term durability measured in decades, for example forestry projects have a durability of 40 to 100 years
  * Engineered solutions such as direct air capture often have long-term durability measured in millennia, for example direct air capture has a durability of 10,000 years

Long-term projects are typically orders of magnitude more expensive than short-term projects.

---
# Neutralising / Carbon Removal

Once emitted, carbon remains in the atmosphere for 5,000 years. To be considered net zero, carbon that has been emitted needs to be permanently removed.

A short-term carbon removal project will only remove carbon for 100 years (or less), after which it is back in the atmosphere, warming up our planet.

This is one of the reasons abatement is preferred to neutralisation; never releasing carbon is better than releasing carbon and trying to keep it out of the atmosphere for 5,000 years.

---
template: titleslide
# Climate Commitments

---
# Climate Commitments

There are many different emissions reduction strategies that an organisation can commit to, from carbon neutral to net zero. Understanding the different meanings and implications of each, and knowing which are implemented by the facilities you use can help you understand how your use of HPC fits within wider climate goals.

.center[![:scale_img 80%](climate-commitments0.png)]

---
# Carbon Neutral

To achieve carbon neutrality an organisation must measure its emissions, then match the total to its emissions offsets through carbon reduction projects. This can include carbon removal projects (neutralisations) and carbon avoidance projects (compensations).

Carbon neutrality is defined by an internationally recognised standard: [PAS 2060]({https://info.eco-act.com/hubfs/0%20-%20Downloads/PAS%202060/PAS%202060%20factsheet%20EN.pdf}).

Although this recommends an organisation sets abatement targets, it does not demand they reduce their emissions. To be considered carbon neutral, an organisation can just measure and offset without investing resources in eliminating their carbon emissions.


---
# Carbon Neutral

To be carbon neutral, you must cover direct emissions (scopes 1 and 2).

The general expectation is that organisations measure and offset their scopes 1 and 2, and business travel from scope 3. However, there is no specific requirement to include that.

Carbon neutral is a significant first step for any organisation since it encourages measurement.

However, there are not enough carbon offsets in the world to offset the emissions of all the organisations.

Any strategy that does not include abatement will not scale or help the world achieve the 1.5ºC set by the Paris Climate Agreement. This is where net zero comes into play.

---
# Net Zero

Net zero means reducing emissions according to the latest climate science and balancing remaining residual emissions through carbon removals (neutralisations).

Net zero, by definition, requires emissions reductions in line with a 1.5ºC pathway. All organisations must do this to achieve net zero global emissions by 2050.

The critical differentiator between net zero and carbon neutral is that net zero focusses on abatement rather than neutralisations and compensations. A net zero target aims to eliminate emissions and only to use offsetting for the residual emissions that you cannot eliminate.

---
# Net Zero

The [standard for net zero](https://files.sciencebasedtargets.org/production/files/foundations-for-net-zero-full-paper.pdf) is being developed by the [Science Based Targets initiative (SBTi)](https://sciencebasedtargets.org/).

They calculate that there is a 66% probability of limiting global warming to 1.5ºC if we reach a level of abatement of about 90% of all GHG emissions by mid-century.

So, to meet a net-zero target, an organisation needs to eliminate 90% of its emissions by 2050.

The remaining emissions can only be offset using neutralisations and permanent carbon removals.

A net-zero strategy would mean that the actual amount of carbon in the atmosphere remains constant.

Also, to be a net-zero target you must cover both direct and indirect, i.e. supply chain emissions (scopes 1, 2, and 3). This is significant since scope 3 often represents the majority of emissions.

For HPC facilities, part of these strategies include educating and putting policies and approaches in place to support users to understand and take action to reduce their emissions and maximise the carbon efficiency of their HPC use.

---
template: titleslide
# Reducing HPC-CI

---
# HPC-CI as part of a net-zero strategy

The HPC-CI is a metric specifically designed to drive the elimination of emissions. The only way to reduce your rate is to invest time and resources into actions that eliminate emissions.

The only activities the HPC-CI recognises as elimination actions are making your use of HPC systems more energy efficient, more hardware efficient, or consuming lower carbon energy sources.


---
# HPC-CI as part of a net-zero strategy

<span style="color:gray"> The HPC-CI is a metric specifically designed to drive the elimination of emissions. The only way to reduce your rate is to invest time and resources into actions that eliminate emissions. </span>

<span style="color:gray"> The only activities the HPC-CI recognises as elimination actions are making your use of HPC systems more energy efficient, more hardware efficient, or consuming lower carbon energy sources. </span>

Offsets are an essential component of any climate strategy; however offsets are not eliminations and therefore are not included in the HPC-CI metric.

Any net zero strategy needs to have plans for how to both eliminate as well as neutralise emissions.

The HPC-CI helps organisations and users drive the elimination of emissions due to HPC system use.

This makes the HPC-CI metric a useful component of any net zero strategy for operation and use of HPC systems.

---
# How can the HPC-CI rate be reduced?

We have mentioned how the HPC-CI metric is designed to drive abatement of emissions but how can users of HPC systems and organisations that procure HPC systems actually improve the HPC-CI metric?

We will look at this but it is worth noting that action is required by all of these parties to reduce emissions from HPC systems.

---
# Reduction in consumption of HPC

While we cover strategies for reducing emissions from a (roughly) constant amount of HPC use or HPC provision, it is clear that a key part of reduction of emissions from HPC use is a reduction in the consumption and provision of HPC.

At a fundamental level we need to reduce the amount of compute we are using, and the amount of compute hardware we are buying.


---
# Reduction in consumption of HPC

<span style="color:gray"> While we cover strategies for reducing emissions from a (roughly) constant amount of HPC use or HPC provision, it is clear that a key part of reduction of emissions from HPC use is a reduction in the consumption and provision of HPC. </span>

<span style="color:gray"> At a fundamental level we need to reduce the amount of compute we are using, and the amount of compute hardware we are buying. </span>

__“We seem to need reminding that computing is not exempt from having to drastically reduce emissions. Instead of assuming computing can innovate the path to a greater future, the bravest and most heroic action the computing sector could take is to show restraint and leadership, …”__ Bran Knowles et al. [Our House Is On Fire: The climate emergency and computing’s responsibility.](https://dl.acm.org/doi/pdf/10.1145/3503916)

---
# Users of HPC systems

* To improve the HPC-CI rate:
  * Ensure that the jobs you are running will produce useful or significant output even if they run correctly – do not run calculations or jobs without a clear understanding of what they add to the research project.
  * Carefully test input files and job scripts with small or short jobs before running at large scale to reduce the likelihood of wasted emissions.
  * Consider if you can achieve the same project goals with fewer jobs or calculations. For example, optimise the sampling choices when exploring parameter spaces.
* Similarly, for people involved in operating and procuring HPC systems, they need to work to ensure that users on the system have the best opportunity to do useful work and reduce wastage.
* This could be achieved through high quality documentation and training, and a service design that supports users in making the most of their resources.

---
# Users of HPC systems

Other strategies for improving the HPC-CI metric depend on the dominant component.

__Operational emissions dominate__

- Improve the energy efficiency of your use - this may involve power or frequency capping of the hardware you are using. (This improves the ratio of `E` to `R` in the HPC-CI equation.)
- Temporal shifting - run when carbon intensity is lower. (Reduces `CI`.)
- Spatial shifting - run on a system where carbon intensity is lower, run on hardware which has better energy efficiency for your use case, e.g. GPU may be more energy efficient for your use. (Reduces `CI`, or improves the ratio of `E` to `R`.)
- Run fewer calculations or jobs. (Reduces `E` and `M`.)


---
# Users of HPC systems

Other strategies for improving the HPC-CI metric depend on the dominant component.

<span style="color:gray"> __Operational emissions dominate__ </span>

- <span style="color:gray"> Improve the energy efficiency of your use - this may involve power or frequency capping of the hardware you are using. (This improves the ratio of `E` to `R` in the HPC-CI equation.) </span>
- <span style="color:gray"> Temporal shifting - run when carbon intensity is lower. (Reduces `CI`.) </span>
- <span style="color:gray"> Spatial shifting - run on a system where carbon intensity is lower, run on hardware which has better energy efficiency for your use case, e.g. GPU may be more energy efficient for your use. (Reduces `CI`, or improves the ratio of `E` to `R`.) </span>
- <span style="color:gray"> Run fewer calculations or jobs. (Reduces `E` and `M`.) </span>


__Embodied emissions dominate__
- Improve the performance of your use - more output per unit of time (even at the expense of energy efficiency through removing any power). (improves the ratio of `M` to `R`.)
- Spatial shifting - run on a system which has lower embodied emissions rate for your use. (Reduces `M`.)
- Run fewer calculations or jobs. (Reduces `E` and `M`.)

---
# Operators and procuring HPC systems

__Operational emissions dominate__
- Improve the energy efficiency of HPC systems - by capping the power or frequency of the hardware provided or purchasing hardware that is more energy efficient. (Improves the ratio of `E` to `R`.)
- Ensure that the power and cooling plant are as efficient as possible to minimise overheads. (Reduces `E`.)
- Enable temporal shifting (either automatically or user controlled) - for example, run workloads with higher power intensities at times when carbon intensity is lower. (Reduces `CI`.)
- Spatial shifting - site HPC systems in locations that have the lowest carbon intensities. (Reduces `CI`.)

---
# Operators and procuring HPC systems

__Embodied emissions dominate__
- Work with users to improve the performance of jobs on the service - more output per unit of time (even at the expense of energy efficiency through removing any power).
- Extend the lifetime of the service as long as possible to extract maximum value from the emissions already in the atmosphere from purchase of the HPC system.
- Purchase HPC systems that have the best ratio of embodied emissions to performance for the workloads that will be run.


---
# Key Points

There are a number of methodologies commonly applied to help in the overall fight against climate change. These fall into the general categories of carbon elimination (abatement), carbon avoidance (compensating), or carbon removal (neutralising).

Abatement is the most effective way to fight climate change although complete carbon elimination is not possible.

Compensating includes the adoption of renewable energy sources, sustainable living practices, recycling, planting trees, etc.

Neutralisations refer to the removal and permanent storage of atmospheric carbon to counterbalance the effect of releasing CO<sub>2</sub> into the atmosphere. Neutralisations tend to remove the carbon from the atmosphere in the short and medium term.

Net zero aims to eliminate emissions and only offset the residual emissions that you cannot eliminate to reach the 1.5ºC target set by the Paris Climate Agreement.

Which strategies users or HPC system operators prioritise to reduce emissions depend on if the operational or embodied emissions dominate.

__A key part of reducing emissions from HPC use is reducing our consumption of HPC resources.__
