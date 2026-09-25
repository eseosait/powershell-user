## Part 9: Create Additional Users with PowerShell

To practice user provisioning and automation, I used a PowerShell script to create multiple employee accounts.

1. Signed in to DC-1 as `jane_admin`.
2. Opened **PowerShell ISE** as an administrator.
3. Created a new script file.
4. Added the user-generation script.
5. Ran the script.
6. Observed the accounts being created.

> Account passwords used in scripts should be protected and should not be published in a GitHub repository.

## 🎥 Video Demonstrations

### Creating Users with PowerShell
[Watch the video demonstration](https://youtu.be/q4gMWIettIw?si=x9_IdAU5z6uieCun)


![PowerShell User Creation] <img width="2200" height="1429" alt="96FCC317-019E-4BF2-8D9A-004E074F2399_1_102_o" src="https://github.com/user-attachments/assets/bc87c73f-24ef-4284-91b6-fd867001ba42" /> <img width="2200" height="1429" alt="32047043-755A-4448-9B4C-C548ADCF981B_1_102_o" src="https://github.com/user-attachments/assets/847de1a6-15b6-4b54-bb35-bdaa38fab5f9" />



## Part 10: Verify the Employee Accounts

After the script completed, I opened Active Directory Users and Computers and confirmed that the new accounts appeared inside the `_EMPLOYEES` Organizational Unit.

I then selected one of the generated accounts and successfully signed in to Client-1 as a standard domain user.

This verified that:

- The user account was successfully created.
- Client-1 was properly joined to the domain.
- Domain authentication was functioning.
- Standard domain users had permission to access Client-1 through Remote Desktop.

![Generated Employee Accounts] <img width="2200" height="1429" alt="313FE463-B05E-4CB8-BC17-F6F584003220_1_102_o" src="https://github.com/user-attachments/assets/db7959e0-294a-4c28-8935-976deecb15a3" />


## Deployment Summary

| Component | Configuration |
|---|---|
| Domain controller | DC-1 |
| Active Directory forest | `mydomain.com` |
| Domain administrator | `jane_admin` |
| Administrative OU | `_ADMINS` |
| Employee OU | `_EMPLOYEES` |
| Client computer OU | `_CLIENTS` |
| Domain client | Client-1 |
| Remote Desktop access | Domain Users |
| User provisioning | PowerShell automation |

## Skills Demonstrated

- Installing Active Directory Domain Services
- Promoting a Windows Server to a domain controller
- Creating a new Active Directory forest and domain
- Managing Active Directory Organizational Units
- Creating users and managing security group membership
- Assigning administrative privileges
- Joining a Windows client to a domain
- Managing computer objects in ADUC
- Configuring Remote Desktop access for domain users
- Automating user account creation with PowerShell
- Testing domain authentication


## Conclusion

In this lab, I successfully deployed Active Directory in Microsoft Azure. I installed Active Directory Domain Services, promoted DC-1 to a domain controller, created and organized domain accounts, joined Client-1 to the domain, enabled access for standard domain users, and automated employee account creation with PowerShell.

This lab provided hands on experience with centralized identity management, domain authentication, administrative permissions, directory organization, endpoint management, and user provisioning.
