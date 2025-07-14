# 🌟 High-Level Design (HLD) — Detailed Notes

---

## 🪜 Step 1: Fundamentals

### 🔹 Serverless vs Serverful

| Feature    | Serverful                        | Serverless                                |
| ---------- | -------------------------------- | ----------------------------------------- |
| Management | You manage servers (e.g., EC2)   | Cloud provider manages infrastructure     |
| Scaling    | Manual/auto by you               | Auto-scaled by provider per request       |
| Pricing    | Pay for uptime                   | Pay per use (execution time, invocations) |
| Use case   | Stateful apps, predictable loads | Event-driven, unpredictable loads         |

Examples: AWS Lambda (serverless), EC2 (serverful).

### 🔹 Horizontal vs Vertical Scaling

* **Horizontal (scale-out):** add more machines → better fault tolerance.
* **Vertical (scale-up):** add CPU/RAM to single machine → limited by hardware.

### 🔹 Threads

Lightweight subprocesses within a process sharing memory; enable concurrency.

### 🔹 Pages

Fixed-size memory blocks (e.g., 4KB); fundamental in virtual memory.

### 🔹 How the internet works

DNS lookup → TCP/UDP → HTTP request → server response → browser renders.
TCP breaks down data into packets, manages their transmission, and reassembles them correctly at the destination, handling potential issues like packet loss or out-of-order delivery. 

---

## 🛢 Step 2: Databases

### 🔹 SQL vs NoSQL

| SQL                  | NoSQL                       |
| -------------------- | --------------------------- |
| Tables, fixed schema | Flexible schema             |
| ACID transactions    | BASE (eventual consistency) |
| Vertical scaling     | Horizontal scaling          |
| Strong consistency   | Tunable consistency         |

Examples: MySQL vs MongoDB, Cassandra.

### 🔹 In-memory DBs

Data kept in RAM → ultra-fast access. Examples: Redis, Memcached.

### 🔹 Data replication & migration

Replication: copies for availability. Migration: move data to new DB/cloud.

### 🔹 Data partitioning & sharding

Split data for scalability. Sharding = partitioning + routing strategy.

---

## ⚖ Step 3: Consistency vs Availability

### 🔹 Data consistency levels

* Strong: all nodes show latest data.
* Eventual: nodes converge over time.
* Tunable: configure consistency per operation.

### 🔹 Isolation levels

| Level            | Prevents                      |
| ---------------- | ----------------------------- |
| Read Uncommitted | Dirty reads                   |
| Read Committed   | Dirty reads                   |
| Repeatable Read  | Non-repeatable reads          |
| Serializable     | Phantom reads, full isolation |

### 🔹 CAP theorem

Cannot guarantee Consistency, Availability, and Partition tolerance simultaneously.

---

## 🧠 Step 4: Cache

### 🔹 What is Cache?

Fast-access layer to store frequently used data.

### 🔹 Write policies

* Write-through: write to cache & DB.
* Write-back: write to cache first, DB later.
* Write-around: write to DB directly.

### 🔹 Replacement policies

* LRU, LFU, Segmented LRU.

### 🔹 CDNs

Globally distributed caches for static content → reduce latency.

---

## 🌐 Step 5: Networking

### 🔹 TCP vs UDP

| Feature    | TCP                | UDP            |
| ---------- | ------------------ | -------------- |
| Connection | Reliable handshake | Connectionless |
| Order      | Guaranteed         | Not guaranteed |
| Speed      | Slower             | Faster         |

### 🔹 HTTP (1/2/3) & HTTPS

* HTTP/1: sequential.
* HTTP/2: multiplexing.
* HTTP/3: QUIC over UDP.
* HTTPS: adds TLS encryption.

### 🔹 WebSockets & WebRTC

* WebSockets: bi-directional.
* WebRTC: peer-to-peer video/audio.

---

## 🏗 Step 6: Load Balancers

### 🔹 Algorithms

* Round-robin, least connections, IP hash.

### 🔹 Consistent Hashing

Hash ring minimizes data reshuffling.

### 🔹 Proxy vs Reverse Proxy

* Proxy: client → proxy → internet.
* Reverse proxy: internet → proxy → servers.

### 🔹 Rate Limiting

Control request rates; avoid overload.

---

## 📨 Step 7: Message Queues

### 🔹 Asynchronous Processing

Producers & consumers decoupled. Examples: Kafka, RabbitMQ.

### 🔹 Pub/Sub

Publishers send messages to topics; subscribers consume.

---

## 🧩 Step 8: Monoliths vs Microservices

### 🔹 Why Microservices?

Independent deployment, scalability.

### 🔹 SPOF & cascading failure

* Avoid with redundancy, circuit breakers.

### 🔹 Containerization

Docker packages app + dependencies.

### 🔹 Migrating to microservices

Start from monolith → extract services.

---

## 📊 Step 9: Monitoring & Logging

### 🔹 Logging & metrics

Track app behavior and performance.

### 🔹 Tools

ELK, Prometheus, Grafana.

### 🔹 Anomaly detection

Detect outliers or spikes.

---

## 🔒 Step 10: Security

### 🔹 Tokens

JWTs for stateless authentication.

### 🔹 SSO & OAuth

* SSO: single login across apps.
* OAuth: delegated access.

### 🔹 ACLs & encryption

Define permissions; encrypt data at rest/in transit.

---

## ⚖ Step 11: System Design Trade-offs

* Push vs Pull.
* Consistency vs Availability.
* SQL vs NoSQL.
* Memory vs Latency.
* Throughput vs Latency.
* Accuracy vs Latency.

---

## 🛠 Step 12: Practice — Design these systems

* YouTube, Twitter, WhatsApp, Uber
* Amazon, Dropbox/Google Drive, Netflix
* Instagram, Zoom, Booking.com/Airbnb

---

✅ *Tip*: Use these notes to revise, create mind-maps, or discuss trade-offs in interviews!
