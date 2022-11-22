# Unit 4

Q1. Diff between TCP and IP / Explain the protocols of transport layer (Note: write the points individually if difference is not asked)

|Params| TCP | IP  |
|:----|:----:|----:|
|Definition|TCP provides the service of exchanging data between applications|IP handles addressing and routing messages to the computers across one or more networks|
|Connection|Connection Oriented|Connection less method|
|Location|Transport|Internet|
|Reliability|Reliable|Unreliable|
|Transfer|Segments to internet layer|Datagrams to physical level|
|Flow control|YES|NO|
|Format|TCP segments have a 20 byte header with >= 0 bytes of data|IP datagrams contain a message, or one fragment of a message, that may be up to 65,535 bytes (octets) in length|

Q2. Protocols of Application layer

    A. TELNET: 
        1. Telnet stands for the TELetype NETwork.
        2. It helps in terminal emulation.
        3. It allows Telnet clients to access the resources of the Telnet server. 
        4. It is used for managing files on the internet. 
    B. FTP:
        1. FTP stands for file transfer protocol. 
        2. It is the protocol that actually lets us transfer files. 
        3. It can facilitate this between any two machines using it.
        4. It is also a program
        5. Command: ftp machinename
    C. TFTP:
        1. The Trivial File Transfer Protocol (TFTP) is the stripped-down, stock version of FTP, but it’s the protocol of choice if you know exactly what you want and where to find it.
        2. A more simple FTP
        3. Command: tftp [ options... ] [host [port]] [-c command]
    D. NFS:
        1. It stands for a network file system. It allows remote hosts to mount file systems over a network and interact with those file systems as though they are mounted locally. 
        2. Command: service nfs start
    E. SMTP:
        1. It stands for Simple Mail Transfer Protocol. It is a part of the TCP/IP protocol. 
        2. Using a process called “store and forward,” SMTP moves your email on and across networks.
        3. It works closely with something called the Mail Transfer Agent (MTA)
        4. Command: MAIL FROM:<mail@abc.com?
    F.  LPD:
        1. It stands for Line Printer Daemon. 
        2. It is designed for printer sharing.
        3. Command: lpd [ -d ] [ -l ] [ -D DebugOutputFile]
    G. X window:
        1. It defines a protocol for the writing of graphical user interface–based client/server applications. The idea is to allow a program, called a client, to run on one computer. 
        2. Port number for X window starts from 6000 and increases by 1 for each server.
        3. Command  Run xdm in runlevel 5
    H. SNMP:
        1. It stands for Simple Network Management Protocol. It gathers data by polling the devices on the network from a management station at fixed or random intervals, requiring them to disclose certain information.
        2. The Port number of SNMP is 161(TCP) and 162(UDP). 
        3. Command: snmpget -mALL -v1 -cpublic snmp_agent_Ip_address sysName.0
    I. DNS:
        1. It stands for Domain Name System. 
        2. Every time you use a domain name, therefore, a DNS service must translate the name into the corresponding IP address.
        3. The Port number for DNS is 53.
        4. Command: ipconfig /flushdns
    J.  DHCP:
        1. It stands for Dynamic Host Configuration Protocol (DHCP). It gives IP addresses to hosts.
        2. There is a lot of information a DHCP server can provide to a host when the host is registering for an IP address with the DHCP server.
        3. Port number for DHCP is 67, 68.
        4. Command: clear ip dhcp binding {address | * }

