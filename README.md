# Luna Addon Protocol
This repository contains information regarding the Luna Addon communication protocol.

Protocol Version: 1

## Table of contents
- [Receive Messages](#receive-messages) (server->client)
  - [init](#rm-init)
  - [mutate](#rm-mutate)
- [Send Messages](#send-messages) (client->server)
  - [init](#sm-init)
  
# <a id="receive-messages">Receive messages</a>
### <a id="rm-init">"init"</a>
Occurs when the client initially joins the server.

| Id   | Type        | Name               | Description
| ---  | ---         | ----               | -----------
| `0`  | `Integer`   | Version            | The server addon protocol version.

### <a id="rm-mutate">"mutate"</a>
Occurs when the server demands a client-sided map gfx mutation.

| Id   | Type        | Name               | Description
| ---  | ---         | ----               | -----------
| `0`  | `Integer`   | Type               | The mutation id.  *See [Mutations](#model-mutations).*
} `1`  | `Integer`   | X                  | The map x coordinate to mutate.
} `2`  | `Integer`   | Y                  | The map y coordinate to mutate.
} `3`  | `Integer`   | Id                  | The gfx id.

# <a id="send-messages">Send messages</a>

### <a id="sm-init">"init"</a>
Sent to request the initialization message.

| Id   | Type        | Name               | Description
| ---  | ---         | ----               | -----------
| `0`  | `Integer`   | Version            | The client addon protocol version.

# <a id="models">Models</a>

### <a id="model-mutations">Mutation Types</a>

| Value | Name
| ----- | ----
| `0`   | Ground
| `1`   | Object
