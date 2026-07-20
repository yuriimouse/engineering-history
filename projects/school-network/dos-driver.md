# DOS driver

**Implementation:** assembly language  
**Primary interface:** DOS INT 21h  
**Evidence status:** architectural mechanism confirmed; intercepted function list incomplete.

## Purpose

Client machines had no hard disk. They booted base DOS and the custom driver from floppy.

The driver intercepted DOS file-service requests through INT 21h and redirected relevant operations through the network to the teacher/server machine. To DOS applications, the remote resource appeared to behave like ordinary disk storage.

Using the DOS service layer avoided requiring application changes and allowed the implementation to work with file and directory semantics rather than emulate a physical disk controller at the BIOS sector level.

## Interrupt constraint

The network adapter had no meaningful buffering. An incoming byte caused an interrupt that could not safely be missed.

Accordingly, assembly-language critical sections were bounded using instruction clock counts. Interrupts could not remain disabled merely until a convenient high-level operation completed.

## Boot environment

The floppy contained:

- base DOS;
- the network driver;
- several additional utilities presented as ordinary DOS commands.

The exact DOS version used in the first 1990 installation remains uncertain. DOS 6.22 may describe a later operational version rather than the original deployment.
