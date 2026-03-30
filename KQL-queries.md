# KQL Queries for Incident Response

This file contains a community-contributed list of Kusto Query Language (KQL) queries useful for incident response and threat hunting. Students are encouraged to add their own queries!

---

## Getting Started with KQL

KQL (Kusto Query Language) is used in Microsoft Sentinel, Microsoft Defender, and Azure Monitor to search and analyse log data. It is a powerful tool for security analysts and incident responders.

---

## Contributed Queries

### 1. List all failed sign-in attempts
```kql
SigninLogs
| where ResultType != 0
| project TimeGenerated, UserPrincipalName, ResultDescription, IPAddress, Location
| order by TimeGenerated desc
```

### 2. Detect multiple failed sign-ins from the same IP
```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts = count() by IPAddress, bin(TimeGenerated, 1h)
| where FailedAttempts > 10
| order by FailedAttempts desc
```

### 3. List recently created user accounts
```kql
AuditLogs
| where OperationName == "Add user"
| project TimeGenerated, InitiatedBy, TargetResources
| order by TimeGenerated desc
```

### 4. Find processes executed on a device
```kql
DeviceProcessEvents
| where DeviceName == "<your-device-name>"
| project TimeGenerated, FileName, ProcessCommandLine, AccountName
| order by TimeGenerated desc
```

### 5. Detect suspicious PowerShell commands
```kql
DeviceProcessEvents
| where FileName =~ "powershell.exe"
| where ProcessCommandLine has_any ("Invoke-Expression", "IEX", "EncodedCommand", "-enc", "DownloadString")
| project TimeGenerated, DeviceName, AccountName, ProcessCommandLine
| order by TimeGenerated desc
```

### 6. List network connections to external IPs
```kql
DeviceNetworkEvents
| where RemoteIPType == "Public"
| project TimeGenerated, DeviceName, RemoteIP, RemotePort, LocalIP
| order by TimeGenerated desc
```

### 7. Search for a specific file hash across devices
```kql
DeviceFileEvents
| where SHA256 == "<paste-hash-here>"
| project TimeGenerated, DeviceName, FileName, FolderPath, ActionType
| order by TimeGenerated desc
```

### 8. Find emails with suspicious attachments
```kql
EmailAttachmentInfo
| where FileType in ("exe", "vbs", "ps1", "bat", "js")
| project TimeGenerated, SenderFromAddress, RecipientEmailAddress, FileName, FileType
| order by TimeGenerated desc
```

---

## Add Your Own Query

Have a useful KQL query? Follow the [contribution guide in the README](README.md) to add it here!

Use this template when adding a new query:

````markdown
### <number>. <Short description of what the query does>
```kql
<your KQL query here>
```
````
