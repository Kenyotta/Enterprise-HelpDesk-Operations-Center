\# KB-008 – Blue Screen (BSOD) Troubleshooting



\---



\# Overview



This Knowledge Base article provides the standard procedure for diagnosing and resolving Blue Screen of Death (BSOD) incidents within the Apex Manufacturing enterprise environment.



A BSOD indicates Windows encountered a critical system error that prevented the operating system from continuing safely. The objective of this procedure is to identify the cause, restore the workstation to service, and determine whether escalation is required.



\---



\# Category



Windows Operating System



\---



\# Supported Systems



\- Windows 10 Enterprise

\- Windows 11 Enterprise

\- Microsoft Intune

\- Microsoft Entra ID

\- Active Directory



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Tier 2 Desktop Support



\---



\# Estimated Resolution Time



\*\*20–45 minutes\*\*



\---



\# Symptoms



Users may report one or more of the following:



\- Blue screen displaying a STOP error

\- Unexpected system restart

\- Computer enters a restart loop

\- Windows fails to boot

\- Device freezes before restarting

\- Frequent crashes while working



\---



\# Possible Causes



\- Faulty hardware

\- Corrupted device drivers

\- Windows Update failure

\- Memory (RAM) errors

\- Storage device failure

\- Corrupted system files

\- Malware

\- BIOS or firmware issues

\- Third-party software conflicts



\---



\# Required Verification



Before troubleshooting, verify:



\- User identity

\- Computer name

\- Asset tag

\- Department

\- Recent hardware or software changes

\- Date and time the issue first occurred



\---



\# Resolution Procedure



\## Step 1 – Record the Stop Code



Document the following information displayed on the BSOD:



\- STOP Code

\- Error message

\- Driver name (if shown)

\- QR code (if available)



Example:



```text

STOP CODE:

CRITICAL\_PROCESS\_DIED

```



\---



\## Step 2 – Determine Whether Windows Boots



If Windows starts normally:



Continue with troubleshooting.



If Windows does not boot:



Attempt:



\- Automatic Repair

\- Safe Mode

\- Windows Recovery Environment (WinRE)



\---



\## Step 3 – Review Recent Changes



Ask the user whether any of the following occurred before the issue began:



\- Windows Update

\- New software installation

\- Driver installation

\- Peripheral device installation

\- BIOS update

\- Hardware replacement



Document all recent changes.



\---



\## Step 4 – Check Event Viewer



Open:



```

Event Viewer

Windows Logs

System

```



Review:



\- Critical Events

\- Error Events

\- BugCheck events

\- Disk errors

\- Driver failures



Document relevant Event IDs.



\---



\## Step 5 – Review Device Manager



Open:



```

Device Manager

```



Verify:



\- No devices display warning icons.

\- Drivers are functioning correctly.



If a driver issue is identified:



\- Roll back the driver.

\- Update to the approved enterprise version.



\---



\## Step 6 – Check System Files



Open an elevated Command Prompt.



Run:



```cmd

sfc /scannow

```



If corruption is detected and repaired:



Restart the workstation.



\---



\## Step 7 – Repair Windows Image



If system file corruption continues:



Run:



```cmd

DISM /Online /Cleanup-Image /RestoreHealth

```



Restart the workstation after completion.



\---



\## Step 8 – Check Disk Health



Run:



```cmd

chkdsk C: /scan

```



If disk errors are detected:



Schedule a full disk repair.



\---



\## Step 9 – Review Memory Health



Run:



```

Windows Memory Diagnostic

```



If memory errors are detected:



Escalate for hardware replacement.



\---



\## Step 10 – Verify Windows Updates



Open:



```

Settings

Windows Update

```



Verify:



\- Updates completed successfully

\- Failed updates addressed

\- Optional driver updates reviewed



\---



\# Validation



Verify the following:



\- Windows starts normally

\- User successfully signs in

\- No additional BSOD events occur

\- Applications launch successfully

\- Event Viewer shows no recurring critical errors

\- Device operates normally



\---



\# Common Stop Codes



| Stop Code | Possible Cause |

|-----------|----------------|

| CRITICAL\_PROCESS\_DIED | Corrupt system files or services |

| IRQL\_NOT\_LESS\_OR\_EQUAL | Faulty drivers or RAM |

| SYSTEM\_SERVICE\_EXCEPTION | Driver or application conflict |

| PAGE\_FAULT\_IN\_NONPAGED\_AREA | Memory or storage issue |

| MEMORY\_MANAGEMENT | RAM failure |

| KMODE\_EXCEPTION\_NOT\_HANDLED | Driver issue |

| INACCESSIBLE\_BOOT\_DEVICE | Storage or boot configuration |



\---



\# Common Issues



\## Restart Loop



Possible causes:



\- Corrupt Windows Update

\- Driver failure

\- Hardware fault



Resolution:



\- Boot into Safe Mode

\- Remove recent updates

\- Roll back drivers



\---



\## BSOD After Windows Update



Resolution:



\- Uninstall recent update

\- Restart workstation

\- Verify Windows stability

\- Pause updates if approved



\---



\## Driver Failure



Resolution:



\- Roll back the driver

\- Install the approved enterprise driver

\- Restart the workstation



\---



\## Hardware Failure Suspected



Indicators include:



\- Memory errors

\- SMART storage warnings

\- Overheating

\- Repeated hardware-related stop codes



Escalate for hardware diagnostics or replacement.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- Multiple BSOD events occur within 24 hours

\- System files cannot be repaired

\- Safe Mode inaccessible

\- Driver rollback unsuccessful

\- Hardware diagnostics fail



Escalate to the Infrastructure or Endpoint Engineering Team if:



\- Multiple workstations experience identical BSODs

\- Enterprise-wide driver issues are identified

\- Windows Update deployment causes widespread failures

\- Firmware or BIOS changes require enterprise remediation



\---



\# Ticket Documentation Example



\*\*Issue\*\*



User reported repeated Blue Screen errors with the stop code `IRQL\_NOT\_LESS\_OR\_EQUAL` after installing a new network adapter driver.



\*\*Resolution\*\*



Reviewed Event Viewer, identified the faulty driver, rolled back to the approved enterprise version, verified successful system startup, and confirmed no additional BSOD events occurred.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- KB-013-Windows-Update-Failure.md

\- KB-015-Software-Installation.md

\- RFC-002-Windows-Monthly-Patching.md

\- Infrastructure/Servers/

\- Security/Security-Baselines/

\- Asset-Inventory.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard Blue Screen (BSOD) troubleshooting procedure. |

