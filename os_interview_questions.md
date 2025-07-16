**Operating Systems - Technical Interview Q&A**

---

**Q1: What is an Operating System? What are its main functionalities?**

An Operating System (OS) is system software that manages computer hardware and software resources and provides services for computer programs.

**Main Functionalities:**
- Process Management
- Memory Management
- File System Management
- Device Management
- Security and Access Control
- User Interface

---

**Q2: What is Multitasking and Multithreading? Differences?**

**Multitasking**: Running multiple processes at the same time.
**Multithreading**: Running multiple threads (lightweight processes) inside a single process.

**Differences:**
| Feature          | Multitasking               | Multithreading              |
|------------------|-----------------------------|------------------------------|
| Unit of work     | Process                     | Thread                       |
| Memory           | Separate                    | Shared                       |
| Overhead         | High                        | Low                          |
| Example          | Chrome + Excel              | Multiple tabs in Chrome      |

---

**Q3: A section of code which can be executed only by one process at a time is called?**

**Critical Section** – a block of code where shared resources are accessed. Only one thread/process can enter at a time to prevent data inconsistency.

---

**Q4: What is a Thread and What is a Process? Differences?**

**Process**: Independent execution unit with its own memory.
**Thread**: Smallest unit of execution inside a process.

| Feature       | Process               | Thread                     |
|---------------|------------------------|-----------------------------|
| Memory        | Separate               | Shared                      |
| Communication | Through IPC            | Directly (shared memory)    |
| Overhead      | Higher                 | Lower                       |

---

**Q5: List some of the states of a Thread.**
- New
- Runnable
- Running
- Blocked
- Waiting
- Timed Waiting
- Terminated

---

**Q6: What problem does Mutual Exclusion and Semaphores address?**
They prevent **race conditions** and ensure **synchronization** while accessing shared resources in concurrent systems.

---

**Q7: When does Deadlock happen? Can a single thread cause it?**

Deadlock occurs when processes are waiting on each other for resources in a cycle.

**Conditions:**
- Mutual Exclusion
- Hold and Wait
- No Preemption
- Circular Wait

**Single thread?** No, deadlock needs two or more processes/threads.

---

**Q8: What is Direct Memory Access (DMA)?**

DMA allows devices to transfer data to/from memory **without CPU involvement**, improving speed and freeing up the CPU.

---

**Q9: What is Virtual Memory and When is it Utilized?**

Virtual Memory uses part of the hard disk as extra RAM. It is used when **RAM is full**, allowing large or multiple programs to run smoothly.

---

**Q10: What is the Purpose of a Scheduling Algorithm?**

To decide **which process runs next** on the CPU. Goals include:
- Maximize CPU use
- Minimize waiting time
- Ensure fairness

---

**Q11: Explain how Round Robin Algorithm works.**

Each process gets a fixed time slice (quantum). If not finished, it goes to the back of the queue. Ensures **fairness**.

---

**Q12: Define Bus and Its Use.**

A **bus** is a communication pathway for transferring data between components.

**Types:**
- Data Bus
- Address Bus
- Control Bus

---

**Q13: List some File Attributes.**
- Name
- Type
- Size
- Location
- Creation Date
- Modified Date
- Owner
- Permissions
- Hidden Flag
- Read-Only Flag

---

**Q14: Where is the Information of All Files Kept?**

Stored in **file system metadata**, such as:
- **Inodes** (Linux/Unix)
- **Master File Table (MFT)** (Windows/NTFS)

---

**Q15: What are Common Security Threats to a File?**
- Unauthorized Access
- Data Leakage
- Malware
- Accidental Deletion
- Ransomware
- Tampering
- Privilege Escalation
- Eavesdropping

---

**Q16: List All File Permissions in an OS.**

**Basic Permissions:**
- Read (r)
- Write (w)
- Execute (x)

**User Types:**
- Owner
- Group
- Others

Windows also uses: Full Control, Read, Write, Execute, Modify

---

**Q17: Explain Secondary Storage Management in OS.**

Deals with **long-term data storage** like HDDs and SSDs.

**Tasks:**
- Allocation
- Free space management
- Disk scheduling
- File system organization
- Backup
- Protection

---

**Q18: Which Command in UNIX is Used to List Directory?**

```bash
ls
```
Shows contents of a directory.

Options:
- `ls -l`: Long format
- `ls -a`: Include hidden files

---

**Q19: Which Command is Used to Create a Directory in UNIX?**

```bash
mkdir directory_name
```

- `mkdir -p a/b/c`: Creates nested directories

---

**Q20: Command to Change File Permissions in UNIX?**

```bash
chmod 755 file.txt
```

- `7` (owner): read + write + execute
- `5` (group/others): read + execute

Symbolic format:
```bash
chmod u+x file.txt
```
