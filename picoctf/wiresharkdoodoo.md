# Wireshark doo dooo do doo

**Points:** 50
**Category:** Forensics

## Description

Locate the flag in [shark1.pcapng](./shark1.pcapng).

## Approach

Opened [shark1.pcapng](./shark1.pcapng) using [Wireshark](https://www.wireshark.org/), followed TCP stream:


Stream 5 (`tcp.stream eq 5`) revealed promising text:
> Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}

Decoded with [ROT13](https://rot13.com/)

## Flag

`picoCTF{p33kab00_1_s33_u_deadbeef}`
