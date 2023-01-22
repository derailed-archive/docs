# Guild

Guilds are Derailed's form of letting communities interact with eachother.

## Guild Structure

| field         | type          |
|---------------|---------------|
| id            | snowflake     |
| name          | string        |
| flags         | integer       |
| owner_id      | snowflake     |
| permissions   | bit int       |

a preview guild may also hold `available` and `approximate_presence_count`, and a gateway guild will hold an `available` field.

## Member Structure

| field         | type          |
|---------------|---------------|
| user_id       | snowflake     |
| guild_id      | snowflake     |
| nick!         | string        |


## *`POST`*: `/guilds`

Creates a Guild, and returns [its object](./guild.md#guild-structure).

| field         | type          |
|---------------|---------------|
| name          | string        |


## *`PATCH`*: `/guilds/:guild_id`

Modifies a Guild, and returns the new [object](./guild.md#guild-structure)

| field         | type          |
|---------------|---------------|
| name          | string        |


## *`GET`*: `/guilds/:guild_id`

Gets a Guild, and returns [its object](./guild.md#guild-structure).
Requires you to be a member of that Guild.


## *`GET`*: `/guilds/:guild_id/preview`

Gets the Guild, and returns its [its preview](./guild.md#guild-structure).

