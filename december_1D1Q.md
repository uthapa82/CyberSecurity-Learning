**1. Botnet ---> short for *'robot network'***
* A piece of malware that infects a computer to carry out commands under the remote control of the attacker
* Group of internet connected devices such as servers, PCs, mobile devices, etc that are affected and controlled by malware
* Used for stealing data, sending spam, performing DDoS attack and more, and also to enable the user to access the device and its connection 
* Under the control of a single attacking party, known as the **bot-herder or bot master**
* common botnet actions 
    * Email Spam
        * used for sending out spam messages , including malware 
        * **The Cutwail Botnet** can send up to 74 billion messages per day 

    * DDoS attacks
        * overload a target network or server with requests 
        * rendering it inaccessible to its intended users 

    * Financial breach 
        * Designed for the direct thefts of funds from enterprises and credit card information 
        * Financial botnets eg. **ZeuS botnet** 

    * Targeted intrusions 
        * smaller botnets designed to compromise specific high-value systems of organization from which attackers can penetrate and intrude further into the network 
        * attackers target their most valuable assets, including financial data, research and development, intellectual property and customer information 

* Created when the bot-herder sends the bot from his CC(command and control servers) to an unknowing recipient using file sharing, email, or social media application protocols 
* Once the recipient opens the malicious file on his computer, the bot reports back to command and control where the bot-herder can dictate commands to infected computers 

![botnet](images/botnet-infrastructure.png)

![botnet 2](images/botnet-2.png)

<br>

**2. Difference between hashing and enryption**

*Encryption*
* two way function where data is passed in as plaintext and comes out as ciphertext
* can be reversed or decrypted 
* process of encoding simple text and other information that can be accessed by the sole authorized entity if it has a decryption key 
* number of encryption systems:
    1. Asymmetric encryption : public-key encryption 
        * deploys two key public and private 
        * slower than symmetric encryption and consumes more processing power when encrypting data 
    2. Symmetric encryption: 
        * same secret key to encrypt and decrypt the message 
        * both sender and the receiver should have the key 
        * oldest technique of encryption 

**Purpose of Encryption**
* Protect data from an unauthorized person who wants to read or get the information 
* Confidentiality 
* Granular access control : user are limited to what they can see and do 
* Authentication: the origin of the message received can be traced 

Examples : AES is symmetric encryption, PGP is an example of an asymmetric encryption algorithm
    

*Hashing*
* also called **digest**
* a number generated from a string of text
* one way meaning the plaintext is scrambled into a unique digest through the use of a salt that cannot be decrypted 
* Technically hashing can be reversed but the computational power needed to decrypt it makes decryption infeasible 
* hashing will take arbitrary input and produce a string with a fixed length
* a hash algorithm is a function that can be used to map out data of random size to data of fixed size 
* hash values, hash codes and hash sums are returned by functions during hashing 

* **Types of hashing algorithms**
    * MD4 : Ronald Rivest , 128 bits length 
    * SHA Algorithm : Secure Hash Algorithm designed by NSA , 160 bits length, SHA, SHA-1, SHA-2 (256 bit) are different versions 
    * RIPMEND

**Purpose of hashing**
1. Compare large amount of data, it's easier comparing hashes than the data itself 
2. Used in Cryptographic applications like a digital signatures 
3. used to generate random strings to avoid duplication of data stored in databases 

![hashing v encryption](images/hashing%20vs%20encryption.png)

**3. PGP :-Pretty Good Privacy -- Philip R. Zimmermann**
* Encryption program or application that implements the OpenPGP public key cryptography standard
* used to encrypt and decrypt email, authenticate messages with digital signatures  and encrypted stored files 
* Original PGP was offered in two versions :
    * Using the RSA for key exchange 
    * Using the Diffie-Hellman for key exchange 
* PGP concepts 
    * Alice and Bob 
    * Web of Trust 
    * Implict Trust : Alice has vetted Bob -- willing to assert (through her own signature) that she found Bob to be who he says he is and that the email and key pair are under Bob's control
    * Explict Trust: Occurs when Carlos, a third generic user is willing to trust Alice's judgement about other individuals 
    * Key Signing 
    * ASCII armor:- also known as Radix-64 encoding is a way of formatting encrypted data in a printable format 
    * Session Key : symmetric encryption key used for just one encryption session

![pgp](images/pgp.png)

