Performance Measurement and Results Evaluation

1. Introduction

The performance evaluation of FIFO, Priority Queuing (PQ), and Weighted Fair Queuing (WFQ) will be based on four key network performance metrics: throughput, packet delay, packet loss, and flow fairness.

These metrics will be used to determine how effectively each scheduling algorithm manages network traffic under simulated bandwidth-constrained conditions.

2. Performance Metrics

2.1 Throughput

Throughput measures the amount of data successfully received over a network during a specific period.

Formula:

Throughput = Successfully received data (bits) / Time taken (seconds)

Unit: Megabits per second (Mbps).

A higher throughput generally indicates better data delivery, provided the comparison uses equivalent traffic and experimental conditions.

2.2 Packet Delay

Packet delay measures the time taken for a packet to travel from its source to its destination.

Formula:

Average Delay = Sum of individual packet delays / Number of packets received

Unit: Milliseconds (ms).

Lower average packet delay generally indicates faster packet delivery.

2.3 Packet Loss

Packet loss represents the percentage of transmitted packets that fail to reach their destination.

Formula:

Packet Loss (%) = ((Packets sent - Packets received) / Packets sent) × 100

A lower packet-loss percentage indicates more reliable packet delivery.

2.4 Flow Fairness

Flow fairness measures how equally available network bandwidth is distributed among competing traffic flows.

The study will use Jain's Fairness Index.

Formula:

J = (x1 + x2 + ... + xn)² / [n(x1² + x2² + ... + xn²)]

Where:

- J represents the fairness index.
- x represents the throughput of an individual flow.
- n represents the total number of competing flows.

The index ranges from 1/n to 1 for positive flow throughputs. A value closer to 1 indicates a more equal distribution of throughput.

3. Comparative Evaluation

The three scheduling algorithms will be evaluated using identical traffic inputs, bandwidth limits and queue configurations.

The following table will be used to record the experimental results.

Performance Metric| FIFO| PQ| WFQ
Throughput (Mbps)| To be measured| To be measured| To be measured
Average delay (ms)| To be measured| To be measured| To be measured
Packet loss (%)| To be measured| To be measured| To be measured
Jain's Fairness Index| To be measured| To be measured| To be measured

4. Results Analysis

The collected results will be analysed using comparative tables and graphs.

The analysis will investigate:

- Which algorithm achieves the highest throughput.
- Which algorithm produces the lowest average packet delay.
- Which algorithm experiences the lowest packet loss.
- Which algorithm provides the fairest bandwidth distribution.

The study will also examine the trade-offs between the algorithms, particularly the possibility of starvation in Priority Queuing and the bandwidth distribution characteristics of Weighted Fair Queuing.

5. Expected Evaluation Outcome

The performance evaluation is expected to provide quantitative evidence of the strengths and limitations of FIFO, PQ and WFQ under the selected bandwidth-constrained simulation conditions.

The final conclusions will be based on measured experimental results rather than assumptions about which algorithm performs best.
