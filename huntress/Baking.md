# Baking CTF Challenge Report

## Challenge Details

- Name: Baking
- Points: 50 
- Category: Warmups
- Solves: 1105
- Difficulty: Easy

## Challenge Description

The challenge description states:

> Do you know how to make cookies? How about HTTP flavored?  
Press the Start button in the top-right to begin this challenge.

## Solution Summary

The solution involved:

- Inspecting the cookies set by the website in the browser
- Noticing the cookie was Base64 encoded
- Decoding the cookie which contained a timestamp of when the cookies started "baking"  
- Modifying the timestamp to be 120 hours ago so the cookies would be finished baking
- Encoding the new timestamp as Base64 and setting it as the cookie value
- Reloading the page caused the website to see the cookie was done baking and give the flag

By decoding the cookie timestamp and manipulating it, we were able to trick the website into thinking enough time had passed for the cookies to be finished baking, resulting in the flag being awarded.

