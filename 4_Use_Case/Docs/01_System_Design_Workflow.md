### 🔷🔶🔷 Chapter 1: System Design Workflow (System Design Interview Approach)

---

### 🔷🔶🔷 Introduction — About This Section

    🔹 System design interviews are designed to evaluate logical
       and analytical thinking.

    🔹 They check the candidate's capability to produce technical
       solutions to real-world problems.

    🔹 The main agenda of system design interview questions is to
       assess the ability to solve open-ended and abstract problems.

    🔹 Context: In a world where AI can generate code, AI cannot
       give an end-to-end solution by itself. Companies and
       organizations are looking for people who can provide
       end-to-end solutions in the most efficient way possible.

    🔹 System design interviews check:
        🔸 Thinking capacity
        🔸 Analytical skill
        🔸 Problem-solving skill

    🔹 So companies can be confident they're hiring the best candidate.

**🟠 There Is No Single "Correct" Answer**

    🔹 People at different experience levels will approach the
       same problem differently.

    🔹 In a system design interview, there is typically NO single
       expected "correct" solution.

    🔹 It is always better to actively interact with the
       interviewer, ask questions, and discuss the problem step by step.

---

### 🔷🔶🔷 The 7 Steps of the System Design Workflow

    🔹 The following seven steps should be followed, in sequence,
       for any system design problem:

        🔸 Step 1: Requirement Clarification
        🔸 Step 2: Estimation and Constraints
        🔸 Step 3: Data Model Design
        🔸 Step 4: API Design
        🔸 Step 5: High Level Design
        🔸 Step 6: Detailed Design
        🔸 Step 7: Identifying and Resolving Bottlenecks

---

### 🔷🔶🔷 Step 1: Requirement Clarification

    🔹 System design interview questions are often open-ended and
       lack precise details.

    🔹 The interviewer usually gives a single-sentence problem statement, e.g.:
        🔸 "Design a system like TinyURL."
        🔸 "Design a taxi booking application like Uber."
        🔸 "Design a data storage application like Google Drive."

    🔹 It is the candidate's duty and responsibility to ask
       questions to the interviewer, to understand the exact scope
       of the problem, and clarify the functional requirements
       EARLY in the interview.

    🔹 Requirements should be categorized into THREE parts:

        🔸 1. Functional Requirements
        🔸 2. Non-Functional Requirements
        🔸 3. Extended Requirements

---

**🔘 1. Functional Requirements**

    🔹 The requirements that the end user specifically demands, as
       basic functionalities the system should offer.

    🔹 All functional requirements should be integrated into the
       system as a required part of the agreement.

**🟠 Example**

    🔹 Asking the interviewer "What features do we need to design
       for this system?" might yield:
        🔸 User authentication should be present.
        🔸 The application should be able to store data into a
           database and retrieve it.
        🔸 There should be role-based access to the application.
        🔸 There should be an option for processing payments.

    🔹 All of these become the Functional Requirements — the user
       has specifically demanded these functions be present.

---

**🔘 2. Non-Functional Requirements**

    🔹 The quality constraints that the system must satisfy,
       according to the project contract.

    🔹 Also called Non-Behavioral Requirements.

    🔹 Examples of Non-Functional Requirements:
        🔸 Performance and speed of the application.
        🔸 Scalability of the application.
        🔸 Availability and reliability of the application.
        🔸 Security concerns to consider for a highly secure system.

    🔹 Non-functional requirements pertain to the QUALITY of the application.

---

**🔘 3. Extended Requirements**

    🔹 "Nice to have" requirements that might be out of the scope
       for the current system, but are still worth noting.

    🔹 Examples of Extended Requirements:
        🔸 Operational and support requirements.
        🔸 Disaster recovery plans.

    🔹 All of this information should be collected from the
       interviewer before moving forward.

---

### 🔷🔶🔷 Step 2: Estimation and Constraints

**🟠 Estimation**

    🔹 Estimation involves making reasonable assumptions about how
       much traffic, data, or resources the system will need to handle.

    🔹 This helps in choosing the right technologies and designing
       scalable components.

**🟠 Example — Google Drive**

    🔹 Assumptions:
        🔸 10 million users per month.
        🔸 Average upload: 2 files per user per day.
        🔸 Average file size: 5 MB.

    🔹 Using this, an estimate of daily data uploaded can be
       calculated: approximately 100 TB per day.

    🔹 This estimate helps decide:
        🔸 What type of storage is needed.
        🔸 What bandwidth is required.
        🔸 What load balancing options should be selected.
        🔸 What database and caching layers need to be implemented.

    🔹 Discussing traffic and usage patterns with the interviewer
       helps estimate the right technology to use.

