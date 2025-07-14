Step 1: Fundamentals
Serverless vs Serverful
Serverless: Developers focus on code, provider manages infrastructure. Auto-scale, pay-per-use (e.g., AWS Lambda).
Serverful: You provision and manage servers (e.g., EC2, self-hosted).

Horizontal vs Vertical Scaling
Horizontal: Add more servers → better scalability and fault tolerance.
Vertical: Increase capacity (CPU, RAM) of single machine → limited by hardware.

Threads
Lightweight processes; share memory space, run concurrently.

Pages
Fixed-size blocks of memory (e.g., 4KB) used in memory management and virtual memory.

How does the internet work?
Devices send data as packets over networks using IP addresses and protocols like TCP/UDP, HTTP; DNS resolves names to IPs; routers/switches direct traffic.

Step 2: Databases
SQL vs NoSQL
SQL: Structured schema, ACID transactions.
NoSQL: Schema-less, scales horizontally, BASE properties.

In-memory DBs
e.g., Redis, Memcached → data stored in RAM → ultra-fast reads/writes.

Data replication & migration
Replication: Copy data across nodes for availability & fault tolerance.
Migration: Moving data to other storage or data centers.

Data partitioning
Splitting data across nodes (e.g., by user ID) for scalability.

Sharding
Specific partitioning → each shard holds a subset of data; reduces load on single DB.

Step 3: Consistency vs Availability
Data consistency & its levels
Strong consistency: All nodes show latest data.
Eventual consistency: Nodes may temporarily differ.

Isolation levels
Read Uncommitted, Read Committed, Repeatable Read, Serializable → define concurrency.

CAP theorem
Can't have all three: Consistency, Availability, Partition Tolerance → must choose two.

Step 4: Cache
What is Cache?
Fast-access storage layer for frequently requested data.
Examples: Redis, Memcached.

Write policies

Write-through: Update cache + DB simultaneously.

Write-back: Update cache first, then DB later.

Write-around: Write to DB, cache only on read.

Replacement policies
LFU (Least Frequently Used), LRU (Least Recently Used), Segmented LRU → decide what to evict.

CDNs
Distribute content closer to users → reduce latency, improve speed.

Step 5: Networking
TCP vs UDP
TCP: Reliable, ordered, slower (handshake).
UDP: Faster, no guarantee, used for real-time.

HTTP (1/2/3) & HTTPS
HTTP/1: Sequential requests.
HTTP/2: Multiplexing → concurrent streams.
HTTP/3: Based on QUIC → lower latency.
HTTPS: Adds encryption (TLS/SSL).

WebSockets
Full-duplex communication, real-time updates.

WebRTC
Peer-to-peer streaming → video/audio.

Step 6: Load Balancers
Algorithms

Stateless: Round-robin, random, least connections.

Stateful: Tracks sessions.

Consistent Hashing
Hash ring → minimal data movement when adding/removing servers.

Proxy vs Reverse Proxy
Proxy: User → proxy → internet.
Reverse proxy: Internet → proxy → servers.

Rate Limiting
Control request rates; avoid abuse & overload.

Step 7: Message Queues
Asynchronous Processing
e.g., Kafka, RabbitMQ → decouple producers/consumers.

Publisher-Subscriber
Producers publish messages to topics; consumers subscribe to topics.

Step 8: Monoliths vs Microservices
Why Microservices?
Independent deployability, scalability.

Single Point of Failure (SPOF)
Component whose failure brings system down.

Avoiding Cascading Failure
Circuit breakers, isolation, timeouts.

Containerization (Docker)
Package app + dependencies → run consistently anywhere.

Migrating to Microservices
Gradually refactor; extract domains.

Step 9: Monitoring & Logging
Logging
Track events, errors.

Monitoring metrics
CPU, memory, response time, request rate.

Anomaly detection
Identify unusual patterns automatically.

Step 10: Security
Tokens
e.g., JWT → store user claims securely.

SSO & OAuth
Single sign-on (SSO): One login across apps.
OAuth: Secure delegated access.

Access control lists, rule engines
Define who can do what.

Encryption
Data protection in transit & at rest.

Step 11: System Design Trade-offs
Push vs Pull: Push → server notifies; Pull → client polls.

Consistency vs Availability: CAP trade-off.

SQL vs NoSQL: Schema vs scalability.

Memory vs Latency: Cache increases memory use but lowers latency.

Throughput vs Latency: Batch requests (higher throughput) vs instant response.

Accuracy vs Latency: Realtime predictions (lower latency) vs accurate batch jobs.

Step 12: PRACTICE
Design systems like:

YouTube

Twitter

WhatsApp

Uber

Amazon

Dropbox / Google Drive

Netflix

Instagram

Zoom

Booking.com / Airbnb
