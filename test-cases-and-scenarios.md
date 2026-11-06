Test Cases and Experimental Scenarios

1. Introduction

This document defines the experimental test cases that will be used to compare First-In-First-Out (FIFO), Priority Queuing (PQ), and Weighted Fair Queuing (WFQ) under bandwidth-constrained network conditions.

The purpose is to ensure that all three scheduling algorithms are evaluated using consistent traffic inputs and network configurations.

2. Experimental Objectives

The experiments aim to:

1. Examine how each scheduling algorithm handles incoming network packets.
2. Evaluate performance under different bandwidth constraints.
3. Observe packet delays and packet loss during network congestion.
4. Assess how effectively each algorithm distributes bandwidth among competing flows.
5. Identify the strengths and limitations of FIFO, PQ, and WFQ.

3. Proposed Test Scenarios

Scenario 1: Normal Network Conditions

Purpose: Establish baseline performance when network demand does not exceed available bandwidth.

- Use identical traffic inputs for all three algorithms.
- Configure sufficient bandwidth to avoid sustained congestion.
- Measure throughput, average packet delay, packet loss and flow fairness.

Expected observation: All algorithms should deliver relatively stable performance, with limited packet loss.

Scenario 2: Moderate Network Congestion

Purpose: Examine scheduling behaviour when traffic demand begins to exceed available bandwidth.

- Increase the offered traffic load.
- Maintain the same bottleneck bandwidth across algorithms.
- Use equivalent queue capacity and drop policies.
- Record all four performance metrics.

Expected observation: Differences in packet delay, throughput distribution and packet loss may become more noticeable.

Scenario 3: Heavy Network Congestion

Purpose: Evaluate algorithm performance when the network experiences high traffic demand.

- Increase offered traffic load significantly.
- Maintain identical network conditions for each algorithm.
- Observe queue build-up and packet drops.
- Record the impact on individual traffic flows.

Expected observation: FIFO may experience increased delays, PQ may favour high-priority traffic while disadvantaging lower-priority traffic, and WFQ may provide more controlled bandwidth sharing according to configured weights.

Scenario 4: Mixed-Priority Traffic

Purpose: Evaluate how scheduling algorithms handle traffic with different priority requirements.

- Define high-priority and low-priority traffic classes.
- Apply identical traffic inputs to each algorithm.
- Configure and document the PQ priority rules.
- Define flow weights for WFQ.
- Compare delay and throughput between traffic classes.

Expected observation: PQ should favour high-priority traffic. WFQ should allocate service according to configured weights. FIFO should process packets in arrival order.

Scenario 5: Unequal Traffic Flows

Purpose: Examine how scheduling algorithms distribute resources among flows with different traffic demands.

- Introduce multiple competing flows.
- Give the flows different offered traffic rates.
- Maintain the same bottleneck bandwidth and queue capacity.
- Measure individual flow throughput and calculate Jain's Fairness Index.

Expected observation: The algorithms may distribute available bandwidth differently. Fairness must be interpreted in relation to the intended flow weights and traffic requirements.

4. Performance Metrics

The following metrics will be collected in every applicable scenario:

Metric| Measurement
Throughput| Successfully received data per unit time
Average packet delay| Average time taken by successfully received packets
Packet loss| Percentage of transmitted packets not received
Flow fairness| Jain's Fairness Index calculated from individual flow throughputs

5. Experimental Controls

To ensure a fair comparison:

- Use the same traffic trace and packet arrival patterns for all algorithms.
- Maintain identical bottleneck bandwidth settings.
- Use comparable total queue capacities.
- Apply the same packet-drop policy.
- Keep experiment duration and measurement intervals consistent.
- Record the PQ priority configuration and WFQ flow weights.
- Repeat experiments where randomness is involved.
- Preserve raw measurements for verification.

6. Expected Challenges

Potential challenges include:

1. Configuring realistic traffic loads.
2. Ensuring the three algorithms receive identical traffic inputs.
3. Preventing differences in queue capacity from biasing the comparison.
4. Measuring packet delay and loss consistently.
5. Interpreting fairness when WFQ uses unequal weights.
6. Avoiding conclusions that cannot be supported by experimental results.

7. Conclusion

These test scenarios provide a structured approach for evaluating FIFO, PQ and WFQ under different network conditions. The results will help establish how each scheduling algorithm performs in terms of throughput, packet delay, packet loss and flow fairness.

Note: Actual results and conclusions will only be added after the experiments have been conducted. The scenarios and expected observations in this document are proposed hypotheses, not measured findings.
