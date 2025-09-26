# Network Traffic and Web Performance Analysis

This project explores network traffic analysis, HTTP payload reconstruction, and web performance evaluation using packet captures (PCAPs) and HTTP Archive (HAR) files.  
The work is divided into three main components:

## Features & Methodology

### **Exercise 1 – Network Throughput Analysis**
- **Goal:** Analyze uplink throughput from 5 clients to a server within a 100-second trace.  
- **Key Tasks:**
  - Extract per-client throughput timelines (`get_data_transfer_intervals`).
  - Plot throughput of each client and total aggregated throughput.
  - Compute fraction of contribution per client over five 20-second intervals.
- **Tools:** Python, [Scapy](https://scapy.readthedocs.io/en/latest/), [Pyshark](https://github.com/KimiNewt/pyshark), `tshark`.

---

### **Exercise 2 – HTTP Payload Extraction**
- **Goal:** Capture, parse, and analyze HTTP responses.  
- **Key Tasks:**
  - Capture traffic with `tcpdump` and export raw payloads as hex dumps.
  - Reassemble and extract HTTP response payloads **without using packet parsing libraries**.
  - Compare compressed payload size with uncompressed plain-text size.
  - Compute compression ratio.
- **Tools:** Python, `gzip`, Wireshark, `tcpdump`, `tshark`.

---

### **Exercise 3 – Web Performance from HAR Files**
- **Goal:** Study web performance under varying network conditions using HAR traces.  
- **Key Tasks:**
  - Collect HAR traces with and without throttling.
  - Extract metrics: page load time, request counts, data size, content-type distributions.
  - Visualize with:
    - CDF of download times
    - CDF of response sizes
    - Scatter plots (resource size vs. download time)
- **Tools:** Python, [haralyzer](https://pypi.org/project/haralyzer/), matplotlib.

---

## 🛠️ Setup & Requirements

- Python 3.8+
- Jupyter Notebook
- Dependencies:
  ```bash
  pip install scapy pyshark haralyzer matplotlib
