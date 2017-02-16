Explain in detail:
● HDFS
● Hadoop cluster
● HDFS blocks 

HDFS
HDFS - HDFS refers to Hadoop Distributed File System, the distributed file system is one which the data is stored to different machines due to very large amount of data.
This large volume amount of data cannot be stored on single machine so distributed file system is adopted. HDFS is the flagship design of distributed file system for Hadoop.
The Definition from book Hadoop the Definitive Guide by Tom White quotes that:
“HDFS is a file system designed for storing very large files with streaming data access
Patterns, running on clusters of commodity hardware.”
Here in the definition large amount of data refers to the humungous amount of data in hundreds of terabytes. And the Streaming of the data access elaborates the idea of the most efficient file processing system i.e. Write once and read many times. Here the time required to fetch large portion of data is important than that of the real time fetching of the data, because Hadoop performs action on large part of data if not all of the data.
The commodity hardware in the definition refers to the commonly used hardware used by the mass public and which cost less than the high end machines. These machines are used in cluster to improve the processing power.
In Hadoop 2.X 
Master Daemon is called as the Name Node which is high end machine which is one in number and slave daemon is called Data node. This data nodes are many in number and they are the commodity machines which coordinate with the master daemon.


Hadoop Cluster 
Hadoop cluster consist of master daemon called as name node and Resource Manager (in Hadoop 2.X) both the master daemons are one in number.
The other machines in cluster are slave daemons these are many in number and are the commodity machines which are low in cost and are not reliable. 
Hence the many copies of the data in from of blocks are kept in more than on slave daemon so that data reliability is removed by replication of the data. 
Different slave daemons are Data node for HDFS and node manager for map reduce.


HDFS Blocks
Blocks in file system refer to the minimal size in which the data can stored and it is few kilobytes for file systems. 
These blocks are transparent to user. Similar concept applies to Hadoop it also has basic bloc of minimum size of 128MB. 
The file system of Hadoop divides the large data into small blocks of minimum size and stores them separately. 
This block size is large in order to reduce the seek cost. 
If the amount to be fetched is very large then then the number of seeks will increase. 
Also time taken for the total data to be accessed will also increase. 

