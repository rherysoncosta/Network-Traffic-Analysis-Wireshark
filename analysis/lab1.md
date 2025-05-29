# Network Traffic Analysis with Wireshark — Practical Lab

## Introduction  
In this lab, I performed a detailed analysis of network traffic captured during a user's connection to an internet website. The purpose was to develop skills in filtering and interpreting packet data using Wireshark, an essential tool for network security investigations.

## Scenario  
As a security analyst, I investigated network traffic related to a user connecting to an internet website. The goal was to filter and analyze the data to:

- Identify source and destination IP addresses;  
- Analyze the protocols used in the communication;  
- Examine specific packets to understand the data exchanged between systems.

## Objectives  
- Analyze network traffic patterns;  
- Apply display filters in Wireshark;  
- Examine DNS and TCP protocols;  
- Identify source/destination relationships.

## Step 1: Initial Exploration of the Capture File  
I opened the `.pcap` file in Wireshark and explored the graphical user interface. I reviewed key columns such as packet number, timestamp, source and destination IP addresses, protocols, packet length, and packet info. I also observed color coding to quickly identify traffic types.

## Step 2: Applying Basic Filters  
I used the filter `ip.addr == 142.250.1.139` to isolate packets involving this IP address. Then, I selected a TCP packet for detailed inspection, examining layers such as Frame, Ethernet II, IPv4, and TCP, including ports, flags, and sequence numbers.

## Step 3: Filtering by IP and MAC Addresses  
I refined the analysis by filtering traffic by source IP (`ip.src`), destination IP (`ip.dst`), and Ethernet MAC address (`eth.addr`). This helped me understand packet flow at different communication layers.

## Step 4: Investigating DNS Traffic  
I filtered UDP packets on port 53 (`udp.port == 53`) to focus on DNS queries and responses. I identified the queried domain (`opensource.google.com`) and confirmed the returned IP address (`142.250.1.139`).

## Step 5: Analyzing TCP Traffic and Payload Content  
I filtered TCP packets on port 80 (`tcp.port == 80`) to analyze HTTP traffic. I also used a filter to find packets containing the text `"curl"` in the payload, which allowed me to identify specific web requests made with the curl command.

## Conclusion  
This lab enhanced my practical skills in network packet analysis, using Wireshark to filter, inspect, and interpret various network protocols and payloads. These competencies are fundamental for cybersecurity roles focused on traffic monitoring and incident response.
