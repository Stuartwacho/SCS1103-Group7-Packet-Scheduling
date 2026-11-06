Data Analysis, Comparative Visualisation and Experiment Reproducibility

1. Introduction

This section outlines the methodology that will be used to analyse, compare, visualise and interpret experimental results obtained from evaluating First-In-First-Out (FIFO), Priority Queuing (PQ) and Weighted Fair Queuing (WFQ).

The analysis will focus on four main performance metrics:

* Throughput.
* Average packet delay.
* Packet loss.
* Flow fairness using Jain’s Fairness Index.

The objective is to establish how the three scheduling algorithms perform under identical bandwidth-constrained network conditions and identify their respective strengths, weaknesses and performance trade-offs.

2. Data Collection and Preparation

Experimental measurements will be collected from network simulations under controlled conditions.

To ensure a fair comparison, all three scheduling algorithms will use:

* The same network topology.
* Identical traffic input and flow characteristics.
* The same available bandwidth.
* Identical queue capacities.
* The same simulation duration.
* Consistent packet-generation conditions.

Where random traffic generation is used, corresponding random seeds will be applied across the algorithms.

The collected measurements will be organised into structured datasets containing the algorithm used, simulation run, traffic flow and corresponding performance measurements.

The data will be checked for missing values, inconsistencies and abnormal observations before analysis.

3. Comparative Data Analysis Methodology

A quantitative comparative approach will be used to evaluate the performance of FIFO, PQ and WFQ.

3.1 Throughput Analysis

Throughput will measure the amount of successfully delivered data over a specified period.

Throughput will be calculated as:

Throughput (Mbps) = Total successfully received data (bits) / Simulation time (seconds) / 1,000,000.

The analysis will compare:

* Overall network throughput.
* Individual flow throughput.
* Throughput distribution among competing flows.

The algorithm achieving higher throughput will demonstrate better utilisation of the available network bandwidth under the tested conditions.

3.2 Average Packet Delay Analysis

Average packet delay will measure the time taken for packets to travel from their source to their destination.

Average delay will be calculated as:

Average Delay = Sum of individual packet delays / Total number of successfully received packets.

The analysis will compare the average delay experienced under each scheduling algorithm.

Where possible, additional delay measurements, such as the 95th percentile, will be considered to identify whether some packets experience significantly longer delays.

Lower delay values will indicate faster packet delivery.

3.3 Packet Loss Analysis

Packet loss will measure the proportion of transmitted packets that fail to reach their destination.

Packet loss will be calculated as:

Packet Loss (%) = [(Packets transmitted - Packets received) / Packets transmitted] × 100.

The analysis will compare packet-loss percentages across FIFO, PQ and WFQ.

This will help establish how effectively each algorithm handles congestion and competing traffic demands.

3.4 Flow Fairness Analysis

Flow fairness will evaluate how equally the available bandwidth is distributed among competing traffic flows.

Jain’s Fairness Index will be used:

JFI = (Σxi)² / [n × Σ(xi²)]

Where:

* xi = Throughput of individual flow i.
* n = Total number of competing flows.

The index ranges from 1/n to 1 for positive flow throughputs.

A value closer to 1 indicates a more equal distribution of throughput among the flows.

The analysis will compare the fairness achieved by each scheduling algorithm.

4. Comparative Statistical Analysis

To improve the reliability of the findings, each scheduling algorithm will be evaluated through repeated simulation runs using consistent experimental conditions.

The following statistical measures will be calculated:

* Mean: To determine the average performance.
* Standard deviation: To measure variation between simulation runs.
* Minimum and maximum: To identify the observed performance range.
* 95% confidence intervals: To communicate uncertainty around estimated mean performance.

Where appropriate, paired statistical comparisons will be conducted using corresponding simulation runs.

A paired t-test may be used when its assumptions are satisfied, while the Wilcoxon signed-rank test may be considered when they are not.

The analysis will establish whether observed performance differences are consistent and statistically meaningful rather than relying only on individual simulation results.

4.1 Percentage Performance Difference

The percentage difference between scheduling algorithms will also be calculated using FIFO as the reference algorithm.

Percentage difference = [(Alternative algorithm result - FIFO result) / FIFO result] × 100.

This will help quantify the relative performance improvement or deterioration achieved by PQ and WFQ.

The direction of improvement will be interpreted according to the metric. For example, higher throughput is generally desirable, whereas lower delay and packet loss are desirable.

5. Comparative Results Tables

The following tables will be used to organise and compare the experimental findings.

5.1 Overall Performance Comparison

