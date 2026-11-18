# Mock Help Desk Tickets

These are simulated tickets based on exercises in my Active Directory home lab (homelab.local). The users are test accounts I created. They are not tickets from a real employer.

## Ticket HD-001: Password reset
- **Date:** 2026-11-16
- **Category:** Account access
- **Priority:** Medium
- **Reported by:** A. Lopez (test user)
- **Issue:** User cannot sign in and needs a password reset.
- **Steps taken:**
  1. Opened Active Directory Users and Computers and went to the Staff OU.
  2. Right-clicked the user and chose Reset Password.
  3. Set a temporary password that meets the domain's password rules.
  4. Ticked "User must change password at next logon".
- **Resolution:** Password reset completed without errors. The user must choose a new password at next sign-in.
- **Status:** Resolved in lab

## Ticket HD-002: Disable an account for offboarding
- **Date:** 2026-11-16
- **Category:** Account management
- **Priority:** Medium
- **Reported by:** HR request (simulated)
- **Issue:** An employee (B. Carter, test user) is leaving, so their account must be disabled.
- **Steps taken:**
  1. Located the user in the Staff OU.
  2. Right-clicked the user and chose Disable Account.
  3. Confirmed the account showed as disabled.
  4. Re-enabled the account to confirm the process can be reversed.
- **Resolution:** Account disabled and re-enabled successfully.
- **Status:** Resolved in lab

## Ticket HD-003: New staff accounts
- **Date:** 2026-11-16
- **Category:** Onboarding
- **Priority:** Low
- **Reported by:** Manager request (simulated)
- **Issue:** Five new staff members need domain accounts.
- **Steps taken:**
  1. Created the accounts in the Staff OU with PowerShell, using a hidden password prompt so the password was never displayed.
  2. Added all five users to the all-staff group.
  3. Checked the results with `Get-ADUser` and `Get-ADGroupMember`.
- **Resolution:** All five accounts were created and listed as members of the all-staff group.
- **Status:** Resolved in lab

## Ticket HD-004: Help desk group access
- **Date:** 2026-11-16
- **Category:** Access request
- **Priority:** Low
- **Reported by:** Manager request (simulated)
- **Issue:** E. Kim (test user) needs membership in the help desk group.
- **Steps taken:**
  1. Ran `Add-ADGroupMember` to add the user to the HelpDesk group only.
  2. Left the other four users out of the group.
- **Resolution:** Command completed with no errors.
- **Status:** Resolved in lab

## Ticket HD-005: Locked-out account
- **Date:** Pending
- **Category:** Account access
- **Priority:** Medium
- **Reported by:** Test user (simulated)
- **Issue:** A user is locked out after 3 failed sign-in attempts, which is the lockout threshold I set in Group Policy.
- **Planned steps:**
  1. Fail a sign-in 3 times from the client VM.
  2. In Active Directory Users and Computers, open the user's properties, go to the Account tab, and unlock the account.
  3. Confirm the user can sign in.
- **Status:** Open. I'll complete this once the Windows 11 client VM is joined to the domain.
