# Rock, Paper, Psychic Challenge Report

## Challenge Details

- Name: Rock, Paper, Psychic
- Points: 50  
- Category: Miscellaneous
- Solves: 368
- Difficulty: Medium

## Challenge Description  

The challenge involves playing rock paper scissors against a "psychic" computer that seems to read your mind.

## Solution Summary

The solution involved:

- Downloading the binary file 
- Opening it in Ghidra to analyze the code
- Identifying the check that prints the fail message string
- Noticing the check branches based on a JZ (jump if zero) instruction
- Modifying the binary in a hex editor, changing JZ to JNZ (jump if not zero)
- Running the modified binary to always pass the check and get the flag

By reverse engineering the binary, we identified the key check to bypass and modified the code to print the flag. 
