# Use of Microservices Architecture

* Status: proposed
* Date: 2025-02-19

## Context and Problem Statement

Our web application requires a database to store user data, product information, and transaction records. The application needs to handle a high number of read and write operations efficiently while ensuring data integrity and availability. The team needs to choose between a relational and a NoSQL database to best meet these requirements.

## Considered Options

* 1. Relational Database (e.g., PostgreSQL)
   - Pros:
     - Strong ACID compliance for transactions.
     - Well-suited for complex queries and data relationships.
     - Mature ecosystem with robust tooling and community support.
   - Cons:
     - Can become a bottleneck under heavy write loads.
     - Schema migrations may be cumbersome.

2. NoSQL Database (e.g., MongoDB)
   - Pros:
     - Excellent scalability and performance for large datasets.
     - Flexible schema design allows for easier changes.
     - Designed for high write loads and quick data retrieval.
   - Cons:
     - Weaker consistency guarantees (eventual consistency).
     - More challenging to execute complex queries that require joins.

3. Hybrid Approach (Using Both Relational and NoSQL)
   - Pros:
     - Leverage strengths of both database types.
     - Ability to optimize performance for different use cases.
   - Cons:
     - Increased complexity in managing two database systems.
     - Higher operational overhead.

## Decision Outcome

Chosen option: "After evaluating the options, we have decided to adopt a **Relational Database (PostgreSQL)** for our application. This choice is driven by the need for strong consistency and ACID transactions, which are critical for our use cases involving user data and transactions. While we acknowledge the potential performance limitations, we believe that PostgreSQL's capabilities, combined with proper indexing and query optimization, will meet our initial requirements.  We will revisit this decision in the future if our scaling needs change significantly or if the application starts to exhibit performance bottlenecks.  ## Date", because comes out best.
