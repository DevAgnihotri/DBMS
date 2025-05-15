### **Process and States of a Process**

A process is simply a running program. It has its own memory, keeps track of what to do next, and uses resources like files and devices while it runs.

#### **States of a Process**

A process typically moves through the following states during its lifetime:

- **New**: The process is being created.
- **Ready**: The process is waiting to be assigned to a processor.
- **Running**: Instructions are being executed.
- **Waiting (Blocked)**: The process is waiting for some event to occur (such as I/O completion).
- **Terminated**: The process has finished execution.

The operating system manages these states and transitions between them to ensure efficient process execution.

### **Principle of Concurrency**

Concurrency means that more than one process or task can make progress at the same time. In an operating system, this happens when the CPU quickly switches between different tasks, so it looks like they are running together, even if only one is running at any moment.

#### **Key Points of Concurrency**

- **Resource Sharing**: Multiple processes may need to access shared resources (like memory, files, or devices) at the same time.
- **Synchronization**: Mechanisms are required to coordinate access to shared resources to prevent conflicts and ensure data consistency.
- **Interleaving Execution**: The execution of processes is interleaved, meaning their instructions are mixed together in time, but not necessarily executed at the same moment.
- **Improved Utilization**: Concurrency helps in better utilization of CPU and other resources by keeping them busy.

Concurrency is fundamental in modern operating systems to achieve efficiency, responsiveness, and resource sharing among multiple users and applications.

### **Mutual Exclusion: Definition, Example, and Analogy**

**Mutual exclusion** is a property of concurrency control, which ensures that only one process or thread can access a critical section (shared resource) at a time. This prevents data inconsistency and race conditions.

#### **Example**

Suppose two processes, P1 and P2, both want to update a shared variable `counter`. If both enter the critical section at the same time and increment `counter`, the final value may be incorrect due to overlapping operations. Mutual exclusion ensures that only one process can increment `counter` at a time, preserving data integrity.

#### **Analogy**

Imagine a single-person restroom with a lock on the door. Only one person can use the restroom at a time. If someone is inside (critical section), others must wait outside (waiting state) until the restroom is free. The lock acts as a mechanism to enforce mutual exclusion, preventing multiple people from entering at once.

**Process Synchronization & Race Condition**

As we understand in a multiprogramming environment a good number of processes compete for limited number of resources. Concurrent access to shared data at some time may result in data inconsistency for e.g.

Race condition is a situation in which the output of a process depends on the execution sequence of process. i.e. if we change the order of execution of different process with respect to other process the output **may change**.

Here is the OCR (extracted text) from the second slide:

---

### **General Structure of a process**

- **Initial Section**: Where process is accessing private resources.

- **Entry Section**: Entry Section is that part of code where, each process request for permission to enter its critical section.

- **Critical Section**: Where process is access shared resources.

- **Exit Section**: It is the section where a process will exit from its critical section.

- **Remainder Section**: Remaining Code.

```c
P()
{
    While(T)
    {
        Initial Section
        Entry Section
        Critical Section
        Exit Section
        Remainder Section
    }
}
```

---

### **Criterion to Solve Critical Section Problem**

- **Mutual Exclusion**:
  No two processes should be present inside the critical section at the same time, i.e. only one process is allowed in the critical section at an instant of time.

- **Progress**:
  If no process is executing in its critical section and some processes wish to enter their critical sections, then only those processes that are not executing in their remainder sections can participate in deciding which will enter its critical section next (means other process will participate which actually wish to enter). There should be no deadlock.

- above 2 are mandatory criterion

- **Bounded Waiting**:
  There exists a bound or a limit on the number of times a process is allowed to enter its critical section and no process should wait indefinitely to enter the CS.
- - this one is optional criterion
