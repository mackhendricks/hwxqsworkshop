# Lab 6: Access S3 Data from HDP (Hadoop)

Prerequites:

1. Your AWS Admin needs to enable a policy that allows your S3 bucket to be accessed from your EC2 instance using IAM

2. You need to add the custom properties to core-site.xml within the HDFS service to enable Hadoop to leverages the IAM roles.  The property names are:
```
fs.s3a.aws.credentials.provider=com.amazonaws.auth.DefaultAWSCredentialsProviderChain
fs.s3a.endpoint=s3.us-east-2.amazonaws.com
```
The steps to implement are below:

1. Login to Ambari
2. Click the HDFS Service
3. Click "Configs" tab
4. Located the "Custom core-site.xml" drill down
5. Click "Add Custom Property".  A screenshot of adding the customer property is below:

![core-site.xml for setting up IAM for Hadoop](/images/Screen%20Shot%202017-08-10%20at%203.01.47%20PM.PNG)

6. Restart HDFS and any affected services

# Lab 6b: Access the S3 bucket

5. Execute the following to test
```
hdfs dfs -ls s3a://[your bucket name]/
```
Questions:

- How do we copy data to/from HDFS

References:

https://community.hortonworks.com/articles/25578/how-to-access-data-files-stored-in-aws-s3-buckets.html
