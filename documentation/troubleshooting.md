# Troubleshooting – Operator Connect Implementation

## Common Issues & Resolutions

---

### 1. Phone Number Cannot Be Assigned

Possible Causes:
- Missing Microsoft Teams Phone license
- Incorrect number type
- Provisioning delay

Resolution:
- Verify license assignment
- Confirm number type is OperatorConnect
- Run Get-CsOnlineUser

---

### 2. Outbound PSTN Calls Fail

Possible Causes:
- Voice routing policy not assigned
- PSTN usage misconfiguration
- License not provisioned

Resolution:
- Check Grant-CsOnlineVoiceRoutingPolicy
- Validate PSTN usage records
- Confirm LineURI configuration

---

### 3. Emergency Calling Misconfiguration

Possible Causes:
- Emergency address not validated
- Location policy missing

Resolution:
- Verify emergency location configuration
- Confirm policy assignment

