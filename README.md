# AUTHOR: Kwandokuhle

1. The Dangers of Data Redundancy
When a company stores the same customer's physical address in three different tables, it creates data redundancy because information is duplicated. This wastes storage space and increases the possibility of errors and inconsistencies. For example, if a customer changes their address and the company only updates one table, the other two tables will still contain the old address. This can result in incorrect deliveries, billing errors and confusion. A properly designed database uses subject-based tables to reduce redundancy and maintain data accuracy and integrity.

2. Primary vs. Foreign Key Enforcement
A Foreign Key constraint acts as a guardrail by ensuring that records in one table are connected to existing records in another table. It prevents orphan records, which are records that refer to information that does not exist in the parent table. For example, a database can have a Customers table with a customer_id as its Primary Key and an Orders table with customer_id as its Foreign Key. If someone tries to insert an order using a customer_id that does not exist in the Customers table, PostgreSQL will reject the entry. This helps maintain data integrity and ensures that the relationships between tables remain correct.
