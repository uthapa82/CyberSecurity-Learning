#### Threats, Attacks and Vulnerabilities 

**1. Malware**
* Viruses (Spread by medium), Worms (Spread by themselves) and Trojans (Disguise as legitimate software) 
    - The RTM Worm : Robert T. Morris (1988)
    - Stuxnet Worm 
    - Remote Access Trojans (RAT)
* Propagation Mechanism: the way that a malware object spreads 
* Payload : the malicious action that the malware performs 
* Understanding Blackdoors and logic bombs 


**2. Understanding Attackers**
* Internal vs external attackers 
* Level of sophistication, access to resources, motivation, intent
* Script Kiddies, Hacktivists, Criminal Syndicates, Competitors (corporate espionage), Nation-state (Advanced persistent threat-APT)
* White Hats, Black Hats, Grey Hats 
* Insider Threats, Privilege Escalation Attacks
    - Background Checks 
    - Least Privilege: give users only the permissions that they need 
    - require mulitple users to carry out sensitive operations 
* Shadow IT : use of unapproved technology services 
* Attack Vectors : Provide an attack Path 
    - Email : phising and malicious content 
    - Social Media : spread malware and be used as part of an influence campaign 
    - Flash Drives and other removable media 
    - USB cables with embedded chip 
    - Card skimmers : magnetic stripes which may then be used in card cloning attacks
    - Cloud services : Scan for improperly secured content and systems 
    - Direct access to systems 
    - Supply Chain tampering and insert backdoors 
    - wireless networks access 
* Zero days and the advanced presistent threat
    - Patches for vulnerabilities 
    - Ethical Disclosure 
        - Notify the vendor of the vulnerability 
        - Provide the vendor a resonable amount of time to create a patch 
        - Disclose the vulnerability publicly 
    - Zero-Day Vulnerability 
    - Window of Vulnerability : the time between the discovery of a zero-day vulnerability and the release of a security update 
    - APT 
        - well-funded and highly skilled 
        - typically government sponsored 
        - access to zero days and other sophisticated weapons 
        - work methodically to gain access to a target 
    - Defending against APTs 
        - build a stron security foundation
        - implement strong encryption 
        - use rigorous monitoring 

**3. Threat Intelligence** 
* set of activities that an organization undertakes to educate itself about changes in the cybersecurity threat landscape, and adapt security controls based upon that information 
* Open-Source Intelligence (use public information)
    - security websites 
    - vulnerability databases 
    - News media 
    - social media 
    - dark web 
    - information sharing centers 
    - file repositories 
    - code repositories 
    - security researchers 
* Email Address Harvesting : searches for valid addresses 
* Timeliness : how promptly is threat intelligence delivered ?
* Accuracy: Is the data correct ?
* Reliability: Is the provider consistent ? 
* Threat Indicators: Properties that describe a threat 
    - Cyber Observable eXpression(CybOX)
    - Structured Threat Information eXpression(STIX)
    - Trusted Automated eXchange of Indicator Information (TAXII)
    - OpenIOC: mandiant threat framework 
    - TAXXI, STIX and CybOX facilitate information sharing 
* Functions Supported by Intelligence 
    - Incident response 
    - Vulnerability Management 
    - Risk Management 
    - Security Engineering 
    - Detection and monitoring 
* ISACs : Information Sharing and Analysis Centers 
* Reputational Threat Research : identify potentially malicious actors based upon their use of IP address, email address, domains etc that were previously used in attacks 
* Behavioral Threat Research : identify potentially malicious actors based upon the similarity of their behaviors to past attackers 
* Research Sources 
    - Vendor websites 
    - Vulnerability Feeds 
    - Cybersecurity Conferences 
    - Academic journals 
    - RFC documents 
    - Local Industry Groups 
    - Social Media 
    - Threat Feeds 
    - Adversary tactis, techniques, and procedures (TTP)
* Threat Modeling : identifies and prioritizes threats 
    - Structured approach to threat management 
        - Asset Focus : use the asset inventory as the basis for the analysis 
        - Threat Focus : identify how specific threats may affect each information system 
        - Service Focus : identify the impact of various threats on a specific service 
* Automating threat intelligence 
    - Automate the blacklisting of IP addresses from threat feeds 
    - Automation may cause disruption so, alert only feature can be enabled initially to determine the possible IP that could be blocked 
    - Combine different threat feeds for more robust filtering 
* Data Enrichment 
    - Automatically supplements incident data 
* Sample Data Enrichment Tasks
    - Perform source address reconnaissance 
    - Retrieve related log records 
    - Trigger a vulnerability scan 
* Security Orchestration, Automation, and Response (SOAR) platforms enhance SIEM capabilities 
* Machine Learning : allows the automated creation of malware signatures 
* Threat hunting 
    - An organized, systematic approach to seeking out indicators of compromise on our networks using expertise and analytic techniques 
    - Begin by establishing a hypothesis 
    - Indicator of Compromise 
        - Unusual binary files 
        - Unexpected processes or resource consumption
        - Deviation in network traffic 
        - Unexplained log entries 
        - Unapproved configuration changes 
    - After discovering a compromise move into incident response 

1. Basic principle underlying threat hunting activities ==> assumption of compromise 
2. Best assists with the automation of security workflows ==> SOAR 
3. STIX is a standardized language used to communicate security information between systems and organizations 
