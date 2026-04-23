**MGO-OOO-Bugs**: A Benchmark of Multi-Granularity Out-of-Order Concurrency Bugs﻿

This repository contains the dataset for our paper on "Out-of-Order (OOO) Execution Bugs" under Weak Memory Models (WMM). We propose a Multi-Granularity Ordering (MGO) taxonomy and collect 58 OOO bug samples across different system abstraction layers.

📂 Repository Structure (MGO Taxonomy)
Our dataset is strictly categorized into three layers based on the triggering level of the concurrency bugs:
* **[Layer1](./Layer1)**: Micro-Instruction Level (32 Samples). Focuses on pure hardware-sensitive reorderings (Store-Store, Store-Load) in fundamental lock-free data structures (e.g., Spinlocks, Ring Buffers).
* **[Layer2](./Layer2)**: Resource Lifecycle Level (24 Samples). Focuses on hardware-agnostic and OS-level reorderings, typically manifesting as Use-After-Free (UAF) or Kernel Panics driven by thread scheduling or interrupts (e.g., Linux Kernel, Drivers).
* **[Layer3](./Layer3)**: Semantic Logic Level (2 Samples). Focuses on complex state machine or protocol disruptions in high-performance distributed systems and networking frameworks (e.g., MySQL, DPDK, sofa-pbrpc).

🏷️ Label Definitions
* **Bug Id**: Our own defined internal reference number for the bug (e.g., L1-01).
* **Source**: The source of the vulnerability or the submission number of the vulnerability.
* **Target System**: The software project or framework where the bug is located (e.g., MySQL, Linux Kernel, DPDK).
* **Type**: The specific manifestation or category of the concurrency error (e.g., UAF, Deadlock, Store-Load reordering).
* **Registered**: The date the bug was initially reported or raised by the community.
* **Resolved**: The date the bug was officially fixed or closed by the developers.

**Layer 1: Micro-Instruction Level**
| Bug Id | Source | Target System | Type | Registered | Resolved |
| :--- | :--- | :--- | :--- | :--- | :--- |
| L1-01 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-02 | [CVE-202X-XXXX]() | Resolved | Store-Store Reordering | Feb 05, 2025 | Feb 10, 2025 |
| L1-03 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-04 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-05 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-06 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-07 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-08 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-09 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-10 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-11 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-12 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-13 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-14 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-15 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-16 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-17 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-18 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-19 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-20 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-21 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-22 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-23 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-24 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-25 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-26 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-27 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-28 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-29 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-30 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-31 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-32 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |

**Layer 2: Resource Lifecycle Level**
| Bug Id | Source | Target System | Type | Registered | Resolved |
| :--- | :--- | :--- | :--- | :--- | :--- |
| L2-01 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-02 | [#789]() | Resolved | Kernel Panic | Mar 12, 2025 | Mar 15, 2025 |
| L2-03 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-04 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-05 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-06 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-07 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-08 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-09 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-10 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-11 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-12 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-13 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-14 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-15 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-16 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-17 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-18 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-19 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-20 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-21 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-22 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-23 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-24 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |

**Layer 3: Semantic Logic Level**
| Bug Id | Source | Target System | Type | Registered | Resolved |
| :--- | :--- | :--- | :--- | :--- | :--- |
| L3-01 | [#999]() | Open | State Machine Error | Apr 01, 2026 | --- |
| L3-02 | [#999]() | Open | State Machine Error | Apr 01, 2026 | --- |
