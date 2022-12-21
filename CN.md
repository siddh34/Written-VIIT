# CN

## Unit 4

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
        
Q. 3. Elaborate Three-way Handshake.
    
    • In a three-way handshake, the first sender sends the SYN message to the receiver then the receiver sends back the SYN ACK message to confirm tha the message has been received.
    • After receiving the SYN ACK message, the sender sends the acknowledgment message to the receiver. 
    • In this way, the connection is established between the computers.
    • Once the connection is established, the data will be delivered.
    • This protocol guarantees the data delivery means that if the data is not received then the TCP will resend the data.
    • It is a process of initiating and acknowledging a connection.
    • Once the connection is established, data transfer begins, and when the transmission process is finished, the connection is terminated by the closing of an   established virtual circuit.

## Unit 5

Q1. Explain the working of MD5 algorithm

## Unit 6

Q.1. Types of attacks.
   
    A.) Active attacks: An Active attack attempts to alter system resources or affect their operations. Active attacks involve some modification of the data stream or the creation of false statements. Types of active attacks are as follows: 

    1. Masquerade
    2. Modification of messages
    3. Repudiation
    4. Replay
    5. Denial of Service
   
    1. Masquerade – 
    A masquerade attack takes place when one entity pretends to be a different entity. A Masquerade attack involves one of the other forms of active attacks.  If an authorization procedure isn’t always absolutely protected, it is able to grow to be extraordinarily liable to a masquerade assault. Masquerade assaults may be performed using the stolen passwords and logins, with the aid of using finding gaps in programs, or with the aid of using locating a manner across the authentication process.
    
    2.  Modification of messages –
    It means that some portion of a message is altered or that message is delayed or reordered to produce an unauthorized effect. Modification is an attack on the integrity of the original data. It basically means that unauthorized parties not only gain access to data but also spoof the data by triggering denial-of-service attacks, such as altering transmitted data packets or flooding the network with fake data. Manufacturing is an attack on authentication. For example, a message meaning “Allow JOHN to read confidential file X” is modified as “Allow Smith to read confidential file X”. 

    3. Repudiation – 
    This attack occurs when the network is not completely secured or the login control has been tampered with. With this attack, the author’s information can be changed by actions of a malicious user in order to save false data in log files, up to the general manipulation of data on behalf of others,  similar to the spoofing of e-mail messages.  

    4. Replay – 
    It involves the passive capture of a message and its subsequent transmission to produce an authorized effect. In this attack, the basic aim of the attacker is to save a copy of the data originally present on that particular network and later on use this data for personal uses. Once the data is corrupted or leaked it is insecure and unsafe for the users.
    
    5. Denial of Service – 
    It prevents the normal use of communication facilities. This attack may have a specific target. For example, an entity may suppress all messages directed to a particular destination. Another form of service denial is the disruption of an entire network either by disabling the network or by overloading it with messages so as to degrade performance.
    
    B.) Passive attacks: A Passive attack attempts to learn or make use of information from the system but does not affect system resources. Passive Attacks are in the nature of eavesdropping on or monitoring transmission. The goal of the opponent is to obtain information that is being transmitted. Types of Passive attacks are as follows: 

    1. The release of message content
    2. Traffic analysis
    1. The release of message content – 
    Telephonic conversation, an electronic mail message, or a transferred file may contain sensitive or confidential information. We would like to prevent an opponent from learning the contents of these transmissions. 
    
    2. Traffic analysis – 
    Suppose that we had a way of masking (encryption) information, so that the attacker even if captured the message could not extract any information from the message. The opponent could determine the location and identity of communicating host and could observe the frequency and length of messages being exchanged. This information might be useful in guessing the nature of the communication that was taking place. The most useful protection against traffic analysis is encryption of SIP traffic. To do this, an attacker would have to access the SIP proxy (or its call log) to determine who made the call.
