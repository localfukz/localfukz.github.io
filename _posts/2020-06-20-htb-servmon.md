---
title: HackThebox - ServMon
author: Skofos
date: 2020-06-20 
categories: [HackTheBox]
tags: [ftp, nsclient++, directory traversal]
---


# Recon
## Nmap
```bash
# Nmap 7.80 scan initiated Sat Apr 11 22:00:41 2020 as: nmap -sC -sV -v -oA nmap/small 10.10.10.184
Increasing send delay for 10.10.10.184 from 0 to 5 due to 11 out of 35 dropped probes since last increase.
Nmap scan report for 10.10.10.184
Host is up (0.17s latency).
Not shown: 994 closed ports
PORT      STATE    SERVICE       VERSION
135/tcp   open     msrpc         Microsoft Windows RPC
139/tcp   open     netbios-ssn   Microsoft Windows netbios-ssn
6699/tcp  open     napster?
8443/tcp  open     ssl/https-alt
| http-methods: 
|_  Supported Methods: GET
| http-title: NSClient++
|_Requested resource was /index.html
| ssl-cert: Subject: commonName=localhost
| Issuer: commonName=localhost
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2020-01-14T13:24:20
| Not valid after:  2021-01-13T13:24:20
| MD5:   1d03 0c40 5b7a 0f6d d8c8 78e3 cba7 38b4
|_SHA-1: 7083 bd82 b4b0 f9c0 cc9c 5019 2f9f 9291 4694 8334
|_ssl-date: TLS randomness does not represent time
40193/tcp filtered unknown
49153/tcp filtered unknown
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_smb2-security-mode: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb2-time: ERROR: Script execution failed (use -d to debug)

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Apr 11 22:05:42 2020 -- 1 IP address (1 host up) scanned in 301.03 seconds
```
