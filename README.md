# LinuxHadoopCommand
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
