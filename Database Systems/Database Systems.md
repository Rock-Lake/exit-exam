# Introduction
A database is a very large, integrated, organized collection of information stored in a [[#^1704ab|database management system]].
This system was developed after passing through 3 levels of development for storing data:
- **Manual Approach:** files are written in paper, labeled and stored in cabinets. Insertion and retrieval is done manually, file-by-file, cabinet-by-cabinet. This is prone to error, difficult to change and cross-reference.
- **File based Approach:** files are created and managed by applications in [[Distributed Systems|distributed systems]]. This leads to data being duplicated or corrupted due to inconsistent data update, a.k.a, *update anomalies*.
- **Database Approach:** data is stored in organized tables called *relations*; designed for simultaneous use by different users and applications. This allows for a central management of data using [[constraints]] to facilitate validity and consistency of a shared data resource.

# Database Management System
A database management system(DBMS) is a software package used for creating and managing large amounts of data efficiently and storing data without degradation over long periods of time. It provides the following services: ^1704ab
- Data storage, retrieval and update
- user accessible catalog
- an [[atomic]] transaction support service
- concurrency control services
- failure recovery services
- access and authorization services
- data regulation (Integrity) services
- data independency services

DBMS provides facilities for database definition, manipulation and control through:
- **Data Definition Language(DDL):** command language for setting up a database, create, delete and alter table, and handle constraints.
- **Data Manipulation Language(DML):** command for end-users/programmers to store retrieve and access data in the database. For example: SQL

DBMS as a system interacts and integrates with:
- **Hardware -** PCs, mainframes, servers, network infrastructures and peripherals
- **Software -** DBMS software, application programs, operating systems
- **Procedures -** rules and regulations on design and use of database
- **Data -** operational data and metadata(database properties)
- **People -** database admins, database designers, system programmers, system analysts, end users, 

DBMS consists of the following structures:
- **Disk space manager -** interacts with the OS file system
- **Buffer manager -** brings pages into RAM from disk
- **Query Evaluation -** optimizes query requests of data
- **File and access code -** brings data from disk to query evaluation system
- **Transaction Lock manager -** manages concurrent access of the stored data
- **Recovery manager -** maintains system log and system restore.

DBMS can be implemented in 3 architectures:
1. **Centralized Client-Server architecture:** combines the DBMS software, application programs, user interface, and hardware into a single system.
2. **Two Tier Client-Server architecture:** connect multiple clients to several DBMS through a communication network.
3. **Three Tier Client-Server architecture:** common for web applications, it separates the user interface into client application, the web connectivity and business logic into web server and the DBMS into the database server.

# Database Development Life Cycle(DDLC)
Since no single database can fit all systems; it thus requires procedure in database design. It consists of the following steps:
1. **Planning** - identify information gap for a database solution
2. **Analysis** - [[feasibility study]], requirement determination and structuring
3. **Design** - this phases consists of 3 sub-phases, each with their own [[Database Model|data abstraction.]]
	1. **Conceptual Design** - structures the information requirements by creating the [[Database Model#^52e5e4|conceptual model]] of the database
	2. **Logical Design** - converts the conceptual model into the [[Database Model|data model]] of the database system that will be used.
	3. **Physical Design** - implements the logical design using the selected DBMS
4. **Implementation** - test and deploy the designed database for use.
5. **Operation and Support** - administer and maintain database operation and provide user support.