* [Additional information](https://www.varonis.com/blog/pgp-encryption) 

**4.Radix -64 Encoding**
* Radix 64 or base 64 is a binary-to-text encoding system that is designed to allow binary data to be represented in ASCII string format 
* allows binary data stored in octets (i.e.bytes to be expressed as printable characters)
* requires the binary input to be split into block of 6
* which are then mapped onto a character set of printable characters 
* Radix-64 characterset includes 
    * A-Z
    * a-z
    * 0-9
    * the additional characters '+' and '/' 
* results in 33% more bytes -- every 3 input bytes is converted to 4 output 

![Radix-64 example](images/Radix-64%20eg.png)

**5. SSL/TLS**
**Secure Sockets Layer**
* standard technology for keeping an internet connection secure and safeguarding any sensitive data that is being sent between two systems 
* preventing adversary from reading and modifying any information transferred including personal details, payment information etc 
* Uses encryption algorithms to scramble data in transit 
* SSL is installed on the server side but there are visual cues on the browser 
    * https:// at the start of the web address 
* Certificate Authorities (CAs) can also authenticate the identity of the owner of website
    * Domain Validation Certificates : control over domain name
    * Organization Validation Certificates: not only domain name, prove that the company is registered and legally accountable as a business 
    * Extended Validation Certificates : 

**Transport Layer Security**
* Updated more secure version of SSL 
* most up tp date TLS certificates with the option of ECC, RSA or DSA encryption 

[additional info](https://www.websecurity.digicert.com/security-topics/what-is-ssl-tls-https)

* Difference between SSL and TLS 

| SSL   |   TLS |
| ----- | ----- |
| supports the Fortezza algorithm | does not support the Fortezza algorithm|
| the message digest is used to create a master secret | a Pseudo-random function is used to create a master secret|
| Message Authentication Code protocol is used | Hashed Message Authentication Code Protocol is used |
| more complex than TLS | Simple |
| less secured | provides high security|
| less reliable and slower | highly reliable and upgraded, provides less latency |
| uses port to set up explicit connection | uses protocol to set up implicit connection| 

**6. How does SSL/TLS Encryption Work**
* Uses both asymmetric and symmetric encryption to protect the confidentiality and integrity of data-in-transit 
* asymmetric encryption is used to establish a secure session between client and a server 
* symmetric encryption is used to exchange data 
    * The client contact the server using a secure URL (Https)
    * server sends the client its certificate and public key 
    * client verifies this with a Trusted Root Certification Authority to ensure the certificate is legitimate 
    * client and server negotiate the strongest type of encryption that each can support 
    * client encrypts a session(secret) key with the server's public key and sends it back to the server 
    * the server decrypts the client communication with its private key and the session is established 
    * the session key(symmetric encryption) is now used to encrypt and decrypt data transmitted between the client and server 

* Both client and server are now using HTTPS(SSL/TLS + HTTP) for their communication 

**7. Difference between RSA and Diffe-Hellman Key Exchange**
* DH approach generates a public and private key on both sides of the transaction but only shares the public key 
* DH is  also known as an exponential key exchange 

* ![DH](images/DH.png)

* Standard for generating a session key in public 
* High processor overhead 
* Not used for bulk or stream encryption but rather to create the initial session key for starting the encrypted session

[more-info](https://www.encryptionconsulting.com/diffie-hellman-key-exchange-vs-rsa/)

* DH Mathematically helps two parties which involves in the communication to generate a Secret key (symmetric key) at each side which are identical and same , this key is used for encryption and decryption at both sides 

* RSA mathematically helps two parties which involves in the communication to generate a pair of keys(public and private) at each side, where public key is used for encrypt and private key is used for decryption 


**8. Data Loss Prevention (DLP)**
* Strategy that detects potential data breaches or data exfiltration transmissions and prevents them by monitoring, detecting and blocking sensitive data while in use (endpoint actions), in-motion(network traffic) and at rest (data storage)

* Data Leakage Prevention 
* Sensitive data, information must be protected against unauthorized access to safeguard the privacy or security of an individual or organization 
* Health Records, Intellectual property, Credit card information 
* implementing SIEM and IDS/IPS to protect coorporate data 
* regulatory and compliance standards such as HIPAA, PCI-DSS, GDPR

*How DLP System work*
* DLP for the endpoint: Data residing on the desktop, lapotp, USB storafe, virtual desktops 
* DLP at Rest or for storage: Ususally unstructured data residing on a server or structured data residing on Databases 
* DLP for Network: Data that transits or leaves the network to the internet 
* DLP for cloud : Data residing in Google Drive, office 365 email, personal email providers 

![DLP](./images/DLP.png)

Techniques used by DLP :

* Pattern Matching
    - content awarness and contextual analysis 
    - capturing the envelope and analyzing the content 
    - regular expressions (regex)
    - most common pattern detected by a DLP is the SSN 

* Fingerprinting
    - algorithms that map data such as documents and files to shorter text strings 
    - Document fingerprinting is especially useful for identifying sensitive data within forms including:
        - Government forms such as tax documents 
        - HIPAA and other regulatory compliance forms 
        - Employee documentation forms used by finance or human resources 

* Symantec DLP :
    - Exact Data Matching (EDM) - detects content by fingerprinting structured data sources, including databases, directory servers, or other structured data files 

    - Index Document Matching (IDM) 
        - detect confedential data stored in unstructured data, including Microsofy office documents: PDFs and binary files such as JPEGs, CAD designs, and multimedia files 
        - also detects "derived" content such as text that has been copied from a source document to another file 


*Top DLP Best practices*
1. Identify the Crown Jewels 
    - Top-down approach
    - Input form technical leaders shared during the maturation of the DLP program in order to enhance value and creativity 

2. Research Multiple Vendors 
    -  Satisfaction with Support, incident, workflow and overall confidence level 
    - Gartner can also be used as a reference to determin the performance of the DLP vendor 

3. Define Incident Response and Remediation 
    - The downfall of DLP installations is poor planning for incident triage 

4. Crawl, Walk, and Run 
    - do not boil the ocean right out of the gate 
    - go for small wins instead of turning on every single policy checkbox available 
    - otherwise it will overwhelm the system and inundate the system with massive amounts of incidents, therefore defeating the purpose of the investment 

5. Perform a Proof of Concept Exercises 
    - goal is to replicate functionality and test the feature sets 
    - pilot program 
    - test compliance needs and observe deficiencies in triage process 

6. Identify the DLP stakeholders and support team   
    - Managed Service Provider that speicalizes in DLP 

7. Regularly inform stakeholders of the State of the DLP Program 
    - informed of the state of the program
    - Consider creating a DLP committee comprised of Executive leadership members and key business unit leaders 

* A network security policy can be created to prevent file uploads to Gmail
* The component utilized to enforce this would be data in motion, or DLP for Network

![DLP framework](./images/DLP-framework.png)

