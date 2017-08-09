# Lab 3: Configuring YARN Capacity Scheduler to control resources

## Part 1: Validate the default queue for Hive Jobs

1. CLick Services
2. Click Hive
3. Click the "Configs" tab
4. Enter "default" in the Properties Filter Box
5. What is the name of the Default Query Queue?


## Part 2: Explicitly Specify the Queue for a Hive Query

1. Click "Hive View 2.0"
2. Click Settings
3. Enter "tez.queue.name" in the key field and enter "bi"
4. What happens?


## Part 3: Add a New Queue

1. Click on "YARN Queue Manager"
2. Add Another Queue called "bi" and give it 20% and reduce the default queue to 80%
3. Save and Restart the Resource Manager
4. Go back to Part 2


## Questions:

1. How do you validate that your queries were submited using the "bi" queue?

    Hint: Jobs tab and click Action

2. How do you actual see the jobs 
