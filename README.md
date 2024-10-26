
# 🐳Wireshark: Network Traffic analysis Lab
Difficulty level : Beginner

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
        [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue)](https://www.linkedin.com/in/nikhil--chaudhari/)
        [![Medium](https://img.shields.io/badge/Medium-Writeups-black)](https://medium.com/@nikhil-c)

## Introduction 🚀

In this lab i will show you how can we analyse network traffic in wireshark in linux system. You will learn to capture, inspect, and understand data packets moving across a network. Using Wireshark also learn to analyse traffic and find malicious things. Here, I designed some exercises to help beginner to learn step by step and clear basics of web traffic analysis. please go throgh each lab exercise and pratice them.

## 🔗Pre-requisites
- basics understanding of ip addresses and protocols.
- knowledge of cammandline interface.
- understanding of OSI or TCP/IP layers.
- curiosity to learn and understand 😉 working.

## ⚙️Lab requirements
- A computer running a Linux distribution(eg: kali linux,Ubuntu)
- internet to download neccessary files.
- Wireshark tool to be installed on linux machine.

## 🛠️ Lab set-up 

1. Update package list
```bash 
sudo apt update
```
2. install Wireshark GUI tool.
```bash 
sudo apt install wireshark
```

3. Add your user to the wireshark group to capture packets without root privileges
```bash
sudo usermod -aG wireshark $(whoami)
```
4. Log-out and log-in back in for the changes to take reflect.

## Exercises:👨🏾‍💻👨🏾‍💻
**Exercise 1: Capturing Network Traffic**
1. &nbsp;&nbsp; Open Wireshark.
&nbsp;&nbsp; 2. Select the network interface to capture traffic  from (e.g., eth0 or wlan0).
    - Click the "Start Capturing Packets" button (blue shark fin).
    - Perform some network activities (e.g., browsing the web).
    - Stop the capture after a few minutes.
    - Observe the captured packets in Wireshark’s main window.
   **Output**: A list of captured packets with details such as source/destination IP, protocol, and length.

2. **Exercise 2: Applying Filters**

     - Start a new packet capture in Wireshark.
     - In the filter bar, type http to display only HTTP traffic.
     - Click "Apply" to filter the results.
     - Experiment with other filters like tcp, ip.addr == <your_ip>, and dns.
     - Observe how the displayed packets change based on the applied filters.
    **Output**: Filtered list of packets that match the criteria specified in the filter bar.

3. **Exercise 3: Analyzing HTTP Traffic**
     - Start a new packet capture in Wireshark.
     - Open a web browser and visit a website.
     - Stop the packet capture.
     - Apply the http filter to display only HTTP traffic.
     - Select an HTTP GET request packet and inspect its details in the packet details pane.
     - Analyze the packet to understand the HTTP request headers and content.
    **Output**: Detailed view of an HTTP GET request with headers and content.

4. **Exercise 4: Identifying Malicious Traffic**
     - Download a sample pcap file containing malicious traffic from a reputable source (e.g., Wireshark sample captures).
     - Open the pcap file in Wireshark.
     - Apply filters to identify suspicious activities, such as tcp.port == 4444 (commonly used by malware).
     - Investigate the packets to determine the nature of the malicious activity.
     - Document your findings and the indicators of compromise (IOCs).
    **Output**: Identification of malicious packets and an understanding of their characteristics.

5. **Exercise 5: Extracting Files from Captures**
     - Start a new packet capture in Wireshark.
     - Download a file from the internet during the capture.
     - Stop the packet capture.
     - pply the http filter and locate the packets related to the file download.
     - Right-click on one of the packets and select "Follow" > "TCP Stream".
     - Save the file from the TCP stream for further analysis.
    **Output**: The extracted file from the network capture saved on your system.


🚩**Conclusion** : These lab exercises are design to practice for beginners those who new to cybersecurity. i am sure that these exercises help you to understand wireshark basics in better way.
If you find this lab useful, please star this repo and keep practicing. Your journey into network security starts here!🎉🎉🎉










