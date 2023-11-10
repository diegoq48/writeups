# Traffic Challenge Writeup

## Overview

This was a forensics challenge where we were given a pcap file containing network traffic. The goal was to analyze the traffic to find communication with a sketchy site and retrieve the flag. 

## Solution

To analyze the pcap file, I spun up an Ubuntu 20.04 VM and installed the rita I copied the zeek logs to the vm and generated a rita rerport 


rita ./$path_to_logs

firefox ./path_to_report


Then we opened the connected domains tab : 



This generated a report of all domains contacted in the traffic. I filtered out the most popular domains and looked for anything that looked suspicious.

Near the bottom I saw a domain called \`sketchy.github.com\` which looked suspicious. Browsing to that domain revealed the flag!

