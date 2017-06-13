# Kontainer.ooo Communication
In this repository we define the communication between single parts of the kontainer.ooo platform.

## Message Definition
The messages for the particular services are in the `messages/` folder denoted by `serviceName.proto`.

## Protocol Definition 
The commands which can be used in the websocket communication are being tracked in the `protocol.json`. The format of this file is:

```javascript
{
  "Service Name": { // eg. 'user'
    "id": "ProtocolID",
    "methods": {
      "Method Name": "ProtocolID", // eg. "GetUser": "USR"
    }
  },
}
```

The *Service Name* is the key to an object which holds the *id* of this service and its *methods*. The *id* is the key to a **ProtocolID** (3 character string). *Methods* is the key to another object which stores function names and their **ProtocolIDs**.
