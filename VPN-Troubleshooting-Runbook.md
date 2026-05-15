# VPN & Remote Connectivity Runbook

## Initial Checks
1. Confirm internet connectivity: `ping 8.8.8.8`
2. Check DNS resolution: `nslookup company.domain.com`
3. Flush DNS cache: `ipconfig /flushdns`
4. Release/renew IP: `ipconfig /release` then `ipconfig /renew`

## VPN Client Issues
1. Reinstall VPN client if corrupted
2. Check firewall rules blocking VPN ports
3. Verify user credentials & MFA token
4. Escalate to L2 if tunnel fails post-auth

## Escalation Criteria
- Issue affects 3+ users → L2 Network team
- Infrastructure-level root cause → L3 + RCA required
