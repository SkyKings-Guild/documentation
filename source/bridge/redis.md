# Setting up Redis [Optional & Advanced]

You can use Redis Pub/Sub to control the bridge bots programmatically from an external source.

This is useful when you want to set up automation for the bridge bots without modifying the original project.

Note that most users will never use this, and we will likely not provide support to you regarding this system.

## Prerequisites
- You have a Redis server installed and running on your machine

Add the redis server's details to the config.json file, then make sure the following are set properly:
- `clientName` is set to something unique, such as your guild's name
- `recieveChannel` is set to the base channel you want to recieve messages from
    - Messages will be recieved on `{recieveChannel}:{clientName}`
- `sendChannel` is set to the channel that the controller is recieving messages on

You can then publish messages to the `{recieveChannel}:{clientName}` channel with the following format:
```json
{
    "type": "request",
    "source": "unique string identifying where the request came from, useful for multiple controllers",
    "uuid": "unique string identifying the request, so you can get a response",
    "endpoint": "'endpoint' of the bridge bot to call",
    "data": {
        "key": "value"
    }
}
```

The bridge bot will then respond with a message on the `sendChannel` with the following format:
```json
{
    "type": "response",
    "source": "clientName",
    "uuid": "same uuid as request",
    "data": {
        "success": false,
        "error": "error message, only present if success is false"
    }
}
```

If an unexpected error occurs, the bridge bot will log the error to console and respond with the following:
```json
{
    "type": "response",
    "source": "clientName",
    "uuid": "same uuid as request",
    "data": {
        "error": "details"
    }
}
```
Note the lack of a `success` key, as something internal raised an exception that wasn't supposed to.