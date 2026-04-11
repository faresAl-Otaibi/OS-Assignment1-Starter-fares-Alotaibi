# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**
A processor is a complete program in itself with its own dedicated memory, while a thread is a small part of the whole that shares memory with the other threads and has nothing of its own. The difference between them lies in size, resources, and privacy. They can be likened to a processor being a large, complete ship; despite its size, movement within it is slow. Threads, on the other hand, are like small ships—numerous and fast. We use threads instead of different processors because we need two features that processors lack: synchronization and speed. Using processors might provide synchronization, but not at good speeds. It might give you high speeds, but you would need many processors, which is unacceptable because you haven't used it in the best way possible. The Round Robin system with threads allows you to use it in the simplest and most efficient way possible.
[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**
In short, this approach prevents monopolies and provides a fair opportunity for everyone. It presents a list of processes ready for execution, but they are lined up in order to take their time. It uses a round-robin system where the order is determined using a first-come, first-served algorithm, forming a continuous loop. After the first one finishes, he become the last ,k, and so on.exmpl: ظû╢ P1 executing quantum [5000ms]
  ظأة Quantum progress: [ظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûê
[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:] 100%
  ظ╕ P1 completed quantum 5000ms ظ¤é Overall progress: [ظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûêظûّظûّ] 90%
     Remaining time: 534ms
  ظ╗ P1 yields CPU for context switch
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**
The first step involves creating the thread using the `new Thread(process)` code, followed by its preparation using the `start()` code. When the system selects the thread and starts it with the `run()` code, it enters a waiting state using `Thread.sleep()` after the `Time Quantum` time has elapsed. At this point, it pauses temporarily or is left by the processor. The final step is that it terminates when its remaining time reaches zero.
[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]  ?Process process = new Process("P1", burstTime, timeQuantum , priority);
Thread thread = new Thread(process);


2. **Runnable**: [When does P1 become Runnable?] processQueue.add(thread);

3. **Running**: [When is P1 Running?] currentThread.start();

4. **Waiting**: [When/why would P1 be Waiting?] Thread.sleep(stepTime); when and why is up

5. **Terminated**: [When is P1 Terminated?] if (remainingTime == 0)

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
