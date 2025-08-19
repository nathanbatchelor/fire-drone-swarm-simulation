# Fire Drone Swarm Simulation

A **real-time multithreaded fire response coordination system** built with Java, featuring autonomous drone fleet management, fault tolerance, and live GUI monitoring.

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Multithreading](https://img.shields.io/badge/Multithreading-Concurrent-blue?style=for-the-badge)
![GUI](https://img.shields.io/badge/GUI-Swing-green?style=for-the-badge)

## 🔥 Project Overview

This system simulates a coordinated emergency response where **autonomous drones** work together to extinguish fires across multiple zones. The simulation features real-time decision making, resource optimization, and comprehensive fault handling.

**Team Project Note:** *Collaborative university project (SYSC3303) - I designed and implemented the core scheduling algorithms, drone coordination logic, fault tolerance mechanisms, and real-time GUI components.*

---

## 🎯 Key Technical Achievements

### **Intelligent Swarm Coordination**
- **Dynamic task assignment** - Drones autonomously request and receive optimal fire assignments
- **Real-time route optimization** - En-route task switching for maximum efficiency  
- **Resource-aware scheduling** - Battery life and agent capacity considered in all assignments

### **Fault Tolerance & Recovery**
- **Arrival timeout detection** - Automatic reassignment if drone fails to reach target
- **Nozzle malfunction handling** - Hardware fault simulation and recovery
- **Communication packet loss** - Network fault tolerance with automatic retry logic

### **Real-Time Performance Monitoring**
- **Live drone tracking** - Real-time position updates on interactive map
- **Performance metrics** - Distance traveled, response times, task completion rates
- **Visual status dashboard** - Battery levels, agent capacity, current states

### **Concurrent Architecture**
- **Thread-safe communication** - UDP-based RPC between components
- **Producer-consumer queues** - FIFO fire event processing with priority handling
- **Synchronized state management** - Race condition prevention across all subsystems

---

## 🚁 System Architecture

```
┌─────────────────┐      ┌─────────────────┐    ┌─────────────────┐
│   Fire Zones    │      │   Scheduler     │    │  Drone Fleet    │
│                 │      │                 │    │                 │
│• Event Detection│◄──►  │ • Task Queue    │◄──►│ • Route Planning│
│ • Zone Mapping  │      │ • Assignment    │    │ • Agent Dropping│
│ • CSV Processing│      │ • Fault Recovery│    │ • Battery Mgmt  │
└─────────────────┘      └─────────────────┘    └─────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 ▼
                        ┌─────────────────┐
                        │   GUI Monitor   │
                        │                 │
                        │ • Live Map      │
                        │ • Drone Status  │
                        │ • Metrics Log   │
                        └─────────────────┘
```

---

## 🖥️ Screenshots

### Real-Time Simulation Dashboard
*Live tracking of drone positions, fire locations, and system status*

### Performance Metrics Output
```
=== METRICS SUMMARY ===
Simulation Duration: 45231 ms

--- Drone Performance ---
Drone 1: 1250.5 meters traveled
Drone 2: 980.3 meters traveled
Avg Response Time: 1.2 seconds
Avg Extinguish Time: 8.7 seconds
```

---

## 🚀 Quick Start

### Prerequisites
- Java 11+ 
- IDE with Swing support (IntelliJ recommended)

### Installation & Run
```bash
git clone https://github.com/yourusername/fire-drone-swarm-simulation.git
cd fire-drone-swarm-simulation

# Open in IntelliJ IDEA
# Run FireIncidentSimulation.java

# Or via command line:
javac -d out src/*.java
java -cp out FireIncidentSimulation
```

### Configuration
Customize simulation parameters in `FireIncidentSimulation.java`:
```java
String fireIncidentFile = "input/test_event_file_with_faults.csv";
String zoneFile = "input/test_zone_file.csv"; 
int numDrones = 10;  // Adjust fleet size
```

---

## 📊 Key Features Demonstrated

| Feature | Implementation |
|---------|---------------|
| **Concurrency** | 10+ threads managing zones, scheduler, and drone fleet |
| **Communication** | UDP-based RPC with serialization and fault tolerance |
| **GUI** | Real-time Swing interface with live updates |
| **Algorithms** | Shortest path routing, resource optimization, task scheduling |
| **Testing** | Fault injection framework for reliability validation |

---

## 🎓 Learning Outcomes

This project demonstrates proficiency in:
- **Concurrent Programming** - Thread safety, synchronization, producer-consumer patterns
- **Distributed Systems** - Network communication, fault tolerance, state management  
- **Software Architecture** - Modular design, separation of concerns, scalable patterns
- **GUI Development** - Real-time interfaces, event-driven programming
- **Algorithm Design** - Optimization, scheduling, pathfinding

---

## 📄 Portfolio Notice
This repository is for **portfolio demonstration purposes only**. 
The code showcases advanced Java development skills including multithreading, 
networking, and real-time systems design.

*This was a collaborative university project - I led development of the scheduling algorithms, 
fault tolerance systems, and GUI components.*

---

*Built with ☕ and lots of concurrent debugging*
