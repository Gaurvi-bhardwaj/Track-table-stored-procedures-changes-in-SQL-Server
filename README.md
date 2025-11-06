# Track-table-stored-procedures-changes-in-SQL-Server
To track changes in tables and stored procedures in sql server
can be done by : 
1. Redgate software
2. cloud
3. using Stored Procedures or triggers

I have created Stored procedure for tracking table changes (table created/dropped, column added/dropped, data type change, nullability change)
and trigger to detect changes in stored procedures(create/alter/drop) who made that change at what time and what exact change.


Run following queries to get results :

1. for table changes:
   
   select * from [dbo].[SchemaChangeLog]  
   order by LogID desc;


3. for stored procedure changes :
   
   SELECT *
   FROM dbo.Log_StoredProcedureVersion
   ORDER BY ChangedDateTime DESC;


   



