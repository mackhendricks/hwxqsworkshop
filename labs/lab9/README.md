# Lab 9: Creating a Hive Policy and Enforcing it

Goal: We will apply a security policy to the table that was created in Lab 6

1. Login into the Ranger Console: http://[management host ip]:6080
2. Locate the Hive section on the Service Manager page
3. Click the "<cluster name>_hive" link
4. Create a new policy called "raw-access"
5. Select the table that was created in Lab 6
6. Deny all access to this table except for the admin user
