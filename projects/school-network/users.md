# Users, permissions, and storage

**Evidence status:** user model confirmed from original recollection.

## Storage areas

The teacher machine's hard disk was divided logically into several classes of storage:

- **System and teacher area:** read-only for ordinary student workstations.
- **Public area:** shared space where users could exchange and modify files.
- **Private area:** a separate directory belonging to each student identity.

## Identity rather than workstation

Private storage was associated with the student, not the physical XT.

At startup the system asked the user to identify themselves. If the name was unknown, the user could create a password. On later sessions, supplying the same identity and password exposed that user's private directory regardless of which workstation was used.

This made the classroom machines interchangeable while preserving personal work.

## Architectural interpretation

The persistent entity was the user. The workstation was only a temporary access point.

This distinction simplified classroom operation and anticipated a pattern now commonly described as centralised home directories or roaming user storage, although the original design arose directly from practical school requirements rather than from those later terms.
