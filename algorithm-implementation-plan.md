Algorithm Implementation and Technical Verification

1. Introduction

This section describes the implementation and verification requirements for three packet scheduling algorithms: First-In-First-Out (FIFO), Priority Queuing (PQ), and Weighted Fair Queuing (WFQ).

The algorithms will be evaluated in a simulated bandwidth-constrained network environment to investigate their scheduling behaviour and performance.

2. FIFO Implementation

FIFO operates using a single queue in which packets are transmitted in the order they arrive.

Implementation requirements:

- Create a single packet queue.
- Insert incoming packets at the rear of the queue.
- Transmit packets from the front of the queue.
- Remove each packet after transmission.

Verification tests:

- Confirm that packets are transmitted in arrival order.
- Confirm that the queue handles multiple incoming packets.
- Test behaviour when the queue becomes full.
- Verify that packets are handled correctly when the queue is empty.

3. Priority Queuing (PQ) Implementation

Priority Queuing uses multiple queues to classify packets according to predefined priority levels.

Implementation requirements:

- Create separate queues for different priority levels.
- Classify incoming packets according to their assigned priority.
- Serve the highest-priority non-empty queue first.
- Serve lower-priority queues when higher-priority queues are empty.

Verification tests:

- Confirm that high-priority packets are served before lower-priority packets when both are waiting.
- Verify that packets within each priority queue follow the defined ordering policy.
- Test behaviour when multiple priority queues contain packets.
- Investigate starvation when high-priority traffic continuously arrives.

4. Weighted Fair Queuing (WFQ) Implementation

WFQ allocates service among competing traffic flows according to assigned weights.

Implementation requirements:

- Identify and classify competing traffic flows.
- Assign a weight to each flow.
- Maintain separate queues or logical scheduling state for each flow.
- Schedule packets according to the configured weighted fair service policy.

Verification tests:

- Confirm that packets from different flows receive service.
- Verify that configured weights influence bandwidth allocation.
- Test the algorithm under different traffic loads.
- Examine whether bandwidth is distributed fairly among competing flows.

5. Comparative Technical Verification

The three algorithms will be tested using equivalent traffic inputs and network configurations.

Test condition| FIFO| PQ| WFQ
Single traffic flow| Test| Test| Test
Multiple competing flows| Test| Test| Test
High network congestion| Test| Test| Test
Limited bandwidth| Test| Test| Test
Queue capacity reached| Test| Test| Test
Continuous high-priority traffic| N/A| Test| N/A
Different flow weights| N/A| N/A| Test

6. Implementation Considerations

The implementation must use consistent network parameters, including bandwidth capacity, queue limits and traffic inputs.

Special attention will be given to:

- Correct packet classification.
- Queue management.
- Scheduling order.
- Packet transmission behaviour.
- Queue overflow and packet dropping.
- Consistency of experimental configurations.


The selected simulation environment and its capabilities will determine the final implementation approach.

7. Expected Outcome

The expected outcome is a technically verified implementation of FIFO, PQ and WFQ scheduling algorithms that can be tested under controlled bandwidth-constrained network conditions.

The verification process will help identify implementation errors and ensure that the algorithms behave according to their intended scheduling principles before performance measurements are conducted.
