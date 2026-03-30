# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**A process is an independent program in execution that has its own memory space, resources, and system state. In contrast, a thread is a lightweight unit of execution that exists within a process and shares the same memory and resources with other threads. Threads are faster to create and manage compared to processes because they do not require separate memory allocation.

In this assignment, threads were used instead of processes because the simulation requires frequent context switching and communication between tasks. Using threads allows efficient scheduling with lower overhead, which aligns with the Round-Robin algorithm implemented in the code. Additionally, threads share data structures such as the ready queue and process map, making synchronization and communication easier compared to separate processes.

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**In Round-Robin scheduling, if a process does not finish within its time quantum, it is preempted and moved back to the end of the ready queue. This allows other processes to get CPU time, ensuring fairness among all processes. The process will wait for its turn again and resume execution in the next cycle. This behavior continues until the process completes its remaining burst time. This approach prevents starvation and improves system responsiveness.

Example from my output:▶ P2 executing quantum [4000ms]
⚡ Quantum progress: [███████████████] 100%
⏸ P2 completed quantum 4000ms │ Overall progress: [███████████░░░░░░░░░] 59%      
   Remaining time: 2737ms
↻ P2 yields CPU for context switch

➕ P2 added to ready queue │ Burst time: 6737ms │ Priority: 4

┌─ Ready Queue ─────────────────────────────────────────────────────────────────    
│ [P4 → P5 → P6 → ... → P17 → P2]
└───────────────────────────────────────────────────────────────────────────────


Explanation of example:

In this example, process P2 was executed for the full time quantum (4000ms), but it did not finish because it still had 2737ms remaining. As a result, it was preempted and yielded the CPU. After that, it was added again to the end of the ready queue, as shown in the queue where P2 appears at the last position. This demonstrates how Round-Robin scheduling rotates processes and ensures each process gets a fair share of CPU time.

Question 3: Thread State
[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]



New:
P1 is in the New state when it is first created and added to the ready queue, as shown in the output:
“➕ P1 added to ready queue │ Burst time: 3666ms”.
At this point, the thread exists but has not started execution yet.
Runnable:
P1 enters the Runnable state after being placed in the ready queue and waiting for the CPU.
This is shown when the ready queue is displayed before execution begins, where P1 is ready but not yet running.
Running:
P1 enters the Running state when the scheduler selects it and starts execution:
“▶ P1 executing quantum [3666ms]”.
During this time, the thread is actively using the CPU.
Waiting:
In this simulation, P1 does not explicitly enter a waiting state because it completes within one quantum.
However, other processes like P2 and P3 effectively experience waiting when they are returned to the ready queue and must wait for their next turn to execute.
Terminated:
P1 reaches the Terminated state after finishing execution completely:
“✓ P1 finished execution!”.
At this point, the thread has no remaining burst time and is removed from the system.
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Server Handling Multiple Requests



**Description**: 
A web server handles multiple client requests simultaneously, where each request is processed by a separate thread.


**Why Round-Robin works well here**: 
Round-Robin scheduling ensures that all requests are handled fairly and no single request blocks others. It improves responsiveness by giving each thread a fixed time slice, allowing the server to serve multiple users efficiently.
### Example 2: Multimedia Player (Audio/Video Streaming)

Description:
A media player uses threads to handle audio decoding, video rendering, and user input simultaneously.

Why Round-Robin works well here:
Round-Robin scheduling ensures smooth playback by giving each task a fair share of CPU time. It prevents lag or freezing by switching between tasks frequently, maintaining responsiveness and synchronization


---

## Summary

Key concepts I understood through these questions:

1-Difference between threads and processes
2-Round-Robin scheduling and fairness
3-Thread lifecycle and execution states

Concepts I need to study more:
Advanced thread synchronization
Deadlocks and race conditions

Deadlocks and race conditions

