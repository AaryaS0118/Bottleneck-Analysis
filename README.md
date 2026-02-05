# Bottleneck-Analysis
Independent manufacturing engineering project analyzing a PET plastic water bottle production line using capacity modeling, bottleneck analysis, and throughput optimization based on industry benchmarks.

# Bottleneck Analysis of a PET Plastic Water Bottle Production Line

## Overview
This project presents an independent manufacturing engineering analysis of a PET plastic water bottle production line. The goal is to identify throughput-limiting bottlenecks, quantify system performance, and evaluate optimization strategies using both analytical capacity modeling and a discrete-event simulation.

The study models a realistic, single-lane bottling line using industry-benchmarked cycle times scaled from publicly available equipment specifications (e.g., Krones and Sidel).

---

## Manufacturing Process Modeled
The production line consists of the following stages:

1. PET Preform Injection Molding  
2. Blow Molding  
3. Bottle Rinsing  
4. Water Filling  
5. Capping  
6. Labeling  
7. Packaging  

Each stage is modeled with a defined cycle time and number of machines to reflect real-world manufacturing constraints.

---

## Analytical Methodology
The analytical portion of the project includes:

- Capacity calculation for each process stage  
- Identification of the bottleneck using minimum-capacity logic  
- System throughput estimation  
- Utilization analysis  
- Evaluation of optimization scenarios  

### Key Formula
Capacity per stage:
\[
\text{Capacity (bottles/hour)} = \frac{3600}{\text{Cycle Time (sec/bottle)}} \times \text{Number of Machines}
\]

The system bottleneck is identified as the stage with the lowest capacity.

---

## Simulation Methodology
To complement the analytical model, a discrete-time simulation was implemented in Python.

### Simulation Characteristics
- Time step: 1 second  
- Simulation horizon: 8 hours  
- Queues modeled between each process stage  
- Multiple machines supported per stage  
- Metrics collected:
  - Throughput (bottles/hour)
  - Total completed units
  - Average work-in-process (WIP)
  - Stage utilization

The simulation validates analytical results and demonstrates dynamic effects such as queue buildup and resource utilization.

---

## Scenarios Evaluated
Three scenarios were analyzed:

1. **Baseline System**  
   - Single blow molding machine  
   - Bottleneck at blow molding  

2. **Add Second Blow Molding Machine**  
   - Increased blow molding capacity  
   - Bottleneck shifts to labeling  

3. **Reduce Blow Molding Cycle Time**  
   - Improved process efficiency  
   - Increased system throughput  

---

## Key Results
- Blow molding was identified as the primary bottleneck in the baseline system.
- Increasing blow molding capacity improved throughput by approximately 25%.
- Once the bottleneck was addressed, downstream processes became the new constraints.
- Simulation results closely aligned with analytical capacity calculations.

---

## Tools & Technologies
- C++
- Google Sheets (analytical modeling & visualization)

---


---

## Data Sources & Assumptions
- Cycle times were derived from publicly available bottling equipment benchmarks.
- Values were scaled to represent a mid-scale, single-lane production line.
- The project does not use proprietary or confidential manufacturing data.

---

## Key Engineering Concepts Demonstrated
- Bottleneck analysis  
- Capacity planning  
- Theory of Constraints  
- Utilization and throughput modeling  
- Manufacturing systems thinking  

---

## Author
**Aarya Sukhadiya**  
B.S. Computer Engineering, San Jose State University  

---

## Notes
This project was created for academic and portfolio purposes to demonstrate applied manufacturing and systems engineering analysis.

