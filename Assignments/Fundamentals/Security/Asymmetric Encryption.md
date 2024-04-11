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

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/a7b0f665-d540-4cdf-9223-c5408efba620)



My private key:

MIICdQIBADANBgkqhkiG9w0BAQEFAASCAl8wggJbAgEAAoGBALlLXeelOobx7NE/ZQtiFjAhq83YB2LXePteGnMV1YqQNhX+QXAmr1CzGsSPTjj2yYzjMsEm4TBJk0V19+kY3DkVOtJMg5QiXMAz9vYBUKPdC7xKCM64EGGzksKNqzhNKVoxrTIBBrRvK0T0K8CcU0Cli/Rd7L1Xwv+oqpHmoFMXAgMBAAECgYADdTOYag3wjL01nnA9SSRO26IAImLo5kp8rmHh+etVPaG0wVzpQd+Nqvn55w63o2tZdLfywM38/7J+3le1AuDBK89JckIG0A0aeRjduUp/qGCLvHNumC+TH/EGTUz0B4+K/YY9tDar/bSqELtDYEgi2Sdmq8ak3hqo74oic4VIoQJBAM5wV3S2/Hz6PeONaN1nTBN/PshF+gAOx1YgtWnOiYdWB1jlwMyByA5j8K+L6TsYAcWiu++k8dfHI5lhPiPC9KcCQQDlx37qVG1Yym6YjqOBOOVQhLi+2QJuSiwnaMpMar4nqwTBfvgfTJK1oDvnaFlBGRlYbYxU4voFoTcSnvEIn8wRAkABOn3qveQGwl536jGDj8fOHeW7v17bfTsGci9iL851tbdZehSJowQTwdh+0vBSX7Qy/uLrbCncRN0bXo7GG7TlAkAc29Rly9q75xjC0k9YwHOUjEbDuW+juG8ZOAEIXfOp+cGsJ600CSL36rr7UlC7a1KSl5ejZapvIJNRJGMzaRZxAkBzrm9yP/f4amaNpYzTxFY49qcxJ4LtUDIFxSKMfzD9brXlXzf1GL4RNArWn/UUKnKC7nZssD+w8pH2huecxRz/

My public key:

MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQC5S13npTqG8ezRP2ULYhYwIavN2Adi13j7XhpzFdWKkDYV/kFwJq9QsxrEj0449smM4zLBJuEwSZNFdffpGNw5FTrSTIOUIlzAM/b2AVCj3Qu8SgjOuBBhs5LCjas4TSlaMa0yAQa0bytE9CvAnFNApYv0Xey9V8L/qKqR5qBTFwIDAQAB


Here I decrypted a message with my private key that my team mate sent me, using the public key I sent him:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3e639db0-4778-4b45-aafc-c550e83cb9f6)


Here I encrypted a message to my team mate, using the public key he sent me:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f5eb7c29-9614-4042-a528-80bbda618e4a)




##  Reflection/Learning

This was a great example of where the right tool for the job makes everything so much easier.  I wasted time trying to use the key pair generator provided in the excercise but it was only half of the solution.  Finding one tool that does everything was a much more efficient use of my time.
