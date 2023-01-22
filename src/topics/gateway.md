# Gateway

The Gateway is Derailed's form of implementing real-time communication via websockets.

## Hello (Server)

Once you've made a connection to the Gateway, it should send:

```json
{
    "op": 2,
    "d": {
        "heartbeat_interval": 45000
    },
    "s": 0
}
```

While currently `heartbeat_interval` is static, we suggest using it so in the future your lib will be safe.

`heartbeat_interval` is based in milliseconds.

## Heartbeating (Client/Server)

To keep your connection with Derailed going, just send:

```json
{
    "op": 0,
    "d": 0
}
```

with `d` being the last sequence, or `s` payload, sent to the client.

In response the client will be sent something like:

```json
{
    "op": 3,
    "d": 0
}
```

This does **reset the sequence to zero.**

## Identify (Client)

Identifying is not too hard, and only requires one field.

Just simply:

```json
{
    "op": 1,
    "d": {
        "token": "token"
    }
}
```

## Ready (Server)

In response to an Identify request, the server will give you an info showing you're
ready to progress:

```json
{
    "op": 4,
    "d": {
        "session_id": "abcdef",
        "user": {...},
        "settings": {...},
        "unavailable_guilds": []
    }
}
```

`session_id` is the id given to your session internally.

`user` is, as the name says, your user object.

`unavailable_guilds` a list of guild ids which you were previously in.

`settings` a user settings object.

## Event (Server)

Sent when an event happens.
Structured like:

```json
{
    "op": 0,
    "t": "EVENT_NAME",
    "d": {...},
    "s": 0
}
```

with `d` being the event data and `s` being your new sequence.
