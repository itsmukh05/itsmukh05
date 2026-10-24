# Requirements

## Functional requirements


**FR1 — Configure simulation parameters:** The simulator must let users set parameters before starting a simulation, including the number of jobs, the number of computing resources and the simulation duration. Users can adjust these settings to match their needs and the simulator uses the selected parameters during the run.

**FR2 — Simulate job arrivals, queues, execution, and completion:** The simulator must show how jobs move through the system from arrival to completion, so users can understand each stage of the job lifecycle.

**FR3 — Allocate jobs to computing resources:** The simulator must assign jobs to available computing resources according to the implemented resource-allocation mechanism and process each job to produce a result.

**FR4 — Record simulation results:** The simulator must record job completion times, queue lengths and resource utilisation, so users can analyse performance and review the results.

**FR5 — Support workload conditions:** The simulator must let users test low, normal, and high-demand workloads to observe how the system behaves under different conditions.

**FR6 — Support predefined test cases:** The simulator must let users run predefined test cases and compare actual results with expected outcomes to verify correctness.

## Non-functional requirements

**NFR1 — Correctness:** The simulator must produce results that match the expected outcomes of test cases.

**NFR2 — Computational performance:** The simulator must measure execution time across different workload sizes so users can understand how runtime changes as the number of jobs increases.

**NFR3 — Reliability:** The simulator must process valid inputs without unexpected errors or crashes.

**NFR4 — Usability:** The simulator must make it easy for users to set parameters and understand the results with clear instructions.


**NFR5 — Reproducibility:** The simulator must allow users to repeat experiments using the same configuration and workload data so results can be checked consistently. The simulator must retain settings for reuse.

**NFR6 — Maintainability:** The simulator must organise code into separate components so individual parts can be tested, fixed or updated without requiring major changes to the whole system.