Version: NAFATH-V4
Track: Networking

Overview
A national service provider depends on multiple IT fields to deliver reliable and secure services. 
Software security ensures that applications store configuration and secrets safely 
and reduces the risk of exposing sensitive information. AI security helps 
identify attacks that manipulate machine learning models or their inputs. Mobile application 
security provides structured checks to verify that apps protect user data and follow recognized security requirements. 
Networking security is essential because incorrect or malicious internet route announcements can redirect traffic away 
from its intended destination. Cybersecurity practices help detect and fix vulnerabilities that attackers could exploit
to gain access or execute malicious actions. Data security and software supply chain transparency help teams understand
which components their systems depend on. Together, these six fields support risk reduction, service reliability, 
and informed technical decisions. This brief also examines BGP route hijacking and how RPKI helps validate route origins.

Software
The Twelve-Factor App methodology recommends storing configuration in environment variables instead of hard-coding 
it into application code. Configuration includes values that may change between deployments, such as service addresses, 
credentials, and hostnames. Keeping these values separate allows teams to change settings without modifying the code. 
It also reduces the risk of exposing credentials when a codebase is shared or made public.
Resource: The Twelve-Factor App - Config - https://12factor.net/config

AI 
Adversarial machine-learning attacks include evasion and poisoning. Evasion attacks modify inputs during model use to 
cause incorrect predictions, even when the model has already been trained. Poisoning attacks manipulate training data, 
for example by adding misleading or incorrectly labelled samples, which can affect what the model learns. The main difference
 is that evasion targets inputs at prediction time, while poisoning targets the training process.
Resource: What Is Adversarial Machine Learning? Types of Attacks & Defenses - https://www.datacamp.com/blog/adversarial-machine-learning

Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) defines security controls for mobile applications. 
It covers areas such as secure data storage, cryptography, authentication, network communication, platform interaction, and privacy. 
Development teams can use these controls as a checklist, while security testers assess whether the application meets the relevant requirements. 
The OWASP Mobile Application Security Testing Guide provides further guidance on testing these security areas.
Resource: OWASP - Mobile Application Security Verification Standard - https://mas.owasp.org/MASVS/

Networking
BGP route hijacking occurs when a network announces an IP prefix it is not authorised to originate, potentially redirecting traffic 
through an unintended network. Resource Public Key Infrastructure (RPKI) supports Route Origin Validation through Route Origin Authorisations (ROAs), 
which identify authorised origins for prefixes. Routers can use this information to classify route announcements. However, origin validation does not 
verify the entire AS path, so RPKI cannot prevent every routing attack.
Resource: RIPE NCC - BGP Origin Validation - https://www.ripe.net/manage-ips-and-asns/resource-management/rpki/bgp-origin-validation/

Cybersecurity
Log4Shell (CVE-2021-44228) is a critical remote-code-execution vulnerability affecting certain versions of Apache Log4j 2, a Java logging library. 
An attacker could exploit a vulnerable application using specially crafted input. Organizations should identify affected systems, install vendor-supported 
security updates, and verify that the fixes are effective. They should also investigate signs of possible compromise rather than relying only on temporary workarounds.
Resource: CISA - Mitigating Log4Shell and Other Log4j-Related Vulnerabilities - https://www.cisa.gov/news-events/cybersecurity-advisories/aa21-356a

Data
A Software Bill of Materials (SBOM) is a structured inventory of software components and their relationships. It helps organizations understand which 
dependencies are included in their systems and identify products that may be affected by a vulnerability. Important information includes component names, versions, 
supplier details, unique identifiers, dependency relationships, and information about the SBOM author and creation time. Accurate SBOM records support vulnerability 
management and software supply-chain transparency.
Resource: CISA - 2025 Minimum Elements for a Software Bill of Materials - https://www.cisa.gov/sites/default/files/2025-08/2025_CISA_SBOM_Minimum_Elements.pdf

Misconception in My Track
Some people think that RPKI completely stops BGP route hijacking, but this is not true. RPKI checks if an IP prefix is allowed to be announced by a specific Autonomous System (AS). 
However, it does not check the whole route or make sure that the traffic follows a secure path. So, RPKI helps reduce routing risks, but other security methods are still needed. 
This limitation is explained in the Summary section of the RIPE NCC BGP Origin Validation resource.

Open Question
How can network operators improve BGP route security when some networks have not deployed RPKI origin validation, and how can they detect suspicious route changes quickly?
