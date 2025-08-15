Policy Overview
Policy Name: Location-Based Access Control
Purpose: Block access from Nigeria.

Configuration Details
Assignments:
Users or Groups: Test User2 (LocationSensitiveUsers)
Exclusions: BreakGlassAccount, ServiceAccounts.
Cloud Apps or Actions
Included: All cloud apps
Excluded: None
Conditions
Locations:
Include: All locations
Exclude: Named trusted locations excluding Nigeria.

Access Controls
Grant: Block access
Session Controls: None

Notes:
Why Block Nigeria?: Based on risk analysis or compliance requirements, Nigeria is excluded from trusted locations.
Testing: Simulated sign-in from Nigeria resulted in blocked access as expected.
Expected Behavior: Any sign-in attempt from Nigeria is denied.
