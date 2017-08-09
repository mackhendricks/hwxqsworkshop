# Lab1: Accessing HDFS and Hive using Ambari Views 

1. Login to Ambari
2. Click "Hive View 2.0"
3. Take note of what happens (why does this happen)
4. Try to add the admin directory by using the "File View"
5. Login to your management node and run the following commands:
```
sudo -u hdfs bash
hdfs dfs -mkdir /user/admin
hdfs dfs -chown admin:hdfs /user/admin

```
6. Click "Hive View 2.0" again
7. What happens now?  Take note of what happened and why
