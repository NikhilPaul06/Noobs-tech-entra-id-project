# Audit Log Evidence Summary

The original exported audit CSV was used during the lab.

For GitHub safety, the raw CSV is intentionally **not included** because exported identity logs can contain tenant identifiers, user identifiers, timestamps, IP addresses and other operational information.

## Observed Lab Activities

The audit trail demonstrated events related to:

- User creation
- Group membership changes
- Device registration
- Registered device owner/user changes
- Password-related operations

## Recommended GitHub Evidence

Use screenshots with sensitive information redacted, or create a synthetic/sample CSV containing no real tenant or user data.

### Security rule

Never commit:

- Passwords
- MFA setup keys
- Recovery codes
- Access tokens
- Client secrets
- Private keys
- Personal IP addresses
- Personal email addresses
- Tenant-specific secrets