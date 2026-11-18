# Active Directory Home Lab

A Windows Server 2022 Active Directory lab built in VirtualBox to practice help desk and systems administration tasks.

## What I built
- Installed Windows Server 2022 as a domain controller (DC01) in VirtualBox
- Configured a static IP, gateway and DNS, and verified connectivity
- Created the homelab.local domain with PowerShell
- Created two OUs (Staff, IT), two security groups (Allstaff, HelpDesk) and five test users
- Practiced common help desk tasks in Active Directory Users and Computers: password reset, disabling and re-enabling an account
- Set an account lockout policy (3 invalid attempts) with Group Policy
- Joined a Windows 11 client VM (CLIENT01) to the domain and signed in as a domain user
- Tested the lockout policy from the client and unlocked the account in Active Directory Users and Computers

## Mock help desk tickets
See the [tickets](tickets/) folder for five simulated tickets based on these exercises.

## Skills practiced
Windows Server, Active Directory, DNS, Group Policy, PowerShell, VirtualBox, troubleshooting, documentation

## Daily log
See the [daily-log](daily-log/) folder for what I did, what went wrong and what I learned each day.

## Contact
LinkedIn: add your profile link
