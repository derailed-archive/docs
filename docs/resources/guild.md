# Guild

Guild's are Derailed's form of letting communities interact with eachother.

## Guild Structure

| field         | type          |
|---------------|---------------|
| id            | snowflake     |
| name          | string        |
| flags         | integer       |
| owner_id      | snowflake     |
| permissions   | Permissions   |

a preview guild may also hold `available` and `approximate_presence_count`, and a gateway guild will hold an `available` field.

## Permissions Structure

| field         | type          |
|---------------|---------------|
| allow         | integer       |
| deny          | integer       |

