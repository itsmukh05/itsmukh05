### User Story 1 — Configure a workload

**As a** researcher, **I want** to configure the number of jobs and their arrival patterns, **so that** I can test the policies under different workload conditions.

**Linked requirement:** FR1

**Acceptance criteria:**
1. The system allows the user to select a workload configuration.
2. The system generates jobs according to the selected configuration.

### User Story 2 — Run allocation policies

**As a** computing system developer, **I want** to run fixed-capacity, threshold-based, and adaptive policies, **so that** I can compare their behaviour.

**Linked requirements:** FR2, FR3, FR4

**Acceptance criteria:**
1. The system can run each of the three policies.
2. Each policy uses the same workload and job scheduling rule during a comparison.

### User Story 3 — Compare results

**As a** campus IT administrator, **I want** to view performance and resource usage measurements, **so that** I can identify which policy is more suitable for a given workload.

**Linked requirements:** FR5, FR6

**Acceptance criteria:**
1. The system displays all four required performance measurements for each policy.
2. The system presents the results in a comparison table or chart.