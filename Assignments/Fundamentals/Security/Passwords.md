## Subject

##  Assignment

1.  Find out what hashing is and why it is preferred over symmetric encryption for storing passwords.

2.  Find out how a Rainbow Table can be used to crack hashed passwords.

3.  Below are two MD5 password hashes. One is a weak password, the other is a string of 16 randomly generated characters. Try to look up both hashes in a Rainbow Table.

03F6D7D1D9AAE7160C05F71CE485AD31

03D086C9B98F90D628F2D1BD84CFA6CA


4.  Create a new user in Linux with the password 12345. Look up the hash in a Rainbow Table.

5.  Despite the bad password, and the fact that Linux uses common hashing algorithms, you won’t get a match in the Rainbow Table. This is because the password is salted. To understand how salting works, find a peer who has the same password in /etc/shadow, and compare hashes.

##  Key Terms



*Encryption* -  scrambles data that can be decoded with a key. The intent is to pass the information to another party, and the recipient will use keys to decipher the data.

*Hashing* -  also scrambles data, but the intent is to prove its authenticity. Administrators can run a check on hashed data to determine the contents haven't been touched or altered while in storage. No deciphering key exists.  Hashing is a cryptographic process that can be used to validate the authenticity and integrity of various types of input. It is widely used in authentication systems to avoid storing plaintext passwords in databases, but is also used to validate files, documents and other types of data

*Salting* - 

*Rainbow Tables* - A rainbow table is a precomputed table for caching the outputs of a cryptographic hash function, usually for cracking password hashes. 

Passwords are typically stored not in plain text form, but as hash values. If such a database of hashed passwords falls into the hands of an attacker, they can use a precomputed rainbow table to recover the plaintext passwords.  

In laymens terms, a rainbow table is essentially a precomputed table that stores these pairs of passwords and their hashes. It's like having a big dictionary where you can look up a hash and find the corresponding password, or vice versa.

+MD5* - A common hashing algorythm.  It has flaws, but it is still used.  For instance, it's 128 bit strength is not strong enough to offer good protection.

##  Resources

[Wikipedia](https://en.wikipedia.org/wiki/Rainbow_table)

ChatGPT

[Nord VPN](https://nordvpn.com/blog/hashing-vs-encryption/)

[Okta](https://www.okta.com/identity-101/hashing-vs-encryption/#:~:text=Consider%20these%20basic%20definitions%3A,is%20to%20prove%20its%20authenticity.)

[CSO](https://www.csoonline.com/article/570229/hashing-explained-why-its-your-best-bet-to-protect-stored-passwords.html)

[Linux Config](https://linuxconfig.org/how-to-hash-passwords-on-linux)



##  Difficulties

##  Results

1.  Hashing is a cryptographic process that can be used to validate the authenticity and integrity of various types of input. It is widely used in authentication systems to avoid storing plaintext passwords in databases, but is also used to validate files, documents and other types of data.

It is preferred over encryption when storing passwords inside databases because in the event of a compromise attackers won’t get access to the plaintext passwords and there’s no reason for the website to ever know the user’s plaintext password. 

3. 1.  Here I found the weak password: welldone!

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/b25be196-d0a4-48a1-9f44-17e2a1a14e99)

3.2.  Here is the stronger, randomly generated password: (not cracked by the rainbow table)

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/bdbf5e0e-4641-43dc-8601-0820f9c287fe)

3.2  I also tried another tool with similar results:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/935c9840-455f-482b-ac20-9572287cee24)


4.  Here I created a user in my VM with password 12345, and then I hashed the password using the sha256sum command:

5.  ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ac45687a-35bc-447f-a0dc-c564e728e1c5)

   This is the hash as generated for the password: 5994471abb01112afcc18159f6cc74b4f511b99806da59b3caf5a9c173cacfc5

   Here is the result when I decrypted it with an online tool:

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f65019cd-9681-4998-91a9-a71f1cf6fee1)

   Here is a colleague's hash:

$6$M4ArJDmkUYKZd5zi$rCsls/VCM9dYCJSOathSO6Z5MkU4QFQURsA6gHe94FF9vz3U.QVVPT5l7M4R5Ol/OAn/3sYXgXTH/WyWTY5Q41:19821:0:99999:7:::

Here I opened the etc/shadow file and at the bottom is my new users password:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/e8e3dbbb-4c6e-40e4-98bf-d6daa76e80e0)





##  Learning/Reflection
