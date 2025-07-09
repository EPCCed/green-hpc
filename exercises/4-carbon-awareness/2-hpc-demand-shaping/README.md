template: titleslide
# Carbon Awareness
## Demand Shaping and Temporal Shifting in HPC
### Exercise 4.2



---
# <span style="color:red">Exercise:</span> Demand Shaping and Temporal Shifting in HPC

A typical HPC system has a wide variety of jobs to schedule and different HPC systems have different scheduling and charging policies
for jobs that run on them.

Write down some ideas on how you could potentially modify the scheduling and charging of jobs to enable demand shaping and/or
temporal shifting on an HPC system?



---
# <span style="color:green">Solution:</span> Demand Shaping and Temporal Shifting in HPC

- **Scheduling based on power intensity**
  - Manual: users place jobs into different queues based on predicted power intensity and are charged accordingly.
  - Automatic: system detects/predicts power intensity of jobs and schedules accordingly.

- **Credit based system**
  - Users earn tokens according to the carbon efficiency of the software they run during a defined *earn* period. This is followed by a *spend* period, when the users with the most tokens get priority on the system.
  - This type of approach has been piloted on the [Fugaku machine](https://doi.ieeecomputersociety.org/10.1109/SC41406.2024.00030) in Japan.

- **Power capping**
  - A system-wide power cap fluctuates with grid carbon intensity.
  - A software app is required to distribute power cap amongst jobs, <br>e.g. [HPE's Powersched](https://cug.org/proceedings/cug2023_proceedings/includes/files/pap113s2-file1.pdf).