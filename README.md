# Python for Networking Tools

This repository contains basic Python scripts and notes related to networking tools and concepts. As part of my journey into network security and computer networking, I'm learning how to use Python to automate and analyze network-related tasks.

## Scripts and Topics

- Simple port scanner using Python
- IP address validation and subnet checks
- Sending HTTP requests with `requests`
- Using `socket` and `scapy` libraries
- Basic network traffic simulation

## Purpose

The goal of this repository is to explore how Python can help in understanding and working with network protocols and tools. I will gradually add more scripts and examples as I progress in my learning.

---
import socket

target = "scanme.nmap.org"
for port in range(20, 25):
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    socket.setdefaulttimeout(1)
    result = s.connect_ex((target, port))
    if result == 0:
        print(f"Port {port} is open")
    s.close()
