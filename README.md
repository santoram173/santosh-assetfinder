# santosh-assetfinder
Educational cybersecurity-style asset discovery dashboard for OSINT learning, DNS/IP visualization, and simulated security intelligence analysis.
# 🔍 SantoshAssetFinder

> **Live Cyber Asset Discovery & External Attack Surface Reconnaissance Tool**

[![License: MIT](https://img.shields.io/badge/License-MIT-cyan.svg)](LICENSE)
[![Status: Live](https://img.shields.io/badge/Status-Live-brightgreen.svg)]()
[![Free Tool](https://img.shields.io/badge/Free-Tool-blue.svg)]()
[![Authorized Use Only](https://img.shields.io/badge/Use-Authorized%20Only-red.svg)]()

**SantoshAssetFinder** is a free, browser-based external attack surface reconnaissance tool. Enter any domain and instantly discover subdomains, DNS records, SSL certificates, IP addresses, geolocation data, and WHOIS/RDAP information — all powered by live public APIs with no server-side infrastructure required.

🌐 **Live Demo:** https://santoram173.github.io/santosh-assetfinder/

---

## ✨ Features

| Feature | Description | API Source |
|---|---|---|
| **Subdomain Enumeration** | Discovers subdomains via certificate transparency logs | crt.sh |
| **DNS Records** | Resolves A, AAAA, MX, NS, TXT, CNAME, SOA records | Cloudflare DoH (1.1.1.1) |
| **WHOIS / RDAP** | Retrieves registrar, creation/expiry dates, nameservers | rdap.org |
| **IP Geolocation** | Maps IPs to city, country, ISP, ASN, cloud hosting flags | ip-api.com |
| **IP Resolution** | Resolves hostnames to IPv4 addresses | Cloudflare DoH |
| **Risk Scoring** | Classifies assets as Low / Medium / High risk | Built-in heuristics |
| **Live Terminal Log** | Real-time step-by-step reconnaissance output | — |
| **Export** | Download results as CSV or JSON, or copy to clipboard | — |

---

## 🚀 Getting Started

### Option A — Use Online (Recommended)
Visit the live GitHub Pages deployment — no installation required.

### Option B — Run Locally
```bash
git clone https://github.com/YOUR-USERNAME/santosh-assetfinder.git
cd santosh-assetfinder
python3 -m http.server 8080
# Open http://localhost:8080 in your browser
```

> **Note:** Running from `file://` will cause CORS errors with live APIs. Always serve via a local web server.

---

## 🔌 Data Sources & Third-Party APIs

This tool uses the following **publicly available, free APIs**:

| API | Purpose | Terms |
|---|---|---|
| [crt.sh](https://crt.sh) | Certificate transparency log search | Public / Free |
| [Cloudflare DoH](https://developers.cloudflare.com/1.1.1.1/encryption/dns-over-https/) | DNS-over-HTTPS resolution | Public / Free |
| [rdap.org](https://rdap.org) | WHOIS via RDAP protocol | Public / Free |
| [ip-api.com](https://ip-api.com) | IP geolocation | Free (non-commercial) |

All data returned is **publicly accessible information**. This tool does not perform active port scanning, exploit testing, or any intrusive operations.

---

## ⚖️ Legal Notice & Disclaimer

**IMPORTANT — READ BEFORE USE**

This tool is provided for **educational, research, and authorized security testing purposes only**.

### ✅ Permitted Uses
- Scanning domains/infrastructure **you own or have explicit written authorization to test**
- Security audits performed by authorized professionals
- Bug bounty reconnaissance within defined program scope
- Academic and educational security research

### ❌ Prohibited Uses
- Scanning systems without explicit owner authorization
- Using results to plan, assist, or execute cyberattacks
- Any activity that violates applicable local, national, or international law

### ⚠️ Legal Framework
Unauthorized use of this tool may violate:
- **USA:** Computer Fraud and Abuse Act (CFAA), 18 U.S.C. § 1030
- **UK:** Computer Misuse Act 1990
- **EU:** Directive 2013/40/EU on attacks against information systems
- **Canada:** Criminal Code, Section 342.1
- Other equivalent cybercrime legislation in your jurisdiction

**The author accepts no liability** for any damages, legal consequences, or misuse resulting from this tool. By using SantoshAssetFinder, you confirm you have proper authorization for all targets scanned.

---

## 🔒 Privacy Policy

- **No data is collected, stored, or transmitted** to any server operated by this project
- All API calls are made **directly from your browser** to third-party services
- No cookies, tracking scripts, or analytics are used
- Scan results exist only in your browser session and are never saved server-side
- Third-party APIs (crt.sh, Cloudflare, rdap.org, ip-api.com) have their own privacy policies

---

## 🏗️ Architecture

```
Browser (Client-Only)
    │
    ├── crt.sh API          → Certificate transparency / subdomain discovery
    ├── Cloudflare DoH      → DNS record resolution
    ├── rdap.org            → WHOIS / domain registration data
    └── ip-api.com          → IP geolocation intelligence
```

Zero backend. Zero database. Zero tracking. Pure client-side HTML/CSS/JS.

---

## 📄 License

Copyright © 2026 Santosh. Released under the [MIT License](LICENSE).

The MIT License permits free use, modification, and distribution with attribution.
See [LICENSE](LICENSE) for full terms including the legal notice on authorized use.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📞 Contact

For security concerns, responsible disclosure, or authorized-use inquiries, open a GitHub Issue.

---

*Built with ♥ for the security community. Use responsibly.*
