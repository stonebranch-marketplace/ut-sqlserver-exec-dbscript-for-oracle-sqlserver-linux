# ut-sqlserver-exec-dbscript-for-oracle-sqlserver-linux
The Universal Task allows to execute an oracle PLSQL block or an SQLServer T-sql statement. It uses an agentless connection via ODBC
towards SQLServer and the oracle basic instant client to connect to an Oracle database.

# Abstract: 

This Universal Task allows to execute an oracle PLSQL block or an SQLSERVER T-sql statement. It uses an agentless connection via ODBC
towards SQLSERVER and the oracle basic instant client to connect to an Oracle database.

# 1	Disclaimer

No support and no warranty are provided by Stonebranch GmbH for this document and the related Universal Task. The use of this document and
the related Universal Task is on your own risk.
Before using this task in a production system, please perform extensive testing.
Stonebranch GmbH assumes no liability for damage caused by the performance of the Universal Tasks

# 2	Introduction

The here described Universal Task allows to execute an oracle PLSQL block or an SQLSERVER T-sql statement. It uses an agentless connection 
via ODBC towards SQLSERVER and the oracle basic instant client to connect to an Oracle database. The connection and execution of the sql 
statements is performed using the python cx_oracle and pyodbc modules. 
Some details about the universal task to monitor a value in a database column

- The Universal Task supports SQLSERVER & Oracle
- MySql and PostgreSQL can be added in the future
- The Universal Task supports both Universal Agent for Linux/Unix and Windows
- You can select different log-levels e.g. Info and debug
- You can execute oracle PLSQL blocks and SQLSERVER T-SQL statements
-	You can decide if the sql-output is provided in the standard out or not
- All Passwords are encrypted using Controller Credentials

# 3	Installation
# 3.1	Software Requirements for Windows Agent

**Universal Template name: UT_EXEC_DBSCRPT_FOR_ORACLE_SQLSERVER**

Related UAC XML Files for template and task: [1]

Requirements to remotely connect from a Windows agent to an Oracle and/or SQLSERVER: 
-	Python 3.7.0-amd64 installed on a windows server where a Universal Agent is installed. 
-	For Python the following modules are required: 
      -	sys, for output re-direct processing
      -	datetime, date and time stamps for messages
      -	pyodbc to perform the ODBC connection
      -	cx_Oracle – Oracle DB support
      -	logging, for python loglevel support
-	Universal Controller V6.4.7.0 or higher
-	Universal Agent V6.4.2.2 or higher installed on a Windows Server
-	Microsoft ODBC driver V17 installed on the Windows SQLSERVER
-	The Windows Server needs to have Visual Studio VS 2013 installed.
-	The Windows Server needs to have oracle instant client Version 18.3.0.0.0 installed. 

# 3.2	Software Requirements for Linux Agent

Will be provided at a later stage

