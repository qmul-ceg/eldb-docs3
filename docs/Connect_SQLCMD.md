# SQLCMD

The SQL Server Command Line Tool (SQLCMD utility) is a SQL utility within the Command Prompt or PowerShell, installed with SSMS and the ODBC for SQL Server driver. It is useful for managing your password on the ELDB SQL Server, as this is less easily managed in the DSN or in DBeaver.

## Check for SQLCMD

To check if SQLCMD utility is installed on your PC, open a Command Prompt or PowerShell and type:
```bash
sqlcmd -?
```
If the SQLCMD utility is installed, the version number and list of available commands will displayed.

If SQLCMD is not installed, it can be downloaded from [Microsoft](<https://docs.microsoft.com/en-us/sql/tools/sqlcmd-utility?view=sql-server-ver15>).
