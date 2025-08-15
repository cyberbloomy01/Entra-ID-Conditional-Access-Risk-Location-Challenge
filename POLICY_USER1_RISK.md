Policy Overview
Policy Name: User Risk - Password Change Enforcement
Purpose: Enforce password change for users flagged with high user risk to mitigate potential account compromise.

Configuration Details
Assignments:
Users or Groups: TestUser1
Exclusions: BreakGlassAccount, ServiceAccounts

Cloud Apps or Actions
Included: All cloud apps
Excluded: None

Conditions
User Risk: High
Sign-in Risk: Not configured (intentionally omitted)

Access Control
Grant: Require password change
Session Controls: None

Notes:
Why User Risk?: More reliable for detecting compromised accounts based on identity signals.
Testing: Verified with TestUser1 using simulated risk elevation.
Expected Behavior: User is prompted to change password upon sign-in when flagged as high risk.


