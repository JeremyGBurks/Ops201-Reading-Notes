## Windows Command Line Tools / What is an SMB Port? A Detailed Description of Ports 445 + 139 

### Summary
Server Message Block Protocol (SMB Protocol) is a client-server communication protocol. It is used for sharing access to files, printers, serial ports, and data on a network. It is a way for computers to talk to one another. This reading covers how SMB protocol works, what the SMB Protocol Dialects are, description of ports 445 and 139, and finally if open ports are dangerous. 


### How does it work?
The client makes a certain requests and the server responds. Once connected it enables users or apps to make requests to a file server and access resources. User of the app can open/read/move/create/update files on remote server.

Originally designed by Barry F. at IBM in 1983

### What are the SMB Protocol Dialects?
* SMB 1.0 (1984): Created by IBM for file sharing in DOS. Introduced opportunistic locking as a client-side caching mechanism for reduced network traffic.
* Samba (1992): Open-source implementation of SMB Protocol
* CIFS (1996): Microsoft-developed SMB dialect debuted in Windows 95. Added support for larger file sizes, transport directly over TCP/IP, symbiotic links, and hard links.
* NQ (1998): Family of portable SMB client and server implementations developed by Visuality Systems. It is portable to non-Windows systems such as Linux, iOS, and Android supports SMB 3.1.1 dialect.
* Netsmb (2004): Family of in-kernel SMB implementations in BSD operating systems.
SMB 2.0 (2006): Released with Windows Vista and Windows Server 2008. Reduced chattiness to improve performance, enhance scalability and resiliency. Added support for WAN acceleration.
* Tuxera SMB (2009): Proprietary SMB implementation runs in kernel or user-space.
* Likewise (2009): Likewise developed a CIFS/SMB implementation that provided a multiprotocol, identity-aware platform for network access to files in OEM storage built on Linux/Unix based platforms. 
* SMB 2.1 (2010): Introduced with Windows Server 2008 R2 and Windows 7. Client oplock leasing model replaced opportunistic locking to enhance caching and improve performance. Introduced large maximum transmission unit (MTU).
* SMB 3.0 (2012) debuted in Windows 8 and Windows Server 2012. Introduced several improvements to availability, performance,backup, security, and management.
* MoSMB (2012): For Linux/Unix based systems. It supports only SMB 2.x and SMB 3.x
* SMB 3.02 (2014): Introduced in Windows 8.1/Windows Server 2012 R2. Included performance updates, ability to disable CIFS.SMB 1.0 support. 
* SMB 3.1.1 (2015): Released with Windows 10/Windows Server 2016. Added support for encryption and preauthentication integrity. 


### What are Ports 139 and 445?
SMB requires an open-port on a computer or server. SMB Ports are generally numbers 139 and 445.  
_Port 139_ is used by SMB Dialects that communicate over NetBIOS--It is a transport layer protocol designed to use in Windows OS over a network.

_Port 445_ is used by newer versions of SMB (after Windows 2000). On top of a TCP Stack allowing SMB to communicate over the internet.

### Are Open Ports Dangerous?
Ports 139 and 445 are not inherently dangerous. There are known issues with exposing these ports to the internet. Check if port is open by using the netstat command. 
Common misconception that an open-port is dangerous. Largely driven by lack of understanding of how open ports work, why they are open, and which ones should not be open.
Open ports are necessary to communicate across the internet. Can become a security risk when the service listening to the port is misconfigured, unpatched vulnerable to exploits, or has poor security rules. 
Most dangerous ports are wormable ports (SMB uses protocol uses a wormable port).
Infected computer will search its Windows network for devices accepting traffic on TCP ports 135-139 or 445 indicating that the system is configured to run SMB.
How to keep Ports 139 and 445 Secure: Avoid exposing SMB ports, patch everything, no single-point of failure, use a firewall or endpoint protection, use a VPN, implement VLANS, use MAC address filtering.

### New Vocab
*SMB Protocol:* client-server communication protocol for sharing access to files etc. It is a way for computers to talk to each other. 

*Response Request protocol:* Client-server approach where client makes specific requests and the server responds accordingly.

*SMB Protocol Dialects:* See above for the numerous SMB Protocol dialects/versions. 

*TCP Stack:* Is the internet protocol suite, it is a set of communication protocols used by the Internet or similar networks

*Opportunistic Locking:* (OpLock) is a form of file locking used to facilitate caching and access control and improve performance

*WAN Acceleration:* It is a collection of technologies and techniques used to improve the efficiency of data transfer across a wide area network 

*Wormable ports:* Ports vulnerable to worms


### Why does this reading matter in relation to what we are studying this week?
Learning about SMB Protocol ties into the Windows troubleshooting topics as well as the command line and ports. This also relates to security as ports 445 and 139 are wormable and not safe to publicly expose (and have not been safe for a decade). 


### Sources Cited
[From UpGuard---What is an SMB Port? ](https://www.upguard.com/blog/smb-port)

