# Modern day cryptography
## The two types of modern cryptography
There are two types of modern cryptography; **private key** cryptography and **public key** cryptography. We will look at each of them in more detail shortly. Independent of whether it is private or public key cryptography, the reason that makes the cryptographic system secure is that there is a hard maths problem that underpins it.

Private key cryptography

Private key cryptography, sometimes called symmetric key cryptography, is a way of keeping secrets safe by using a secret key that only the sender and the recipient know. Think of the secret key as a password that only you and your friend know. The reason it is called private key cryptography is because the key must remain private in order for the encryption to be secret.

When you want to send a secret message to your friend, you use the secret key to encrypt the message so that nobody else can read it. This process is called encryption. Once the message is encrypted, you can send it to your friend over a channel of communication which need not be secure. When your friend receives the message, they use the same secret key to decrypt the message and read it. This process is called decryption. Because nobody else knows the secret key, nobody else can decrypt the message and read it. It is essential in private key cryptography that the secret that is shared between the sender and receiver is kept secret.

The illustration below shows how Alice sends a message to Bob using a private key cryptography technique.

[ Insert Illustration ]
