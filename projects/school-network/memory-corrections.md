# Memory corrections

## 2026-07-21 — Serhii and adapter hardware

The electronics specialist was named **Serhii**. His surname is not currently
remembered. Yurii and Serhii worked together mainly on technical projects.

Before the school-network project, Serhii localised used printers imported from
Europe and the United States, mostly Epson models but also other brands. Yurii
wrote DVK-2 drivers that loaded character-remapping data and a graphical
Cyrillic image or font bitmap. He received 50 roubles per driver while his
student stipend was 40 roubles.

### Hardware correction

Earlier reconstruction described a serial controller plus a programmable
4-bit controller.

Current recollection replaces that model with:

- a **16550 UART**;
- a **PROM programmed by Serhii**;
- no separate programmable controller;
- no adapter buffer memory.

The PROM implemented the required hardware logic. Its exact type and internal
logic remain unknown.

The lack of buffer memory explains why the assembly-language DOS driver had to
service interrupts promptly and why critical sections were bounded in processor
clock cycles.

This correction supersedes the earlier controller description while preserving
it in Git history as part of the reconstruction process.
