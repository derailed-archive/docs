# Channel

Channels are isolated, stateful, and permanently stored objects which can support being sent messages to.
Their main purpose is to allow a higher level of abilities else than a single global channel or single Guild channel like in
IRC-based chat applications.


## Channel Structure

While they aren't in the database, nor to Derailed itself, this structure separates channels by type
to make a easier reading experience.

### Common Channel

Fields put on every channel, no matter the type.

| field         | type          |
|---------------|---------------|
| id            | snowflake     |
| type          | snowflake     |

### Common Guild Channel

Fields put on every channel *inside* a Guild, no matter the type.

| field         | type          |
|---------------|---------------|
| guild_id      | snowflake     |
| parent_id!    | snowflake     |
| position      | integer       |


## Channel Types

| type          | structure                                             |
|---------------|-------------------------------------------------------|
| 0             | [Category Channel](./channel.md#common-guild-channel) |
| 1             | [Text Channel](./channel.md#common-guild-channel)     |
