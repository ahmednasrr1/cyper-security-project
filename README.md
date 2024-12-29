# cyper-security-project
OWASP Juice Shop Penetration Testing

Project Overview

This repository documents penetration testing against the OWASP Juice Shop to explore common vulnerabilities in web applications. It includes scenarios, methodologies, and outcomes to enhance understanding of attack techniques and defenses.

Directory Structure

📁 OWASP-Juice-Shop-Penetration-Testing
├── 📁 Attack-Scenarios
│   ├── 1-Enumeration-to-Find-Admin-Path.md
│   ├── 2-Brute-Force-Admin-Credentials.md
│   └── 3-XSS-in-Product-Search.md
├── 📁 Resources
│   ├── Tools.md
│   └── Useful-Links.md
├── 📁 Reports
│   ├── Executive-Summary.md
│   ├── Vulnerabilities-Report.md
│   ├── Exploitation-and-Simulation.md
│   └── Conclusion.md
├── 📁 Videos
│   └── Video-Report.mp4
├── README.md
└── LICENSE

1. Attack Scenarios

1.1 Enumeration to Find Admin Path
	•	Scenario:
The attacker explores the application, guessing or analyzing URL structures to discover hidden paths.
	•	Outcome:
The attacker identifies the admin functionality, opening possibilities for further exploitation.
	•	Tools:
	•	Gobuster
	•	Dirb

1.2 Brute Force on Admin Credentials
	•	Scenario:
After finding the admin login page, the attacker uses a tool like Hydra with the email admin@juice-sh.op to guess the password. The absence of rate-limiting or account lockout enables successful brute-forcing.
	•	Outcome:
Full admin access is achieved, granting complete control over the application.
	•	Tools:
	•	Hydra
	•	Burp Suite

1.3 Cross-Site Scripting (XSS) in Product Search
	•	Scenario:
The attacker injects malicious JavaScript into the product search bar. The unsanitized input reflects back to the user’s browser and executes.
	•	Outcome:
	•	Theft of session cookies.
	•	Redirection to malicious websites.
	•	Execution of arbitrary JavaScript.
	•	Tools:
	•	OWASP ZAP

2. Resources

Tools Used
	•	Hydra: For brute-force attacks.
	•	Burp Suite: Intercepting and modifying requests.
	•	Gobuster and Dirb: For URL enumeration.
	•	OWASP ZAP: For scanning and XSS payload injection.

Useful Links
	•	OWASP Juice Shop
	•	Kali Linux
