# EGFWD_RTOS 🚦
**Advanced Embedded Systems Track - Real-Time OS Implementation**

![RTOS](https://img.shields.io/badge/RTOS-FreeRTOS-blue?style=for-the-badge&logo=freertos)
![Platform](https://img.shields.io/badge/Platform-STM32_/_ARM-00356A?style=for-the-badge&logo=stmicroelectronics)
![Track](https://img.shields.io/badge/Track-EG__FWD_Advanced-green?style=for-the-badge)
![Author](https://img.shields.io/badge/Author-Abdelrahman--Elnahrawy-blue?style=for-the-badge&logo=github)

This repository contains the RTOS project for the **EG_FWD Advanced Embedded Systems Track**. It demonstrates the shift from sequential Super-Loop architectures to concurrent multi-tasking environments, focusing on task synchronization, resource management, and deterministic timing.

---

## 🎯 Project Objectives
The core of this project is to manage multiple asynchronous hardware events using an RTOS kernel (typically FreeRTOS). Key focuses include:
* **Task Management:** Creating and prioritizing independent threads of execution.
* **Inter-Task Communication (ITC):** Using Queues to pass data between tasks safely.
* **Resource Synchronization:** Implementing Semaphores and Mutexes to prevent race conditions and Priority Inversion.
* **Deterministic Timing:** Utilizing Software Timers and Delay functions to ensure real-time responsiveness.

---

## 🏗️ System Architecture

The application is divided into functional tasks, each with its own stack and priority level.



### Implemented Kernel Objects:
* **Binary Semaphores:** Used for task synchronization with hardware interrupts (e.g., UART Data Received).
* **Mutexes:** Protecting shared hardware resources (e.g., an LCD or I2C bus) from concurrent access.
* **Message Queues:** Buffering data between producer and consumer tasks to decouple processing speeds.

---

## 🛠️ Tech Stack & Tools
* **Kernel:** FreeRTOS / Custom Kernel
* **Architecture:** ARM Cortex-M
* **Development Environment:** STM32CubeIDE / Keil uVision
* **Debugging:** ST-LINK / SEGGER J-Link (Task-aware debugging)

---

## 📂 Project Structure
```text
/EGFWD_RTOS
  ├── /Inc
  │    ├── FreeRTOSConfig.h  # Kernel configuration and preemption settings
  │    └── tasks.h           # Task function prototypes
  ├── /Src
  │    ├── main.c            # Kernel initialization and task creation
  │    └── freertos.c        # Task implementations and hook functions
  ├── /Middlewares           # FreeRTOS source files
  └── README.md
  ```
## 🚀 Key Learning Outcomes
Context Switching: Understanding how the CPU saves and restores registers during a TCB switch.

Priority Preemption: Observing how the scheduler handles higher-priority tasks in real-time.

Deadlock Avoidance: Designing systems that prevent circular dependencies in resource locking.

## 👤 Author
Abdelrahman Elnahrawy EG_FWD Advanced Embedded Systems Scholar

## 📄 License
This project is part of the EG_FWD scholarship program and is open-source under the MIT License.
