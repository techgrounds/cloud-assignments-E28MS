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



##  Difficulties

##  Results

1.  Hashing is a cryptographic process that can be used to validate the authenticity and integrity of various types of input. It is widely used in authentication systems to avoid storing plaintext passwords in databases, but is also used to validate files, documents and other types of data.

It is preferred over encryption when storing passwords inside databases because in the event of a compromise attackers won’t get access to the plaintext passwords and there’s no reason for the website to ever know the user’s plaintext password. 

##  Learning/Reflection
