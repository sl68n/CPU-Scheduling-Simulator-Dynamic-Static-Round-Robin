# CPU Scheduling Simulator – Dynamic & Static Round Robin

![Course](https://img.shields.io/badge/Course-CPCS361-orange)
![Language](https://img.shields.io/badge/Language-Java-blue)
![Topic](https://img.shields.io/badge/Topic-Operating%20Systems-purple)
![Scheduler](https://img.shields.io/badge/Scheduler-Dynamic%20%26%20Static%20RR-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A CPU Scheduling Simulator developed to model and compare  
**Dynamic Round Robin (DRR)** and **Static Round Robin (SRR)** scheduling algorithms.

Developed for CPCS361 – Operating Systems  
King Abdulaziz University

---

# 📌 Project Overview

CPU scheduling is a core component of operating systems.  
This simulator models:

- Process arrivals
- Memory allocation
- Device allocation
- Ready Queue
- Hold Queue 1 (Priority-based)
- Hold Queue 2 (FIFO)
- CPU execution cycles
- Final statistics generation

The goal is to evaluate how Dynamic Round Robin adapts compared to Static Round Robin under different workloads.

---

# ⚙️ System Specifications

- JDK 24
- Windows 11
- 16GB RAM
- Java Implementation
- Event-driven simulation engine

---

# 🧠 Scheduling Algorithms

## 🔹 Static Round Robin (SRR)

- Fixed Time Quantum = 10 + Team Number
- Simpler implementation
- Works well with uniform workloads
- May suffer from Convoy Effect

---

## 🔹 Dynamic Round Robin (DRR)

- Time Quantum = Average Remaining Burst Time (AR)
- Adaptive scheduling
- Improves responsiveness
- Reduces waiting time in mixed workloads

If only one process exists →  
Quantum = Remaining Burst Time

---

# 🏗️ System Components

## Process Structure
Each process includes:

- PID
- Arrival Time
- Burst Time
- Remaining Time
- Memory Requirement
- Device Requirement
- Priority Level
- Start Time
- Finish Time

---

## Queues

- Ready Queue
- Hold Queue 1 (Sorted by memory priority)
- Hold Queue 2 (FIFO)
- Finished Process Table

---

## Resource Management

- Memory Manager
- Device Manager
- Admission Control
- Resource Release after Completion

---

# 🧪 Experiments & Results

Two main configurations were tested:

## 📊 Config 1 (M=100)

Dynamic RR:
- Slightly lower Turnaround Time
- Slightly lower Waiting Time

Improvement:
- Turnaround improved by 0.16 ms
- Waiting improved by 0.77 ms

---

## 📊 Config 2 (M=200)

Dynamic RR:
- 12.4% better Turnaround Time
- 14.2% better Waiting Time

---

## 📊 Stress Test (100 Jobs – Uniform Medium Workload)

Results:
- Static RR slightly better (~1.5%)
- Fixed quantum matched workload distribution
- DRR sometimes sliced jobs too frequently

---

## 📊 Convoy Effect Test (10 Long + 40 Short Jobs)

Result:

Dynamic RR significantly better  
Waiting time reduced by over 9%

Reason:
DRR lowers quantum when short jobs dominate  
Short jobs complete faster  
Prevents starvation

---

# 📈 Key Insights

- DRR adapts to workload dynamically
- DRR reduces starvation in mixed environments
- SRR can outperform DRR in uniform CPU-bound workloads
- Memory availability strongly affects admission
- Scheduler design significantly impacts turnaround & waiting time

---

# 🚀 Concepts Applied

- CPU Scheduling
- Round Robin
- Dynamic Quantum Calculation
- Resource Allocation
- Memory Management
- Device Allocation
- Queue Handling
- Event-driven Simulation
- Performance Benchmarking

---

# 📊 Metrics Calculated

- Turnaround Time
- Waiting Time
- Completion Time
- Average Statistics
- System Snapshots
- Finished Job Table

---

# 👨‍💻 Author

Sultan Yasir Alasami  
Abdulaziz Sattam Alobaili  
Faisal Hussein Alghamdi  

College of Computing & Information Technology  
King Abdulaziz University  

---

# 📌 Course Information

CPCS361 – Operating Systems  
Group 3
