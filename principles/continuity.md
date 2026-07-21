# Continuity

## Source

[Yurii]

> Завтра мене трамвай переїде, а котик залишиться голодний і наступник не зможе зробити патч.

## Editorial interpretation

This is an engineering principle rather than black humour.

**A system should not depend on one irreplaceable person.**

Documentation, Git history, architecture notes and reconstruction journals exist
so another engineer can continue the work.

This principle appears repeatedly in Yurii's work:

- preserve project history in Git;
- document architecture, not only code;
- separate sources from interpretation;
- make projects understandable by a successor;
- treat the repository as the durable memory of the project.

The repository itself should survive the loss of any participant.
