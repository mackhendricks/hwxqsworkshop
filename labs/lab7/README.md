# Lab 7: Installing Ranger

Goal: To understand how to install Ranger and to get experience with installing new HDP services in general

Prequites:

1. ssh to your management node (aka node with Ambari)
2. execute the following  commands:
```
sudo grant all privileges on *.* to 'super'@'%' identified by 'welCome123' with grant option;
sudo useradd biuser
sudo echo welCome123 | passwd biuser # This user will be used later
sudo groupadd bigroup
```


1. Login to Ambari
2. Click Actions (bottom left)
3. Select "Add Service"
4. Select "Ranger" and "Ranger KMS"
5. Select "I have met all the requirements above" and click "Proceed"

Question:

- What database will the ranger policies reside?

6. Assign Masters Page: Make sure Ranger is located on the same server as Ambari.  Otherwise, move Ranger to that server.  Click "Next" 
7. Assign Slaves and Clients: Take the defaults and click "Next"
8: Customize Services:
- Ranger Admin Tab:
  - Ranger DB Host: internal DNS name of your Ambari server
  - Ranger DB password: welCome123
  - Database Administrator (DBA) username: super
  - Database Administrator (DBA) password: welCome123
- Ranger Audit Tab:
 - Disable Audit to Solr
 

