\# Live Polling and Voting System (UDP)



\## Overview

This project implements a Live Polling and Voting System using UDP socket programming in Python. Multiple clients can send votes to a server, which collects the votes and broadcasts live results to all connected clients.



The system also performs statistical packet loss analysis to measure lost UDP packets.



---



\## Features

\- Multi-client voting system

\- UDP socket communication

\- Live result broadcasting

\- Duplicate vote detection

\- Packet loss analysis using sequence numbers



---



\## Project Structure



C\_N\_project

│

├── server.py

├── client.py

├── README.md

└── .gitignore



---



\## Packet Format



Vote packet:

VOTE|client\_id|sequence\_number|candidate



Example:

VOTE|101|5|A



Server broadcast packet:

RESULT|A:5|B:3|C:2



---



\## Packet Loss Analysis



Packet Loss Rate = (Lost Packets / Total Packets Sent) × 100



Sequence numbers are used to detect missing packets from clients.



---



\## How to Run



Start the server:

python server.py



Start clients in separate terminals:

python client.py



Enter Client ID and vote (A/B/C).



---



\## Example Output



===== LIVE RESULTS =====

A:2

B:1

C:0

========================



---



\## Author

Siddesh V S  

Computer Networks Project

