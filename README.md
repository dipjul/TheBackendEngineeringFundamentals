# The Backend Engineering Fundamentals

### OSI Model
  Open System Interconnection by International Organization for Standardization in 1984. It provides a framework for creating and implementing networking standards, devices, and internetworking schemes.
  | Group  | Layer No. | Layer Name  | Description |
  | ------ | --------- | ----------- | ----------- |
  | Top Layers | 7 |	Application |	Provide a user interface for sending and receiving data |
  | - | 6	| Presentation |	Encrypt, format, and compress data for transmission |
  | - | 5	| Session |	Initiate and terminate a session with the remote system |
  | Bottom Layers |	4 |	Transport |	Break the data stream into smaller segments and provide reliable and unreliable data delivery |
  | - | 3	| Network	| Provide logical addressing |
  | - | 2	| Data Link	| Prepare data for transmission |
  | - | 1	| Physical |	Move data between devices |
  #### Application Layer
  The Top layer of the OSI model is the application layer. It provides the protocols and services that are required by the network-aware applications to connect to the network. FTP, TFTP, POP3, SMTP, and HTTP are examples of standards and protocols used in this layer.
  #### Presentation Layer
  Conversion, compression, and encryption are the main functions that the Presentation layer performs on the sending computer while on the receiving computer these functions are reconversion, decompression, and decryption. ASCII, BMP, GIF, JPEG, WAV, AVI, and MPEG are examples of standards and protocols that work in this layer.
  #### Session Layer
  The session layer is responsible for establishing, managing, and terminating communications between two computers. RPCs and NFS are examples of the session layer.
  #### Transport Layer
  The main functionalities of the Transport layer are segmentation, data transportation, and connection multiplexing. For data transportation, it uses TCP and UDP protocols. TCP is a connection-oriented protocol. It provides reliable data delivery.
  #### Network Layer
  Defining logical addresses and finding the best path to reach the destination address are the main functions of this layer. Routers work in this layer. Routing also takes place in this layer. IP, IPX, and AppleTalk are examples of this layer.
  #### Data Link Layer
  Defining physical addresses, finding hosts in the local network, specifying standards and methods to access the media are the primary functions of this layer. Switching takes place in this layer. Switches and Bridges work in this layer. HDLC, PPP, and Frame Relay are examples of this layer.
  
  This layer has two sub-layers: MAC(Media Access Control) and LLC(Logical Link Control)
  #### Physical Layer
  The Physical Layer mainly defines standards for media and devices that are used to move data across the network. 10BaseT, 10Base100, CSU/DSU, DCE, and DTE are examples of the standards used in this layer.
  
  <hr>
  
