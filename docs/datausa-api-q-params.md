
| **parameter**         | **accepted values**                                                             | **description**                                                                                                                                                                                     |
| -------------         | -------------                                                                   | -------------                                                                                                                                                                                       |
| `force`               | `schema_name.table_name` (Example)                                              | Forces the use of a particular data table.                                                                                                                                                          |
| `limit`               | integer                                                                         | Limits the number of rows returned by the query.                                                                                                                                                    |
| `order`               | any available column name                                                       | Column name to use for ordering the resulting data array.                                                                                                                                           |
| `show (required)`     | any available attribute                                                         | A comma-separated list of attributes to show in the query.                                                                                                                                          |
| `sort`                | `desc` or `asc`                                                                 | Changes the sort order of the returned data array.                                                                                                                                                  |
| `sumlevel (required)` | any available sumlevel for the given attribute                                  | This restricts the data fetched to only display the specified sumlevel(s). If more than one "show" attribute is specified, sumlevel must be a comma-separated list with a value for each attribute. |
| `required`            | any available column name                                                       | A comma-separated list of column names to be returned in the query.                                                                                                                                 |
| `where`               | [see documentation](https://github.com/DataUSA/datausa-api/wiki/Data-API#where) | Advanced filtering of columns, similar to the WHERE clause on SQL.                                                                                                                                  |
| `year`                | `latest`, `oldest`, `all`, 4-digit year                                         | Filters the returned data to the given year.                                                                                                                                                        |

