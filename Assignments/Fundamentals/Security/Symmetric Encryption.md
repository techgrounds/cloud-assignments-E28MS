##  Subject
This is the introduction into cryptography, an essential part of security and crucial to understanding how to protect data and resources from unauthorised access with malicious intent.

##  Assignment

1.  Find one more historic cipher besides the Caesar cipher.


2.  Find two digital ciphers that are being used today.


3.  Send a symmetrically encrypted message to one of your peers via the public Slack channel. They should be able to decrypt the message using a key you share with them. Try to think of a way to share this encryption key without revealing it to everyone. You are not allowed to use any private messages or other communication channels besides the public Slack channel. 

4.  Analyse the shortcomings of symmetric encryption for sending messages.

##  Key Terms

Symmetric Cipher - this is where the same key is used to encrypt and decrypt information.  It is also known as single key encryption.



Ceaser Cipher - AKA the Ceaser Shift - This is where a plain text message is encrypted by replacing each letter with a different letter of the alphabet , based on a fixed shift of the letters.  

Steganography - Hiding a secret message inside or on top of something that is not secret



##  Resources

[Geeks for Geeks](https://www.geeksforgeeks.org/symmetric-cipher-model/)

[SECplicity](https://www.secplicity.org/2017/05/25/historical-cryptography-ciphers/)

[SimpliLearn](https://www.simplilearn.com/data-encryption-methods-article)

[Khan Academy](https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:online-data-security/xcae6f4a7ff015e7d:data-encryption-techniques/a/symmetric-encryption-techniques)

ChatGPT

[AES Decryption Tool](https://the-x.cn/en-US/cryptography/Aes.aspx)

[Steganography](https://stylesuxx.github.io/steganography/)

[CompTIA](https://www.comptia.org/blog/what-is-steganography)



##  Difficulties
I found it challenging to work out how to complete a message that only one person could access as our team don't have such a long history together.  I modified the assignment so all the team members would be able to decrypt my message but not the learning coaches.  It was also difficult to know how much information to give them, so I ended up not spelling out the tools they would need to get the key hidden in the steganography image.  

I also found it challenging to decrypt a team mates message that he hid in a Mega file.  I managed to locate a clue by inspecting the file so I know which decryption method to try but I haven't been able to locate the information that I need to decrypt.  Unfortunately, due to time constraints, I may have to leave it at that.

##  Results

# 1.  The Vigenere Cipher is another historic cipher:
  
  
    A Vigenere Cipher uses a table based on multiple Caeaser Shifts, so it makes decryption using frequency analysis much more difficult.  Here is a step by step breakdown of how it works:

[Khan Academy Encryption Techniques](https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:online-data-security/xcae6f4a7ff015e7d:data-encryption-techniques/a/symmetric-encryption-techniques)

This is the table for decrypting the Vigenere Cipher, as long as you know the shift key.

	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z
A	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z
B	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A
C	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B
D	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C
E	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D
F	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E
G	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F
H	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G
I	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H
J	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I
K	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J
L	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K
M	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L
N	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M
O	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N
P	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O
Q	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P
R	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q
S	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R
T	T	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S
U	U	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T
V	V	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U
W	W	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V
X	X	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W
Y	Y	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X
Z	Z	A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y



# 2.  Two types of digital ciphers (also known as encryption algorythms) that are in use today are:


*RSA (Rivest-Shamir-Adleman): RSA is an asymmetric encryption algorithm used for secure data transmission. It relies on the difficulty of factoring large prime numbers to secure communications.

*AES (Advanced Encryption Standard) : AES is a symmetric encryption algorithm widely used to encrypt sensitive data. It supports key lengths of 128, 192, or 256 bits and is considered highly secure.






# 3.  In order to get a secret message to my team, I used AES encryption and steganography:
   

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c2b16470-d5a8-49ed-985c-488396ecd9c1)




Here is the message and key :


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/30a274aa-d906-45a1-bffb-b84e288ebeb0


# 4.  Disadvantages of symmetrical encryption:

   *  Getting the key to someone without others also getting it
   *  Not good for large groups
   *  For the purposes of this excercise, it felt like a multi step, cumbersome process that was not efficient to execute
   *  If people lost their key, they won't be able to decrypt the message



##  Learning/Reflection

I found this excercise unexpectedly fun but also frustrating as I have no experience with decrypting.  It was interesting to note the vast amount of tools out there to encrypt and decrypt information.  It was challenging to think through the whole assignment and difficult to complete it with people you don't know well, and certainly not on individual level.
