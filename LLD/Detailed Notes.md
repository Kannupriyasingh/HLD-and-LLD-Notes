# 📦 Low-Level Design (LLD) — Detailed Notes

## 🧰 **Object Oriented Programming (OOP)**

### Encapsulation

* Bind data (fields) and methods together.
* Hide internal state; only expose via public methods (getters/setters).
* Benefits: data integrity, easier maintenance.

### Abstraction

* Expose essential features, hide details.
* Use abstract classes/interfaces to define contracts.
* Example: `PaymentMethod` interface, implemented by `CreditCard`, `UPI`.

### Inheritance

* Allows new classes to reuse code from existing classes.
* Supports hierarchy: base → derived.
* Example: `Vehicle` → `Car`, `Bike`.

### Polymorphism

* One interface, many implementations.
* Compile-time (method overloading), run-time (method overriding).
* Enables flexible, decoupled code.

### SOLID Principles

* **SRP**: Class should have one responsibility.
* **OCP**: Classes open for extension, closed for modification.
* **LSP**: Subtypes must be substitutable for base types.
* **ISP**: Prefer multiple specific interfaces over single fat interface.
* **DIP**: Depend on abstractions, not concrete implementations.

---

## 🧩 **Design Patterns**

### Creational Patterns

* **Singleton**: Single shared instance; lazy or eager initialization.
* **Factory Method**: Create objects without specifying concrete classes.
* **Builder**: Step-by-step object construction.

### Structural Patterns

* **Proxy**: Control access, add logging, caching.
* **Bridge**: Decouple abstraction from implementation.
* **Adapter**: Make incompatible interfaces work together.
* **Decorator**: Add behavior dynamically.

### Behavioral Patterns

* **Strategy**: Choose algorithm at runtime.
* **Observer**: Notify subscribers of state changes.
* **Command**: Encapsulate request as object.
* **State**: Change behavior based on internal state.
* **Template Method**: Define skeleton, defer steps to subclasses.

---

## 🧵 **Concurrency & Thread Safety**

* Use synchronized blocks, locks (ReentrantLock).
* Read-write locks for frequent reads, rare writes.
* Avoid shared mutable state; prefer immutability.
* Use thread-safe collections (`ConcurrentHashMap`).
* Producer-consumer: use blocking queues.
* Identify & avoid race conditions.
* Atomic classes for counters.
* Thread-safe dependency injection in frameworks like Spring.

---

## 📊 **UML Diagrams**

* **Class Diagram**: Attributes, methods, relationships (association, aggregation, composition).
* **Sequence Diagram**: Object interaction over time (messages, calls).
* **Activity Diagram**: Workflows, branching logic.
* **State Diagram**: Object lifecycle, state transitions.
* **Component Diagram**: System's physical components.

---

## 📡 **APIs**

* RESTful design: nouns as resources, verbs as HTTP methods.
* Clear request/response models (DTOs).
* Versioning strategies: URL (`/v1/`), header, media type.
* Extensibility: optional fields, backward-compatible changes.
* Use pagination, filtering, sorting for large datasets.
* Follow DRY, SRP to keep controllers/services focused.
* Avoid God classes: split by responsibility.
* Use consistent naming, error handling, and documentation (OpenAPI).

---

## ⚙ **Common LLD Problems & Key Classes**

* **Tic Tac Toe / Chess**: Board, Player, Move, GameController.
* **Splitwise**: User, Expense, SplitStrategy, BalanceSheet.
* **Parking Lot**: Vehicle, Slot, ParkingFloor, Ticket, Payment.
* **Elevator System**: Elevator, Controller, Request, Display, Door.
* **Notification System**: Notification, Channel (Email, SMS), Sender, Template.
* **Food Delivery App**: User, Restaurant, MenuItem, Order, DeliveryPartner.
* **Movie Booking**: Theater, Screen, Show, Seat, Booking, Payment.
* **URL Shortener**: URLMapping, HashGenerator, RedirectionHandler.
* **Logging Framework**: Logger, Appender (Console, File), Formatter.
* **Rate Limiter**: TokenBucket, SlidingWindowCounter, RequestTracker.

---

✅ Use these notes to go deeper: add sequence diagrams, identify design patterns used, and write class diagrams for each system.
