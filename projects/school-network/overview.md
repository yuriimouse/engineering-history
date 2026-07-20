# Diskless school computer network

**Period:** 1989–1990 and later deployments  
**Status:** reconstruction in progress

## Problem

At the end of the 1980s, schools were receiving IBM PC/XT-class computers with 640 KB of RAM, one floppy drive, and no hard disk. Schools nevertheless needed usable computer classrooms.

Commercial networking products did not solve the central problem. They were costly, required unavailable hardware, and generally assumed more capable client machines.

The project therefore started from the available equipment rather than from an existing network product.

## System concept

One teacher machine, an XT or AT 286 with a hard disk, supplied shared storage and services. Diskless student XT machines booted a small DOS environment from floppy and loaded a custom assembly-language network driver.

The driver intercepted DOS file services through INT 21h and exposed remote storage in a form ordinary DOS applications could use without modification.

The system included:

- a custom coaxial physical network;
- compact node addressing and command encoding;
- token-based medium access with token recovery;
- remote DOS file services;
- read-only system storage;
- a public file-exchange area;
- private storage attached to user identity rather than workstation identity;
- login and first-use password creation.

## Architectural significance

The design treated the computer as a replaceable access point and the student as the persistent entity. A student could use another workstation and still receive the same private storage.

The architecture was derived from constraints:

- no local hard disks led to centralised storage;
- expensive or unsuitable network products led to a custom adapter and protocol;
- minimal adapter memory led to interrupt-driven processing with strictly bounded critical sections;
- scarce bandwidth led to bit-packed commands and optional extension bytes;
- interchangeable workstations led to user-centred private storage.

This document records the overall model. Detailed protocol, hardware, DOS, and user-management reconstruction is kept in separate files.
