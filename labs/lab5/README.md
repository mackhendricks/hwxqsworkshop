# Lab 5:  Create a flow from a remote system to S3 (Raw Layer)

Assumptions: You have access to a S3 bucket

## Part 1:  Add the GetFile processor to the flow

1. Drag the "Add Process" widget to the palette
2. Filter for the "GetFile" processor
3. Click "Add"
4. Double click on the newly added "GetFile" processor
5. Click "Properties"
6. Update the following properties:
  - Input Directory: /tmp/inboundToS3
7. Click on the "Settings" tab
8. Change the Name of the processor to "inboundToS3"

## Part 2: Add the S3 Processor to the flow

1. Drag the "Add Process" widget to the palette
2. Filter for "S3" and select the "PutS3Object" processor
3. Click "Add"
4. Double click on the newly added "PutS3Object" processor
5. Click "Properties"
6. Update the following properties:
  - 


## Part 3: Connect the GetFile and S3 Processor together
