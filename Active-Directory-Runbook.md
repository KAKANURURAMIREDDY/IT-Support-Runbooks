# Active Directory Runbook

## User Provisioning
1. Verify request via ServiceNow ticket
2. Create account in AD with correct OU placement
3. Assign role-based groups (RBAC)
4. Set temporary password, force reset on login
5. Confirm M365 license assignment

## Password Reset
1. Verify user identity
2. Reset via ADUC or PowerShell: `Set-ADAccountPassword`
3. Unlock account if locked: `Unlock-ADAccount`
4. Confirm user can log in

## Account Unlock
1. Check lockout source via `Get-ADUser -Filter * -Properties LockedOut`
2. Unlock: `Unlock-ADAccount -Identity username`
3. Document root cause in ServiceNow KBA
