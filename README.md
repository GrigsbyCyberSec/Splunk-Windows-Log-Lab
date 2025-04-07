# Splunk Windows Log Analysis Lab

## 🔧 Tools Used
- Splunk Enterprise (Free Trial)
- Windows Event Logs
- EventCode 4625 (Failed Login Events)

## 🎯 Objective
Simulate real-world log analysis by detecting failed login attempts (EventCode 4625) on a Windows system using Splunk. This lab demonstrates the ability to search, filter, and visualize system log data—core skills for security analysts.

## 🧪 What I Did
- Installed Splunk Enterprise on a local Windows machine
- Ingested Windows Event Logs into Splunk via the local event log monitor
- Queried logs using:
  - `index=main EventCode=4625`
  - `index=main EventCode=4625 | stats count by Account_Name`
- Analyzed failed login patterns and created visualizations using the Splunk interface

## 📸 Screenshots

### Search Results for Failed Logins
![Failed Logins Search](images/splunk_failed_login_search.png)

### Grouped Login Attempts by Account Name
![Stats by Account Name](images/splunk_login_stats_by_account.png)

## 🧠 What I Learned
- How to identify and investigate Windows login failure events
- Use of Splunk's search language (SPL) to filter and analyze logs
- Recognized that failed logins can originate from system accounts (machine accounts with `$`) in addition to user accounts
- Confirmed that not all failed logins indicate malicious activity—but they can be an early sign of brute-force or misconfigurations

## ✅ Next Steps
- Simulate failed logins from a real user account to enrich dataset
- Explore EventCode 4624 (successful logins)
- Set up basic alerts for multiple failed logins in a short timeframe
