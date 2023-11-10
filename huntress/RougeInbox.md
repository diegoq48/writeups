# Rogue Inbox CTF Challenge Report

## Challenge Details

- Name: Rogue Inbox
- Points: 50
- Category: Forensics
- Solves: 538
- Difficulty: Medium  

## Challenge Description

The challenge description states:

> You've been asked to audit the Microsoft 365 activity for a recently onboarded as a customer of your MSP.

> Your new customer is afraid that Debra was compromised. We received logs exported from Purview... can you figure out what the threat actor did? It might take some clever log-fu!

## Solution Summary 

The solution involved:

- Reviewing the Microsoft 365 logs provided
- Noticing a suspicious set of inbox rules created by the user Debra
- Each rule had a one letter name which spelled out the flag when combined
- Extracting the one letter name of each rule to get the flag

By inspecting the mailbox rules created, we were able to extract the flag which was spelled out across the rule names.