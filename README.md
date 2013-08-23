tinyupload
==========

Type: Executable


Description


The executable that uploads jBASE raw data and exploded data to SQL Server.

 If a SQL Model string is passed as the 8th argument, the process will attempt to convert the data to the SQL datatype defined by the model.

 If the conversion results in an error (i.e. attempting to convert a letter to a number), the result will be a SQL "NULL" value. If the datatype was defined as a string but exceeded the column length, the string would be truncated before uploading.

 Because of runtime datatype checking described above, the process ensures that all rows will be uploaded to SQL Server.  
 


Arguments:


Position 

Description

0 A valid SQL Server connection string. 
1 The schema name for the destination table. 
2 The name of the destination table. 
3 A valid Windows path. 
4 The name of the file to be uploaded. 
5 The number of columns to the destination table. 
6 The file size in bytes. 
7 The SQL Model if available, a pipe "|" delimited array represented as a string. 

At the command prompt or batch file, run the following for exploded data (for troubleshooting only):

![Alt text](http://eztier.com/documentation/t24/jbase-sql-etl/images/args/tinyupload2.png)
 

