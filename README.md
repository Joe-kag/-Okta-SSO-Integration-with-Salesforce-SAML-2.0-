📌 Overview

This project demonstrates the implementation of Single Sign-On (SSO) using Okta as the Identity Provider (IdP) and Salesforce as the Service Provider (SP).

The objective was to configure SAML 2.0 authentication, enabling secure and seamless access to Salesforce through centralized identity management.

🏗️ Architecture
Okta → Identity Provider (IdP)
Salesforce → Service Provider (SP)
Protocol → SAML 2.0

Authentication Flow:

User accesses Salesforce
Redirected to Okta for authentication
Okta validates user credentials
SAML assertion is generated and sent to Salesforce
User gains access without re-entering credentials

<img width="1920" height="913" alt="1" src="https://github.com/user-attachments/assets/eec86b92-b1dc-4d8d-9364-01dafacf9f64" />


🛠️ Technologies & Concepts
Okta (IdP)
SAML 2.0
Salesforce SSO Configuration
Identity Federation
Attribute Mapping
⚙️ Implementation Steps
🔹 1. Configure Salesforce for SSO
Enabled SAML authentication in Salesforce
Configured:
Assertion Consumer Service (ACS) URL
Entity ID (Audience URI)
Created and configured Single Sign-On Settings

<img width="1890" height="696" alt="3" src="https://github.com/user-attachments/assets/b245e3fb-3d67-4ab7-aba9-b2f5711c0e79" />


🔹 2. Configure SAML Application in Okta
Created a new SAML 2.0 application in Okta
Defined:
ACS URL (from Salesforce)
Audience URI (Entity ID)
NameID format (Email/Username)
Configured attribute statements for identity mapping

<img width="1920" height="924" alt="done " src="https://github.com/user-attachments/assets/03e5c5a8-36c9-4ed6-82e3-321598ffd945" />


🔹 3. Establish Trust Between Okta and Salesforce
Uploaded IdP metadata from Okta into Salesforce
Verified certificate and issuer details
Ensured proper trust relationship between IdP and SP
🔹 4. Assign Users & Access
Assigned users to the Salesforce application in Okta
Verified correct username/email alignment between systems
Ensured users had appropriate access permissions

<img width="1872" height="922" alt="9a" src="https://github.com/user-attachments/assets/a662617e-54c1-433f-abe7-9dc6101185c4" />


🔹 5. Testing & Validation
Initiated login via Okta dashboard
Successfully authenticated into Salesforce using SSO
Verified seamless access without additional credentials

<img width="1903" height="925" alt="7a" src="https://github.com/user-attachments/assets/2e640483-230b-4892-990b-ef6f735fcdb7" />

<img width="1905" height="976" alt="4a" src="https://github.com/user-attachments/assets/8b890e70-c7c8-4c1b-b777-a2a7ee112954" />

<img width="1872" height="922" alt="9a" src="https://github.com/user-attachments/assets/d6994ff6-6f24-47a6-9246-1be3fe057264" />




✅ Key Outcomes
Implemented secure SAML-based SSO
Centralized authentication using Okta
Improved user experience by eliminating multiple logins
Demonstrated real-world identity federation workflow

⚠️ Challenges & Resolutions
ACS URL / Entity ID mismatch
Issue: Authentication failed due to incorrect configuration
Fix: Validated and aligned values between Okta and Salesforce
Attribute Mapping Errors
Issue: User could not authenticate
Fix: Adjusted NameID to match Salesforce username/email
Certificate / Metadata Issues
Issue: Trust relationship failed
Fix: Re-imported correct IdP metadata from Okta

🚀 Future Improvements
Enforce Multi-Factor Authentication (MFA) in Okta
Implement role-based access via groups
Enable Just-In-Time (JIT) provisioning
Add monitoring and logging for authentication events
💡 Project Value

This project demonstrates hands-on experience with:

SAML 2.0 authentication
Identity federation
Cloud application integration
Troubleshooting real-world SSO issues

It aligns directly with responsibilities in:

Identity & Access Management (IAM)
Cloud Security Engineering
Security Operations (SOC)

👤 Author
Joseph Kageche
Cybersecurity Analyst | Cloud & IAM Enthusiast
