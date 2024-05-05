### Cybersecurity Incident Report

### Background
You work as a security analyst for a travel agency that advertises sales and promotions on the company’s website. The employees of the company regularly access the company’s sales webpage to search for vacation packages their customers might like. 
One afternoon, you receive an automated alert from your monitoring system indicating a problem with the web server. You attempt to visit the company’s website, but you receive a connection timeout error message in your browser.
You use a packet sniffer to capture data packets in transit to and from the web server. You notice a large number of TCP SYN requests coming from an unfamiliar IP address. The web server appears to be overwhelmed by the volume of incoming traffic and is losing its ability to respond to the abnormally large number of SYN requests. You suspect the server is under attack by a malicious actor. 
You take the server offline temporarily so that the machine can recover and return to a normal operating status. You also configure the company’s firewall to block the IP address that was sending the abnormal number of SYN requests. You know that your IP blocking solution won’t last long, as an attacker can spoof other IP addresses to get around this block. You need to alert your manager about this problem quickly and discuss the next steps to stop this attacker and prevent this problem from happening again. You will need to be prepared to tell your boss about the type of attack you discovered and how it was affecting the web server and employees.

### Section 1
Task: Identify the type of attack that may have caused this 
network interruption
One potential explanation for the website's connection timeout error message is that the server is overwhelmed with requests. 

The logs show that the server is receiving a large number of TCP SYN requests from an unfamiliar IP address.

This event could be the result of a SYN-flood attack.



### Section 2
Task: Explain how the attack is causing the website to malfunction. When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol. Explain the three steps of the handshake.

1. The client that wants to connect with a server sends a SYN message (TCP segment) indicating that it is likely to start communicating and with what segment sequence number.

2. The server responds with a SYN/ACK message to ACKnowledge the client request and to SYNchronise segment numbers.

3. The client sends an ACK message in response and the data transfer begins.

When a malicious actor sends a large number of SYN packets all at once, the server becomes overwhelmed with the volume of messages it must parse and responses it must give, slowing or stopping its ability to respond.

Task: Explain what the logs indicate and how that affects the server.

The logs indicate that a malicious actor sent a large volume of SYN packets as part of a SYN flood attack. This overwhelmed the server, which could no longer respond to requests, which then resulted in timeout errors.


