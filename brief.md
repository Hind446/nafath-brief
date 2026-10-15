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
## Networking
A BGP route hijack occurs when an autonomous system announces an IP prefix it is not authorized to originate, potentially redirecting traffic through an unintended network or causing a service outage. Resource Public Key Infrastructure (RPKI) helps by allowing networks to validate whether an autonomous system is authorized to originate a prefix, using Route Origin Authorizations (ROAs). However, origin validation does not verify the complete AS path, so it cannot prevent every routing attack or route leak.

Resource: RPKI Documentation: Securing BGP - https://rpki.readthedocs.io/en/latest/rpki/securing-bgp.html
## Cybersecurity
Log4Shell (CVE-2021-44228) is a critical remote code execution vulnerability in certain versions of Apache Log4j 2, a widely used Java logging library. It can allow an attacker to trigger malicious behavior by sending crafted input to an affected application. The vulnerability received a CVSS score of 10.0, the highest severity rating. Organizations should identify affected systems, upgrade to a fixed supported Log4j version, and investigate potentially compromised systems.

Resource: CISA: Mitigating Log4Shell and Other Log4j-Related Vulnerabilities - https://www.cisa.gov/news-events/cybersecurity-advisories/aa21-356a
## Data
A Software Bill of Materials (SBOM) is a structured inventory of software components and their relationships. It helps organizations identify dependencies, investigate vulnerabilities, and understand software supply-chain risks. Minimum data fields include the component name and version, software producer, component identifiers, dependency relationships, and SBOM author. Updated guidance also includes component hashes, licenses, the tool used to generate the SBOM, a timestamp, and generation context. These details improve traceability and automated analysis.

Resource: CISA: Updated Minimum Elements for a Software Bill of Materials - https://content.govdelivery.com/accounts/USDHSCISA/bulletins/422a7eb
## Misconception in My Track
A common misconception is that applying a software update alone always proves that a system affected by Log4Shell is secure. In reality, organizations must identify all affected systems, apply appropriate fixes, and investigate signs of possible exploitation. Log4Shell (CVE-2021-44228) is a critical remote code execution vulnerability in Apache Log4j 2. Patching is essential, but security teams should also assess exposure and investigate potential compromise. The supporting guidance appears in CISA’s advisory, “Mitigating Log4Shell and Other Log4j-Related Vulnerabilities.”

Resource evidence: CISA: Mitigating Log4Shell and Other Log4j-Related Vulnerabilities - https://www.cisa.gov/news-events/cybersecurity-advisories/aa21-356a
## Open Question
How can security teams efficiently detect and investigate signs of exploitation after patching a critical vulnerability across a large and complex organization?