**🟠 Constraints**

    🔹 Constraints are the limitations that must be worked within
       while designing a system.

    🔹 These can be technical, business, legal, or operational constraints.

**🟠 Example — Google Drive Constraints**

    🔹 Latency constraints -> e.g. each file upload should
       complete within 5 seconds.

    🔹 Storage constraints -> e.g. a regular user gets 15 GB,
       premium users get 1 TB.

    🔹 Budget constraints -> e.g. monthly cloud cost should not
       exceed $50,000.

    🔹 These questions should be asked to the interviewer to
       arrive at an actual plan of action.

---

### 🔷🔶🔷 Step 3: Data Model Design

    🔹 After gathering requirements, estimations, and constraints,
       there should now be a good idea of what the application does.

    🔹 This idea is used to start designing the DATABASE SCHEMAS.

    🔹 Data model design helps understand the DATA FLOW — the core
       of every system design.

    🔹 In this step, different ENTITIES and the RELATIONSHIPS
       between them are defined.

**🟠 Questions to Answer in This Step**

    🔹 What are the different entities in the system?

    🔹 What are the relationships between these entities?

    🔹 How many tables are needed for this application?

    🔹 Which type of database should be used — SQL or NoSQL?

**🟠 Output**

    🔹 By the end of this step, an Entity Relationship (ER)
       Diagram should be produced.

    🔹 Example: For an e-commerce application, this might result
       in 5 tables, with fields defined for each table.

    🔹 Note: These diagrams need not be 100% perfectly correct,
       but they should accurately relate to the problem statement
       in question.

---

### 🔷🔶🔷 Step 4: API Design

    🔹 API design helps define the BEHAVIOR of the system explicitly.

    🔹 While designing the API, no actual code needs to be
       written — just a simple interface definition is sufficient.

**🟠 Example — E-commerce Application**

    🔹 Define the application's functions/behaviors (its API), such as:
        🔸 List Product
        🔸 Get Product
        🔸 Create Product
        🔸 Update Product
        🔸 Delete Product

    🔹 Along with each function: its parameters and expected return type.

**🟠 RESTful API Style (Optional)**

    🔹 If designing the APIs in a RESTful manner, define:
        🔸 The HTTP method and endpoint for listing all products.
        🔸 The HTTP method and endpoint for getting a single product.
        🔸 The HTTP method and endpoint for creating a product.
        🔸 ...and so on.

    🔹 No need to go into the actual coding details of these
       endpoints — just a list of APIs (and optionally their
       responses) is sufficient for this step.

---

### 🔷🔶🔷 Step 5: High Level Design

    🔹 High Level Design is the process of breaking down a system
       into major functional building blocks/components, and
       defining how they interact with each other.

    🔹 This step helps identify the different components required
       to solve the problem.

**🟠 Questions to Answer in This Step**

    🔹 Is it best to design a monolithic or a microservice architecture?

    🔹 What are the core parts of the system?

    🔹 How do they communicate with each other?

    🔹 What are the different types of databases that can be used here?

**🟠 Example Output**

    🔹 A diagram showing components like: entry point, data
       ingestion, load balancers, streaming components (e.g.
       Amazon Kinesis Stream for a data analytics use case), and
       so on — along with how they communicate.

    🔹 The exact components used will depend on the specific
       problem statement being solved.

---

### 🔷🔶🔷 Step 6: Detailed Design

    🔹 In this step, the major components identified in the High
       Level Design are explored in DETAIL.

    🔹 This is the step where abstract building blocks are turned
       into concrete technical solutions.

    🔹 The exact technology, data structures, and algorithms to be
       used are specified here.

    🔹 It's ensured that each component is implementable,
       scalable, and testable in nature.

**🟠 Examples of What's Covered in This Step**

    🔹 What languages will be used to implement the solution?

    🔹 What frameworks should be used?

    🔹 What exact database will be used to implement the solution?

    🔹 What type of communication should occur between different
       components of the system?

    🔹 The exact tech stack and algorithms needed to solve the
       problem statement are defined here.

---

### 🔷🔶🔷 Step 7: Identifying and Resolving Bottlenecks

    🔹 In this final step, bottlenecks and approaches to mitigate
       them are discussed.

    🔹 A bottleneck can be any component or part of the system
       that slows down the overall performance of the system.