Performance metric	FIFO	PQ	WFQ
Throughput (Mbps)	Pending	Pending	Pending
Average delay (ms)	Pending	Pending	Pending
Packet loss (%)	Pending	Pending	Pending
Jain’s Fairness Index	Pending	Pending	Pending

Actual measurements will be entered after the experiments have been completed.

5.2 Comparative Performance Analysis

A second table will be used to highlight the relative performance differences.

Metric	PQ vs FIFO (%)	WFQ vs FIFO (%)
Throughput	Pending	Pending
Average delay	Pending	Pending
Packet loss	Pending	Pending

Fairness differences will be reported separately using the absolute difference in Jain’s Fairness Index.

Individual flow measurements will also be retained to support the fairness analysis.

6. Data Visualisation Methodology

Comparative graphs will be developed to communicate the experimental findings clearly.

Python, using libraries such as Pandas and Matplotlib, may be used to process the datasets and generate the visualisations.

6.1 Throughput Comparison

A grouped bar chart will compare the throughput achieved by FIFO, PQ and WFQ.

Where multiple traffic flows are used, throughput will also be presented per flow.

This will help identify which algorithm achieves better bandwidth utilisation and how throughput is distributed among competing flows.

6.2 Average Packet Delay Comparison

A comparative bar chart will display the average packet delay for each algorithm.

Error bars will be included to represent variability or 95% confidence intervals.

A lower average delay will indicate faster packet delivery under the measured conditions.

6.3 Packet Loss Comparison

A bar chart will display the packet-loss percentage recorded for each scheduling algorithm.

This will help identify which algorithm handles congestion more effectively.

6.4 Flow Fairness Comparison

A bar chart will compare Jain’s Fairness Index values for FIFO, PQ and WFQ.

Values closer to 1 will indicate more equal throughput distribution among competing flows.

6.5 Throughput and Delay Over Time

Line graphs will be used to show how throughput and packet delay change throughout the simulation period.

This will help identify performance fluctuations, congestion periods and possible instability in scheduling behaviour.

6.6 Performance Variability

Box plots will be used where repeated simulation measurements are available.

These will show the distribution of results, including the median, spread and potential outliers.

This will help determine whether an algorithm produces consistent performance across repeated experiments.

7. Interpretation of Comparative Results

The findings will be interpreted by examining the performance of each scheduling algorithm against the four selected metrics.

The analysis will investigate:

* Which algorithm achieves the highest throughput?
* Which algorithm produces the lowest average packet delay?
* Which algorithm experiences the lowest packet loss?
* Which algorithm distributes bandwidth most fairly?
* How consistent is each algorithm across repeated simulation runs?

The analysis will also examine the trade-offs between performance metrics.

For example, PQ may reduce the delay experienced by high-priority traffic while disadvantaging lower-priority flows. WFQ may provide a more controlled distribution of bandwidth according to configured weights, while FIFO serves packets in their arrival order.

These behaviours will be treated as possible explanations to investigate, not predetermined experimental conclusions.

The final conclusions will be based on actual measurements and statistical evidence.

8. Experiment Reproducibility

To ensure that the experiments can be repeated and independently verified, the group will document:

* Dataset source and exact trace filename.
* Simulation software and version.
* Network topology.
* Available bandwidth.
* Queue capacity and overflow policy.
* Scheduling algorithm configurations.
* Traffic classification rules.
* WFQ weight allocation.
* Simulation duration.
* Number of simulation runs.
* Random seeds, where applicable.
* Measurement and calculation procedures.
* Data-processing scripts and visualisation tools.

The same experimental conditions will be maintained when comparing corresponding scheduling algorithms.

9. Results Documentation and Version Control

The experimental findings, datasets, scripts and visualisations will be stored in the GitHub repository using an organised directory structure.

Proposed structure:

results/
    datasets/
        raw/
        processed/
    tables/
        comparative-results.csv
    graphs/
        throughput-comparison.png
        delay-comparison.png
        packet-loss-comparison.png
        fairness-comparison.png
        performance-over-time.png
        performance-variability.png
    scripts/
        data_analysis.py
        visualisation.py
    analysis.md

The group will retain the original numerical measurements and processing scripts so that the results can be independently checked and reproduced.

10. Expected Outcome

The expected outcome is a quantitative and visual comparison of FIFO, PQ and WFQ under simulated bandwidth-constrained network conditions.

The methodology will provide a structured approach to evaluating throughput, packet delay, packet loss and flow fairness.

The combination of comparative statistics, graphical visualisation and documented experimental procedures will support transparent interpretation, reliable conclusions and reproducibility of the research findings.