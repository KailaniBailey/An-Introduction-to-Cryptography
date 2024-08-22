# Modern day cryptography
## The two types of modern cryptography
There are two types of modern cryptography; **private key** cryptography and **public key** cryptography. We will look at each of them in more detail shortly. Independent of whether it is private or public key cryptography, the reason that makes the cryptographic system secure is that there is a hard maths problem that underpins it.

Private key cryptography

Private key cryptography, sometimes called symmetric key cryptography, is a way of keeping secrets safe by using a secret key that only the sender and the recipient know. Think of the secret key as a password that only you and your friend know. The reason it is called private key cryptography is because the key must remain private in order for the encryption to be secret.

When you want to send a secret message to your friend, you use the secret key to encrypt the message so that nobody else can read it. This process is called encryption. Once the message is encrypted, you can send it to your friend over a channel of communication which need not be secure. When your friend receives the message, they use the same secret key to decrypt the message and read it. This process is called decryption. Because nobody else knows the secret key, nobody else can decrypt the message and read it. It is essential in private key cryptography that the secret that is shared between the sender and receiver is kept secret.

The illustration below shows how Alice sends a message to Bob using a private key cryptography technique.

[ Insert Illustration ]

Private key cryptography is extensively used on the internet. Any time you go to a website using a secure connection you are using a private key cryptographic system. There are lots of different symmetric key encryption systems. For example Data Encryption Standard (DES), and Advanced Encryption Standard (AES). You probably haven't heard of these but AES is really important and you probably use it everyday - in fact you are using it right now, without even knowing.

AES is used to secure internet traffic, so whenever you visit a website and you see the little padlock next to the address bar this indicates that your connection is secure, and it is secured using AES! 

Hypertext Transfer Protocol Secure (HTTPS) is a protocol used to securely transfer data over the internet. Whenever you visit a website and you see the padlock next to the website address this indicates that the browser is connecting securely to the server using HTTPS. It is a combination of the standard HTTP protocol and the Secure Sockets Layer/Transport Layer Security (SSL/TLS ) encryption protocol. AES is one of the encryption algorithms used in SSL/TLS to provide secure communication between web browsers and servers.

AES is considered to be a highly secure encryption algorithm, with no known successful attacks against it. It is used in a variety of applications, including secure communications, data storage, and financial transactions. Its widespread adoption and strong security make it an important tool for protecting sensitive information in today's digital world.

Public key cryptography

Public key cryptography is sometimes also called asymmetric key cryptography. With public key cryptography the key has two parts known as the public key and the private key. The two keys have different purposes in the encryption and decryption system.

Suppose that Alice and Bob want to communicate with each other. They both create a pair of keys, so Alice has a private and a public key and Bob has a separate pair of private and public keys. Alice's public key and Bob's public key can be freely distributed to anyone.

When Alice wants to send a message to Bob she takes Bob's public key and encrypts the message and then send the encrypted message to Bob via some channel of communication. When Bob receives the encrypted message he can then use his private key to decrypt the encrypted message to recover the original message that Alice wanted to send. The special thing about public key cryptography is that the public key can only encrypt messages but can't be used to decrypt messages.
