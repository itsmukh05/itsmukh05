**Part C: Specialized Technology, Fundamental Concepts**

### C1:Concepts

1. Discrete-Event Simulation (DES)
Discrete-Event Simulation (DES) is a simulation method that represents a system by processing events that occur at particular points in time. Instead of continuously updating the system, the simulation changes its state when an event occurs, such as a job arriving, starting execution, or completing execution.

For this project, DES can represent a campus computing service where students submit jobs, such as document-processing tasks or programming jobs. When several students submit jobs around an assignment deadline, the number of waiting jobs may increase. The simulator can model how jobs are placed in a queue and assigned to available computing servers.

2. First-Come, First-Served (FCFS)
Job scheduling determines the order in which waiting jobs are assigned to available computing resources. First-Come, First-Served (FCFS) is a basic scheduling algorithm that processes jobs in their arrival order. It is useful as a starting point because its rules are simple and its results can be checked manually.

Worked Example :
| **Job** | **Arrival Time (min)** | **Execution Time (min)** |
|---------|-----------------------:|-------------------------:|
| J1      | 0                      | 4                        |
| J2      | 1                      | 3                        |
| J3      | 2                      | 5                        |
| J4      | 3                      | 2                        |
| J5      | 4                      | 3                        |

Simulation timeline
| **Time** | **Server 1** | **Server 2** | **Queue** | **Completed Jobs** |
|----------|--------------|--------------|-----------|--------------------|
| t0       | J1           | Idle         | -         | -                  |
| t1       | J1           | J2           | -         | -                  |
| t2       | J1           | J2           | J3        | -                  |
| t3       | J1           | J2           | J3, J4    | -                  |
| t4       | J3           | J4           | J5        | J1, J2             |
| t5       | J3           | J4           | J5        | J1, J2             |
| t6       | J3           | J5           | -         | J1, J2, J4          |
| t7       | J3           | J5           | -         | J1, J2, J4          |
| t8       | J3           | J5           | -         | J1, J2, J4          |
| t9       | Idle         | Idle         | -         | J1, J2, J3, J4, J5  |

Assume both servers are initially available and jobs follow FCFS scheduling. J1 starts on Server 1 at time 0. When J2 arrives at time 1, it starts on Server 2. J3 and J4 arrive while both servers are occupied, so they wait in the queue. At time 4, J1 and J2 finish, allowing J3 and J4 to begin execution. J4 finishes at time 6, and Server 2 then starts processing J5. J3 and J5 both finish at time 9.

This example demonstrates how a DES model can represent job arrivals, queue changes, server availability, and job completion. The simulator's recorded results can be compared with these expected outcomes to test correctness.

### C2. Frameworks, Models, Methods and Tools

Three relevant technologies or approaches for this project are Discrete-Event Simulation, First-Come, First-Served scheduling, and CloudSim. Each serves a different purpose in understanding or developing a resource-allocation simulator.

**1. Discrete-Event Simulation (DES) - Simulation Method**
- DES models a system by processing events at specific simulation times. For this project, events may include job arrival, job execution starting, job completion, and a server being activated or deactivated.

- DES is suitable for representing campus computing workloads because the simulator can update the queue and server status when these events occur. It can also record the time taken to process jobs and measure the simulator's computational performance.

**2. First-Come, First-Served (FCFS) - Scheduling Algorithm**
- FCFS assigns waiting jobs in the order they arrive. It provides a straightforward baseline for checking whether jobs are handled correctly.

- In this project, FCFS can be used to establish the expected order of job execution in predefined test cases. The simulator's output can then be compared with manually calculated results to evaluate correctness. FCFS alone does not provide adaptive resource allocation because it determines job order rather than when to add or remove computing resources.

**3. CloudSim - Simulation Framework**
- CloudSim is a framework designed to model and simulate cloud computing environments. It supports the study of computing resources, virtual machines, application workloads, and resource-provisioning or scheduling policies (Calheiros et al., 2011).

- For this project, CloudSim is relevant as an existing framework to study when deciding how to represent computing resources and allocation behaviour. It could be used as a foundation if its features fit the project requirements, or its concepts could inform the design of a smaller, custom-built simulator.

- The choice between CloudSim and a custom implementation should be made after examining the project requirements, implementation complexity, and available time.

**4. Python - Programming Language and Development Tool**

Python is a programming language that can be used to implement the simulator's logic, generate synthetic workloads, process simulation results, and conduct performance tests. Its use in this project would depend on the final implementation choice.

## C3 Fit to your problem

Why these approaches fit the project
DES, FCFS, and CloudSim address different aspects of the project.
- DES provides a way to model jobs arriving, waiting, executing, and completing over time.
- FCFS provides a simple scheduling baseline that helps verify the simulator's results.
- CloudSim provides an existing framework to investigate how computing resources and allocation policies can be represented in a simulation.

Together, these approaches support the development and evaluation of a campus computing workload simulator. DES can represent changes in workload and server status, while FCFS can help establish expected results for correctness testing. CloudSim offers a reference point for deciding whether to build a custom simulator or use an existing framework.

**Benefits**

The main benefits of using DES are:
- **Controlled testing:** Different workload conditions can be tested without disrupting an actual campus computing service.
- **Repeatability:** The same job data and configuration can be reused to check whether DES produces results. 
- **Performance measurement:** Execution time and other selected metrics can be recorded across different workload sizes.
- **Flexibility:** The model can be extended to include servers, alternative scheduling rules or adaptive resource allocation policies. 


**Limitations**

Despite these benefits, several limitations must be considered.
- **Workload assumptions:** Simulated jobs may not represent the full complexity of real campus computing tasks. For example, actual jobs may have different resource requirements, execution times, or arrival patterns.
- **Adaptive behaviour requires rules:** DES does not automatically make resource allocation adaptive. The simulator needs a defined policy specifying when resources should be added or removed and how workload changes are detected.
- **Implementation complexity:** Using an existing framework such as CloudSim may require time to learn its part and adapt them to the project. A custom simulator may be easier to tailor but its behaviour and correctness must be tested carefully.
- **Limited real-world validation:** If the project uses workloads instead of actual campus data the simulator's findings will show behaviour under the chosen assumptions not prove how a real campus system would perform.

**Alternative**

- An alternative is to test resource allocation directly on a real computing environment. Real-system testing can provide observations of actual job processing and resource usage, but it requires access to suitable infrastructure and may interfere with normal operations.

- DES allows workload scenarios to be tested in a controlled and repeatable way without changing a live system. For this project, DES is the preferred approach because the main focus is developing a simulator and evaluating its correctness and computational performance. However, simulation results will depend on the assumptions and workload data used.

- In conclusion, DES provides a practical method for representing campus computing workloads and evaluating the behaviour of a resource-allocation simulator. FCFS can support correctness testing, while CloudSim provides an existing framework for comparison during technology selection. The final implementation should follow the requirements agreed for the project, particularly whether dynamic server activation and deactivation are required.

