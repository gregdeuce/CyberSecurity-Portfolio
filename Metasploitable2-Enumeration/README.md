# Metasploitable2 Service Enumeration

## Overview

This lab documents service enumeration against a deliberately vulnerable Metasploitable2 virtual machine from a Kali Linux virtual machine on an isolated lab network.

## Objective

Identify reachable TCP ports and detect the services and versions exposed by the target.

## Lab Environment

- **Attacker VM:** Kali Linux
- **Target VM:** Metasploitable2
- **Target IP:** `192.168.56.101`
- **Tool:** Nmap 7.99
- **Scan type:** TCP service/version detection (`-sV`)

> **Safety:** Metasploitable2 is intentionally vulnerable. Keep it on an isolated host-only lab network and do not expose it to the internet or an untrusted network. Only scan systems you own or are authorized to assess.

## Command Used

```bash
nmap -sV 192.168.56.101 -oN nmap-services.txt
```

This command scans common TCP ports, attempts to identify the services and versions, and saves the output in `nmap-services.txt`.

## Results Summary

- **Host status:** Up
- **Open TCP ports reported:** 23
- **Filtered TCP ports reported:** 977
- **Scan duration:** Approximately 16.55 seconds

The results below are copied from the Nmap service/version detection output. Version detection is indicative and does not, by itself, prove that a service is exploitable.

| Port | Service | Detected version / notes |
|---:|---|---|
| 21/tcp | FTP | vsftpd 2.3.4 |
| 22/tcp | SSH | OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0) |
| 23/tcp | Telnet | Linux telnetd |
| 25/tcp | SMTP | Postfix smtpd |
| 53/tcp | DNS | ISC BIND 9.4.2 |
| 80/tcp | HTTP | Apache httpd 2.2.8 ((Ubuntu) DAV/2) |
| 111/tcp | RPC | rpcbind 2 (RPC #100000) |
| 139/tcp | NetBIOS/SMB | Samba smbd 3.X–4.X (workgroup: WORKGROUP) |
| 445/tcp | SMB | Samba smbd 3.X–4.X (workgroup: WORKGROUP) |
| 512/tcp | rexec | netkit-rsh rexecd |
| 513/tcp | rlogin | OpenBSD or Solaris rlogind |
| 514/tcp | rsh | Netkit rshd |
| 1099/tcp | Java RMI | GNU Classpath grmiregistry |
| 1524/tcp | Bindshell | Metasploitable root shell (Nmap service label) |
| 2049/tcp | NFS | Versions 2–4 (RPC #100003) |
| 2121/tcp | FTP | ProFTPD 1.3.1 |
| 3306/tcp | MySQL | 5.0.51a-3ubuntu5 |
| 5432/tcp | PostgreSQL | 8.3.0–8.3.7 |
| 5900/tcp | VNC | Protocol 3.3 |
| 6000/tcp | X11 | Access denied |
| 6667/tcp | IRC | UnrealIRCd |
| 8009/tcp | AJP | Apache JServ Protocol v1.3 |
| 8180/tcp | HTTP | Apache Tomcat/Coyote JSP engine 1.1 |

## Initial Assessment

The scan identifies several legacy services and remote-access protocols that warrant further review in a controlled lab, including Telnet, rsh/rlogin, FTP, SMB, database services, VNC, and web services.

These are **enumeration findings, not confirmed vulnerabilities**.
