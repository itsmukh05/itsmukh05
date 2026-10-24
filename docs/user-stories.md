### User Story 1. Configure a workload Scenario

**User Story 1:** As a campus IT administrator, I want to configure the number of jobs and available computing resources, so that I can examine different workload scenarios.

**Related requirements:** FR1, FR5.

**Acceptance criteria:**
- The simulator accepts valid values for the number of jobs, available servers, and simulation duration.
- The simulator can run both normal-demand and high-demand synthetic workloads using the configured parameters.


### User Story 2. Simulate Job Allocation

**User story:** As a computing resource manager, I want to simulate how jobs are assigned to available computing resources, so that I can understand how jobs are processed under different workload conditions.

**Related requirements:** FR2, FR3, FR4.

**Acceptance criteria:**
- The simulator records job arrival, execution start, and completion times.
- When all servers are busy, newly arriving jobs are handled according to the implemented queueing and resource-allocation rules.
- The simulator records queue lengths and resource utilisation during the simulation.


### User Story 3. Evaluate Simulator Correctness and Performance

**User story:** As a simulator developer, I want to compare simulation results with expected outcomes and measure execution time, so that I can evaluate the correctness and computational performance of the simulator.

**Related requirements:** FR6, NFR1, NFR2.

**Acceptance criteria:**
- The simulator produces the expected results for all specified predefined test cases.
- Execution time is recorded for workloads of 100, 1,000, and 10,000 jobs with at least three runs for each workload size.
- The recorded measurements can be used to compare computational performance across workload sizes.
