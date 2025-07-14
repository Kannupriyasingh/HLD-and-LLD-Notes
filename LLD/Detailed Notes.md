# 📦 Low-Level Design (LLD) — Notes

## 📝 **Detailed Notes**

### Step 1: Object Oriented Programming

* **Encapsulation:** combine data & methods; protect internal state.
* **Abstraction:** focus on relevant features; hide complexity.
* **Inheritance:** share/reuse code, e.g., base class `Vehicle` → `Car` & `Truck`.
* **Polymorphism:** override methods; run-time and compile-time polymorphism.
* **SOLID:**

  * SRP: one responsibility.
  * OCP: open for extension, closed for modification.
  * LSP: derived classes must substitute base.
  * ISP: no fat interfaces.
  * DIP: depend on abstractions.

### Step 2: Design Patterns

* **Singleton:** one instance.
* **Factory:** create objects based on input.
* **Proxy:** control access to objects.
* **Bridge:** separate abstraction & implementation.
* **Strategy:** select algorithm at runtime.
* **Observer:** subscribe to changes.
* **Command:** encapsulate requests as objects.

### Step 3: Concurrency & Thread Safety

* Dependency injection frameworks must be thread-safe.
* Locking: mutex, semaphore, read-write lock.
* Producer-consumer queues (blocking queues).
* Handle race conditions by synchronization.
* Use concurrent collections & atomic classes.

### Step 4: UML Diagrams

* **Class diagram:** classes & relationships.
* **Sequence diagram:** object interactions over time.
* **Activity diagram:** workflows.
* **State diagram:** object states & transitions.

### Step 5: APIs

* Design RESTful APIs; choose proper nouns & verbs.
* Model request & response DTOs.
* API versioning (`/v1/`, headers).
* Follow DRY, SRP.
* Avoid God classes: split services logically.

### Step 6: Common LLD Problems

* Tic tac toe: board, player, move classes.
* Splitwise: user, expense, balance service.
* Parking lot: vehicle, slot, ticket, payment.
* Elevator: controller, elevator, request.
* Notification system: sender, channel, template.
* Food delivery: user, order, restaurant, delivery.
* Movie booking: theater, show, seat, booking.
* URL shortener: URL mapping, hash generator.
* Logging: log levels, appenders.
* Rate limiter: token bucket, sliding window.

---

✅ Use these notes to revise, create diagrams, or practice system design interviews!
