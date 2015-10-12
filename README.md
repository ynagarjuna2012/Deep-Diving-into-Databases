##Deep Diving into **Advanced Database Management** 

*Courses / Resources*:

 - UC Berkeley -CS186
 - Stanford University -Intro to Relational Databases 
 - Other Youtube Misc'
 - *Books :*
	 -  Database Systems - Elmasri,Navathe
 - Online References :
	 - [A Quick-Start Tutorial on Relational Database Design](http://www3.ntu.edu.sg/home/ehchua/programming/sql/relational_database_design.html)
 - Datasets - MySQL Dumps :
	 - [Reference Database  Source Blog Article](https://www.percona.com/blog/2011/02/01/sample-datasets-for-benchmarking-and-testing/)
		 - [A sample MySQL database with an integrated test suite by Unity](https://github.com/datacharmer/test_db)
		 - [BIRT Sample Data on Eclipse Website ](http://www.eclipse.org/birt/documentation/sample-database.php)
		 - [IMDB File Data](http://www.imdb.com/interfaces)
		 - [MySQL Dev Resources](http://dev.mysql.com/doc/index-other.html)
		 - [North Wind - MySQL](https://github.com/dalers/mywind) - MySQL Version. Original Version is provided my Microsoft to work with SQL Server 2005 & 2008. An Excellent resource of an sample database to learn how to optimize queries along with conceptual stimulation with real backup data seeded into the database.
	
 - [Database Model Sample References](http://www.databaseanswers.org/data_models/index.htm)

###Using XAMPP on windows 

other alternatives being existed in order to avoid the the  confusion I prefer using XAMPP. Feel free to use any database installation (Postgres,SQLite) or MySQL workbench installation.

Since XAMPP is self contained independent installation we cannot run it directly in command prompt by 

    >  mysql
   > Throws Error : 
   > C:\Users\UserName>mysql
       'mysql' is not recognized as an internal or external command,
	    operable program or batch file.

This is mainly because MySQL executable is not in our system path which comes with XAMPP installation as I mentioned is an independent environment which is entirely isolated with your System Variable 
>(Don't worry about system variables and System Paths.) Those are merely not useful as of now 

###How to start using MySQL installation then ?
Well there is an easy way on Windows every program need to have an executable file in order to use. So lets find where the MySQL's executable resides which came with the XAMPP installation.  

> In the below mentioned you can find mysql binary executable 
> Note : For every program you encounter problem you will have to find the executable files ending with .exe in order run it.On windows normally all the programs resides in `c:/Program Files/` 
> >`c:/xampp/mysql/bin/`
>  
>  Now 
>> `mysql -u root` 
>
> Here 2 things need to keep in mind is that you may get the error as shown below 
> >`ERROR 2003 (HY000): Can't connect to MySQL server on 'localhost' (10061)`
> 
> This is mainly because with normal MySQL installation `mysqld.exe` will run automatically but here while using XAMPP we need to manually start it A simple way of doing it is by just following the below steps

 > 1. Open XAMPP Control Panel
 > 2. Press ***START***  button 
 > 
 > and then run 
 >> `mysql -u root
 > `Since where -u means *usename*  and root is the name of user or username
 > Some may suggest doing running 
 > `mysql -u root -p`

 > Since XAMPP MySQL default installation don't come with any password.
 > after that you may see something similar in your command prompt which confirms you are in a track.
 > > Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 1
Server version: 5.6.21 MySQL Community Server (GPL)
Copyright (c) 2000, 2014, Oracle and/or its affiliates. All rights reserved.
Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.
Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

#### Listing out databases on your server or Checking how many databases exists on the server.
>This is a simple command which show all the databases that are on your server.
>>`show databases;`
>*Note: Semi Colon " ;  " is necessary in order to get the results otherwise it may results in weird behavior if you encounter such situation shown below just enter ; and press enter*
>
>This will splits out a result similar to shown below.
>> mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| cdcol              |
| mysql              |
| performance_schema |
| phpmyadmin         |
+--------------------+
7 rows in set (0.06 sec)

#### How to check how many relations (Tables) exists in a database ?
> First we need to use a database or change our reference to a database in which we need to see the relations(tables). This can be achieved by simply using the below commands. 
>> `use "databasename" --> generalized representation` 
>
>> Usage :
>**`use mysql`**
> `mysql` is the name of the database
> 
> Below command shows the tables in a database.
>> `show tables`
>
> Above command splits out a result similar as shown below 
> >+---------------------------+
| Tables_in_mysql           |
+---------------------------+
| columns_priv              |
| db                        |
| event                     |
| func                      |
| general_log               |
| help_category             |
| help_keyword              |
| help_relation             |
| help_topic                |
| innodb_index_stats        |
| innodb_table_stats        |
| ndb_binlog_index          |
| plugin                    |
| proc                      |
| procs_priv                |
| proxies_priv              |
| servers                   |
| slave_master_info         |
| slave_relay_log_info      |
| slave_worker_info         |
| slow_log                  |
| tables_priv               |
| time_zone                 |
| time_zone_leap_second     |
| time_zone_name            |
| time_zone_transition      |
| time_zone_transition_type |
| user                      |
+---------------------------+
28 rows in set (0.03 sec)




