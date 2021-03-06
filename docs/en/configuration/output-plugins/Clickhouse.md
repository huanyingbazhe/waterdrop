## Output plugin : Clickhouse

* Author: InterestingLab
* Homepage: https://interestinglab.github.io/waterdrop
* Version: 1.0.0

### Description

Write Rows to ClickHouse via [Clickhouse-jdbc](https://github.com/yandex/clickhouse-jdbc). You need to create the corresponding table in advance.


### Options

| name | type | required | default value |
| --- | --- | --- | --- |
| [database](#database-string) | string |yes|-|
| [fields](#fields-list) | list | yes |-|
| [host](#host-string) | string | yes |-|
| [password](#password-string) | string | no |-|
| [table](#table-string) | string | yes |-|
| [username](#username-string) | string | no |-|

##### database [string]

ClickHouse database.

##### fields [list]

Field list which need to be written to ClickHouse。

##### host [string]

ClickHouse hosts, format as `hostname:port`


##### password [string]

ClickHouse password, only used when ClickHouse has authority authentication.

##### table [string]

ClickHouse table name.

##### username [string]

ClickHouse username, only used when ClickHouse has authority authentication.

### Examples

```
clickhouse {
    host = "localhost:8123"
    database = "nginx"
    table = "access_msg"
    fields = ["date", "datetime", "hostname", "http_code", "data_size", "ua", "request_time"]
}
```

