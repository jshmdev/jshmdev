### Cybersecurity Incident Report
Network Traffic Analysis

### Part 1
Task: Provide a summary of the problem found in the DNS and ICMP 
traffic log.
* The UDP protocol reveals that port 53 is unreachable when attempting to access the company website www.yummyrecipesforme.com
* This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message “udp port 53 unreachable” 
* The port noted in the error message is used for DNS.
* The most likely issue is a misconfigured firewall blocking traffic on port 53.



### Part 2
Task: Explain your analysis of the data and provide at least one cause of the incident.
* The precise time of the initial incident is unknown, but technicians replicated the error at 13:24:32.192571.
* The IT team became aware of the incident because several customers contacted the company to report that they were unable to access the company website.
* IT investigated the incident, replicating the error to generate ICMP and DNS logs using tcpdump which were analysed to reveal more detail.
* The DNS server 203.0.113.2.domain is unreachable via the well-known port assigned to the service, port 53. This means that browsers do not have the
* The most likely cause of the incident is a misconfigured firewall that is prevent ingress and/or egress of data packets to the port in question.


