# Operating System (OS) Overview

The Operating System (OS) acts as an intermediary between the user and the hardware.

## **Structure of Operating System**

- A common approach is to partition the task into small components, or modules, rather than have one monolithic system. Each of these modules should be a well-defined portion of the system, with carefully defined inputs, outputs, and functions.

---

### **Simple Structure**

- Many operating systems do not have well-defined structures. Frequently, such systems started as small, simple, and limited systems and then grew beyond their original scope.

- MS-DOS is an example of such a system.

- Not divided into modules. Its interface, levels and functionality are not well separated.

### **Layered Approach**

With proper hardware support, operating systems can be broken into pieces. The operating system can then retain much greater control over the computer and over the applications that make use of that computer.

1. Implementers have more freedom in changing the inner workings of the system and in creating modular operating systems.

2. Under a top-down approach, the overall functionality and features are determined and are separated into components.

3. Information hiding is also important, because it leaves programmers free to implement the low-level routines as they see fit.

4. A system can be made modular in many ways. One method is the layered approach, in which the operating system is broken into a number of layers (levels). The bottom layer (layer 0) is the hardware; the highest (layer _N_) is the user interface.

![Layered Approach](https://miro.medium.com/v2/resize:fit:1040/1*dGC4LbUB7I00LHgpYlyhVA.png)

---

## OS Services

### 1. Resource Manager/Allocator

- The OS controls and coordinates the use of system resources among various application programs in an unbiased fashion.

### 2. Platform Provider

- The OS provides a platform on which other application programs (application software) can be installed.
- It provides an environment within which programs are executed.

**Example:**

- Windows, Linux, and macOS are platforms that allow you to run applications like browsers, games, and office tools.

---

## Major Components of Operating System

1. **Kernel**

   - **Central Component:** Manages the system's resources and communication between hardware and software.

2. **Process Management**

   - **Process Scheduler:** Determines the execution of processes.
   - **Process Control Block (PCB):** Contains process details such as process ID, priority, status, etc.
   - **Concurrency Control:** Manages simultaneous execution.

3. **Memory Management**

   - **Physical Memory Management:** Manages RAM allocation.
   - **Virtual Memory Management:** Simulates additional memory using disk space.
   - **Memory Allocation:** Assigns memory to different processes.

4. **File System Management**

   - **File Handling:** Manages the creation, deletion, and access of files and directories.
   - **File Control Block:** Stores file attributes and control information.
   - **Disk Scheduling:** Organizes the order of reading or writing to disk.

5. **Device Management**

   - **Device Drivers:** Interface between the hardware and the operating system.
   - **I/O Controllers:** Manage data transfer to and from peripheral devices.

6. **Security and Access Control**

   - **Authentication:** Verifies user credentials.
   - **Authorization:** Controls access permissions to files and directories.
   - **Encryption:** Ensures data confidentiality and security.

7. **User Interface**

   - **Command Line Interface (CLI):** Text-based user interaction.
   - **Graphical User Interface (GUI):** Visual, user-friendly interaction.

8. **Networking**
   - **Network Protocols:** Rules for communication between devices on a network.
   - **Network Interface:** Manages connection between the computer and the network.

---

## Goals and Functions of OS

- **Goals** are the ultimate destination, but we follow **functions** to implement them.

### Goals

- **Primary:** User friendliness
- **Secondary:** Efficiency and reliability

### Functions of Operating System

1. **Process Management:** Involves handling the creation, scheduling, and termination of processes, which are executing programs.
2. **Memory Management:** Manages allocation and deallocation of physical and virtual memory spaces to various programs.
3. **I/O Device Management:** Handles I/O operations of peripheral devices like disks, keyboards, etc., including buffering and caching.
4. **File Management:** Manages files on storage devices, including their information, naming, permissions, and hierarchy.
5. **Network Management:** Manages network protocols and functions, enabling the OS to establish network connections and transfer data.
6. **Security & Protection:** Ensures system protection against unauthorized access and security threats through authentication, authorization, and encryption.

---

Sure! I'll explain each function of an operating system (OS) in **very simple English** so that you can learn it easily.

---

### **Important Functions of an Operating System**

An **Operating System (OS)** is like the manager of a computer. It controls everything happening inside the computer and makes sure everything works smoothly. Below are its important functions:

---

### **1. Memory Management**

- Memory (RAM) is like a workspace where programs run.
- The OS decides which program gets how much memory and keeps track of free space.
- It ensures that one program doesn’t take memory from another.
- It also moves programs between RAM and storage (like a hard drive) when needed.

🔹 **Example:** When you open a game and a web browser at the same time, the OS manages memory so both can work properly without crashing.

---

### **2. Processor Management (CPU Management)**

- The CPU (Central Processing Unit) is like the brain of the computer.
- The OS decides which program or task should use the CPU and for how long.
- If many programs are running, the OS quickly switches between them so they all work smoothly.
- This is called **multitasking**.

🔹 **Example:** If you're watching a video while typing in a document, the OS makes sure both tasks share the CPU efficiently.

---

### **3. Device Management**

- A computer has many devices like a keyboard, mouse, printer, USB drives, etc.
- The OS acts as a bridge between these devices and the computer.
- It helps the devices send and receive data properly.
- The OS uses special programs called **drivers** to help devices communicate.

🔹 **Example:** When you plug in a printer, the OS helps the computer understand how to use it.

---

### **4. File Management**

- A computer stores data in files and folders.
- The OS organizes, saves, opens, renames, and deletes files.
- It keeps track of where files are stored on the hard drive or SSD.
- It also manages file permissions (who can open or edit a file).

🔹 **Example:** When you save a Word document or a photo, the OS keeps it safe and allows you to find it later.

---

### **5. Security**

- The OS protects the computer from **unauthorized access** and **viruses**.
- It allows users to set **passwords**, **permissions**, and **firewalls** to keep data safe.
- It also protects against **hackers** and **malware**.

🔹 **Example:** When you log in to your computer with a password, the OS ensures that only you can access your files.

---

### **6. Control Over System Performance**

- The OS checks how well the computer is working.
- It monitors the **CPU, memory, and other resources** to make sure they are not overloaded.
- If something is slowing down the system, the OS tries to fix it.

🔹 **Example:** If a program is using too much memory and slowing down the computer, the OS may close it or give a warning.

---

### **7. Job Accounting**

- The OS keeps a record of what programs and users are using the system.
- This is useful in large businesses where many people share one computer.
- It helps track resource usage for **billing** and **management purposes**.

🔹 **Example:** In an office, the OS records which employees used the printer and how many pages they printed.

---

### **8. Error Detecting Aids**

- The OS constantly checks for errors in the system.
- If there is a problem (like a **corrupt file** or **hardware failure**), the OS alerts the user.
- It may also try to fix small issues automatically.

🔹 **Example:** If your hard drive has a problem, the OS may show a warning and suggest fixing it.

---

### **9. Coordination Between Other Software and Users**

- The OS makes sure that all programs, users, and devices work together properly.
- It helps different software talk to each other.
- It allows **multiple users** to use the same computer at different times.

🔹 **Example:** If you are downloading a file while listening to music, the OS ensures both work smoothly without stopping.

---

## Types of OS

![8 Types of Operating Systems in Simple Words (With Examples)](https://tse1.mm.bing.net/th?id=OIP.5ElHCZxt6oab-3iS95wAggHaFB&pid=Api)

Certainly! Let's delve into the various types of operating systems in a detailed yet easy-to-understand manner, suitable for your college exams. We'll also include images to help visualize each type.

---

### 1. Batch Operating System

**Definition:** Batch operating systems execute batches of jobs without user interaction. Users prepare their tasks offline and submit them to the computer operator, who groups similar tasks into batches for processing.

**Key Features:**

- **Job Scheduling:** Groups similar jobs to optimize processing.
- **No Immediate User Interaction:** Users cannot interact with their programs during execution.
- **Efficient for Repetitive Tasks:** Ideal for tasks that require similar processing.

**Example:** Early IBM mainframe systems used batch processing for tasks like payroll and inventory management.

**Image:**
![Batch Operating System](https://www.founderjar.com/wp-content/uploads/2021/11/Batch-Operating-System.png)

---

## Spooling

### Simultaneous Peripheral Operations Online

1. In a computer system, input-output devices such as printers are very slow relative to the performance of the rest of the system.

2. Spooling is a process in which data is temporarily held in memory or other volatile storage to be used by a device or a program.

3. Data from a card reader is first stored in memory (or disk), and then sent to the printer when it is ready to process the data. This allows the CPU and other components to continue working without waiting for the slow device to finish.

4. The most common implementation of spooling can be found in typical input/output devices such as the keyboard, mouse and printer. For example, in printer spooling, the documents/files that are sent to the printer are first stored in the memory. Once the printer is ready, it fetches the data and prints it.

---

### 8. Multiprogramming Operating System

**Definition:** Multiprogramming operating systems allow multiple programs to reside in memory simultaneously, managing their execution to optimize CPU usage.

**Key Features:**

- **Increased Throughput:** Maximizes CPU utilization by reducing idle time.
- **Efficient Memory Management:** Allocates memory to multiple programs effectively.
- **Job Scheduling:** Determines the order in which programs execute based on priority and resource availability.

* **Multiple Jobs:** Keeps several jobs in main memory simultaneously, allowing more efficient utilization of the CPU.

* **Job Execution:** The OS picks and begins to execute one of the jobs in memory.

* **Waiting Jobs:** Eventually, a job may need to wait for a task, such as an I/O operation, to complete.

---

### 2. Time-Sharing Operating System

**Definition:** Time-sharing operating systems allow multiple users to use a computer system simultaneously by rapidly switching between tasks, giving the impression that each user has their own dedicated system.

**Key Features:**

- **Multitasking:** Runs multiple tasks by allocating time slices to each.
- **User Interaction:** Users can interact with their programs during execution.
- **Efficient Resource Utilization:** Maximizes CPU usage by reducing idle time.

**Example:** UNIX is a classic example of a time-sharing operating system.

**Multitasking Operating system/time sharing/Multiprogramming with Round Robin/ Fair Share**

1. **Time sharing** (or multitasking) is a logical extension of **multiprogramming**, it allows many users to share the computer simultaneously. The CPU executes multiple jobs (**May belong to** different user) **by switching among** them, but the switches occur so frequently that, each user is given the impression that the **entire computer system** is dedicated to **his/her** use, even though it is being **shared among many** users.

2. In the modern operating systems, we are able to play **MP3 music**, edit documents in Microsoft Word, surf the Google Chrome all running at the same time. (**by context switching, the illusion of parallelism is achieved**)

3. For multitasking to take place, firstly there should be multiprogramming i.e. presence of multiple programs ready for execution. And secondly the concept of time sharing.

4. These OS use time quantum is a core component of time-sharing operating systems, as it enables CPU time to be divided fairly among multiple users or processes through rapid context switching.

**Image:**
![Time-Sharing Operating System](https://www.founderjar.com/wp-content/uploads/2021/11/Time-Sharing-Operating-System.png)

---

### Multiprocessing Operating System / tightly coupled system

1. **Multiprocessor Operating System** refers to the use of two or more central processing units (CPU) within a single computer system. These multiple CPU's share system bus, **memory and other peripheral devices**.

2. Multiple concurrent processes each can run on a separate CPU, here we achieve a true parallel execution of processes.

3. Becomes most important in computer system, where the complexity of the job is more, and CPU divides and conquers the jobs. Generally used in the fields like artificial intelligence and expert system, image processing, weather forecasting etc.

Here is the OCR result from the image:

---

**Multiprocessor Systems**

| **Point**           | **Symmetric Processing**                                  | **Asymmetric Processing**                                  |
| ------------------- | --------------------------------------------------------- | ---------------------------------------------------------- |
| **Definition**      | All processors are treated equally and can run any task.  | Each processor is assigned a specific task or role.        |
| **Task Allocation** | Any processor can perform any task.                       | Tasks are divided according to processor roles.            |
| **Complexity**      | Generally simpler as all processors are treated the same. | More complex due to the dedicated role of each processor.  |
| **Scalability**     | Easily scalable by adding more processors.                | May require reconfiguration as processors are added.       |
| **Performance**     | Load is evenly distributed, enhancing performance.        | Performance may vary based on the specialization of tasks. |

---

| **Point**                       | **Multi-Programming**                                              | **Multi-Processing**                                                   |
| ------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------------- |
| **Definition**                  | Allows multiple programs to share a single CPU.                    | Utilizes multiple CPUs to run multiple processes concurrently.         |
| **Concurrency**                 | Simulates concurrent execution by rapidly switching between tasks. | Achieves true parallel execution of processes.                         |
| **Resource Utilization**        | Maximizes CPU utilization by keeping it busy with different tasks. | Enhances performance by allowing tasks to be processed simultaneously. |
| **Hardware Requirements**       | Requires only one CPU and manages multiple tasks on it.            | Requires multiple CPUs, enabling parallel processing.                  |
| **Complexity and Coordination** | Less complex, primarily managing task switching on one CPU.        | More complex, requiring coordination among multiple CPUs.              |

---

### 4. Real-Time Operating System (RTOS)

**Definition:** Real-time operating systems process data and events that require immediate attention, ensuring tasks are completed within a specified time constraint.

**Key Features:**

- **Deterministic Response:** Guarantees responses within a fixed time period.
- **Reliability:** Essential for critical applications where delays are unacceptable.
- **Priority Scheduling:** Manages tasks based on priority levels.

**Example:** VxWorks is an RTOS used in embedded systems like aerospace and defense applications.

Here is the OCR result of the table comparing **Hard Real-Time** and **Soft Real-Time Operating Systems**:

---

**(Chapter-1: Introduction)**
**Real Time System**

| **Point**                | **Hard Real-Time Operating System**                                   | **Soft Real-Time Operating System**                        |
| ------------------------ | --------------------------------------------------------------------- | ---------------------------------------------------------- |
| **Deadline Constraints** | Must meet strict deadlines without fail.                              | Can miss deadlines occasionally without failure.           |
| **Response Time**        | Fixed and guaranteed.                                                 | Predictable, but not guaranteed.                           |
| **Applications**         | Used in life-critical systems like medical devices, nuclear reactors. | Used in multimedia, user interfaces, etc.                  |
| **Complexity and Cost**  | Typically more complex and costlier.                                  | Less complex and usually less expensive.                   |
| **Reliability**          | Must be highly reliable and fault-tolerant.                           | High reliability desired, but some failures are tolerable. |

**Image:**
![Real-Time Operating System](https://www.founderjar.com/wp-content/uploads/2021/11/Real-Time-Operating-System.png)

### **What is the Kernel?**

The **kernel** is the core component of an operating system. It acts as a bridge between the hardware and software, managing system resources and enabling communication between applications and the hardware. The kernel is responsible for critical tasks such as process management, memory management, device management, and system security.

#### Key Responsibilities:

1. **Resource Management:** Allocates CPU, memory, and I/O devices to processes.
2. **Process Management:** Handles process creation, scheduling, and termination.
3. **Memory Management:** Manages RAM allocation and virtual memory.
4. **Device Management:** Facilitates communication between hardware devices and software.
5. **System Security:** Ensures secure access to system resources.

---

### **Types of Kernels**

#### 1. **Microkernel**

- **Definition:** A microkernel is a minimalistic kernel that includes only essential functions like inter-process communication and basic hardware management. Other services, such as file systems and device drivers, run in user space.
- **Reason for Use:** Microkernels are designed for modularity and reliability. By isolating services in user space, they reduce the risk of system crashes caused by kernel bugs.
- **Analogy:** Imagine a small control room that delegates tasks to specialized departments (user space services). If one department fails, the control room remains unaffected.

#### 2. **Monolithic Kernel**

- **Definition:** A monolithic kernel integrates all operating system services, including device drivers, file systems, and memory management, into a single large block of code running in kernel space.
- **Reason for Use:** Monolithic kernels prioritize performance by allowing direct communication between components without the overhead of context switching.
- **Analogy:** Think of a single, large factory where all departments work in the same open space. While efficient, a problem in one department can disrupt the entire factory.

#### 3. **Reentrant Kernel**

- **Definition:** A reentrant kernel allows multiple processes to execute the same kernel code simultaneously by ensuring that the code is non-modifiable and uses separate data for each process.
- **Reason for Use:** Reentrant kernels are essential for multitasking and concurrency, as they prevent processes from interfering with each other.
- **Analogy:** Picture a library where multiple people can read the same book (kernel code) at the same time, but each person uses their own notebook (process data) to take notes.

---

### **Comparison of Kernel Types**

| **Feature**     | **Microkernel**                                          | **Monolithic Kernel**                       | **Reentrant Kernel**                     |
| --------------- | -------------------------------------------------------- | ------------------------------------------- | ---------------------------------------- |
| **Modularity**  | Highly modular, services run in user space.              | Less modular, all services in kernel space. | Shared kernel code with separate data.   |
| **Performance** | Slower due to user-kernel communication.                 | Faster due to direct communication.         | Efficient for multitasking.              |
| **Stability**   | More stable, as bugs in services don't crash the kernel. | Less stable, as bugs can crash the system.  | Stable due to isolated process data.     |
| **Complexity**  | More complex to implement.                               | Simpler to implement.                       | Requires careful design for concurrency. |

---

### **Conclusion**

The choice of kernel type depends on the system's requirements. Microkernels are ideal for reliability and modularity, monolithic kernels excel in performance, and reentrant kernels are crucial for multitasking and concurrency. Each type has its strengths and trade-offs, making them suitable for different use cases.

## Microkernel Systems

- In the mid-1980s, researchers at Carnegie Mellon University developed an operating system called **Mach** that modularized the kernel using the **microkernel** approach.

- This method structures the operating system by removing all nonessential components from the kernel and implementing them as system and **user-level programs**. The result is a small kernel.

- One benefit of the microkernel approach is that it makes extending the operating system easier. All new services are added to user space and consequently do not require modification of the kernel.

- When the kernel does have to be modified, the changes tend to be fewer, because the microkernel is a smaller kernel.

- The **MINIX 3 microkernel**, for example, has only approximately **12,000 lines of code**. Developer **Andrew S. Tanenbaum**.

![Micro-Kernel](https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/images/Chapter2/2_14_microkernelArchitecture.jpg)

---

### Reentrant Kernels

A **reentrant kernel** is a type of operating system kernel that allows multiple processes to share the same kernel code simultaneously. This is achieved by ensuring that the kernel code does not modify itself and uses separate data for each process.

#### Key Features:

1. **Code Sharing:** The kernel code is shared among processes, reducing memory usage.
2. **Separate Data:** Each process has its own data, ensuring no interference between processes.
3. **Concurrency:** Multiple processes can execute kernel functions at the same time without conflicts.

#### Benefits:

- **Efficiency:** Saves memory by sharing code.
- **Scalability:** Supports multiple processes effectively.
- **Stability:** Prevents processes from interfering with each other.

#### Example:

Modern operating systems like Linux and Windows use reentrant kernels to handle multitasking efficiently.

#### Analogy:

Think of a reentrant kernel as a library where multiple people can read the same book (code) at the same time, but each person uses their own notebook (data) to take notes.

### Monolithic Kernel

A **monolithic kernel** is a type of operating system architecture where the entire operating system, including the core services like process management, memory management, file system management, and device drivers, runs in a single address space in kernel mode.

#### Key Features:

1. **Single Address Space:** All components of the OS operate in the same memory space, which allows for faster communication between them.
2. **High Performance:** Since there is no overhead of context switching between kernel components, monolithic kernels are generally faster.
3. **Tightly Coupled Components:** All functionalities are integrated into one large block of code, making it less modular.

#### Benefits:

- **Efficiency:** Direct communication between components leads to better performance.
- **Simplicity:** Easier to implement compared to microkernels.

#### Drawbacks:

- **Stability Issues:** A bug in one component can crash the entire system.
- **Difficult Maintenance:** Modifying or updating one part of the kernel can affect the entire system.

#### Example:

Operating systems like **Linux**, **Windows NT**, and early versions of **UNIX** use monolithic kernels.

#### Analogy:

Think of a monolithic kernel as a single, large factory where all departments (e.g., production, packaging, shipping) work in the same building without walls separating them. While this setup allows for quick communication, a problem in one department can disrupt the entire factory.
