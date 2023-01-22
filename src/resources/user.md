# User
Users are Derailed's root controllers,
they have access to most, or if not all, of
our featureset and get supreme reign over bots 

## User Structure

| field         | type      |
|---------------|-----------|
| id            | snowflake |
| username      | string    |
| discriminator | string    |
| email?        | string    |
| flags         | integer   |
| system        | boolean   |
| suspended     | boolean   |


## *`POST`*: /register

Creates and Registers a new user. Adds an extra `token` field with your token.

| field         | type      |
|---------------|-----------|
| username      | string    |
| email         | string    |
| password      | string    |


## *`PATCH`*: /users/@me

Creates and Registers a new user.

| field         | type              |
|---------------|-------------------|
| username      | string            |
| email         | string            |
| password      | string            |
| discriminator | integer-string    |


## *`POST`*: /login

Logs in and makes a new token for an existing account.
Adds an extra `token` field with your token.

| field         | type              |
|---------------|-------------------|
| email         | string            |
| password      | string            |
