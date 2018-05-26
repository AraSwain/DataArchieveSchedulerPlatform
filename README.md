# Data Archieve Scheduler Platform
This is a scheduler which will archive the data from transactional database to hdfs with Oozie scheduler.

**Problem Statement:**
  In our transcational database (Oracle/MySQL/Cassandra), we store all our transactional data, which is huge. So it is practically impossible to store decades of data in our database.

**Solution:**
  So we will keep only last 60 days of data in our transactional database and move the remaining data to a historical database or a distributed storage(HDFS).

**Steps Involved**
- Write a SQOOP script to move the data from MySQL/Cassandra to HDFS (or Hive).
- Make sure the SQOOP script move the data which is older than 60 days.
- Create a scheduler with Oozie to schedule the SQOOP script, which will run on a particular time of the day.
- Create a main class which will call the scheduler.

**Tools used**
- Java 8
- HDFS
- Hive
- SQOOP
- Oozie
- MySQL/Cassandra
