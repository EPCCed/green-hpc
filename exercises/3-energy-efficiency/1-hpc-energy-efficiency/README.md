template: titleslide
# Energy Efficiency
## Energy Efficiency on HPC Systems
### Exercise 3.1



---
# <span style="color:red">Exercise:</span> Energy efficiency on HPC systems

The [GROMACS application](https://docs.archer2.ac.uk/research-software/gromacs/) running on ARCHER2 for a simulation time of 0.02 ns<br>
has the following performance for a range node of counts and CPU frequency settings.

| <br>Nodes |||| 2.0 GHz<br>Runtime [s], kWh |||| 2.25 GHz + boost<br>Runtime [s], kWh |
| ---:      |||| ---:                        |||| ---:                                 |
| 1         |||| 369, 0.0464                 |||| 288, 0.0464                          |
| 2         |||| 198, 0.0450                 |||| 156, 0.0465                          |
| 3         |||| 155, 0.0438                 |||| 109, 0.0465                          |
| 4         |||| 117, 0.0471                 ||||  93, 0.0513                          |

What are the most energy efficient combinations of node count and CPU frequency <br>in terms of kWh/ns?

Which combination has the worst performance and what is the percentage difference between this and
the best-performing combination?



---
# <span style="color:green">Solution:</span> Energy efficiency on HPC systems

We can compute the energy efficiency in kWh/ns by dividing the energy use by the simulation time in nanoseconds,
which is 0.02 ns.

| <br>Nodes |||| 2.0 GHz<br>Runtime [s], kWh/ns |||| 2.25 GHz + boost<br>Runtime [s], kWh/ns |
| ---:      |||| ---:                        |||| ---:                                 |
| 1         |||| 369, 2.32                 |||| 288, 2.32                          |
| 2         |||| 198, 2.25                 |||| 156, 2.32                          |
| 3         |||| 155, 2.19                 |||| 109, 2.32                          |
| 4         |||| 117, 2.36                 ||||  93, 2.56                          |

So, the most energy efficient combination is 3 nodes at 2 GHz CPU clock frequency and the worst is 4 nodes with 2.25 GHz + boost CPU clock frequency.
And the worst case is around 17% less energy efficient than the best case.

While this difference may not amount to much energy for a single run, it can lead to a significant reduction in consumed energy if many simulations
are to be run as part of a project.