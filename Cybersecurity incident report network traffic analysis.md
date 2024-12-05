# Cybersecurity Incident Report: 

# Network Traffic Analysis

| Part 1: Provide a summary of the problem found in the DNS and ICMP  traffic log.  |  |
| :---- | ----- |
| The UDP protocol reveals that: port 53 is unreachable when attempting to access DNS service for the website www.yummyrecipesforme.com.  
This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message: “udp port 53 unreachable”.  
The port noted in the error message is used for: communication, by translating domain names into IP addresses.  
The most likely issue is: the request did not go through to the DNS server because the DNS port is not listening.  |  |
|  |  |

| Part 2: Explain your analysis of the data and provide at least one cause of the incident. |
| :---- |
| Time incident occurred: 1:24 pm  
Explain how the IT team became aware of the incident: Several of the client's customers have reported to not be able to access the website www.yummyrecipesforme.com.
Explain the actions taken by the IT department to investigate the incident: The network security team has been running tests with the network protocol analyzer tcpdump. They are investigating the logs to determine the source of the problem.  
Note key findings of the IT department's investigation (i.e., details related to the port affected, DNS server, etc.): port 53 which is associated with translating domain names into IP addresses is unreachable.   
Note a likely cause of the incident: There are too many requests to the DNS server causing it to crash and become unresponsive. Signs indicate a possibility of an attack. |

