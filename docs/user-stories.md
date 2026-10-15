# User Stories

Format: As a [type of user], I want [goal], so that [reason or benefit].

## User Story 1: Submit Computing Workloads

As a student, I want to submit computing workloads for simulation, so that I can evaluate how my jobs may be handled.

**Related Requirements:** FR1, FR2

**Acceptance Criteria**
- Given I have a computing workload, when I submit it, then the system accepts it for simulation.
- Given a workload has been submitted, when the simulation runs, then resource allocation is simulated.

## User Story 2: Compare Resource Allocation Policies

As a researcher, I want to compare fixed-capacity, threshold-based, and adaptive resource allocation policies, so that I can evaluate their performance under different workload conditions.

**Related Requirements:** FR3, FR4, FR5, FR6, NFR3

**Acceptance Criteria**
- The system simulates fixed-capacity, threshold-based, and adaptive resource allocation policies.
- The system records average waiting time, average completion time, maximum queue length, and active server usage for each policy.
- The system allows results from all three policies to be compared under the same workload conditions.
- Repeating a simulation with the same workload, policy settings, and random seed produces the same results.

## User Story 3: Review Simulation Results

As a campus IT administrator, I want simulation results presented clearly, so that I can evaluate resource usage and system performance.

**Related Requirements:** NFR1, NFR2, NFR4

**Acceptance Criteria**
- The system completes a simulation of 1,000 jobs within 10 seconds under the documented test configuration.
- A user can configure a workload and start a simulation using no more than five main interaction steps.
- The implementation separates workload generation, resource allocation policies, and performance measurement into distinct modules.