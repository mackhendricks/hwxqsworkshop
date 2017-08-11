# Lab 7: Installing Ranger

Goal: To understand how to install Ranger and to get experience with installing new HDP services in general

Prerequisites:

1. ssh to your management node (aka node with Ambari)
2. execute the following  commands:
```
sudo mysql -e "grant all privileges on *.* to 'super'@'%' identified by 'welCome123' with grant option;"
sudo mysql -e "grant all privileges on *.* to 'super'@'localhost' identified by 'welCome123' with grant option;"
sudo mysql -e "flush privileges;"
sudo useradd biuser
sudo echo welCome123 | sudo passwd --stdin biuser # This user will be used later
sudo groupadd bigroup
```

Part A: Adding the Ranger Service

1. Login to Ambari
2. Click Actions (bottom left)
3. Select "Add Service"
4. Select "Ranger" and "Ranger KMS"
5. Select "I have met all the requirements above" and click "Proceed"

Question:

- What database will the ranger policies reside?

6. Assign Masters Page: Make sure Ranger is located on the same server as Ambari.  Otherwise, move Ranger to that server.  Click "Next" 
7. Assign Slaves and Clients: Take the defaults and click "Next"
8. Customize Services:
-Ranger
  - Ranger Admin Tab:
    - Ranger DB Host: internal DNS name of your Ambari server
    - Ranger DB password: welCome123
    - Database Administrator (DBA) username: super
    - Database Administrator (DBA) password: welCome123
  - Ranger Audit Tab:
    - Disable Audit to Solr
-Ranger KMS 
  - Ranger KMS DB host: internal DNS name of your Ambari server
  - Ranger KMS DB password: welCome123
  - Database Administrator (DBA) username: super
  - Database Administrator (DBA) password: welCome123
  - KMS Master Secret Password: welCome123

Click "Next"
Dependent Configuration Changes: Click "OK" to accept all the changes 
9. Review: Click "Deploy" to start the install
 
 
 Part B: Logging into the Ranger Console
 
 1. Open up a Web Browser and navigate to http://[management_node_ip]:6080/
 2. Bookmark this URL.  You will need it for the next labs
 3. The username and password is admin/admin
 
 Part C: Enabling Ranger Plug-in for HDFS and Hive
 
 1. Login into Ambari
 2. Click Ranger
 3. Click Configs
 4. Click "Ranger Plugin" tab
 5. Enable the "HDFS Ranger" and "Hive Ranger" Plugin
 6. Click Save
 7. Click "OK" to accept all Dependent Configurations
 8. Restart all required components
  
 
 
 
 

