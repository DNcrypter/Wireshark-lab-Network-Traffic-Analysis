
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
### 🏋🏻‍♂️ Exercise 1: Capturing Network Traffic

**Objective**: Learn to capture live network traffic using Wireshark.

1. Open Wireshark.
2. Select the network interface to capture traffic from (e.g., `eth0` or `wlan0`).
3. Click the "Start Capturing Packets" button (blue shark fin).
4. Perform some network activities (e.g., browsing the web).
5. Stop the capture after a few minutes.
6. Observe the captured packets in Wireshark’s main window.

**Output**: A list of captured packets with details such as source/destination IP, protocol, and length.

### 🏋🏻‍♂️ Exercise 2: Applying Filters

**Objective**: Use Wireshark filters to narrow down and focus on specific types of traffic.

1. Start a new packet capture in Wireshark.
2. In the filter bar, type `http` to display only HTTP traffic.
3. Click "Apply" to filter the results.
4. Experiment with other filters like `tcp`, `ip.addr == <your_ip>`, and `dns`.
5. Observe how the displayed packets change based on the applied filters.
  
**Output**: Filtered list of packets that match the criteria specified in the filter bar.

### 🏋🏻‍♂️ Exercise 3: Analyzing HTTP Traffic

**Objective**: Examine HTTP packets to understand web traffic.

1. Start a new packet capture in Wireshark.
2. Open a web browser and visit a website.
3. Stop the packet capture.
4. Apply the `http` filter to display only HTTP traffic.
5. Select an HTTP GET request packet and inspect its details in the packet details pane.
6. Analyze the packet to understand the HTTP request headers and content.

**Output**: Detailed view of an HTTP GET request with headers and content.

### 🏋🏻‍♂️ Exercise 4: Identifying Malicious Traffic

**Objective**: Detect and analyze potential malicious traffic in a network capture.

1. Download a sample pcap file containing malicious traffic from a reputable source (e.g., Wireshark sample captures).
2. Open the pcap file in Wireshark.
3. Apply filters to identify suspicious activities, such as `tcp.port == 4444` (commonly used by malware).
4. Investigate the packets to determine the nature of the malicious activity.
5. Document your findings and the indicators of compromise (IOCs).

**Output**: Identification of malicious packets and an understanding of their characteristics.

### 🏋🏻‍♂️ Exercise 5: Extracting Files from Captures

**Objective**: Extract and analyze files transferred over the network.

1. Start a new packet capture in Wireshark.
2. Download a file from the internet during the capture.
3. Stop the packet capture.
4. Apply the `http` filter and locate the packets related to the file download.
5. Right-click on one of the packets and select "Follow" > "TCP Stream".
6. Save the file from the TCP stream for further analysis.

**Output**: The extracted file from the network capture saved on your system.


## 🚩**Conclusion** :  
These lab exercises are design to practice for beginners those who new to cybersecurity. i am sure that these exercises help you to understand wireshark basics in better way.
If you find this lab useful, please star this repo and keep practicing. Your journey into network security starts here!🎉🎉🎉










