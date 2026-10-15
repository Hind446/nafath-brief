Version: NAFATH-V4
Your track: Cybersecurity

## Overview
Securing the software supply chain means protecting the software, tools, dependencies, and processes used to build and deliver applications. This mission explores six connected areas: secure software configuration, adversarial machine learning, mobile application security, BGP route hijacking and RPKI, the Log4Shell vulnerability, and Software Bills of Materials (SBOMs). These topics show how security risks can appear at different stages, from development and third-party libraries to network routing and data transparency. Understanding the risks helps developers make safer design choices, identify weaknesses, and use trusted security practices. The research will use reliable sources, prioritizing official documentation and primary references, to explain key concepts, practical protections, and remaining limitations. For the Software track, the focus is on where application configuration and secrets should be stored and why they should not be hard-coded into source code.
## Software
The Twelve-Factor App recommends storing deployment-specific configuration in environment variables rather than hard-coding it in source code. Examples include database credentials, API keys, and service URLs. Keeping configuration separate allows the same codebase to run in different environments without code changes. It also reduces the risk of exposing secrets when code is shared publicly. Sensitive values should be managed securely and never committed to a source repository.

Resource: The Twelve-Factor App: Config - https://12factor.net/config
## AI
Adversarial machine learning attacks target the behavior or training process of machine-learning systems. In an evasion attack, an attacker changes an input at inference time to cause an incorrect prediction without necessarily changing the training data. In a poisoning attack, the attacker manipulates training data or the learning process to influence the model. Other categories include privacy attacks, which may expose information about training data. Defenses depend on the attack type and system lifecycle.

Resource: NIST AI 100-2 E2025: Adversarial Machine Learning - https://csrc.nist.gov/pubs/ai/100/2/e2025/final
## Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) defines security controls for assessing mobile applications, including Android and iOS apps. Its control groups cover secure storage, cryptography, authentication, network communication, platform interaction, code quality, resilience, and privacy. Developers can use MASVS as a security baseline during design and development, while testers can check implementations against its controls. The OWASP Mobile Application Security Testing Guide (MASTG) provides practical testing guidance to help verify those controls.

Resource: OWASP MASVS - https://mas.owasp.org/MASVS/
