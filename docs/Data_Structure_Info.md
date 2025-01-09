# Database Information

All ELDB databases are primarily based on a star schema consisting of a central CORE table, containing every registered patient (1 line per
patient), linked by a patient identifier to multiple tables containing the details for patients found for specific Registers, Measures and
Activities. Additional columns and Lookup tables are provided where useful to assist with classification and categorisation.

In eldb2024 the database schema, build history and design is set out in the following tables:

***
## Tables: `db_tables`
List of all tables within the database

fieldname     | description
----------    |------------
sc            | table schema
table_name    | table name
object_id     | table id, as defined by server
create_date   | creation date of table
create_time   | creation time of table
modified_date | last modification date of table
modified_time | last modification time of table
column_count  | count of columns within table
row_count     | count of rows in table

***
## Columns: `db_columns`
List of all columns within the database

fieldname     | description
----------    |------------
sc             | table schema
table_name     | table name
object_id      | table id, as defined by server
column_id      | column id and order of column within table
column_name    | column name
datatype       | column data type
max_length     | maximum length of data within column
is_nullable    | column may contain NULLs. Yes (1) or No (0).
is_primary_key | column is included within the table's Primary Key
is_index       | column is included within a table index
column_count   | count of entries in column

***
## Codes: `db_codes`
List of codes, with counts, for each code column in the database

fieldname   | description
----------  |------------
id          | code id within the table
table_name  | table name
column_name | column name
code        | SNOMED code
code_name   | code description
code_count  | count of codes within column

See the [NHS Digital PCD Portal](<https://digital.nhs.uk/data-and-information/data-collections-and-data-sets/data-collections/quality-and-outcomes-framework-qof/quality-and-outcome-framework-qof-business-rules/primary-care-domain-reference-set-portal>) for more information on the standard codesets.

***
## Counts: `db_counts`
Patient counts by Practice for each Register and Activity table within the database.

fieldname                                 | description
----------                                |------------
area_id                                   | area id for GP Practice
ods_code                                  | ODS (Organisation Data Service) identifier for the GP Practice.
practice_name                             | GP Practice name.
clinical_system                           | clinical data system (EMIS, SystmOne) used within the GP Practice. This is based on information from CEG reporting.
*column for each register/activity table* | patient count for table by GP Practice.

***
## Routines: `db_routines`
List of all stored procedures and functions within the database. Use for build and admin.

fieldname     | description
----------    |------------
sc            | routine schema
routine_name  | routine name
object_id     | id, as defined by server
type          | routine type (P = stored procedure, FN = function, TT = table type)
create_date   | creation date
create_time   | creation time
modified_date | last modification date
modified_time | last modification time
