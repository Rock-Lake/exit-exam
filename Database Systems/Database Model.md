A data model is an abstraction on the complex views of how data is stored and managed in the database. It is used as a communication tool among designers, programmers and end users.

All data models consist of the following building blocks:
- **Entity** - anything about which data is collected and stored.
- **Attribute** - the property of an entity
- **Relationship** - an association among entities. It can be one-to-one, one-to-many or many-to-many relationship
- **Constraint** - restriction placed on the data

When developing data models, properly identifying the business rules is essential to model the entities, attributes, relationships and constraints of the proposed data model. Business rules are the set of rules and regulations used in day-to-day operation of data in the company.

Data models can be divided into 3 categories:
- **Conceptual Model** - also known as *logical schema*, it is representing a global view of the database, this model is used to create an abstract model of grouping the data into entities and their relationships independently of software and hardware constraints. ^52e5e4
- **Internal Model** - it represents the implementation of the conceptual model through the chosen [[Database Systems#^1704ab|DBMS]].
- **Physical Model** - it shows the way data is stored on physical media and methods of accessing it.

The conceptual model can be developed in one of two ways:
 - create an [[Entity-Relationship Model|entity-relationship model]]
 - use a set of algorithms called [[Normalization|normalization]] 