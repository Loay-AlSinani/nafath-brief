
Version: NAFATH-V4
Track: Cybersecurity

## Overview
Software supply chain security protects the software, services, and components that an organization depends on. A national service provider may use external software libraries, AI models, mobile applications, and internet networks. A weakness in any of these areas can affect the whole service. For example, an insecure software component may contain a known vulnerability, an AI model may be manipulated, or incorrect network routes may redirect traffic. Organizations can reduce these risks by protecting application secrets, testing mobile applications, checking network routes, updating vulnerable software, and recording software components. These actions help security teams identify problems and respond more quickly. Security should be considered throughout the software lifecycle, from development to maintenance. My cybersecurity research focuses on the Log4Shell vulnerability, which showed how a widely used software component can create serious risks for many organizations.
## Software
The Twelve-Factor App method recommends storing application configuration in environment variables instead of hard-coding it in the source code. Configuration includes database connections and credentials for external services. Keeping configuration separate from code makes applications easier to deploy in different environments and reduces the risk of exposing secrets in a code repository. Environment variables must still be protected from unauthorized access.
Resource: The Twelve-Factor App - Config - https://12factor.net/config

## AI
Adversarial machine learning includes attacks that try to influence a model's behavior. In an evasion attack, an attacker changes input data to cause an incorrect prediction. In a poisoning attack, an attacker changes or introduces harmful data during training to influence the model. These attacks happen at different stages of the machine learning process. Organizations should protect training data, test models against harmful inputs, and monitor their behavior after deployment.
Resource: NIST AI 100-2 E2023 - Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://csrc.nist.gov/pubs/ai/100/2/e2023/final

## Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) defines security requirements for mobile applications. It covers areas such as secure data storage, cryptography, authentication, network communication, and privacy. Developers and security testers can use its control groups to check whether an application follows important security practices. MASVS helps organize security testing, but teams must still test the application and verify that the required controls are correctly implemented.
Resource: OWASP Mobile Application Security Verification Standard (MASVS) - https://mas.owasp.org/MASVS/

## Networking
BGP allows networks to exchange information about internet routes. In a route hijacking attack, an unauthorized or incorrect route announcement can cause traffic to follow an unintended path. RPKI helps network operators check whether an autonomous system is authorized to announce an IP address prefix. This reduces certain routing risks, but RPKI origin validation does not verify every network along the path. It therefore cannot prevent every type of BGP attack.
Resource: RIPE NCC - BGP Origin Validation - https://www.ripe.net/manage-ips-and-asns/resource-management/rpki/bgp-origin-validation/

## Cybersecurity
Log4Shell is a critical vulnerability in Apache Log4j 2, identified as CVE-2021-44228. In affected versions, an attacker could exploit JNDI lookup behavior to execute code remotely under vulnerable conditions. The vulnerability received a maximum CVSS score of 10.0 because of its serious potential impact and ease of exploitation. Apache released fixes for affected versions, including Log4j 2.15.0 for Java 8 and later. Organizations should identify affected components and apply the correct security updates.
Resource: Apache Logging Services - Security - https://logging.apache.org/security.html

## Data
A Software Bill of Materials (SBOM) is a formal record of software components and their supply chain relationships. It helps organizations understand which components are included in their products and investigate whether known vulnerabilities affect them. NTIA identifies seven minimum data fields: supplier name, component name, component version, other unique identifiers, dependency relationships, SBOM data author, and timestamp. Keeping this information accurate helps security teams track dependencies and respond to software risks.
Resource: NTIA - The Minimum Elements for a Software Bill of Materials (SBOM) - https://www.ntia.gov/files/ntia/publications/sbom_minimum_elements_report.pdf

## Misconception in My Track
A common misconception is that upgrading Log4j to version 2.15.0 completely fixed every security issue related to Log4Shell. However, Apache reported that the fix for CVE-2021-44228 was incomplete in certain non-default configurations. This led to the related vulnerability CVE-2021-45046. The lesson is that organizations should not assume one security update resolves every related risk. They should review official advisories, identify the versions they use, and apply the appropriate fixes. Security teams should also confirm that affected applications are actually using the updated components.
## Open Question
How can organizations automatically discover vulnerable third-party software components across their systems and confirm that the correct security updates have been applied?
