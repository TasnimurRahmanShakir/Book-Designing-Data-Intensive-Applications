# Designing Data-Intensive Applications (DDIA) 🏛️

[![Book](https://img.shields.io/badge/Book-O'Reilly-orange.svg)](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/)
[![Author](https://img.shields.io/badge/Author-Martin%20Kleppmann-blue.svg)](https://martin.kleppmann.com/)
[![Topic](https://img.shields.io/badge/Topic-Distributed%20Systems-green.svg)](#)

> **"The Big Ideas Behind Reliable, Scalable, and Maintainable Systems"**

This repository serves as a comprehensive study guide and technical reference for Martin Kleppmann's "Designing Data-Intensive Applications." It explores the internal workings of databases, distributed systems, and the trade-offs required to build modern, high-scale applications.

---

## 🚀 The Three Pillars
Every system described in the book is evaluated through these three fundamental lenses:

* **🛡️ Reliability:** The system should continue to work correctly even when things go wrong (hardware/software faults, human error).
* **📈 Scalability:** The system's ability to handle growth in data volume, traffic, or complexity.
* **🛠️ Maintainability:** Designing for the people who will operate and evolve the system over time.

---

## 📑 Roadmap

### **Part I: Foundations of Data Systems**
* **Ch 1:** Reliability, Scalability, and Maintainability.
* **Ch 2:** Data Models and Query Languages (SQL vs. NoSQL vs. Graph).
* **Ch 3:** Storage and Retrieval (LSM-Trees, B-Trees, Bitcask).
* **Ch 4:** Encoding and Evolution (Avro, Protocol Buffers, JSON).

### **Part II: Distributed Data**
* **Ch 5:** Replication (Single-leader, Multi-leader, Leaderless).
* **Ch 6:** Partitioning (Key range vs. Hash-based sharding).
* **Ch 7:** Transactions (Isolation levels, ACID, Race conditions).
* **Ch 8:** The Trouble with Distributed Systems (Unreliable clocks, Network delays).
* **Ch 9:** Consistency and Consensus (Linearizability, Raft, Paxos).

### **Part III: Derived Data**
* **Ch 10:** Batch Processing (MapReduce, Dataflow engines).
* **Ch 11:** Stream Processing (Message brokers, Kafka, CDC).
* **Ch 12:** The Future of Data Systems.

---

## 🧠 Technical Cheat Sheet

| Term | Quick Definition |
| :--- | :--- |
| **LSM-Tree** | Log-Structured Merge-Tree. Optimized for **high write throughput**. (e.g., Cassandra, RocksDB). |
| **B-Tree** | Balanced Tree. The standard for **read-heavy** workloads and relational databases. |
| **ACID** | Atomicity, Consistency, Isolation, Durability. The gold standard for safety in transactions. |
| **CAP Theorem** | Consistency, Availability, Partition Tolerance. You can only pick two (usually). |
| **SSTable** | Sorted String Table. A fundamental component of LSM-Tree storage. |
| **Quorum** | The minimum number of nodes that must vote for a distributed operation to succeed. |
| **CDC** | Change Data Capture. Observing a database log and emitting a stream of changes. |
| **Idempotence** | An operation that can be performed multiple times without changing the result beyond the first application. |

---

## 📊 Storage Engine Comparison

| Feature | LSM-Trees (Log-Structured) | B-Trees (In-place Update) |
| :--- | :--- | :--- |
| **Writes** | Very fast (Append-only) | Slower (Overwriting pages) |
| **Reads** | Slower (Check multiple files) | Faster (Direct path) |
| **Compaction** | Necessary to reclaim space | Not needed (Pages are reused) |
| **Workload** | Best for Write-Heavy | Best for Read-Heavy |

---

## 🛠️ Ecosystem Spotlight
The book explains the architecture behind these industry-standard tools:
* **Databases:** PostgreSQL, MySQL, MongoDB, Cassandra, HBase, Neo4j.
* **Streaming:** Apache Kafka, Apache Flink, RabbitMQ.
* **Distributed Coordination:** Apache ZooKeeper, etcd.
* **Processing:** Apache Spark, Hadoop MapReduce.

---

## 📜 Key Quotes
> *"Data is at the center of many challenges in system design today. Difficult issues need to be figured out, such as scalability, consistency, reliability, efficiency, and maintainability."*

> *"Software keeps changing, but the fundamental principles remain the same."*

---

## 📝 Study Progress
- [ ] **Part I: Foundations** - [ ] **Part II: Distributed Data** - [ ] **Part III: Derived Data** ---

### 🤝 Contributing
Feel free to fork this repository, add your own chapter summaries, or open an issue if you'd like to discuss a specific architectural trade-off!