**🟠 Questions to Discuss in This Step**

    🔹 Do we have enough database replicas?

    🔹 Is there any single point of failure to identify?

    🔹 Is database sharding required?

    🔹 How can the system be made more robust?

    🔹 How can the availability of the cache be improved?

    🔹 Various such questions are asked to identify and resolve
       different bottlenecks in the system design.

---

### 🔷🔶🔷 Additional Concepts — Extending the System Design Workflow

    🔹 The following points add further practical depth to the
       workflow described above.

**🔘 Useful Back-of-the-Envelope Numbers for Estimation**

    🔹 Some commonly useful reference numbers when doing quick
       estimation (Step 2) in interviews:
        🔸 1 char (ASCII) ≈ 1 byte.
        🔸 1 million (10^6) requests/day ≈ ~12 requests/second on
           average (rough rule of thumb: divide daily count by ~86,400 seconds).
        🔸 Reading from memory (RAM) is orders of magnitude faster
           than reading from disk (SSD/HDD), which in turn is much
           faster than a round-trip network call.
        🔸 A reasonable single server can often handle low
           thousands of requests per second for simple operations,
           though this varies greatly by workload.

    🔹 These numbers are approximate and meant to help ballpark
       capacity requirements quickly — not to be taken as precise
       benchmarks.

**🔘 Common Non-Functional Requirement Trade-offs to Mention**

    🔹 When discussing non-functional requirements, it often helps
       to explicitly reference concepts covered earlier in the
       course, such as:
        🔸 CAP Theorem trade-offs (Consistency vs Availability
           during a network partition).
        🔸 PACELC trade-offs (Latency vs Consistency when there's
           no partition).
        🔸 Whether the system is read-heavy or write-heavy (which
           affects caching, replication, and denormalization decisions).

**🔘 Communication Tips for the Interview Itself**

    🔹 Think out loud — narrate the reasoning behind each decision,
       rather than jumping straight to a diagram.

    🔹 Start broad (high level design) before diving into details
       — avoid getting stuck on one component too early.

    🔹 Explicitly call out trade-offs at each step (e.g. "I'm
       choosing a NoSQL database here because writes will be much
       more frequent than reads, at the cost of some consistency
       guarantees").

    🔹 Manage time across the seven steps — spending too long on
       requirement clarification can leave insufficient time for
       high-level and detailed design, which are usually weighted
       more heavily by interviewers.

---

### 🔷🔶🔷 Summary — System Design Workflow at a Glance

    🔸 Why It's Asked        ->  To evaluate logical/analytical
                                thinking and the ability to
                                produce end-to-end solutions to
                                open-ended, abstract problems —
                                there is no single "correct" answer.

    🔸 Step 1: Requirement   ->  Clarify Functional Requirements
       Clarification              (must-have features), Non-Functional
                                Requirements (quality attributes:
                                performance, scalability,
                                availability, security), and
                                Extended Requirements (nice-to-have,
                                e.g. disaster recovery).

    🔸 Step 2: Estimation    ->  Estimate expected traffic, data
       and Constraints            volume, and resource needs (e.g.
                                daily storage for Google Drive);
                                identify technical, business,
                                legal, and operational constraints
                                (e.g. latency limits, storage
                                quotas, budget caps).

    🔸 Step 3: Data Model    ->  Define entities and their
       Design                     relationships; decide SQL vs
                                NoSQL; produce an ER diagram.

    🔸 Step 4: API Design    ->  Define the system's behavior as a
                                simple list of API
                                functions/endpoints, with
                                parameters and return types — no
                                actual coding required.

    🔸 Step 5: High Level    ->  Break the system into major
       Design                     components (monolith vs
                                microservices, core services,
                                databases) and define how they
                                communicate — produce a
                                high-level architecture diagram.

    🔸 Step 6: Detailed      ->  Specify the exact tech stack,
       Design                     frameworks, databases,
                                algorithms, and inter-component
                                communication mechanisms —
                                ensuring implementability,
                                scalability, and testability.

    🔸 Step 7: Bottlenecks   ->  Identify and resolve weak points
                                — single points of failure,
                                insufficient replication, sharding
                                needs, cache availability — to
                                make the system more robust.

    🔹 Following these seven steps in sequence provides a
       structured, repeatable approach to tackling any system
       design problem — whether in an interview or in real-world
       application design — ensuring nothing important is
       overlooked and the solution aligns with what's actually
       being asked for.

---