

Normal forms are a set of guidelines or rules applied to database schema design to minimize redundancy and dependency issues, thereby improving data integrity and efficiency. There are several normal forms, each building upon the principles of the previous one. Let's discuss the most commonly recognized normal forms:

**First Normal Form (1NF):**

Definition: A relation is in first normal form if it contains only atomic values and there are no repeating groups or arrays.
Key Points:
Each attribute value must be atomic, meaning it cannot be further divided into smaller pieces.
Each column in a table must contain only one value per row.
No repeating groups or arrays are allowed. Each attribute must have a single value for each record.

**Second Normal Form (2NF):**

Definition: A relation is in second normal form if it is in 1NF and every non-prime attribute is fully functionally dependent on the primary key.
Key Points:
It removes partial dependencies, meaning attributes are dependent on the entire primary key, not just part of it.
If a table has a composite primary key, each non-prime attribute must be dependent on the entire composite key, not just a part of it.

**Third Normal Form (3NF):**

Definition: A relation is in third normal form if it is in 2NF and every non-prime attribute is non-transitively dependent on the primary key.
Key Points:
It removes transitive dependencies, meaning no non-prime attribute should be dependent on another non-prime attribute.
If attribute B is functionally dependent on attribute A, and attribute C is functionally dependent on attribute B, then attribute C should be directly dependent on attribute A.
Boyce-Codd Normal Form (BCNF):

Definition: A relation is in Boyce-Codd normal form if every determinant is a candidate key.
Key Points:
It is a stronger version of 3NF, ensuring that every determinant (attribute that determines another attribute's value) is a candidate key.
BCNF eliminates some anomalies that may still be present in 3NF.

**Fourth Normal Form (4NF):**

Definition: A relation is in fourth normal form if it is in BCNF and has no multi-valued dependencies.
Key Points:
It removes multi-valued dependencies, ensuring that there are no dependencies between non-key attributes.
Beyond 4NF, there are higher normal forms like Domain-Key Normal Form (DK/NF), Fifth Normal Form (5NF), and Sixth Normal Form (6NF), but they are less commonly discussed and applied in practice.

Normalization is an iterative process where a database designer refines the database schema to achieve higher normal forms while ensuring that the design still meets the specific requirements and performance goals of the application.
