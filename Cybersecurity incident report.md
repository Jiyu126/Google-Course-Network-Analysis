# Scenario 2
# Cybersecurity Incident Report

| Section 1: Identify the type of attack that may have caused this  network interruption |  |
| :---- | ----- |
| One potential explanation for the website's connection timeout error message is: The web server is too slow at responding due to network traffic so the gateway server sent an error message to the user’s browser.  
The logs show that: The IP address 203.0.113.0 is constantly sending SYN requests to the web server.  
This event could be: A denial of service attack.  |  |
|  |  |

| Section 2: Explain how the attack is causing the website to malfunction |
| :---- |
| When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol. Explain the three steps of the handshake: 
1\. The visitor would send a SYN or synchronize packet to try to establish connection to the web server  
2\. The server would send a SYN, ACK packet back to the visitor to show that it synchronizes and acknowledges this connection.  
3\. The visitor would send an ACK packet back to acknowledge and establish the connection.  
Explain what happens when a malicious actor sends a large number of SYN packets all at once: The increased traffic slows down the real requests and responses to and from the server. Eventually the server would stop responding and crash.  
Explain what the logs indicate and how that affects the server: the logs indicate that the excessive traffic is causing errors in handling requests from visitors. The gateway server is sending timeout connection errors and also RST, ACK packets, prompting users to send another SYN packet to the server. The new incoming SYN packets from real users combined with the DoS attack causes the server to crash and stop responding to any requests. |

