# Dumpster Fire CTF Challenge Report 

## Challenge Details

- Name: Dumpster Fire
- Points: 50
- Category: Forensics  
- Solves: 969
- Difficulty: Easy

## Challenge Description

The challenge description states:

> We found all this data in the dumpster! Can you find anything interesting in here, like any cool passwords or anything? Check it out quick before the foxes get to it!

## Solution Summary

The solution involved:

- Extracting the attachments which contained a tar archive of a Firefox profile
- Mounting the Firefox profile directory 
- We open the firefox browser and inspect the saved credentials
- We find a login whose password was the flag

By mounting the Firefox profile and inspecting saved credentials, we were able to find login details that granted access the flag.