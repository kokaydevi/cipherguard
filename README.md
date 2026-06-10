# 🔐 CipherGuard — Password Strength Analyzer

> A cybersecurity tool that analyzes password strength in real time, detects data breaches using the HaveIBeenPwned API, and generates cryptographically random passwords — all in a single HTML file with zero setup.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![HaveIBeenPwned](https://img.shields.io/badge/API-HaveIBeenPwned-red?style=flat)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)

---

## 🖥️ Live Demo

**[→ Open CipherGuard](https://kokaydevi.github.io/cipherguard/password-checker.html)**


---

## 📸 Screenshot

![CipherGuard Screenshot](screenshot.png)

<img width="1600" height="696" alt="WhatsApp Image 2026-06-10 at 2 03 53 PM" src="https://github.com/user-attachments/assets/3a203c62-0bda-4385-8962-5e11c6b4110f" />
<img width="1600" height="845" alt="WhatsApp Image 2026-06-10 at 2 04 09 PM" src="https://github.com/user-attachments/assets/3ca58ae7-a0df-4796-9e5d-03b4940d761f" />


# 🔐 CipherGuard — Password Strength Analyzer

> A cybersecurity tool that analyzes password strength in real time, detects data breaches using the HaveIBeenPwned API, and generates cryptographically random passwords — all in a single HTML file with zero setup.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![HaveIBeenPwned](https://img.shields.io/badge/API-HaveIBeenPwned-red?style=flat)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)

---


## ✨ Features

| Feature | Description |
|---|---|
| 🔴 **Strength Meter** | Rates password as Weak / Medium / Strong / Very Strong with animated color bar |
| ⚡ **Real-time Analysis** | Strength, score, and suggestions update instantly as you type |
| 🛡️ **Breach Detection** | Checks HaveIBeenPwned's database of 10+ billion leaked passwords |
| 💡 **Smart Suggestions** | Tells you exactly what's missing to make your password stronger |
| ⚙️ **Password Generator** | Generates cryptographically secure passwords with custom length and character sets |
| 📊 **Security Score /100** | Weighted score based on length, character variety, and common pattern penalties |
| 📋 **Copy to Clipboard** | One-click copy of any generated password |
| 📱 **Mobile Friendly** | Fully responsive — works on any screen size |

---

## 🔒 Privacy — How the Breach Check Works

This tool uses **k-Anonymity** — a privacy model that means your password is **never sent over the network**.

Here's exactly what happens:

```
1. Your password is SHA-1 hashed locally in the browser
   "mypassword" → "91DFD9DDB4198AFBE5EFE6F4F80F7C21"

2. Only the FIRST 5 characters of the hash are sent to the API
   API receives → "91DFD"

3. The API returns ALL hashes that begin with "91DFD" (hundreds of them)

4. Your browser checks if YOUR full hash is in that list — locally
   No one ever sees your actual password or full hash
```

This is the same method used by browsers like Firefox and Chrome for their built-in breach alerts.

---

## 🚀 How to Use

### Option 1 — Just open the file
```
1. Download password-checker.html
2. Double-click to open in any browser
3. Done — no installation, no server, no dependencies
```

### Option 2 — Clone the repo
```bash
git clone https://github.com/your-username/cipherguard.git
cd cipherguard
# Open password-checker.html in your browser
```

---

## 📊 Scoring System

The Security Score (0–100) is calculated as follows:

| Criteria | Points |
|---|---|
| 6+ characters | +5 |
| 8+ characters | +10 |
| 12+ characters | +10 |
| 16+ characters | +10 |
| 20+ characters | +10 |
| 32+ characters | +5 |
| Has uppercase letters | +10 |
| Has lowercase letters | +10 |
| Has numbers | +10 |
| Has special characters | +10 |
| All 4 character types | +10 (bonus) |
| **Penalties** | |
| All lowercase only | −10 |
| All numbers only | −15 |
| Repeated characters (aaa) | −10 |
| Contains common words (password, 123456…) | −20 |

---

## 🛠️ Tech Stack

- **Frontend:** Pure HTML5, CSS3, Vanilla JavaScript
- **API:** [HaveIBeenPwned v3](https://haveibeenpwned.com/API/v3) — free, no API key required
- **Hashing:** Web Crypto API (`crypto.subtle.digest`) — runs in browser
- **Randomness:** `crypto.getRandomValues()` — cryptographically secure
- **No backend, no framework, no build tools, no dependencies**

---

## 📁 Project Structure

```
cipherguard/
│
├── password-checker.html    # The entire application (single file)
└── README.md                # This file
```

---

## 🎓 About This Project

Built as part of my **Cybersecurity Internship** with **CSRBOX in partnership with IBM**, under the guidance of trainer **Ayush Kumar**.

This project demonstrates practical application of:
- Client-side cryptography (SHA-1, k-Anonymity)
- Secure API integration without exposing sensitive data
- Real-time UI feedback for security decisions
- Cryptographically secure random number generation

**Semester 5 — B.Tech Computer Engineering**

---

## 📄 License

MIT License — feel free to use, modify, and share.

---

## 🙏 Acknowledgements

- [HaveIBeenPwned](https://haveibeenpwned.com/) by Troy Hunt for the breach database API
- [Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API) — MDN Documentation

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔴 **Strength Meter** | Rates password as Weak / Medium / Strong / Very Strong with animated color bar |
| ⚡ **Real-time Analysis** | Strength, score, and suggestions update instantly as you type |
| 🛡️ **Breach Detection** | Checks HaveIBeenPwned's database of 10+ billion leaked passwords |
| 💡 **Smart Suggestions** | Tells you exactly what's missing to make your password stronger |
| ⚙️ **Password Generator** | Generates cryptographically secure passwords with custom length and character sets |
| 📊 **Security Score /100** | Weighted score based on length, character variety, and common pattern penalties |
| 📋 **Copy to Clipboard** | One-click copy of any generated password |
| 📱 **Mobile Friendly** | Fully responsive — works on any screen size |

---

## 🔒 Privacy — How the Breach Check Works

This tool uses **k-Anonymity** — a privacy model that means your password is **never sent over the network**.

Here's exactly what happens:

```
1. Your password is SHA-1 hashed locally in the browser
   "mypassword" → "91DFD9DDB4198AFBE5EFE6F4F80F7C21"

2. Only the FIRST 5 characters of the hash are sent to the API
   API receives → "91DFD"

3. The API returns ALL hashes that begin with "91DFD" (hundreds of them)

4. Your browser checks if YOUR full hash is in that list — locally
   No one ever sees your actual password or full hash
```

This is the same method used by browsers like Firefox and Chrome for their built-in breach alerts.

---

## 🚀 How to Use

### Option 1 — Just open the file
```
1. Download password-checker.html
2. Double-click to open in any browser
3. Done — no installation, no server, no dependencies
```

### Option 2 — Clone the repo
```bash
git clone https://github.com/your-username/cipherguard.git
cd cipherguard
# Open password-checker.html in your browser
```

---

## 📊 Scoring System

The Security Score (0–100) is calculated as follows:

| Criteria | Points |
|---|---|
| 6+ characters | +5 |
| 8+ characters | +10 |
| 12+ characters | +10 |
| 16+ characters | +10 |
| 20+ characters | +10 |
| 32+ characters | +5 |
| Has uppercase letters | +10 |
| Has lowercase letters | +10 |
| Has numbers | +10 |
| Has special characters | +10 |
| All 4 character types | +10 (bonus) |
| **Penalties** | |
| All lowercase only | −10 |
| All numbers only | −15 |
| Repeated characters (aaa) | −10 |
| Contains common words (password, 123456…) | −20 |

---

## 🛠️ Tech Stack

- **Frontend:** Pure HTML5, CSS3, Vanilla JavaScript
- **API:** [HaveIBeenPwned v3](https://haveibeenpwned.com/API/v3) — free, no API key required
- **Hashing:** Web Crypto API (`crypto.subtle.digest`) — runs in browser
- **Randomness:** `crypto.getRandomValues()` — cryptographically secure
- **No backend, no framework, no build tools, no dependencies**

---

## 📁 Project Structure

```
cipherguard/
│
├── password-checker.html    # The entire application (single file)
└── README.md                # This file
```

---

## 🎓 About This Project

Built as part of my **Cybersecurity Internship** with **CSRBOX in partnership with IBM**, under the guidance of trainer **Ayush Kumar**.

This project demonstrates practical application of:
- Client-side cryptography (SHA-1, k-Anonymity)
- Secure API integration without exposing sensitive data
- Real-time UI feedback for security decisions
- Cryptographically secure random number generation

**Semester 5 — B.Tech Computer Engineering**

---

## 📄 License

MIT License — feel free to use, modify, and share.

---

## 🙏 Acknowledgements

- [HaveIBeenPwned](https://haveibeenpwned.com/) by Troy Hunt for the breach database API
- [Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API) — MDN Documentation
