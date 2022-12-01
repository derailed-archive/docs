# User
Users are Discoursy's root controllers,
they have access to most, or if not all, of
our featureset and get supreme reign over bots 

## User Structure

| field         | type      |
|---------------|-----------|
| id            | snowflake |
| username      | string    |
| discriminator | string    |
| email?        | string    |
| flags?        | integer   |
| app?          | boolean   |
| system?       | boolean   |
| verified?     | boolean   |
