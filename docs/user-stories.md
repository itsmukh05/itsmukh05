# User Stories

Format: As a [type of user], I want [goal], so that [reason or benefit].

## User Story 1: Submit Computing Workloads

As a student, I want to submit computing workloads for simulation, so that I can evaluate how my jobs may be handled.

**Related Requirements:** REQ-F01, REQ-F02

**Acceptance Criteria**
- Given I have a computing workload, when I submit it, then the system accepts it for simulation.
- Given a workload has been submitted, when the simulation runs, then resource allocation is simulated.

## User Story 2: Compare Resource Allocation Policies

As a researcher, I want to compare fixed-capacity, threshold-based, and adaptive resource allocation policies, so that I can evaluate their performance under different workload conditions.

**Related Requirements:** REQ-F03, REQ-F04, REQ-F05, REQ-N02

**Acceptance Criteria**
- The system supports adaptive resource allocation based on workload demands.
- The system records resource allocation results for evaluation.
- The system allows results from different resource allocation strategies to be compared.
- Repeating a simulation with the same inputs and settings produces consistent results.

## User Story 3: Review Simulation Results

As a campus IT administrator, I want simulation results presented clearly, so that I can evaluate resource usage and system performance.

**Related Requirements:** REQ-N01, REQ-N03

**Acceptance Criteria**
- Simulation results are displayed within 2 seconds after a completed simulation under the defined test conditions.
- Simulation results are organized in a clear format that users can understand and evaluate.