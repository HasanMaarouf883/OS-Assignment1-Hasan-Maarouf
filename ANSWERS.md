# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

A process is a fully independent program with its own memory space, which makes it heavy and slow to switch. A thread is a smaller part of a process that shares memory and resources with other threads, making it much lighter and faster. We used threads in this assignment because creating full processes would consume too much memory and make sharing the Ready Queue very difficult. Using threads allowed us to simulate CPU multitasking efficiently with very low overhead.

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

If a process needs more time than the allowed time quantum, it is temporarily paused. The CPU is taken away, and the process is sent back to the end of the Ready Queue to wait for its next turn. For instance, my time quantum was 5000ms, but P1 needed 7879ms, so it couldn't finish in one round.

Example from my output:
```
û╢ P1 executing quantum [5000ms]
  أة Quantum progress: [ûêûêûêûêûêûêûêûêûêûêûêûêûê] 100%
  ╕ P1 completed quantum 5000ms ¤é Overall progress: [ûêûêûêûêûêûêûêûêûêûêûêûّûّûّ  ûّûّûّûّûّ] 63%
     Remaining time: 2879ms
  ╗ P1 yields CPU for context switch

  ئـ P1 (Priority:3) added to ready queue ¤é Burst time: 7879ms
```

**Explanation of example:**
In the pasted output, P1 runs for its full 5000ms quantum. Since it still has 2879ms of work left, it yields the CPU and prints a context switch message. Finally, the scheduler adds P1 back to the end of the Ready Queue so the next process (P2) can start.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: P1 is in the New state when we first create its Process object and pass it to a new Thread, but before calling start().

2. **Runnable**: P1 becomes Runnable when it enters our processQueue and waits for the CPU, or when it returns to the queue after its quantum finishes.

3. **Running**: P1 is in the Running state when the scheduler pulls it from the queue and it actively executes its time slice inside the run() method.

4. **Waiting**: P1 enters a Timed Waiting state when we call Thread.sleep() in our code to simulate the actual processing time.

5. **Terminated**: P1 is Terminated when its remaining time hits 0ms, finishing its execution and exiting the system completely.
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Web Servers]

**Description**: 
Web servers use threads to handle hundreds of users trying to open a website at the exact same time.

**Why Round-Robin works well here**: 
Round-Robin is perfect here because it ensures absolute fairness for all connected users. It prevents one user downloading a huge file from freezing the website for everyone else. By giving each connection a small time slice, the server stays fast and responsive.

### Example 2: [Desktop Operating Systems]

**Description**: 

Modern operating systems run many background apps simultaneously, like a music player, an antivirus, and a web browser.

**Why Round-Robin works well here**: 

Round-Robin forces heavy background apps to share the CPU with lighter apps quickly. Because the time quantum is so small, the context switching happens in milliseconds. This allows users to listen to music smoothly without any lag while browsing the internet or scanning files.
---

## Summary

**Key concepts I understood through these questions:**
1. The difference between a heavy OS process and a lightweight thread.
2. How the Round-Robin algorithm uses a queue to prevent process starvation.
3. The complete lifecycle of a thread from creation to termination.

**Concepts I need to study more:**
1. How to prevent race conditions when multiple threads modify the same variable.
2. The differences between Round-Robin and other algorithms like Shortest Job First.
