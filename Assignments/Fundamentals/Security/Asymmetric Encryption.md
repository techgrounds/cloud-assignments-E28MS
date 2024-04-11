##  Subject
Assymmetric encryption is where there are different keys used at each end of the encryption/decryption process; the sender and the recipient use two different keys. Asymmetric encryption, also known as public key encryption, uses a public key-private key pairing: data encrypted with the public key can only be decrypted with the private key.

TLS (or SSL), the protocol that makes HTTPS possible, relies partially on asymmetric encryption. A client will obtain a website's public key from that website's TLS certificate (or SSL certificate) and use that to initiate secure communication. The website keeps the private key secret.

##  Assignment

Generate a key pair.

Send an asymmetrically encrypted message to one of your peers via the public Slack channel. They should be able to decrypt the message using a key. 

The recipient should be able to read the message, but it should remain a secret to everyone else. You are not allowed to use any private messages or other communication channels besides the public Slack channel. Analyse the difference between this method and symmetric encryption.

##  Key Terms

RSA Key Pair -  involves a public key and a private key. The public key can be known by everyone and is used for encrypting messages. The intention is that messages encrypted with the public key can only be decrypted in a reasonable amount of time by using the private key.

##  Resources

[Khan Academy](https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:online-data-security/xcae6f4a7ff015e7d:data-encryption-techniques/a/public-key-encryption)


[DevGlan](https://www.devglan.com/online-tools/rsa-encryption-decryption)


[CloudFlare](https://www.cloudflare.com/en-gb/learning/ssl/what-is-asymmetric-encryption/)


[Simplilearn Cryptography](https://www.simplilearn.com/tutorials/cryptography-tutorial/asymmetric-encryption)


##  Difficulties

Understanding how the public and private keys relate to each other and enables the encryption wasn't obvious to me at first.  After a few attempts to get it to work, the practical steps were clear.  After a few tries with my team mates, we realised that we were getting muddled up with which key to use when. See below for results.

##  Results

After multiple tries and discussion, I understand the process as follows:

The *recipient* generates a key pair, containing a private and public key.

The public key gets sent to the *sender*.

The *sender* creates a message, encrypts it with the *recipient's* public key, and sends it. 

The *recipient* uses the private key to unscramble the message. 

If the *recipient* wants to respond, the process moves in reverse. 



Here I generated a key pair:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/87478ed9-4a35-4c4c-8f99-315e291e5243)


Here I shared the public key with my team member:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/48cc305c-d96b-4056-aed4-45cb251bdc6f)


Using the same tool, I was able to decrypt his message making use of the public key.


##  Reflection/Learning

This was a great example of where the right tool for the job makes everything so much easier.  I wasted time trying to use the key pair generator provided in the excercise but it was only half of the solution.  Finding one tool that does everything was a much more efficient use of my time.
