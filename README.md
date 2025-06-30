# Task 5: Capture and Analyze Network Traffic Using Wireshark

## Objective
Capture live packets using Wireshark, identify at least **three different network protocols**, and develop hands-on experience in packet analysis and protocol awareness.

---

## Tools Used
- **Wireshark** – Network protocol analyzer
- **Command Prompt** – To generate traffic (`ping`, `nslookup`)
- **Chrome** – To visit websites and generate HTTP traffic

---

## Steps Performed

1. **Installed Wireshark** on the system.
2. **Started live capture** on the active network interface (Wi-Fi).
3. Generated traffic by:
   - Visiting websites (e.g., `tryhackme.com`, `github.com`, `google.com`, `cisco.com`)
   - Running the command: `ping google.com`
   - Performing DNS lookup using: `nslookup cocsit.org.in`
4. **Stopped the capture** after 2 minutes.
5. **Applied protocol filters** in Wireshark:
   - `http`
   - `dns`
   - `tcp`
   - `icmp`
6. Identified and analyzed packet details for each protocol.
7. Exported the capture as a `.pcapng` file.

---

## Protocols Identified and Analyzed

| Protocol | Description                          | Function |
|----------|--------------------------------------|----------|
| **HTTP** | HyperText Transfer Protocol          | Used for loading web pages |
| **DNS**  | Domain Name System                   | Resolves domain names to IP addresses |
| **TCP**  | Transmission Control Protocol        | Ensures reliable data transmission |
| **ICMP** | Internet Control Message Protocol    | Used for network diagnostics (e.g., ping) |

---

## Files

-`capture_running.png` – Live capture in progress  
- `task5-capture.pcapng` – Exported capture file
- `http_filter.png` – Filtered view showing HTTP packets  
- `dns_query.png` – DNS query packet details  
- `icmp_ping.png` – ICMP echo request and reply packets (NO packets)
- `icmpv6_ping.png` - ICMPv6 echo request and reply packets
- `tcp_flags.png` – TCP handshake packets (SYN, ACK)


---

## 📌 Key Wireshark Filters Used

```wireshark
http        # To see HTTP GET/POST requests
dns         # To view DNS queries and responses
tcp         # To analyze TCP handshakes and sessions
icmp        # To observe ping-related packets (NO packets)
icmpv6        # To observe ping-related packets
