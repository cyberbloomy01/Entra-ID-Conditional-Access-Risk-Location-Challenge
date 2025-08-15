Task 1:  Create two test users in the tenant. What usernames and license 
assignments did you choose? Why did you choose those roles/assignments?

Answer:

    I created two users in the tenant :
        1. Test_user1
        2. Test_user2
<img width="1910" height="910" alt="Screenshot 2025-08-15 073531" src="https://github.com/user-attachments/assets/09434f10-f14a-4fb6-9f6c-cd28b1c6edb6" />
<img width="1906" height="930" alt="Screenshot 2025-08-15 073617" src="https://github.com/user-attachments/assets/0092c23f-b18b-48ee-986d-242fc266f516" />



Task 2: Create a Conditional Access Policy Based on User Risk
Action: Created a policy targeting test users.
Condition: User risk set to High.
Control: Required password change.
Status: Policy created and enabled.

Task 3: Create a Conditional Access Policy Based on Location
Action: Defined named locations (e.g., Nigeria IP range).
Condition: Block access from non-trusted locations.
Control: Block access.
Status: Policy created and tested.

Task 4: Combine Risk and Location in a Single Policy
Action: Created a policy combining user risk and location.
Condition: High user risk + access from non-trusted location.
Control: Block access.
Status: Policy created and verified.

Task 5: Test Policies with a Test User
Action: Used a test user with simulated risk.
Result: Verified that access was blocked or MFA was triggered based on conditions.
Status: Testing successful.

Task 6: Monitor Sign-in Logs
Action: Navigated to Sign-in logs in Entra ID.
Insight: Verified policy enforcement and risk detection.
Status: Logs reviewed and documented.

Task 7: Review Named Locations
Action: Created and reviewed trusted IP ranges.
Purpose: Used in location-based Conditional Access policies.
Status: Locations configured correctly.

Task 8: Document Policies
Action: Documented all policies with: (Name, Conditions, controls, target users)
Status: Documentation Complete

Task 9: Hardening Recommendations & Next Steps
Monitoring Improvement: Use Sentinel workbooks, alerts, and reviews to track policy effectiveness and reduce false positives.
Policy Refinement: Refine policies by targeting user groups, excluding service/emergency accounts, and adding device compliance checks.
Documentation & Training: Provide user guides, document policy rationale, and create help desk runbooks for blocked sign-ins.

