This project, 'Terning's Final Gift', is a web platform built to host a final farewell event for the users of the 'Terning' service. It features a first-come, first-served giveaway designed to thank the community for their support.

The core technical challenge was to build a system capable of withstanding a massive, instantaneous traffic spike—the 'Thundering Herd' problem—at the moment the event starts. The goal was to prevent server crashes, eliminate race conditions for the limited gifts, and ensure data integrity under extreme load.

To address these challenges, I implemented an asynchronous, event-driven architecture. Redis is used for real-time inventory management with atomic operations and distributed locking to manage concurrency. Kafka serves as a message queue to decouple the initial user request from the slower database-intensive tasks, ensuring high responsiveness. The entire application is containerized with Docker and monitored using Prometheus and Grafana.

The result is a resilient and scalable system that delivers a smooth user experience even under heavy traffic. This project demonstrates a deep understanding of distributed systems, performance optimization, and modern back-end technologies.
