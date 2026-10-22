# Requirements

## Functional requirements (what the system must DO)

**FR1:** The system shall generate computing jobs with configurable arrival times and processing durations.

**FR2:** The system shall simulate a fixed-capacity resource allocation policy.

**FR3:** The system shall simulate a threshold-based resource allocation policy using predefined thresholds.

**FR4:** The system shall simulate an adaptive resource allocation policy using queue length and recent job arrival rates.

**FR5:** The system shall calculate average waiting time, average completion time, maximum queue length, and active server usage for each policy.

**FR6:** The system shall display a comparison of the results for all three policies under the same workload conditions.

## Non-functional requirements (how the system must PERFORM)

**NFR1 — Performance:** The system shall complete a simulation of 1,000 jobs within 10 seconds on the development computer under the documented test configuration.

**NFR2 — Usability:** A user shall be able to configure a workload and start a simulation using no more than five main interaction steps.

**NFR3 — Reliability:** The system shall produce the same results when the same workload, policy settings, and random seed are used.

**NFR4 — Maintainability:** The implementation shall separate workload generation, resource allocation policies, and performance measurement into distinct modules.