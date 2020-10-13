# Luna Addon Protocol
This repository contains information regarding the Luna Addon communication protocol.

Protocol Version: 1

## Table of contents
- [Receive Messages](#receive-messages)
  - [init](#rm-init)
- [Send Messages](#send-messages)
  - [init](#sm-init)
  
# <a id="receive-messages">Receive messages</a>
### <a id="rm-init">"init"</a>
Occurs when the client initially joins the server.

| Id   | Type        | Name               | Description
| ---  | ---         | ----               | -----------
| `0`  | `Integer`   | Version            | The server addon protocol version.

# <a id="send-messages">Send messages</a>

### <a id="sm-init">"init"</a>
Sent to request the initialization message.

| Id   | Type        | Name               | Description
| ---  | ---         | ----               | -----------
| `0`  | `Integer`   | Version            | The client addon protocol version.
