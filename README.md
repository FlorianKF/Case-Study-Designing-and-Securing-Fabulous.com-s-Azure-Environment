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
|Legacy Application Support|Microsoft Entra Domain Services|
