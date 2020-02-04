# Wolvsec Bootcamp

0. [Introduction](#intro)
1. [Web Applications](#web)
2. [Reverse Engineering](#rev)
3. [Binary Exploitation](#pwn)
4. [Cryptography](#crypto)
5. [Penetration Testing](#pentest)
6. [Slides](#slides)

<h2 id="intro">Introduction</h2>

Welcome to the Wolverine Security Capture The Flag bootcamp! We hope you will enjoy attacking software and systems. This document lists the topics covered during the bootcamp. Bootcamp duration can vary from 1 week long, to 1 semester. Stay tuned for upcoming events :)

Minimum tools required for CTFs can be found on our [setup page (click here)](https://gitlab.umich.edu/wolvsec/wolvsec/blob/master/setup.md). Please install these before attending as the internet isn't always fast :(

<h2 id="web">Day 1: Web Application</h2>

* Client side: HTML, CSS, JS
* Server side: Java, PHP, Python, Ruby
* Database: SQL, Mongo, 
* HTTP Protocol
	* Application Programming Interface (API)
* Tools
	* Browser Proxies: Burp, ZAP
	* HTTP requests
* Attacks in CTFs
	* XSS / Session Hijacking
	* SQL injection
	* IDOR
	* RCE
* Advanced
	* Bypassing

<h2 id="rev">Day 2: Reverse Engineering</h2>

* File formats
* Executable formats: ELF, PE, Mach-o, APK,...
* Dynamic Loading: .so, DLL
* Disassemblers: GHIDRA
	* Setup
* Debuggers: gdb/gef, x64dbg
* Patching
	* LD_PRELOAD
	* Breakpoints: 0xcc


<h2 id="pwn">Day 3: Binary Exploitation</h2>

* Netcat
* Stack overflow
	* Stack structure
	* Stack canaries
	* ROP chains
* Format string
* Heap overflow
	* Heap structure
	* Fastbin dup
	* Use After Free
	* Off-by-one
	* Unlink
	* House of force
* Advanced
	* Integer overflow
	* IO_FILE
	* Kernel exploit


<h2 id="crypto">Day 4: Cryptography</h2>

* Base64
* Hashing
	* Merkle-Damgard
	* Length Extension
	* MD5
* Classical
	* Caeser KCA, KPA, CPAA
	* Vigenere
* Symmetric
	* XOR
	* ECB
	* CBC
* Asymmetric
	* RSA
	* Diffie-Hellman

<h2 id="pentest">Penetration Testing</h2>

* Reconnaissance
	* nmap
* Enumeration
* Exploitation
	* Metasploit, exploit-db
* Privilege Escalation
	* Linux
	* Windows
* Post Exploitation
	* CNC

<h2 id="slides">Slides</h2>

* [Introduction](https://docs.google.com/presentation/d/12VkQauDZLfSIQGquYYDbeYF_f0b3v2W3GHyO2CerVQk/edit?usp=sharing)
* [Web](https://docs.google.com/presentation/d/1-x961yuRFC-pMCxPtd-8m5LD0hP4PE4SW1DNAl9j328/edit?usp=sharing)
* [Binary Exploitation]()
* [Reverse Engineering]()
* [Bootcamp 1: Reverse Engineering](https://docs.google.com/presentation/d/1v8HuVKXxUzgs_zCXmfZ9NWypdWhVXiboLmYMHkphx-M/edit?usp=sharing)
