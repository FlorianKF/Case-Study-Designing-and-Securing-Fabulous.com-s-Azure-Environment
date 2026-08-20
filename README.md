# Case-Study-Designing-and-Securing-Fabulous.com-s-Azure-Environment
This case study is a simulated scenario created for educational purposes. It is inspired by Microsoft Copilot exercises and AI-assisted learning to demonstrate the practical application of Azure security concepts.


# Scenario

***Fabulous.com***, a fast-growing e-commerce company, has recently migrated its infrastructure to Microsoft Azure. 
As the business expands, the company must provide secure access to employees, external partners, and customers while protecting sensitive business and customer data from evolving cyber threats.

The IT department has been tasked with designing a Zero Trust security architecture that ensures secure authentication, controlled access to Azure resources, and effective protection against security incidents.
The solution must also support legacy applications requiring domain services and enable secure collaboration with external organizations.

In addition, the company wants to assess how Azure security services can help detect, prevent, and respond to potential cyberattacks while maintaining business continuity.

Objectives

This case study aims to demonstrate how Azure security services work together by:

- Illustrating how Single Sign-On (SSO), Multi-Factor Authentication (MFA), Conditional Access, and Azure Role-Based Access Control (RBAC) support a Zero Trust security model;
- Explaining the roles of Microsoft Entra ID, Microsoft Entra Domain Services, and Microsoft Entra External ID through practical business scenarios;
- Simulating a security incident to show how encryption, Azure Key Vault, Defense in Depth, and Microsoft Defender for Cloud help protect Azure resources, reduce security risks, and improve the organization's security posture.



# Proposed Solution

## 1. Identity Management

To meet its identity and access management requirements, ***Fabulous.com*** requires a centralized identity platform capable of supporting employees, external partners, customers, and legacy applications. To address these business requirements, the following Azure services have been selected

|Bussiness requierement| Azure Service|Purpose|
|-----|----|-----|
|Employee Identity Management| Microsoft Entra ID| It´s the primary identity provider for employees, enables centralized Authentication, Single Sign-On (SSO), and secure access to Azure resources|
|Legacy Application Support|Microsoft Entra Domain Services|This provides managed domain services such as domain join, LDAP, Kerberos, and Group Policy for legacy applications without requiring the deployment of domain controllers|
|External collaboration|Microsoft Entra External ID|Enables secure collaboration with external users as: suppliers, logistics partners, customers... by allowing them to access only the resources they need while using their existing identities|

## 2. Authentication and Access Management

To implement a Zero Trust architecture, ***Fabulous.com*** should combine several Microsoft Entra security features as Single Sign-On (SSO), Multi-Factor Authentication (MFA), Conditional Access, and Azure Role-Based Access Control (RBAC) depending of used cases.

|Azure ID services|Purposes|Bussiness Benefits|
|---|----|----|
|Single Sign-On (SSO)|Will allow employees to authenticate once through Microsoft Entra ID and securely access multiple business applications|Improves productivity and reduces password fatigue and forgetfulness|
|Multi-Factor Authentication (MFA)|This will require a second authentication factor, such as Microsoft Authenticator in addition in case of using a password|Reduces the risk of unauthorized access and reinforces access security|
| Onditional Acces|Evaluates every sign-in request based on user identity, device compliance, geographic location, and sign-in risk before granting access|It will enhance security by allowing Azure to authorize access, require multi-factor authentication, or block unauthorized login attempts based on security conditions|
|Azure Role-Based Access Control (RBAC)|This will determine the actions that each authenticated user is authorized to perform|Implements the principle of least privilege, ensuring users receive only the permissions required for their responsibilities|


#### Accordingly, users at ***Fabulous.com*** will be assigned different Azure roles based on their responsibilities, ensuring that each user receives only the permissions required to perform their job functions.
For example:

|Users| Azure Role|Permissions|
|---|---|---|
|Customer|Reader|View Azure resources only|
|Developer| Contributor|Could create, modify, and delete Azure resources, but could not manage access|will get full control over resources, including access management|
|Administrator| Owner|Will get the full control over Azure resources, including access management|


## 3. Security Incident Simulation

A cybercriminal has launched a credential compromise campaign against ***Fabulous.com*** using several attack techniques including: 

- Phishing:
- Password spraying,
- Dictionary attacks,
- And credential stuffing.

Their goal is to gain unauthorized access to confidential customer information and other sensitive Azure resources.
The attacker aims to escalate privileges, exfiltrate sensitive business data, and disrupt normal business operations.
We will explain how:

- Encryption, 
- Azure Key Vault, 
- Defense in depth, 
- And Microsoft Defender for Cloud
  
Help protect Azure resources, mitigate security risks, and improve the security posture of the ***Fabulous.com***

### A- Encryption

If encryption enabled, sensitive customer data stored in Azure Storage will be encrypted at rest and in transit. Even in the event of unauthorized access, the information remains unreadable without the appropriate encryption keys.

### B- Azure Key Vault

Encryption keys, certificates, and application secrets of ***Fabulous.com*** most be securely stored in Azure Key Vault instead of being embedded in the application code. This significantly reduces the risk of credential exposure. Even if the attacker compromises a user account, access to Azure Key Vault remains restricted unless the compromised identity has been explicitly granted the required permissions.

### C- Defense in Depth

With this, multiple security layers will protect Fabulous.com's Azure environment:

- Microsoft Entra ID
- Multi-Factor Authentication
- Conditional Access
- Azure Firewall
- Network Security Groups
- Encryption
- Azure RBAC

So, if one security layer is compromised, additional layers continue protecting the environment.

### D- Microsoft Defender for Cloud

Microsoft Defender for Cloud will continuously monitor Azure resources and identify:

- Security misconfigurations
- Vulnerabilities
- Suspicious activities
- Potential cyber threats

It will generate security alerts, provide remediation recommendations, and improve the Fabulous.com's Secure Score.

## In sum;
This solution will provide ***Fabulous.com*** with a secure, scalable, and resilient Azure environment that protect identities, applications, and data while supporting business growth and maintaining business continuity.


