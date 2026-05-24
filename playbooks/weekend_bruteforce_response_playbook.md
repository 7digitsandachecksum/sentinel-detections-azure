Logic app Workflow is as follows:

Condition: 
Friday 7PM → Monday 7AM
@or(
  and(
      equals(dayOfWeek(utcNow()),5),
      greaterOrEquals(int(formatDateTime(utcNow(),'HH')),19)
  ),
  equals(dayOfWeek(utcNow()),6),
  equals(dayOfWeek(utcNow()),0),
  and(
      equals(dayOfWeek(utcNow()),1),
      less(int(formatDateTime(utcNow(),'HH')),7)
  )
)

Update user

Account Enabled = False

Revoke user sign-in sessions

securityadmin@companyname.com
 Subject line: 
[Sentinel Automated Response] User Account Disabled Due to Weekend Brute Force Activity

Automated Sentinel response has been triggered.

User Account:
@{AccountUPN}

Actions Taken:

* Account disabled in Microsoft Entra ID
* Active sign-in sessions revoked
* Potential brute force and anomalous IP activity detected

Detection Details:

* Failed Login Threshold: 7
* Detection Window: Weekend Off-Hours
* Incident ID: @{IncidentNumber}

Please review the incident in Microsoft Sentinel for further investigation.
 
