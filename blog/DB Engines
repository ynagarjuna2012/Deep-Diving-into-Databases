


 All About DB Engines in MySQL (MYISAM & InnoDB)
===========================================

 - **InnoDB:** The default storage engine in MySQL 5.7. 
	 - ***InnoDB is a transaction-safe (ACID compliant) storage engine for MySQL that has commit, rollback, and crash-recovery capabilities to protect user data***. 
	 
	 - ***InnoDB row-level locking (without escalation to coarser granularity locks)*** and Oracle-style consistent nonlocking reads increase multi-user concurrency and performance.
	 -  ***InnoDB stores user data in clustered indexes to reduce I/O for common queries based on primary keys.*** 
	
	 - To **maintain data integrity, InnoDB also supports FOREIGN KEY referential-integrity constraints.** For more information about InnoDB, see [ The InnoDB Storage Engine.](http://dev.mysql.com/doc/refman/5.7/en/innodb-storage-engine.htm)
	 
		 - Note : 
			 - From MySQL version 5.5 InnoDB became the default engine in order to check the engine support and default engine that your server supports use the below command  
	 
	          >`SHOW engines;`
	          
			 - By default means when we try to create the tables using the command it automatically defines InnoDB is the storage engine.
			 > `CREATE TABLE some_database_name`
			 

 
 
 - **MyISAM:** These tables have a small footprint. ***Table-level locking limits*** the performance in read/write workloads, so it is often used in read-only or read-mostly workloads in Web and data warehousing configurations.



 - **Note :**
    Contents of this documents holds true only for MySQL version of 5.7 and other version if backward / forward compatibility exists.Please feel free to check the official MySQL documentation.

 - **Sources :**
	 - Primary Resources :
		 - [CH-15 Alternative Storage Engines - MySQL Dev Center Documentation](http://dev.mysql.com/doc/refman/5.7/en/storage-engines.html)
 This page contains all the available storage engines provided by MySQL for different purposes 
		 - [InnoDB Storage Engine - MySQL Dev Center Documentation](http://dev.mysql.com/doc/refman/5.7/en/innodb-storage-engine.html)
   MySQL acquired InnoDB around 2005 to improve their services.
   
 - Outdated yet useful Information :
	 - [Which is faster InnoDB or MyISAM](http://dba.stackexchange.com/questions/17431/which-is-faster-innodb-or-myisam)
	 - [What are the main differences between InnoDB and MyISAM](http://dba.stackexchange.com/questions/1/what-are-the-main-differences-between-innodb-and-myisam) 


----------


