# ◈ Internet Protocol Troubleshooting Commands
**Course ID**: `265-[NF]-Lab - Internet Protocol Troubleshooting Commands`

## 🎯 Project Objective
Executing standard Network Diagnostic Utilities mapped across OSI Layers 3, 4, and 7 within a Linux EC2 instance to systematically isolate, analyze, and resolve infrastructure reachability, transport-level connection issues, and application HTTP/S responses.

## ⚙️ Technical Implementation
* **Layer 3 (Network):** Executed `ping -c 5` to confirm ICMP reachability and measure packet loss, followed by `traceroute` to analyze multi-hop routing paths, gateway hops, and network latency.
* **Layer 4 (Transport):** Utilized `netstat -tp` to inspect active stateful TCP connections and local socket bindings, and configured `telnet` to test low-level TCP handshakes on Port 80.
* **Layer 7 (Application):** Formulated verbose HTTP/S requests via `curl -vLo /dev/null` to analyze SSL/TLS handshake negotiations, server redirect headers, and status code responses.

## 📸 Lab Evidence

| Step | OSI Layer & Focus | Verification Artifact |
| :--- | :--- | :--- |
| **01** | SSH Terminal Session | [01_ssh_puTTY_session.png](images/01_ssh_puTTY_session.png) |
| **02** | L3 ICMP Reachability (`ping`) | [02_ping_8888.png](images/02_ping_8888.png) |
| **03** | L3 Route & Hop Latency (`traceroute`) | [03_traceroute_8888.png](images/03_traceroute_8888.png) |
| **04** | L4 Active Sockets (`netstat`) | [04_netstat_connections.png](images/04_netstat_connections.png) |
| **05** | L4 TCP Port Verification (`telnet`) | [05_telnet_google_80.png](images/05_telnet_google_80.png) |
| **06** | L7 HTTP/S Verbose Headers (`curl`) | [06_curl_verbose_aws.png](images/06_curl_verbose_aws.png) |

## 🛠️ Operational Intelligence (Troubleshooting)
* **Real-World Challenge:** Isolating network failures often leads to misidentifying issues (e.g., assuming a web application is down when a Security Group is blocking inbound traffic or an ISP hop is dropping packets).
* **Engineering Resolution:** Applied a bottom-up OSI troubleshooting approach. Verified basic layer 3 IP route reachability using `ping` and `traceroute`, verified layer 4 stateful socket connections with `telnet`, and inspected layer 7 HTTP response headers (`301`/`302` redirects) using `curl`.
* **"What If" Scenario:** In a production microservices environment, instead of manual CLI execution across individual instances, I would implement **AWS VPC Reachability Analyzer** and **CloudWatch Network Monitor** to automatically trace path connectivity and trigger alerts for packet drop anomalies.

## 📊 Technical Competence
* **Demonstrated Skills:** Network Diagnostics, OSI Layer Isolation, CLI Administration, Stateful Connection Inspection, and Application Header Analysis.
