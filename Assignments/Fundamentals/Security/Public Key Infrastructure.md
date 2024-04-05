##  Subject
Self signed certificates ties together several concepts covered in our first week of Security Fundamentals.  Self signed certificates are in the SSL/TLS protocol and is about security and authentication. It allows for the encryption of data communications over open networks, safeguarding against tampering and interception.  In addition, the use of SSL certificates authenticates communicating parties.  

Here are some advantages and risks of Self Signed Certificates:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ed8d280c-e1d5-4c2e-8f2b-1744b2bdd97f)


##  Assignment

Create a self-signed certificate on your VM.

Analyze some certification paths of known websites (ex. techgrounds.nl / google.com / ing.nl).

Find the list of trusted certificate roots on your pc/laptop (bonus points if you also find it in your VM).

##  Key Terms

Self-signed certificate - 

Certification path - 

Trusted certificate roots - 

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



##  Difficulties

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



  







##  Reflection/Learning
