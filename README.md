# 🛡️ Internal Certificate Authority with OpenSSL

This project simulates the setup of an **internal Certificate Authority (CA)** using OpenSSL, allowing a company to issue HTTPS certificates to internal applications **without paying for commercial SSL certificates**.

---

## 📌 Features

- ✅ Self-signed CA setup with a secure private key
- ✅ Signed HTTPS certificates for internal domains (e.g., `devportal.altschool.local`)
- ✅ Certificate Signing Requests (CSR) and validation
- ✅ End-to-end certificate chain verification
- ✅ All steps and outputs logged in `report.txt`

---

## 🧰 Tools Used

- `OpenSSL`
- Linux shell (tested on Kali/Ubuntu)
- Git for version control

---

## 🛠️ How It Works

### 🔐 Task 1: Create CA Infrastructure
- Generate CA private key (`ca.key.pem`)
- Create self-signed CA certificate (`ca.cert.pem`)

### 🌐 Task 2: Issue Certificate to Web Server
- Generate private key and CSR for `devportal.altschool.local`
- Sign CSR using your CA to generate `devportal.cert.pem`

### ✅ Task 3: Verify Chain
- Use `openssl verify` to validate the server cert against the CA

---
## 📂 File Structure
internal-ca/
├── ca/
│ ├── ca.cert.pem
│ ├── ca.key.pem
│ └── ca.srl
├── server/
│ ├── devportal.cert.pem
│ ├── devportal.csr.pem
│ └── devportal.key.pem
├── report.txt
└── README.md

yaml
Copy code

---

## 🚫 .gitignore

To protect sensitive files, the following are excluded from GitHub:

---

## 📖 Author

**Babatunde Goriola-Obafemi**  
Cybersecurity Associate | AltSchool Africa  
[GitHub Profile](https://github.com/Nobleteesage)
