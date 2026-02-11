# Implementation Guide

## Operator Connect Configuration Steps

### Connect to Teams PowerShell

```powershell
Install-Module MicrosoftTeams
Connect-MicrosoftTeams
```

### Assign Phone Number

```powershell
Set-CsPhoneNumberAssignment -Identity user@company.com -PhoneNumber +491234567890 -PhoneNumberType OperatorConnect
```

### Grant Voice Routing Policy

```powershell
Grant-CsOnlineVoiceRoutingPolicy -Identity user@company.com -PolicyName "OperatorConnectPolicy"
```

### Verify Assignment

```powershell
Get-CsOnlineUser -Identity user@company.com | Select DisplayName, LineURI
```

---

## Validation Checklist

- PSTN inbound test
- PSTN outbound test
- Emergency call validation
- Voicemail test
- Policy assignment verification
