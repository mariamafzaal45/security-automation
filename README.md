# THE ARZENS 

## Threat Intelligence Automation & Infrastructure as Code Security

This repository contains  **THE ARZENS (TAS) Engineering Internship Program — AI, Automation & Security Engineering Track**.

The project focuses on two major areas:

* 🛡️ Threat Intelligence Automation
* ☁️ Infrastructure as Code (IaC) Security

---

## 📌 Project Overview

### Week 06 — Threat Intelligence Automation

This section focuses on collecting, enriching, scoring, and managing Indicators of Compromise (IOCs).

**Tasks:**

1. Threat Intelligence Platform Architecture
2. Threat Intelligence Enrichment Engine
3. IOC Manager & Automation

The enrichment engine integrates threat intelligence sources such as:

* VirusTotal
* AbuseIPDB
* AlienVault OTX
* MISP

Features include:

* IOC validation
* Threat enrichment
* Risk scoring
* Confidence scoring
* API rate-limit handling
* Caching
* IOC expiration
* SIEM blocklist export
* Automated reporting

---

### Week 07 — Infrastructure as Code Security

This section focuses on securely deploying and configuring cloud infrastructure using:

* Terraform
* Ansible
* AWS

**Tasks:**

4. IaC Security Architecture
5. Secure Terraform Infrastructure
6. Ansible Hardening & Compliance

Security controls include:

* Secure VPC configuration
* Restricted security groups
* Private and encrypted S3 storage
* EC2 hardening
* SSH hardening
* Firewall configuration
* Fail2ban
* Audit logging
* Compliance checks
* Infrastructure validation

---

## 📂 Repository Structure

```text
Week06_07_Assignment/
│
├── Week06_TI/
│   ├── Task1_TI_Architecture/
│   ├── Task2_TI_Enrichment/
│   └── Task3_IOC_Manager/
│
├── Week07_IaC/
│   ├── Task4_IaC_Architecture/
│   ├── Task5_Terraform/
│   └── Task6_Ansible/
│
└── MASTER_README.md
```

---

## 🔐 API Keys & Credentials

**Never upload real API keys, AWS credentials, passwords, or secrets to GitHub.**

Use placeholders such as:

```text
YOUR_VIRUSTOTAL_API_KEY
YOUR_ABUSEIPDB_API_KEY
YOUR_OTX_API_KEY
```

For AWS, configure credentials through the AWS CLI or environment variables.

Add sensitive files such as:

```text
terraform.tfvars
.env
```

to `.gitignore`.

---

## 🛠️ Technologies Used

| Technology     | Purpose                        |
| -------------- | ------------------------------ |
| Python         | Threat intelligence automation |
| VirusTotal     | IOC enrichment                 |
| AbuseIPDB      | IP reputation                  |
| AlienVault OTX | Threat intelligence            |
| MISP           | Threat intelligence platform   |
| JSON           | IOC storage                    |
| Terraform      | Infrastructure provisioning    |
| AWS            | Cloud infrastructure           |
| Ansible        | Configuration management       |
| UFW            | Firewall                       |
| Fail2ban       | Attack protection              |
| Auditd         | Security auditing              |

---

## ▶️ Running the TI Enrichment Tool

Install dependencies:

```bash
pip install -r requirements.txt
```

Single IOC:

```bash
python ti_enricher.py --indicator 8.8.8.8
```

Batch processing:

```bash
python ti_enricher.py --input-file sample_indicators.csv
```

JSON output:

```bash
python ti_enricher.py --indicator 8.8.8.8 --format json
```

CSV output:

```bash
python ti_enricher.py --input-file sample_indicators.csv --format csv
```

---

## ▶️ Running the IOC Manager

Add IOCs:

```bash
python ioc_manager.py --add-file sample_indicators.csv
```

Update IOCs:

```bash
python ioc_manager.py --update-all
```

Check expired IOCs:

```bash
python ioc_manager.py --expire-check
```

Export SIEM blocklist:

```bash
python ioc_manager.py --export-blocklist
```

---

## ☁️ Terraform

Initialize Terraform:

```bash
terraform init
```

Format:

```bash
terraform fmt
```

Validate:

```bash
terraform validate
```

Create a plan:

```bash
terraform plan
```

Apply infrastructure:

```bash
terraform apply
```

Destroy test infrastructure:

```bash
terraform destroy
```

Always review the Terraform plan before applying changes.

---

## 🔧 Ansible

Test connectivity:

```bash
ansible all -m ping
```

Run the complete playbook:

```bash
ansible-playbook site.yml
```

Run security hardening:

```bash
ansible-playbook security.yml
```

Perform a dry run:

```bash
ansible-playbook site.yml --check --diff
```

---

## 🧪 Security Considerations

This project follows basic security best practices including:

* Least-privilege access
* No hard-coded credentials
* API rate-limit handling
* Local caching
* IOC lifecycle management
* Restricted network access
* Encrypted storage
* SSH hardening
* Firewall configuration
* Audit logging
* Compliance validation

---

## 📚 References

* MISP Project
* VirusTotal API Documentation
* AbuseIPDB API Documentation
* AlienVault OTX
* HashiCorp Terraform Security Best Practices
* AWS Security Best Practices
* Ansible Documentation

---

## 👩‍💻 Author

**Mariam Afzaal**

THE ARZENS
AI, Automation & Security Engineering Track

---

## ⚠️ Disclaimer

This repository was created for **educational and internship purposes**.

Only use the tools and configurations on systems and infrastructure that you own or have explicit permission to test.

Real API credentials and cloud credentials should never be committed to this repository.
