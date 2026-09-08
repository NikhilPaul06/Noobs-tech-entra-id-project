# Noobs Tech Ltd — Microsoft Entra ID Identity & Access Management Lab

## 📌 Project Overview

This project simulates a small company's identity and access environment using Microsoft Entra ID.

**Scenario:** Noobs Tech Ltd has IT, HR and Finance departments. The goal is to implement basic identity management, group-based access, device identity, MFA protection and identity monitoring.

## 🎯 Objectives

- Create and manage Entra ID users
- Create security groups
- Assign users to department groups
- Implement Azure RBAC using group-based access
- Join a Windows 11 Pro device to Microsoft Entra ID
- Enable Microsoft Entra Security Defaults
- Test MFA
- Review Sign-in Logs
- Review Audit Logs

## 🏗️ Architecture

```text
                         Noobs Tech Ltd
                                |
                        Microsoft Entra ID
                                |
          +---------------------+----------------------+
          |                     |                      |
        Users                 Groups                Devices
          |                     |                      |
     +----+----+          +-----+-----+              NIKSUKH
     |    |    |          |     |     |
   Rahul Amit Priya      IT    HR  Finance
     |    |    |         Team  Team   Team
     |    |    |          |
     +----+    +----------+      |
          |                    |
          +--------------------+
                   |
             Azure RBAC
                   |
      Virtual Machine Contributor
                   |
               IT-Team
```

## 👥 Users

| User | Department | Group |
|---|---|---|
| Rahul | IT | IT-Team |
| Amit | IT | IT-Team |
| Priya | HR | HR-Team |
| Neha | Finance | Finance-Team |

> Note: Real tenant usernames/domains are intentionally not included in this repository.

## 👥 Security Groups

- `IT-Team`
- `HR-Team`
- `Finance-Team`

Membership type used: **Assigned**

## 🔐 RBAC

The `IT-Team` group was assigned the **Virtual Machine Contributor** role at the Azure subscription scope.

This demonstrates group-based Azure RBAC rather than assigning permissions separately to every IT employee.

## 💻 Device Management

A Windows 11 Pro laptop named `NIKSUKH` was successfully joined to Microsoft Entra ID.

Observed in Entra admin center:

- Join type: **Microsoft Entra joined**
- Enabled: **Yes**
- Owner: **Rahul**
- MDM: **None**

> This lab demonstrates Entra device identity. It does not demonstrate Microsoft Intune enrollment.

## 🔒 Security

Custom Conditional Access policies were not configured because the lab tenant did not have sufficient licensing.

Instead, **Microsoft Entra Security Defaults** were enabled to provide baseline identity protection and MFA.

## 📊 Monitoring

### Sign-in Logs

Used to investigate authentication activity such as:

- User
- Application
- Date/time
- Status
- IP address
- Authentication activity

### Audit Logs

Used to track directory changes such as:

- User creation
- Group membership changes
- Device registration
- Device ownership/user registration
- Password-related operations

## 🧪 Key Evidence

The lab successfully demonstrated:

- ✅ 4 Entra ID users
- ✅ 3 security groups
- ✅ Group membership
- ✅ Group-based Azure RBAC
- ✅ Windows 11 device joined to Entra ID
- ✅ Security Defaults enabled
- ✅ MFA test completed
- ✅ Sign-in Logs reviewed
- ✅ Audit Logs reviewed

## 🧠 Key Concepts Learned

### Authentication vs Authorization

**Authentication:** "Tum kaun ho?"

Example: Rahul signs in with username, password and MFA.

**Authorization:** "Tumhe kya karne ki permission hai?"

Example: IT-Team receives Virtual Machine Contributor access.

### Sign-in Logs vs Audit Logs

| Log | Main question |
|---|---|
| Sign-in Logs | Who attempted to sign in? |
| Audit Logs | What changed in the directory? |

## 📁 Suggested Evidence

Screenshots can be stored in the `evidence/` folder using names such as:

```text
01-users.png
02-groups.png
03-group-membership.png
04-rbac.png
05-entra-device-join.png
06-device-in-entra.png
07-security-defaults.png
08-mfa-test.png
09-sign-in-logs.png
10-audit-logs.png
```

Do **not** upload screenshots containing passwords, MFA secrets, recovery codes, access tokens or other sensitive information.

## 🚀 Future Improvements

Possible next phases:

1. Microsoft Entra ID P1/P2 lab
2. Conditional Access policies
3. Microsoft Intune device enrollment
4. Device compliance policies
5. Privileged Identity Management (PIM)
6. Administrative Units
7. Access Reviews
8. Identity Governance
9. Microsoft Sentinel integration

## 💼 CV Bullet

> Built a Microsoft Entra ID identity and access management lab for a simulated organisation, implementing users, security groups, group-based Azure RBAC, Microsoft Entra joined Windows device, Security Defaults/MFA, and Sign-in/Audit Log monitoring.

## 🏷️ Technologies

`Microsoft Azure` `Microsoft Entra ID` `Azure RBAC` `Windows 11 Pro` `MFA` `Identity & Access Management`