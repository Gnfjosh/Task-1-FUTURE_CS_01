# Task1-FUTURE_CS_01
# Task 1:Vulnerability Assessment Report for a Live Website
**Task ID:** FUTURE_CS_01
**Target:** http://zero.webappsecurity.com

## Project Overview
This project involves performing a comprehensive vulnerability assessment on a live test environment. The goal was to identify, classify,and provide weakness at both the infrastructure and application layers.

## Tool Used 
* **Nmap:** Used for network reconnaissance, port scanning, and service version detection.
* **OWAS ZAP (Zaproxy):** Used for automated web application scanning and identifying security misconfigurations.
* **Canva:** Used for the professional design and presentation of the final Vulnerability Assessment Report

## Key finding
1. **Outdated Infrastructure:** ZAP identified that the server is running ( Apache 2.2.6),an end-of-life software version with numerous known vulnerabilities.
2. **Missing Securityb Header:** ZAP identified several missing defensive headers,including X-Frame-Options (Clickjacking protection) and Contenting-Security-Policy.
3. **Absence of Anti-CRSF Token:** Critcal forms on thev website lack protection against Cross-Site Request Forgery (CRSF), which could allow unauthorized actions on behalf of authenticated users.

## Deliverables
* **[ https://www.canva.com/design/DAHDFr_8uJ0/R0M4Dj_IAed8smdz0yHLrQ/edit?utm_content=DAHDFr_8uJ0&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton]**: View the full, professionally designed report.
* **Evidence Folder:** Contains raw screenshots of Nmap ann ZAP  scan results as proof of work.

## Remediation Summary
* **Patching:** Upgade web server to a current,supported version (Apache 2.4.x or higher).
* **Configuration:** Implement missing HTTP security headers to mitigate common web attacks.
* **Development:** Integrate Anti-CRSF tokens into all state-changing web forms.
