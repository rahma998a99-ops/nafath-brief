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

Cybersecurity

Data

Misconception in My Track

Open Question