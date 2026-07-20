# Hardware and physical network

**Evidence status:** partly confirmed memory; component identities remain open questions.

## Confirmed recollection

A custom adapter was designed around inexpensive serial hardware and a programmable 4-bit controller. The network used coaxial cable and supported runs of up to approximately 100 metres.

The adapter had effectively no receive memory. The DOS-side interrupt handler therefore had to service incoming data before the next byte displaced it or was otherwise lost.

## Real-time consequence

The assembly code could not leave interrupts disabled for an unbounded or merely approximate duration. Critical paths were analysed instruction by instruction using known processor clock counts.

This was not general performance tuning. It was a correctness requirement imposed by the absence of buffering in the adapter.

## Open details

The exact serial controller, programmable controller, electrical signalling, bitrate, termination, and adapter circuit remain to be reconstructed.
