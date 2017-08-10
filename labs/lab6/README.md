# Lab 6: Access S3 Data from HDP (Hadoop)

1. Create a user on your management node that has the same name as your user in AWS S3 by executing the following command:
```
sudo adduser [username]
```
2. Login into Ambari
3. Add the following values to HDFS
  - fs.s3a.access.key
  - fs.s3a.secret.key
4. Restart HDFS, Hive and all dependent services
5. Execute the following to test
```
su [username]
hdfs dfs -ls s3a://[your bucket name]/
```
Questions:

- How do we copy data to/from HDFS

References:

https://community.hortonworks.com/articles/25578/how-to-access-data-files-stored-in-aws-s3-buckets.html
