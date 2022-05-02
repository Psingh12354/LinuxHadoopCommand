# LinuxHadoopCommand

```
Hadoop BigData Ubuntu  

Contents 
Users 

Ubuntu  

user:- ubh01  

Password :- root  

Mysql  

User:- root  

Password:- password  

User:- sqoop  

Password:- password  

 

 

### Command 

 

To start hdfs service  

$HADOOP_HOME/sbin/start-dfs.sh 

To stop hdfs service  

$HADOOP_HOME/sbin/stop-dfs.sh 

To start yarn service  

$HADOOP_HOME/sbin/start-yarn.sh 

To stop yarn service  

$HADOOP_HOME/sbin/stop-dfs.sh 

To start hbase service  

$HBASE_HOME/bin/start-hbase.sh 

To stop hbaseservice  

$HBASE_HOME/bin/stop-hbase.sh 

 

 

How to Start a Shell or Use a service 

Hive  

hive 

Scala  

scala 

Python  

python 

Spark scala  

spark-shell  

Pyspark  

pyspark 

Hbase  

Hbase shell 

Mysql  

Sudo mysql -u sqoop -p 

Sqoop  

sqoop -version  

Service verifications  

 

To check if hdfs service are running or not  

sudo jps  

output  

datanode 

namenode 

resourcemanager  

 

Java  

Java --version 

Scala 

Scala --version 

Python  

python & then hit enter verify version and hit CTRL+D 

 

```


```
Hadoop File System Commands

Syntax Overview

The basic syntax of HDFS commands is as follows:

$ hadoop fs -command [extra arguments]
For example:

$ hadoop fs -ls
The first part “hadoop fs” is always the same for file system related commands. After that is very much like typical Unix/Linux commands in syntax. Besides managing the HDFS itself, there are commands to import data files from local file system to HDFS, and export data files from HDFS to local file system. These commands are unique therefore deserve most attention.

[-put ... ]
[-copyFromLocal ... ]
[-moveFromLocal ... ]
[-get [-ignoreCrc] [-crc] ]
[-getmerge [addnl]]
[-copyToLocal [-ignoreCrc] [-crc] ]
[-moveToLocal [-crc] ]
A Typical Use Case

When using Hadoop, you need to move your data to a HDFS before processing it, and optionally move the result back to your local file system. Here is a typical flow:

$ hadoop fs -mkdir test
$ hadoop fs -put input.txt test/input.txt
$ hadoop fs -ls test
$ hadoop fs -cat test/input.txt
$ hadoop jar mr.jar WordCount test/input.txt test/output
$ hadoop fs -ls test/output
$ hadoop fs -lss test
$ hadoop fs -get test/output .


Other Useful Commands

$ hadoop fs -chmod 777 test/input.txt
$ hadoop fs -cp test/input.txt test/input1.txt
$ hadoop fs -cp test/input.txt test/input1.txt
$ hadoop fs -rmr test

Space use in bytes for individual files or directories
$ hadoop fs -du

Space used in bytes in summary, therefore only one entry is given
$ hadoop fs -dus
$ hadoop fs -count /test

Getting Help
$hadoop fs -help
```
