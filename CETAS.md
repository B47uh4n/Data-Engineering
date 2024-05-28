# CETAS(CREATE EXTERNAL TABLE as SELECT)

### We can use CETAS in dedicated SQL pool or serverless SQL pool to complete the following tasks
- Create External Table
- Export, in parallel, the result of a Transact-SQL SELECT statement to :
   -Hadoop
   -Azure Storage Blob
   -Azure Data Lake Storage Gen2

##  EXTERNAL TABLE Yaratma Template'i
```sql
CREATE SCHEMA NYCTaxi

CREATE EXTERNAL TABLE NYCTaxiPassengersCountStats
WITH
(
   LOCATION = 'datayı tutmak istedigimiz folder path',
   DATA_SOURCE = external_data_source_name(daha once olusturdugumuz external data source),
   FILE_FORMAT = external_file_format_name(daha once olusturdugumuz external file format)
)
   AS <select_statement>
[;]

<select_statement> ::=
   [ WITH <common_table_expression>[, . . .n]]
   SELECT <select_criteria>
```

- Bu templatede gerekli kısımların girilmiş halini de yazacağım v16-dk14ten
