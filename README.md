# psSDP
psSDP: PowerShell based SDP (Support Diagnostic Package)

as an alternative to traditional Microsoft **Support Diagnostic Packages**

### Purpose
Collect **SDP** speciality report on windows system

### Usage
To start data collection, run in an elevated PowerShell window

 ` .\get-psSDP.ps1 [Net | Dom | CTS | Print | HyperV | Setup | Mini | Nano | repro] `
 
 Example for SDP Networking Diagnostic:
  `.\get-psSDP.ps1 Net`

 Example for SDP Basic data collection:
 `.\get-psSDP.ps1 Mini`
  
If you get an error that running scripts is disabled, run "Set-ExecutionPolicy Bypass –force" and then run ".\get-psSDP.ps1" again. 

Action: Send us the file _%computername%_<date>_<tec>_SDP.zip


**Powershell ExecutionPolicy**
--------------------------
Make sure script execution is allowed in PowerShell

-	Run: 

 ` Get-ExecutionPolicy`

-	If the policy comes back AllSigned, Default, or Restricted then scripting needs to be enabled.
-	Save the output to restore the policy when troubleshooting is complete
-	Run: 

`  Set-ExecutionPolicy -ExecutionPolicy Unrestricted`
