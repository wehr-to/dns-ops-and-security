# 🌐 dns-ops-and-security

This repository explores DNS from both operational and security perspectives. It includes labs, threat detection techniques, protocol comparisons, and real-world misconfig scenarios. DNS is often a blind spot, this repo aims to change that.

## 🧠 Why This Repo Exists

DNS is one of the most exploited and least understood layers in modern infrastructure. From **tunneling** and **data exfiltration**, to **misconfigured records**, to **abuse of DNS over HTTPS (DoH)** — DNS is where visibility often breaks down.

This project simulates what secure, well-observed DNS looks like — across on-prem, cloud, and encrypted transports.

## 📦 Key Topics Covered

| Area                   | Description |
|------------------------|-------------|
| `dns-basics/`          | How resolution works, record types, caching behavior |
| `dns-security/`        | Tunneling detection, DNSSEC validation, sinkholes |
| `dns-over-encryption/` | DoH vs DoT, Cloudflare & Firefox testing, Wireshark side-by-side |
| `split-horizon-dns/`   | Use cases, risks, and split config with BIND |
| `cloud-dns/`           | Route 53 & GCP DNS security and visibility best practices |
| `/etc/hosts-labs/`     | TTL tricks, redirect scenarios, simulation of tampered entries |
| `labs/`                | Traffic manipulation, spoofing, logging visibility tests |

## 🧪 Example Lab: Detecting DNS Tunneling

- Deploy `tcpdump` and capture DNS traffic
- Look for long Base64-style payloads in TXT records
- Use `dnstop` or `Wireshark` to graph query length vs entropy
- Simulate detection using Suricata or Zeek signatures

## 🛠 Tools Used

- `tcpdump`, `dnstop`, `dig`, `nslookup`
- `Wireshark`, `Suricata`, `Zeek`
- `dnsmasq`, `BIND`, `Unbound`
- Cloudflare DoH CLI, Firefox DoH, Route 53 configs

## 👥 Who Should Use This

- Blue teamers building detection logic for DNS abuse
- Infra and SRE engineers hardening DNS in cloud or hybrid environments
- Red teamers learning covert channel techniques
- Students preparing for Security+, CySA+, OSCP, or lab interviews

## 📘 Lab Scenarios Include

- Modifying `/etc/hosts` to simulate MITM redirection
- DNS tunneling detection (data exfil via TXT records)
- TTL misconfig and cache poisoning implications
- Split-horizon DNS attack surface exploration
- Comparing DoH vs standard DNS in Wireshark

