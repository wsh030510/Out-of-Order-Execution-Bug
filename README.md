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
| [L1-01](./Layer1/1-Linuxeasy.c) | [#123]() | Linux Kernel | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-02](./Layer1/2-DPDK.c) | [CVE-202X-XXXX]() | DPDK | Store-Store Reordering | Feb 05, 2025 | Feb 10, 2025 |
| [L1-03](./Layer1/3-seL4-dynamic.c) | [#123]() | sel4 | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-04](./Layer1/4-MySQL.c) | [#123]() | MySQL | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-05](./Layer1/5-StackOverflowEasy.c) | [#123]() | General Testing | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-06](./Layer1/6-ompi.c) | [#123]() | Open MPI | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-07](./Layer1/7-OpenBLAS.c) | [#123]() | OpenBLAS | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-08](./Layer1/8-CVE-2020-11739-Xen.c) | [#123]() | Xen | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-09](./Layer1/9-CVE-2020-25603-Xen.c) | [#123]() | Xen | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-10](./Layer1/10-ceph.c) | [#123]() | Ceph | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-11](./Layer1/11-MariaDBEasy.c) | [#123]() | MariaDB | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-12](./Layer1/12-DragonWell8Easy.cpp) | [#123]() | JDK | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-13](./Layer1/13-JDK.c) | [#123]() | JDK | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-14](./Layer1/14-libfabric.c) | [#123]() | libfabric | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-15](./Layer1/15-openmpi.c) | [#123]() | Open MPI | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-16](./Layer1/16-includeos.c) | [#123]() | IncludeOS | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-17](./Layer1/17-mysql.c) | [#123]() | MySQL | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-18](./Layer1/18-JDK-8179954.c) | [#123]() | JDK | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-19](./Layer1/19-ompi.cpp) | [#123]() | Open MPI | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-20](./Layer1/20-barrier.cpp) | [#123]() | General Testing | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-21](./Layer1/21-crossbeam.c) | [#123]() | Crossbeam | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-22](./Layer1/22-MariaDB.c) | [#123]() | MariaDB | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-23](./Layer1/23-mcs.c) | [#123]() | DPDK | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-24](./Layer1/24-mysql_rwlock_deadlock.c) | [#123]() | MySQL | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-25](./Layer1/25-mysql_volatile_bug.c) | [#123]() | MySQL | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-26](./Layer1/26-mysql-99556.c) | [#123]() | MySQL | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-27](./Layer1/27-mysql-ut-realx.c) | [#123]() | MySQL | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-28](./Layer1/28-pso_test.c) | [#123]() | General Testing | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-29](./Layer1/29-sofa_pbrpc_hang.c) | [#123]() | sofa-pbrpc | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-30](./Layer1/30-tso_test.c) | [#123]() | General Testing | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-31](./Layer1/31-unsafe_publish.c) | [#123]() | General Testing | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| [L1-32](./Layer1/32-datarace.cpp) | [#123]() | General Testing | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |

**Layer 2: Resource Lifecycle Level**

| Bug Id | Source | Target System | Type | Registered | Resolved |
| :--- | :--- | :--- | :--- | :--- | :--- |
| [L2-01](./Layer2/1-rds.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-02](./Layer2/2-vlan.c) | [#789]() | Linux Kernel | Kernel Panic | Mar 12, 2025 | Mar 15, 2025 |
| [L2-03](./Layer2/3-vlan-s.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-04](./Layer2/4-xsk2.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-05](./Layer2/5-fs.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-06](./Layer2/6-bpf.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-07](./Layer2/7-xdp2.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-08](./Layer2/8-watchqueue.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-09](./Layer2/9-tls2.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-10](./Layer2/10-smc2.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-11](./Layer2/11-gsm.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-12](./Layer2/12-xsk.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-13](./Layer2/13-xdp.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-14](./Layer2/14-vmci.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-15](./Layer2/15-tls.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-16](./Layer2/16-nbd.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-17](./Layer2/17-unix.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-18](./Layer2/18-unix-s.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-19](./Layer2/19-tcve-2016-8655.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-20](./Layer2/20-tcve-2017-2636.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-21](./Layer2/21-tcve-2018-12232.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-22](./Layer2/22-tcve-2019-6974.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-23](./Layer2/23-watchqueue.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| [L2-24](./Layer2/24-xsk.c) | [#456]() | Linux Kernel | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |

**Layer 3: Semantic Logic Level**

| Bug Id | Source | Target System | Type | Registered | Resolved |
| :--- | :--- | :--- | :--- | :--- | :--- |
| [L3-01](./Layer3/L3-1.c) | [#999]() | Linux Kernel | State Machine Error | Apr 01, 2026 | --- |
| [L3-02](./Layer3/L3-2.c) | [#999]() | Linux Kernel | State Machine Error | Apr 01, 2026 | --- |
