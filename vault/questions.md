# Open questions

These details should not be presented as confirmed until they are remembered or supported by evidence.

## Hardware and physical layer

- What exact UART or serial controller was used: 8250, 16450, 16550, or another device?
- What exact programmable 4-bit controller was used?
- What signalling method and bitrate were used on the coaxial cable?
- How were termination, collision avoidance, and electrical fault conditions handled?

## Command format

- Which nibble of the extension byte encoded chunk size, and which encoded chunk count?
- How was chunk size derived from its four-bit code?
- Did a zero nibble represent zero, one, sixteen, or a special case?
- What were the eight command codes?
- Was there a checksum or CRC?

## Token protocol

- How long did a node listen before declaring that it held the token?
- Were startup delays identical, address-dependent, randomised, or otherwise prioritised?
- How was the next node selected when token transfer failed?
- Could two nodes ever declare token ownership simultaneously, and how was that resolved?
- Was the teacher/server node treated specially?

## DOS integration

- Which INT 21h functions were intercepted?
- Did the system expose one logical drive or several?
- How were DOS file handles mapped to server-side state?
- How were directory enumeration, seek, rename, delete, and locking handled?
- Was DOS 6.22 used from the first installation, or only in a later revision?

## Users and storage

- How were usernames and passwords stored?
- Were passwords hashed, transformed, or stored directly?
- How were private directories named?
- What permissions did the teacher have over student areas?
