# IAM Least Privilege Enforcement

## Objective
To automate the detection of over-permissioned IAM identities in AWS by comparing the permissions granted versus those actually used. This project enforces the Principle of Least Privilege and supports cloud security audits aligned with NIST CSF and CIS benchmarks.

---

##  Background
Over-permissioned IAM users and roles are a leading cause of lateral movement in cloud breaches. Many accounts have broad permissions they never use, increasing the attack surface. This tool identifies and flags such risks, allowing security teams to take preventive action.

---

##  Tools & Technologies Used
- **AWS CLI / Boto3 (Python SDK)** – Access AWS IAM data programmatically.
- **IAM Access Analyzer** – Review permissions granted and detect unused ones.
- **Python (Pandas, Boto3, Matplotlib)** – Data analysis and visualization.
- **Streamlit** – For an interactive web-based dashboard.

---

##  Architecture
1. Extract IAM user and role policies using AWS CLI/Boto3.
2. Use Access Analyzer or CloudTrail logs to evaluate actual service usage.
3. Compare permissions granted vs used.
4. Visualize and flag over-permissioned accounts.
5. Generate a remediation report.

---

## 📸 Screenshot

---![IAM_Least_Privilege_Screenshot](https://github.com/user-attachments/assets/20f8006c-ef17-4e47-bb93-c3096fe54ee8)

---

##  Sample Findings
| IAM User | Permissions Granted | Permissions Used | Over-Permission (%) | Action Needed |
|----------|---------------------|------------------|----------------------|----------------|
| Alice    | 20                  | 5                | 75%                  | ✅ Review & Remove |
| Bob      | 50                  | 10               | 80%                  | ✅ High Risk |
| Charlie  | 80                  | 30               | 62.5%                | ⚠️ Moderate Risk |


---

##  Skills Learned
- Cloud security principles (Least Privilege, Identity Hardening)
- AWS IAM and Access Analyzer
- Python scripting with AWS APIs
- Risk quantification and dashboard visualization
- Compliance mapping (NIST, CIS Benchmarks)

---

##  Compliance Standards Referenced
- **NIST 800-53**: AC-6 Least Privilege
- **NIST Cybersecurity Framework** (Identify/Protect)
- **CIS AWS Foundations Benchmark v1.4**
- **ISO/IEC 27001:2022** – A.9.2.3 Management of privileged access rights

---

## 🔗 References
- [AWS IAM Access Analyzer](https://docs.aws.amazon.com/IAM/latest/UserGuide/access-analyzer.html)
- [CIS AWS Benchmark](https://www.cisecurity.org/benchmark/amazon_web_services)
- [NIST CSF](https://www.nist.gov/cyberframework)




