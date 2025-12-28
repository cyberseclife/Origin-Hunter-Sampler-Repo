# 🏛️ ORIGIN-HUNTER v1.0
> **Elite Attack Surface Mapping & WAF-Bypass Suite**

Origin-Hunter is a surgical reconnaissance engine built to strip away the "Security Theater" of modern Web Application Firewalls. While standard tools rely on basic brute-forcing, Origin-Hunter utilizes live infrastructure fingerprints to expose the "True Origin" servers that targets think are hidden.

---

## 🔥 Key Technical Advantages

* **🎯 The SSL Sniper:** Automatically extracts Subject Alternative Names (SANs) from live SSL certificates to discover subdomains that never appear in standard wordlists.
* **📡 Origin-Match Engine:** Uses a high-fidelity **Body_Match(100%)** algorithm to identify the raw IP address of the backend server. If a server serves the target’s content without WAF headers, it flags a Critical bypass.
* **🛡️ WAF Fingerprinting:** Native detection for AWS WAF, Cloudflare, and Akamai, providing immediate context on the target's defensive layer.
* **⚡ The Siege Engine:** Optimized Go-concurrency capable of processing **4.8M+ record wordlists** with ultra-stable thread management and zero connection poisoning.
* **📦 Zero-Dependency Binary:** Statically linked for Linux; move the binary to your Proxmox lab or a remote VPS and start the hunt instantly.

---

## 📸 Product in Action
![Scan Results](assets/hero_shot.png)
*Figure 1: High-concurrency origin discovery with 100% Body Match verification.*

---

## 🛡️ Founders Edition Pricing
Origin-Hunter is currently in **Early Access Launch**. Secure your license now at 50% off the standard retail price.

* **Status:** 🟢 20/20 Early Bird Licenses Remaining
* **Launch Price:** $249.99 USD (One-time payment) Runs from 12/28/25-1/15/26
* **Includes:** Statically linked v1.0 binary, lifetime v1.x updates, and implementation documentation.

---

## 💳 How to Purchase
To acquire a commercial license and the v1.0 binary, please use the authorized payment link below.

[**→ Get Origin-Hunter Founders License - $249.99**](https://cyberguardian78.gumroad.com/l/tqxegc)

---

## 🛠️ Quick Start (Post-Purchase)
Once you have received your binary, simply set permissions and run:

```bash
chmod +x origin-hunter
./origin-hunter -t example.com -w wordlist.txt -threads 100
or for global availability
go install .
or
sudo cp origin-hunter /usr/local/bin/origin-hunter
