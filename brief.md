
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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
