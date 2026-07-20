# Network protocol

**Evidence status:** core structure remembered; field semantics and command table incomplete.

## Command byte

The first byte combined node addressing and command selection:

```text
7               3 2             0
+----------------+---------------+
| node address   | command       |
| 5 bits         | 3 bits        |
+----------------+---------------+
```

The five high bits identified the hardware node. Address zero was used for a general or broadcast command. The three low bits selected one of eight command codes.

A command definition determined whether an extension byte followed.

## Extension byte

For commands requiring block parameters, a second byte was divided into two nibbles:

```text
7             4 3             0
+---------------+---------------+
| chunk field   | count field   |
| 4 bits        | 4 bits        |
+---------------+---------------+
```

One field encoded chunk size and the other encoded the number of chunks. Their exact order and value mapping remain to be confirmed.

This format allowed simple operations to remain one byte long while block transfers gained compact length information only when required.

## Token ownership

Only the node holding the token could initiate read, write, or token-transfer operations.

At startup, or after apparent token loss, a node listened to the network. If no traffic arrived during the listening interval, it could broadcast an announcement equivalent to:

> Token is mine.

Nodes hearing that announcement stopped attempting to claim the medium.

After completing its work, the token holder addressed a token-transfer command to another node. The recipient confirmed ownership by announcing that it now held the token. If no confirmation arrived, the current holder attempted transfer to the next node.

This allowed inactive or failed workstations to be skipped without stopping the network.

## Reconstruction gaps

The timing rules, simultaneous-claim resolution, complete command table, acknowledgement format, error detection, and retransmission policy remain open.
