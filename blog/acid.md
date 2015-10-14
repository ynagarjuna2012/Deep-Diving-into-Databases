


ACID
====

ACID : An acronym standing for 

 -  Atomicity,
 -  Consistency,
 -  Isolation,
 -  Durability.

 
These properties are all desirable in a database system, and are all closely tied to the notion of a transaction. The transactional features of InnoDB adhere to the ACID principles.

Transactions are atomic units of work that can be committed or rolled back. When a transaction makes multiple changes to the database, either all the changes succeed when the transaction is committed, or all the changes are undone when the transaction is rolled back.

The **database remains in a consistent state at all times** -- after each commit or rollback, and while transactions are in progress. If related data is being updated across multiple tables, queries see either all old values or all new values, not a mix of old and new values.

**Transactions are protected (isolated) from each other while they are in progress; they cannot interfere with each other or see each other's uncommitted data. This isolation is achieved through the locking mechanism.** *Experienced users can adjust the isolation level, trading off less protection in favor of increased performance and concurrency*, when they can be sure that the transactions really do not interfere with each other.

The **results of transactions are durable:** once a commit operation succeeds, the changes made by that transaction are safe from power failures, system crashes, race conditions, or other potential dangers that many non-database applications are vulnerable to. Durability typically involves writing to disk storage, with a certain amount of redundancy to protect against power failures or software crashes during write operations. (In InnoDB, the doublewrite buffer assists with durability.)


Source: [MySQl Glossary](http://dev.mysql.com/doc/refman/5.7/en/glossary.html#glos_acid)