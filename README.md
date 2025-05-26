# Elevate_Labs_Task1
This Repo is related to the internship Task given by elevate labs this is task 1

i used Nmap for scanning ports 

nmap -sS 10.0.2.12/24 
to find open ports 
which are 
135/tcp open msrpc
445/tcp open microsoft-ds
9080/tcp open glrpc

services running on it is mentioned above 


potential security risk in the above open ports are ?

port 135

Exploitable for remote code execution (e.g., MS03-026, used by the Blaster Worm).

Can be used for enumerating services, users, and system details.

Often targeted in Windows SMB-related attacks

port 445

Targeted in WannaCry, NotPetya, and EternalBlue attacks (based on MS17-010).

Enables unauthenticated access to shares if misconfigured.

Can allow wormable RCE (Remote Code Execution) vulnerabilities.

port 9080

Often runs web apps without HTTPS, exposing sensitive data.

May expose admin consoles vulnerable to brute force or RCE.

Default configurations may be insecure (e.g., default passwords)


nmap -sS 10.0.2.12/24 -oN scan_result.txt 

to save the file in text format 
