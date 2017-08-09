# Lab 2a: Importing a HIVE Table Using the Ambari Hive View

1. Login to Ambari
2. Click "Hive View 2.0"
3. Click the "New Table" Button
4. CLick the 'Upload Table" Button
5. Click the "Is first row header?" Checkbox
6. Click "Upload from Local"
7. Drag or browse to this file /sampledata/loandata.csv (it will take a few minutes to load)
8. Enter "1" for all the precision fields in the size column of the table schema definition.
9. Click "Create" (it will take a bit for your table to be created)

## Questions

- Locate the DDL that was created for this table.  
- What file format was the data stored in?
- Under the Authorization Tab you get an authorization error.  Why is this?

Lab 2b: Excuting a Query

1. Click the Query table within the "Hive View 2.0"
2. Enter the following query:
```
select * from loandata limit 10;
```
3. Execute Query (the results are at the bottom of the page)
4. Run the Query again and click "Visual Explain"