### TCP/IP
  TCP/IP stands for Transmission Control Protocol/ Internet Protocol. TCP/IP Stack is specifically designed as a model to offer highly reliable and end-to-end byte stream over an unreliable internetwork
  ![image](https://user-images.githubusercontent.com/20329508/194799658-2d5f3b36-1222-4266-b97b-78a1df08d832.png)
  
  ![image](https://user-images.githubusercontent.com/20329508/194799832-a3bf5a6e-8dde-4963-aedc-20811c4aecd1.png)

  
  TCP/IP model is developed by ARPANET (Advanced Research Project Agency Network).
  Some widely used most common TCP/IP protocol are:

  ![image](https://user-images.githubusercontent.com/20329508/194826313-8bb5c9da-f9ca-4641-a3b6-8897793ce443.png)

  #### TCP:
  Transmission Control Protocol is an internet protocol suite which breaks up the message into TCP Segments and reassembling them at the receiving side.

  #### IP:
  An Internet Protocol address that is also known as an IP address is a numerical label. It is assigned to each device that is connected to a computer network which uses the IP for communication. Its routing function allows internetworking and essentially establishes the Internet. Combination of IP with a TCP allows developing a virtual connection between a destination and a source.

  #### HTTP:
  The Hypertext Transfer Protocol is a foundation of the World Wide Web. It is used for transferring webpages and other such resources from the HTTP server or web server to the web client or the HTTP client. Whenever you use a web browser like Google Chrome or Firefox, you are using a web client. It helps HTTP to transfer web pages that you request from the remote servers.

  #### SMTP:
  SMTP stands for Simple mail transfer protocol. This protocol supports the e-mail is known as a simple mail transfer protocol. This protocol helps you to send the data to another e-mail address.

  #### SNMP:
  SNMP stands for Simple Network Management Protocol. It is a framework which is used for managing the devices on the internet by using the TCP/IP protocol.

  #### DNS:
  DNS stands for Domain Name System. An IP address that is used to identify the connection of a host to the internet uniquely. However, users prefer to use names instead of addresses for that DNS.

  #### TELNET:
  TELNET stands for Terminal Network. It establishes the connection between the local and remote computer. It established connection in such a manner that you can simulate your local system at the remote system.

  #### FTP:
  FTP stands for File Transfer Protocol. It is a mostly used standard protocol for transmitting the files from one machine to another.
  <hr>
  
  #### [How OSI and TCP/IP work?](https://youtu.be/3kfO61Mensg)
  
  <hr>

### IP Address
An Internet Protocol address (IP address) serves two main functions: network interface identification and location addressing.
IPv4 defines an IP address as a 32-bit number. However, because of the growth of the Internet and the depletion of available IPv4 addresses, a new version of IP i.e., IPv6, using 128 bits for the IP address, was standardized in 1998.

<hr>

### NAT
  Network address translation (NAT) is a method of mapping an IP address space into another by modifying network address information in the IP header of packets while they are in transit across a traffic routing device. The technique was originally used to bypass the need to assign a new address to every host when a network was moved, or when the upstream Internet service provider was replaced, but could not route the network's address space. It has become a popular and essential tool in conserving global address space in the face of IPv4 address exhaustion. One Internet-routable IP address of a NAT gateway can be used for an entire private network.
  ![image](https://user-images.githubusercontent.com/20329508/194806584-3040cdf4-1551-4bad-a15f-a0fce34bd7f9.png)

#### Routing
Network address translation can be used to mitigate IP address overlap. Address overlap occurs when hosts in different networks with the same IP address space try to reach the same destination host. This is most often a misconfiguration and may result from the merger of two networks or subnets, especially when using RFC 1918 private network addressing. The destination host experiences traffic apparently arriving from the same network, and intermediate routers have no way to determine where reply traffic should be sent to. The solution is either renumbering to eliminate overlap or network address translation.

#### Load balancing
In client–server applications, load balancers forward client requests to a set of server computers to manage the workload of each server. Network address translation may be used to map a representative IP address of the server cluster to specific hosts that service the request.

<hr>

### Virtual IP Addressing
A virtual IP address (VIP or VIPA) is an IP address that does not correspond to a physical network interface. 
![image](https://user-images.githubusercontent.com/20329508/194818785-855f2c07-9b17-4f8b-bb6b-dbddfa25fdb6.png)

![image](https://user-images.githubusercontent.com/20329508/194818964-2a08f081-ff42-40be-871d-df3374d1722b.png)

Uses for VIPs include network address translation (especially, one-to-many NAT), fault-tolerance, and mobility. It advertises virtual links connected via itself to all of its actual network interfaces.

<hr>

### iptables
iptables allows a system administrator to configure the IP packet filter rules of the Linux kernel firewall. The filters are organized in different tables, which contain chains of rules for how to treat network traffic packets. Different kernel modules and programs are currently used for different protocols. On most Linux systems, iptables is installed as /usr/sbin/iptables and documented in its man pages.

![iptables](https://user-images.githubusercontent.com/20329508/194821305-30539c80-9d8a-4524-a211-b5f512bbfaf6.png)

![iptables1](https://user-images.githubusercontent.com/20329508/194821868-66ab88d5-1328-448d-8141-a3a4d8127a23.png)

![iptables3](https://user-images.githubusercontent.com/20329508/194823527-71fa7248-6102-42df-8269-d1c54f99b199.png)

<hr>

#### [iptables - I: Advance](https://youtu.be/NAdJojxENEU)
#### [iptables - II: Advance](https://youtu.be/-CraNvj48J0)
<hr>

### TCP & UDP
TCP, which stands for Transmission Control Protocol, and UDP, or User Datagram Protocol, are part of the internet protocol suite, layer 4 (Transport). TCP and UDP are different methods to send information across the internet.

#### TCP Pros
- acknowledgement
- guranteed delivery
- connection based
- congestion control
- ordered packets

#### TCP Cons
- larger packets
- more bandwidth
- slower than UDP
- stateful
- server memory (DoS)

#### UDP Pros
- smaller package
- less bandwidth
- faster than TCP
- stateless

#### UDP Cons
- no acknowledgement
- no guranteed delivery
- connectionless
- no congestion control
- no ordered packets
- no security

#### [TCP vs UDP](https://youtu.be/qqRYkcta6IE)
<hr>

### TCP 3-way handshake
#### Connection Establishment Process
![image](https://user-images.githubusercontent.com/20329508/194834935-a688a253-1bba-4a64-b0c6-e3dae31978b8.png)

#### Closing Connection Process
![image](https://user-images.githubusercontent.com/20329508/194835123-402a45b0-182b-4c18-a5d8-aebc6e6569a5.png)
<hr>

### When to use UDP vs TCP?
When data integrity is your top priority, then TCP will always be the best choice. The protocol guarantees complete delivery and accurate reconstruction of the original data. When streaming video, however, accuracy is less important than continuity. This is why real-time applications like audio and video streaming will often use UDP.
<hr>

### Stateless vs Stateful applications
In a traditional stateful web application, the server is doing all of the work associated with recreating a web page. A stateless application doesn't save any client session (state) data on the server where the application lives. By using a Representational State Transfer (REST) API, developers can augment HTTP to produce stateless apps.

When an application is stateful, it relies on saved client session data to process new transactions. A stateful app still uses a database for back-end storage, but it also uses the server where the application runs to store data from previous interactions. This allows the app to process subsequent transactions in the context of preceding ones. Stateful systems use databases like any application, but they also maintain "state data" (related to client authentication and past requests) on the server itself. Stateful apps are fast because they don't need to process as much data in each client request. This makes stateful apps fast and it allows clients to interact with the application within the historical context of previous interactions.

Stateful apps bind clients and users to the same server so it can process subsequent requests in the context of previous ones. Stateful apps work best under predictable workloads that the system can manage. If traffic grows, you can't simply replicate a stateful app and redirect new client requests because users will need to start from scratch. This makes stateful apps more prone to system unavailability when client traffic increases.

A stateless application or stateless process doesn't store any data related to past transactions on its server. It accepts each transaction or user interaction like a blank slate without knowledge of previous interactions. Similar to a Coke machine, the stateless app receives a single short-term request and delivers a single response. This is why many of the apps (clients) on your phone or computer have a cache. A stateless system acts like a nameless agent that clients use to interact with the databases it connects with.

Since the application is stateless, a load balancer can infinitely replicate new instances of it and balance client requests across those instances. This allows the system to scale and manage any level of traffic. Similar to the security guard, DreamFactory waits for a client to submit an API request.

The decision to use stateful versus stateless apps boils down to your scalability requirements and what you need the app to do. If your app needs to store session data to process transactions in-context and if the server can handle the expected processing load, a stateful system is probably best. On the other hand, if you are building an app that needs to process REST API transactions, provide information in response to client requests – and traffic levels can grow exponentially – a stateless app is what you’ll be working with.
<hr>

### HTTP
  It is a aapplication layer protocol, functions as a request–response protocol in the client–server model. 
  An example HTTP request:
  ![image](https://user-images.githubusercontent.com/20329508/195249102-e78ebeda-d220-4cfb-b067-b3398f2fe14e.png)

  An example response:
  ![image](https://user-images.githubusercontent.com/20329508/195249164-e5435ad7-f7b9-42f2-9fc0-9ae476edc19a.png)

  #### HTTP 1.0 over TCP
  - new TCP connection for each request
  - slow
  - buffering

  #### HTTP 1.1 over TCP
  ![image](https://user-images.githubusercontent.com/20329508/195250864-a6da3bdd-dc2c-4653-afe8-f75e5f73f0ec.png)

  - persisted TCP connection
  - low latency
  - streaming with chunked transfer
  - pipelining (disabled by default)
  
  ![image](https://user-images.githubusercontent.com/20329508/195251181-e52d6b39-a015-4c86-a72c-28816580db9f.png)

  #### HTTP 2 over TCP
  - compression
  - multiplexing
  - server push
  - SPDY (initial version of HTTP2 by google)
  - secure by default
  - protocol negotiation during TLS (NPN/ALPN)

![image](https://user-images.githubusercontent.com/20329508/195253974-3ee453d4-ec61-4b6e-b7cd-9d62422de732.png)


### Journey of an HTTP request
  1. HTTP request (format as shown earlier) is created
  2. Transport Layer  
    - TCP handshake  
    - If a message is too large to be sent in one go, it is broken down into several segments that each have their own sequence number (situated in a header field, as well). This way, when they arrive at their destination, they will be processed in the correct order.  
    - The HTTP request is encapsulated in a TCP segment, which has a header and data payload. The Transport Layer is responsible for sending the segment from the requesting application to the correct process in the server. It uses the use of ports: integers in the range of 0–65535 that act as identifiers for a specific application or process in a host.  
    ![image](https://user-images.githubusercontent.com/20329508/195340082-5b0574c4-4ded-42f0-9075-acce1eacdd74.png)

  3. Internet Layer  
    - Onwards, downwards, to the Internet Layer. This is where TCP segments are turned into IP packets by the Internet Protocol (IP) The Internet Protocol is the one that enables a packet to travel from your home to a server on the other side of the world. An IP address might look something like this: 207.126.144.100, for IPv4, or this: 2a02:687:1211:7500:c8cb:bcf9:7acb:a966,. for IPv6.  
    ![image](https://user-images.githubusercontent.com/20329508/195340164-93fb2b43-8aba-4a03-a584-61b5914623e6.png)

  4. Data Link Layer  
    - Ethernet wraps the IP packet, containing the TCP segment, into a frame. The frame takes its final form: it becomes a stream of bits travelling as electrical signals (or light signals or radio waves) towards the destination MAC address’— the router that will act as a gateway to the outside world. It's much like how real packages travel across the world: each courier processes the package and dispatches it to the next courier until it reaches its final destination.  
    ![image](https://user-images.githubusercontent.com/20329508/195340239-35deb5ad-df9d-4d65-a065-01d96823d12d.png)

  
### HTTP GET / through Switches, Routers, Gateways, and Proxies
![http](https://user-images.githubusercontent.com/20329508/195497332-21156ead-d5fa-4b7b-a87f-c3ac2ff8adee.png)

![httpExternal](https://user-images.githubusercontent.com/20329508/195497607-1191a764-f582-4e25-b225-55d4dcba4e53.png)

![httpProxy](https://user-images.githubusercontent.com/20329508/195497940-2f3c6175-4efc-4082-85ff-80e54fda20cd.png)

### cURL Verbose mode
```
curl -v https://www.stackoverflow.com
*   Trying 151.101.1.69:443...
* TCP_NODELAY set
* Connected to www.stackoverflow.com (151.101.1.69) port 443 (#0)
* ALPN, offering h2
* ALPN, offering http/1.1
* successfully set certificate verify locations:
*   CAfile: /etc/ssl/certs/ca-certificates.crt
  CApath: /etc/ssl/certs
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
* TLSv1.3 (IN), TLS handshake, Server hello (2):
* TLSv1.2 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (IN), TLS handshake, Server key exchange (12):
* TLSv1.2 (IN), TLS handshake, Server finished (14):
* TLSv1.2 (OUT), TLS handshake, Client key exchange (16):
* TLSv1.2 (OUT), TLS change cipher, Change cipher spec (1):
* TLSv1.2 (OUT), TLS handshake, Finished (20):
* TLSv1.2 (IN), TLS handshake, Finished (20):
* SSL connection using TLSv1.2 / ECDHE-RSA-AES128-GCM-SHA256
* ALPN, server accepted to use h2
* Server certificate:
*  subject: CN=*.stackexchange.com
*  start date: Sep  4 13:06:50 2022 GMT
*  expire date: Dec  3 13:06:49 2022 GMT
*  subjectAltName: host "www.stackoverflow.com" matched cert's "*.stackoverflow.com"
*  issuer: C=US; O=Let's Encrypt; CN=R3
*  SSL certificate verify ok.
* Using HTTP2, server supports multi-use
* Connection state changed (HTTP/2 confirmed)
* Copying HTTP/2 data in stream buffer to connection buffer after upgrade: len=0
* Using Stream ID: 1 (easy handle 0x5604558be8c0)
> GET / HTTP/2
> Host: www.stackoverflow.com
> user-agent: curl/7.68.0
> accept: */*
>
* Connection state changed (MAX_CONCURRENT_STREAMS == 100)!
< HTTP/2 301
< cache-control: private
< content-type: text/html; charset=utf-8
```
### HTTP Code 502 Bad Gateway
The server was acting as a gateway or proxy and received an invalid response from the upstream server.

The 502 error code is a by-product of the source or origin server being out of order. A range of connectivity issues, a server that is powered down, or spikes in traffic can all lead to this message. Communication issues between online servers or DNS issues such as incorrectly cached IP addresses play a big role in the appearance of this error.

If your website is generating a 502 status code error, then try disabling the firewall or the CDN if you are behind one. Website themes and browser plugins can also cause the error as well. If disabling the plugins does not help then try updating your website theme. Most hosting providers have customer support teams that can triage the issue with you.

Error codes use by cloudflare for more meaningfull error:

![image](https://user-images.githubusercontent.com/20329508/195806075-a44554cf-818f-4ce3-a823-4de79b7da2c7.png)

### HTTP  CONNECT method
#### HTTP Proxy
  - Client wants to connect to a server beyond its reach
  - Client doesn't know how to communicate target-server protocol
  - Proxy has access to the server and knows how to talk to it
  - Client connects the Proxy and Proxy makes the request on behalf of the client to the target server

![image](https://user-images.githubusercontent.com/20329508/196020889-6c103f21-4123-4dd9-a675-24a5f0705de4.png)

#### HTTPS Proxy
- In HTTPS Proxy, the proxy decrypts and serves its certificate to the client instead of that of the target server
- Proxy sees everything(BAD, but good for debugging web traffic)
- We need a way to establish End to End encryption between the client and the target server

![image](https://user-images.githubusercontent.com/20329508/196021143-d7ff3f3d-5915-4d1b-bae8-d22faf85b17a.png)

#### HTTP CONNECT
- Creates a tunnel between the client and the target server
- Client sends HTTP CONNECT to Proxy containing target server
- Proxy creates a TCP connection to target server
- Once successful, proxy returns success to client
- Any packet the client sends goes as-is to the target server
- This includes TLS handshake, establishing e2e

![image](https://user-images.githubusercontent.com/20329508/196021388-83e0a293-8994-4df1-b6f0-a172385e4f58.png)

![image](https://user-images.githubusercontent.com/20329508/196021535-5e5f43e0-c837-471c-9ec6-a29d4cdba050.png)

#### HTTP CONNECT Chaining
![image](https://user-images.githubusercontent.com/20329508/196021674-e7d66347-be0c-4361-abbf-8be64dfd4959.png)

**Pros:**
- Connect to secure servers
- Support protocols that normally not supported through proxies (WebSockets, WebRTC)
- Proxy can't read encrypted traffic
- Chained Proxies CONNECT

**Cons**
- Only TCP, Can't proxy UDP traffic (won't work with QUIC/DNS)
- Each CONNECT opens new TCP, expensive, (no multiplexing)
- Bad implementation would allow tunneling to port (eg 25 SMTP can load to spam email)

**MASQUE: Multiplexed Application Substrate over QUIC Encryption**
***Why MASQUE?***
- Allows UDP tunneling, Can't proxy UDP traffic with CONNECT (won't work with QUIC/DNS)
- Allows multiplexing, each CONNECT opens new TCP to same host, expensive
- Secure, bad CONNECT implementation would allow tunneling to port (eg 25 SMTP can load to spam email)

### HTTP/2
#### HTTP 1.1
- We can't utilize the same connection for parallel requests
- Browsers use 6 connections, all those connections can be use for sending more request (to overcome the above issue)

#### HTTP 2
- Multiplexed streams, as we have identifier for streams, we can compress the header too

![image](https://user-images.githubusercontent.com/20329508/196023812-d739f08b-af66-460e-b7ca-7a9cc995f158.png)

- Server push

![image](https://user-images.githubusercontent.com/20329508/196023824-b0f67378-231b-4da8-8ad3-9f88e20b1941.png)

**Pros:**
- Multiplexing over Single Connection
- Compression (Header & Data)
- Server Push
- Secure by default
- Protocol Negotiation during TLS (ALPN)

**Cons:**
- Server push can be abushed when configured incorrectly
- Can be slower when in mixed mode (Backend is http/2 but load balancer is http 1 or vice versa)


### WebSockets
![image](https://user-images.githubusercontent.com/20329508/196024821-56760d3f-ef78-4fa2-b151-f6af84b6273a.png)

![image](https://user-images.githubusercontent.com/20329508/196024861-4655f16a-db9c-4bbf-b633-65b8517dc023.png)

#### WebSockets usecases:
- Chatting
- Live Feed
- Multiplayer gaming
- Showing client progress/logging

**Pros:**
- Full-duplex (no polling)
- HTTP compatible
- Firewall friendly (standard)

**Cons:**
- Proxying is tricky
- L7 Load Balance challenging (timeouts)
- Stateful, difficult to horizontally scale

**Do you have to use WebSockets?**
- NO! Rule of thumb - do you absolutely need bidirectional communication?
- Long polling
- EventSource

### HTTP/2 limitation that leads to QUIC or HTTP/3
HTTP/2 over TCP suffers from a slight inefficiency caused by TCP. Consider the following example: Suppose you have 3 streams A, B and C. Denote packets (frames) of each stream by lower case letters (a, b, c) and a sequence number. Let's have a look at what happens with HTTP/2 over TCP when the following sequence is sent:

server ---> a2, c2, b2, *c1, b1, a1 ---> client

Where the *c1 means that this frame was lost. The receiving end (client) must wait for a re-transmission of the lost *c1 frame before it can pass later frames to the application layer (namely b2,c2,a2), because the communication is over TCP and TCP guarantees in-order delivery!

That is in contrast to HTTP/3 & QUIC, where over UDP these are just independent packets, thus the loss of *c1 would not delay the delivery of b2, c2 and a2 to the application layer!

### QUIC or HTTP/3


### gRPC over HTTP/3
### Should RabbitMQ implement QUIC Protocol for their Channels Message Queue?
### Can QUIC Protocol improve Database Performance in Web Applications?
### Facebook moves their backend and frontend to QUIC
### Symmetrical and Asymmetrical Encryption
### TLS
### TLS Handshake
### Web Servers
### Proxy and Reverse Proxy Server
### Anatomy of a Proxy Server
### Layer 4 vs Layer 7 proxying
### NginX
### NGINX Internal Architectur - Workers
### HAProxy
### Envoy Proxy
### Slack migrating millions of WebSockets from HAProxy to Envoy
### Load balancing Server-Sent Events
### Load balancing in Layer 4 vs Layer 7
### Load Balance multiple RTMP Servers to Horizontally Scale Streaming
### Can you Max-out the connections between load balancer and backend servers?
### Caching is hard
### Long Polling, how it deffers from push, pull and SSE
### First port your computer hits
### ACID Transactions - Relational Database
### Primary Key and Secondary key
### B Tree and B+ Tree
### Database Indexing
### Leaking Postgres database connections
### Database Engines
### Fail-over and High-Availability
### Active-Active vs Active-Passive Cluster to achieve High Availability
### Connection Pooling in PostgresSQL
### Horizontal vs Vertical Database Partitioning
### Database Partitioning
### Database Sharding
### Can you get Eventual Consistency in Relational Database?
### Avoid Double Booking and Race Conditions
### 

