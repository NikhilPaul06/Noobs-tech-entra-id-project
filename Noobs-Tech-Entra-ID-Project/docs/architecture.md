# Architecture Notes

## Identity Flow

```text
User
  |
  v
Microsoft Entra ID
  |
  +--> Authentication
  |      |
  |      +--> Password
  |      +--> MFA / Security Defaults
  |
  +--> Group membership
  |      |
  |      +--> IT-Team
  |      +--> HR-Team
  |      +--> Finance-Team
  |
  +--> Authorization
         |
         +--> Azure RBAC
                |
                +--> Virtual Machine Contributor
```

## Device Flow

```text
Windows 11 Pro
      |
      | Microsoft Entra Join
      v
Microsoft Entra ID
      |
      v
Device identity recorded in Entra Devices
```

## Logging Flow

```text
Authentication events
        |
        v
   Sign-in Logs

Directory changes
        |
        v
    Audit Logs
```