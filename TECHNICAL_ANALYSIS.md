# Technical Analysis: LethalCompany

## Sample Info
- Type: Python Infostealer
- Platform: Windows
- Capabilities: Credential theft, keylogging, screenshots

## Key Findings:

### Persistence (T1547.001)
- Registry: HKCU\Software\Microsoft\Windows\CurrentVersion\Run\WindowsGfxDriver
- File: %APPDATA%\WindowsGraphics\win_gfx_driver.exe

### Data Theft (T1555.003)
- Targets: Chrome, Edge, Brave, OperaGX
- Method: DPAPI + AES-GCM decryption
- SQL: SELECT origin_url, username_value, password_value FROM logins

### Exfiltration (T1567.002)
- Discord webhooks for C2
- User ID: 773495051854675979
- Keywords: login, bank, steam, gmail, wallet

### Surveillance
- Keylogger: 60s intervals
- Screenshots: Every 2 mins + critical triggers

## MITRE ATT&CK:
- T1547.001, T1555.003, T1056.001, T1113, T1567.002
