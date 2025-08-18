Task 1:  Create two test users in the tenant. What usernames and license 
assignments did you choose? Why did you choose those roles/assignments?

Answer:

    I created two users in the tenant :
        1. Test User1 
        2. Test User2
<img width="1910" height="910" alt="Screenshot 2025-08-15 073531" src="https://github.com/user-attachments/assets/09434f10-f14a-4fb6-9f6c-cd28b1c6edb6" />
<img width="1906" height="930" alt="Screenshot 2025-08-15 073617" src="https://github.com/user-attachments/assets/0092c23f-b18b-48ee-986d-242fc266f516" />

    Test User1 License = Microsoft 365 E5 Developer (without Windows and Audio Conferencing)
    Test User2 License = Microsoft 365 E5 Developer (without Windows and Audio Conferencing)

    I assigned Microsoft 365 E5 licenses to both users to enable Identity Protection features<img width="1234" height="63" alt="image" src="https://github.com/user-attachments/assets/70a9cdca-ef98-43c1-ad9f-63670b5b5521" />
 
    
<img width="1920" height="910" alt="Screenshot (1)" src="https://github.com/user-attachments/assets/045f8b02-9e2f-49f4-b402-554d7a1b9620" />
<img width="1920" height="894" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/7c581393-e8aa-4287-9d3e-642392fd70ca" />

   

Task 2: Design a sign-in risk Conditional Access policy scoped to User1 that enforces 
a password change for sign-in risks of Medium and High. Exactly which policy 
settings will you use (policy name, user assignment, risk levels, grant/session 
controls, and policy state)? Explain your configuration choices and any 
limitations you considered.

Answer:
       1. Test User 1 Password Change Policy
       2. Test User 1 Sign-in Risk Policy

1. Test User 1 Password Change Policy
Policy Name: Test User 1 Password Change Policy
User Assignment: Test User 1
Risk Level: High, Medium, Low
Grants:  Multifactor Authentication, Password Change
Controls: Grant access
Policy State: On

<img width="1893" height="905" alt="Screenshot 2025-08-15 110146" src="https://github.com/user-attachments/assets/0b89a913-cea3-4d51-b4cd-af278a9bdfaa" />
<img width="1913" height="920" alt="Screenshot 2025-08-15 110321" src="https://github.com/user-attachments/assets/25d6fb00-1e27-4bf5-8a79-71a4042e7644" />

2. Test User 1 Sign-in Risk Policy
Policy Name: Test User 1 Skin-in Risk Policy
User Assignment: Test User 1
Risk Level: High, Medium
Grants: Block Access
Controls:
Policy State: Report only

<img width="1915" height="891" alt="Screenshot 2025-08-15 112652" src="https://github.com/user-attachments/assets/af1d0156-6280-43b6-afb4-c0a51766b219" />
<img width="1887" height="902" alt="Screenshot 2025-08-15 112625" src="https://github.com/user-attachments/assets/85cbd75b-24aa-4859-af16-1babd45b771c" />

Configuration Choices: I created two policies for Test user 1, namely Password change and Sign-in Risk. I choose this configuration method because of the limitation encountered during the configuration.

Limitation: Password change cannot be configured for Sign- in risk policy hence the need to create password change policy for Test User 1 and granted access while the the sign -in risk policy was blocked as shown in the screenshots respectively.

3. How will you simulate a Medium/High sign-in risk for User1 to verify the policy 
triggers? Describe the simulation method(s) you used and why.

Answer: 
      1. Used API Graph to compromise, Test User 1 account.
      2. Logged in with another browser using a VPN ( I used Brave Browser) to trigger anomalous iP address connection
      3. Password Change was prompted for the Password change policy 
      4. For sign in risk policy trigger, anomalous IP address was flaged by Entar ID, blocking the sign-in from teh user.

      
<img width="1892" height="811" alt="Screenshot 2025-08-15 105003" src="https://github.com/user-attachments/assets/5d2a759d-ad04-455f-8b91-3317f0662380" />
<img width="1173" height="791" alt="Screenshot 2025-08-15 103116" src="https://github.com/user-attachments/assets/2a16e7ba-a5e0-4c6c-9fe3-5714cc78d130" />

4. Capture and describe the enforcement outcome for User1. What visible 
experience does the user see? Which logs or Identity Protection entries show 
the detection and enforcement? Attach screenshots as evidence.


5. Design a location Conditional Access policy scoped to User2 that blocks 
sign-ins originating from Nigeria. Precisely which conditions and assignments 
are configured (policy name, user assignment, named location(s), 
included/excluded locations, grant control, policy state)? Explain your choices.

6. 
