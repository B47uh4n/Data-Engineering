```sql
-- Crete an external file format for PARQUET files
CREATE EXTERNAL FILE FORMAT file_format_name
WITH(
    FORMAT_TYPE = PARQUET
    [ , DATA_COMPRESSION = {
        'org.apache.hadoop.io.compress.SnappyCodec'
      | 'org.apache.hadoop.io.compress.GzipCodec'   }
    ]);
```

```sql
-- Crete an external file format for DELIMITED TEXT files
CREATE EXTERNAL FILE FORMAT file_format_name
WITH(
    FORMAT_TYPE = DELIMITEDTEXT
    [ , DATA_COMPRESSION = 'org.apache.hadoop.io.compress.GzipCodec' ]
    [ , FORMAT_OPTIONS ( <format_options> [ ,...n ] ) ]
    );

<format_options> ::=
{
    FIELD_TERMINATOR = field_terminator
    | STRING_DELIMETER = string_delimeter
    | First_Row = integer
    | USE_TYPE_DEFAULT = { TRUE | FALSE }
    | Encoding = {'UTF8' | 'UTF16' }
    | PARSER_VERSION = { 'parser_version'}
}
```

https://www.youtube.com/watch?v=t7iLD6Cgv-I&list=PLMWaZteqtEaIZxPCw_0AO1GsqESq3hZc6&index=15&pp=iAQB
