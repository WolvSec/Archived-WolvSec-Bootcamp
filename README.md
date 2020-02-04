# Wolvsec Bootcamp

1. [Web Applications](#web)
2. [Reverse Engineering](#rev)
3. [Binary Exploitation](#pwn)
4. [Cryptography](#crypto)
5. [Penetration Testing](pentest)

<h2 id="web">Web Application</h2>

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

<h2 id="rev">Reverse Engineering</h2>

* File formats
* Executable formats: ELF, PE, Mach-o, APK,...
* Dynamic Loading: .so, DLL
* Disassemblers: GHIDRA
	* Setup
* Debuggers: gdb/gef, x64dbg
* Patching
	* LD_PRELOAD
	* Breakpoints: 0xcc


<h2 id="pwn">Binary Exploitation</h2>

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


<h2 id="crypto">Cryptography</h2>

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
