# Inbox

Raw recollections are collected here before they are structured.

Entries may be incomplete, contradictory, uncertain, or written in shorthand. That is expected. Do not polish them merely for style.

## School network: recollections captured on 2026-07-20

- Development began in 1989.
- The first classroom was installed around the middle of 1990.
- Client machines were IBM PC/XT systems with 640 KB of RAM, one floppy drive, and no hard disk.
- A teacher's XT or AT 286 had a hard disk and acted as the central machine.
- The physical network used coaxial cable and supported a total length of up to approximately 100 metres.
- The adapter was built from inexpensive serial hardware and a programmable 4-bit controller.
- The adapter had effectively no receive buffer. Missing an interrupt could therefore mean losing a byte.
- Critical sections in the DOS-side code were evaluated in processor clock cycles.
- The DOS driver was written in assembly language.
- The driver intercepted DOS services through INT 21h and made a remote resource appear as a hard disk.
- A command byte used five high bits for the hardware node number, with zero used as a general or broadcast address, and three low bits for the command.
- Some commands indicated that an extension byte followed.
- The extension byte was divided into two four-bit fields: one encoded chunk size, and the other encoded the number of chunks.
- Access to the shared medium was controlled by a token.
- A node initially listened to the network. If it heard nothing for a defined interval, it could announce that it held the token.
- Other nodes hearing that announcement remained passive.
- The token holder could issue read and write operations with arguments.
- The token holder could pass the token to an addressed node.
- If that node did not acknowledge ownership by announcing that it held the token, the current holder tried the next node.
- Server storage was divided conceptually into read-only system and teacher data, a public exchange area, and private user storage.
- Private storage belonged to the student identity, not to a particular computer.
- On startup the system asked who the user was.
- An unknown user could create a password.
- On later logins the same user received access to the same private directory from any workstation.
- Client boot media contained base DOS, the network driver, and several commands that appeared to users as ordinary DOS commands.
