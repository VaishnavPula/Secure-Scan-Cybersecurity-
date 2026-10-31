# SecureScan – Cybersecurity Vulnerability Scanner

A beginner-friendly Flask project for **authorized, educational website security checks**.

## Features
- Responsive dashboard UI
- Website URL input and validation
- Basic HTTP security-header review
- HTTPS/TLS certificate and negotiated protocol inspection
- Basic cookie attribute review
- Server/technology banner disclosure checks
- Severity labels and an indicative score
- PDF report export
- Recent scan history stored locally in `scan_history.json`

## Safety scope
Only scan websites you own or have explicit written permission to test. This project performs non-invasive checks only. It does **not** exploit vulnerabilities, brute-force credentials, crawl sites, or perform arbitrary port scans. It blocks private/local/reserved IP addresses and disables redirects so a scan cannot silently move to a different host. The score is educational and is not a guarantee that a website is secure.

## Requirements
- Python 3.10+
- Internet connection for scanning public websites

## Setup on Windows (PowerShell)
```powershell
cd cybersecurity_vulnerability_scanner
py -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
python app.py
```

If PowerShell blocks activation, run this for the current terminal:
```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\venv\Scripts\Activate.ps1
```

Open `http://127.0.0.1:5000` in your browser.

## Setup on macOS / Linux
```bash
cd cybersecurity_vulnerability_scanner
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Suggested demo
Use a public website only when you have permission to assess it. A website that redirects may return a redirect response; this scanner intentionally does not follow redirects. Try a domain you control and compare its findings before and after configuring security headers.

## Project structure
```text
cybersecurity_vulnerability_scanner/
├── app.py
├── requirements.txt
├── README.md
├── templates/
│   └── index.html
└── static/
    └── style.css
```

## Limitations / future improvements
- Add authentication and per-user scan history.
- Add CSV export and scheduled scans.
- Add configurable authorized port checks with strict scope controls.
- Add unit tests and a richer TLS configuration audit.
- Add CSRF protection and production deployment configuration before public hosting.

## Disclaimer
This software is provided for learning. The user is responsible for obtaining authorization before scanning any target. Do not use it against systems without permission.
