# Lab 5:  Create a flow from a remote system to S3 (Raw Layer)

Assumptions: You have access to a S3 bucket

## Part 1:  Add the GetFile processor to the flow

1. Drag the "Add Process" widget to the palette
2. Filter for the "GetFile" processor
3. Click "Add"
4. Right click and click "Configure" on the newly added "GetFile" processor
5. Click "Properties"
6. Update the following properties:
  - Input Directory: /tmp/inboundToS3
7. Click on the "Settings" tab
8. Change the Name of the processor to "inboundToS3"

## Part 2: Add the S3 Processor to the flow

1. Drag the "Add Process" widget to the palette
2. Filter for "S3" and select the "PutS3Object" processor
3. Click "Add"
4. Right click and click "Configure" on the newly added "PutS3Object" processor
5. Click "Properties"
6. Update the following properties with your S3 information or use my bucket:
  - Bucket: 
  - Access Key (optional)
  - Secret Key (optional)
  - Region: 
 7. Change the Name of the processor to "StoreTOS3" and select the Failure and Success checkbox

## Part 3: Connect the GetFile and S3 Processor together

1. Drag the GetFIle Processor arrow to the S3 Processor
2. Click the "Run" button to start the entire flow
3. Observe what happens.  Fix the problem and try to run the flow 
4. Create a file in /tmp/inboundToS3 by executing the following
```
echo -e "memberID,first,last\n10000,Mack,Hendricks\n10001,Chris,Torres" > /tmp/inboundToS3/members_08102017_1.csv

```
5. Log into AWS, navigate to the S3 browser.  Your file should be there.  *** NOTICE HOW FAST IT TRANSFERS THE FILES TO S3***




