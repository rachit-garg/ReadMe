
# HDFS
## Overview of HDFS


HDFS is the distributed file system. 
> #### HDFS Components: 
>> NameNode, Secondary NameNode, DataNodes

> #### Properties Files:
>> * /etc/hadoop/conf/core-site.xml
>> * /etc/hadoop/conf/hdfs-site.xml


### HDFS Commands:
#### To view the usage:

```shell
hdfs dfs -help <command>
ex: hdfs dfs -help ls
```

#### Listing files: 

```shell
hdfs dfs -ls /dir
hdfs dfs -ls -R /dir
hdfs dfs -ls -S -r /dir
hdfs dfs -h /dir
```
#### Create and Remove Dir:
```shell
hdfs dfs -mkdir /path/dirname
hdfs dfs -mkdir -p /path/dir1/dir2

// with -p it will create the dir1 if dir1 doesn't exists

hdfs dfs -rm -R /path/dir
hdfs dfs -rmdir /path/dir

// with rmdir dir must be empty
```

#### Copying files and directories into HDFS:
```shell
hdfs dfs -copyFromLocal /path/local-dir /path/hdfs-dir

flags : -p, -f, -l 
```

#### Files and directory permission:

```shell

```


#### Getting Files and Directories from HDFS:
```shell
hdfs dfs -copyToLocal <src> <localDes>
```
#### Previewing text files in hdfs:

```shell
hdfs dfs -cat /hdfs-path/file-name
hdfs dfs -tail /hdfs-path/file-name
```

#### Size of Filesystem and data sets using df and du:
```shell

hdfs dfs -du -h /user/hive
hdfs dfs -df -h /user/hive/dataset

```

#### BlockSize and Replication
```shell

```

#### Metadata of files 
```shell
hdfs fsck
```