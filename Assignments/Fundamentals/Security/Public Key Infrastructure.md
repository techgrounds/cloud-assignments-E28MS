##  Subject
Self signed certificates ties together several concepts covered in our first week of Security Fundamentals.  Self signed certificates are in the SSL/TLS protocol and is about security and authentication. It allows for the encryption of data communications over open networks, safeguarding against tampering and interception.  In addition, the use of SSL certificates authenticates communicating parties.  

Self-signed certificate transactions usually present a far smaller attack surface by eliminating both the complex certificate chain validation,and certificate revocation checks like CRL and OCSP.

Here are some advantages and risks of Self Signed Certificates:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ed8d280c-e1d5-4c2e-8f2b-1744b2bdd97f)


##  Assignment

Create a self-signed certificate on your VM.

Analyze some certification paths of known websites (ex. techgrounds.nl / google.com / ing.nl).

Find the list of trusted certificate roots on your pc/laptop (bonus points if you also find it in your VM).

##  Key Terms

Self-signed certificate - These are public key certificates that are not signed by a Certificate Authority

Root certificiate -  a root certificate is a public key certificate that identifies a root certificate authority (CA).

CRL - a list of digital certificates that have been revoked by the issuing certificate authority (CA) before their scheduled expiration date and should no longer be trusted". CRLs are no longer required by the CA/Browser forum as alternate certificate revocation technologies (such as OCSP) are increasingly used instead. Nevertheless, CRLs are still widely used by the CAs.

OCSP- Online Certificate Status Protocol is an Internet protocol used for obtaining the revocation status of an X.509 digital certificate

X.509 - In cryptography, X.509 is an International Telecommunication Union (ITU) standard defining the format of public key certificates. X.509 certificates are used in many Internet protocols, including TLS/SSL, which is the basis for HTTPS, the secure protocol for browsing the web. They are also used in offline applications, like electronic signatures.

SSL -  Secure Sockets Layer is a communication protocol, or set of rules, that creates a secure connection between two devices or applications on a network. 

TLS -  Transport Layer Security is the upgraded version of SSL that fixes existing SSL vulnerabilities. TLS authenticates more efficiently and continues to support encrypted communication channels.

Root Certificate Authority (Root CA): This is the top-level certificate in the chain. It is self-signed and is used to sign intermediate CAs.

Intermediate Certificate Authority (Intermediate CA): This certificate is signed by the Root CA. It is used to sign server certificates.

Server Certificate: This certificate is signed by the Intermediate CA and is presented by the server to the client during an SSL/TLS handshake.



##  Resources

[Key Factor](https://www.keyfactor.com/blog/self-signed-certificate-risks/)

[Amazon Difference Between SSL and TLS](https://aws.amazon.com/compare/the-difference-between-ssl-and-tls/#:~:text=SSL%20is%20technology%20your%20applications,that%20fixes%20existing%20SSL%20vulnerabilities.)

[Moon Point](https://support.moonpoint.com/os/windows/certificates/trusted_root.php)

[SSL Certificate Location](https://serverfault.com/questions/62496/ssl-certificate-location-on-unix-linux)

ChatGPT

[Wikipedia Self Signed Certificate](https://en.wikipedia.org/wiki/Self-signed_certificate)

[Wikipedia Certificate Revocation](https://en.wikipedia.org/wiki/Certificate_revocation)

[Wikipedia Root Certificate](https://en.wikipedia.org/wiki/Root_certificate)





##  Difficulties

No particular difficulties encountered during this assignment.

##  Results

1.  Here I created a self-signed certificate on my VM:  

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ed843398-2ed0-48eb-a268-3e3a2a7ad699)

2.  Here I inspected the certificate for Zalando.nl, by opening the developer tools and investigating the Security tab.  In the 'Details' section of the security tab is a lot of information that can be further inspected.

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6be55b2d-64b6-47b5-aac6-9abc7ccc458c)
   

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3b8c0ebb-c0ed-4ec1-a09a-4838f2ab0217)
   

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0b18f73e-a2c0-4ab5-b958-b3fea9910609)

   
   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3b5b60f2-1938-40a9-b4fe-63f4524873b7)

3.  I found the trusted root certificates on my account by opening certificate manager (certmgr.msc) in the Run command line.  I have 64 certificates but I couldn't take a print screen. When I investigated this, it seems that this is to ensure the security of my system.

I first tried this: /etc/ssl/certs/ca-certificates.crt:   But got a permission denied message.


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/072ac071-88f8-47d8-9b46-bc16e1009faf)



However, when I went to etc/ssl/certs and long listed the contents of the folder, I got this:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c31eb91f-a088-4f8b-86a0-b40472cd3a28)

And when I tried to cat the contents of the trusted root folder, it worked:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/af4edcb3-e9ab-4f7d-8b0d-d536d00f40b5)


##  Reflection/Learning
I found this assignment interesting as there was so much information available on websites I use regularly that I knew nothing about.  I feel like I'm getting pieces of the security puzzle but until I can put it into practice it's difficult to feel like I understand how it all fits together and what the interdependencies are.  I am keen to get more hands-on experience.


##  Fun fact:

The file ssl-cert-snakeoil.pem is a certificate file typically found on Debian-based Linux systems, such as Ubuntu. It's part of the default SSL/TLS configuration provided by the ssl-cert package.


The term "snakeoil" in the filename is often used humorously in the context of security to refer to a self-signed certificate or a certificate used for testing purposes. The "ssl-cert" part of the filename indicates that it's related to SSL/TLS certificates.
