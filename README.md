# Cybersecurity-practice-labs
Hands-on cybersecurity projects and practical lab documentation
#  Nmap Lab 01: TCP Port Scanning

1. Project Overview

    This project demonstrates basic TCP port scanning using Nmap on a local Kali Linux environment.
    The objective is to understand TCP port states, identify listening services, and document scan results.

2.  Lab Environment

	•	Operating System: Kali Linux
	•	Virtualization: VirtualBox
	•	Tool: Nmap
	•	Target: Local Kali Linux machine
	•	Testing Scope: Authorized local testing

3.  Objective
   The objectives of this exercise are to:

	  1.	Perform a TCP port scan.
	  2.	Identify open and closed ports.
  	3.	Understand the meaning of filtered ports.
  	4.	Practise basic service detection.
	  5.	Document findings professionally.

4.  Initial Scan Results


     Port     |    Service          |                  State

     22/TCP	    |    SSH	           |                 Closed

     80/TCP	    |    HTTP	           |                 Closed

     443/TCP     |    HTTPS	           |                Closed
  
     631/TCP    	|   IPP	            |                Closed


     Interpretation

      The scan identified the four listed TCP ports as closed.

      A closed port indicates that the target responded to the scan but no application was accepting TCP connections on that port at the time of testing.

      The results do not establish whether other ports are open.

5.   Commands Used

      Scan selected TCP ports:

      sudo nmap -sT -p 22,80,443,631 127.0.0.1

      Scan the first 1,000 TCP ports:

      sudo nmap -sT -p 1-1000 127.0.0.1

      Detect services on selected ports:

      sudo nmap -sV -p 22,80,443,631 127.0.0.1

 6.  Key Findings

      •	Nmap can identify TCP port states.

      •	Closed ports do not necessarily indicate that a host is offline.

      •	Service detection attempts to identify applications associated with accessible ports.

     	•	Results can differ depending on the target address, network path, and filtering configuration.

 7.  Lessons Learned

      This exercise provided practical experience with TCP port scanning, port-state interpretation, and basic service detection.

      Further testing will investigate the differences between loopback and virtual-machine network-interface scan results.

 8.   Authorization
     
All scans in this project are intended for systems owned by the learner or systems for which explicit authorization has been granted.
 
 
 ## 9. Scan Evidence
 The screenshot below shows the results of my Nmap TCP port scanning exercise.
 ![Nmap Scan Results] (Screenshot_2026-10-09_at_15.43.59.png)
