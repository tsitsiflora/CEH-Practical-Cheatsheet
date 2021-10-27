# CEH-Practical-Cheatsheet
For this exam I'm writing

NMAP

Scan a single IP	            nmap 192.168.1.1
Scan a host	                    nmap www.testhostname.com
Scan a range of IPs	            nmap 192.168.1.1-20
Scan a subnet	                nmap 192.168.1.0/24
Scan targets from a text file	nmap -iL list-of-ips.txt

Scan a single Port	                nmap -p 22 192.168.1.1
Scan a range of ports	            nmap -p 1-100 192.168.1.1
Scan 100 most common ports (Fast)	nmap -F 192.168.1.1
Scan all 65535 ports	            nmap -p- 192.168.1.1

Scan using TCP connect	                nmap -sT 192.168.1.1
Scan using TCP SYN scan (default)	    nmap -sS 192.168.1.1
Scan UDP ports	                        nmap -sU -p 123,161,162 192.168.1.1
Scan selected ports - ignore discovery	nmap -Pn -F 192.168.1.1

Detect OS and Services	            nmap -A 192.168.1.1
Standard service detection	        nmap -sV 192.168.1.1
More aggressive Service Detection	nmap -sV --version-intensity 5 192.168.1.1
Lighter banner grabbing detection	nmap -sV --version-intensity 0 192.168.1.1

Save default output to file	        nmap -oN outputfile.txt 192.168.1.1
Save results as XML	                nmap -oX outputfile.xml 192.168.1.1
Save results in a format for grep	nmap -oG outputfile.txt 192.168.1.1
Save in all formats	                nmap -oA outputfile 192.168.1.1


Scan using default safe scripts	    nmap -sV -sC 192.168.1.1
Get help for a script	            nmap --script-help=ssl-heartbleed
Scan using a specific NSE script	nmap -sV -p 443 –script=ssl-heartbleed.nse 192.168.1.1
Scan with a set of scripts	        nmap -sV --script=smb* 192.168.1.1

Gather page titles from HTTP services	nmap --script=http-title 192.168.1.0/24
Get HTTP headers of web services	    nmap --script=http-headers 192.168.1.0/24
Find web apps from known paths	        nmap --script=http-enum 192.168.1.0/24


SQLMAP

