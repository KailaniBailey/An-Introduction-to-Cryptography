# Rivest-Shamir-Adleman (RSA) encryption
## What is RSA?
RSA is a popular and widely used public-key cryptography algorithm named after its inventors Ron Rivest, Adi Shamir, and Leonard Adleman. It's used for secure communication over the internet, such as online transactions, email, and messaging apps.

The RSA algorithm uses two large prime numbers to generate a public and a private key pair. A prime number is a number that only has two numbers which divide it without leaving a remainder. For example, the following numbers are all prime, . The public key is used to encrypt messages, while the private key is used to decrypt them. The security of the algorithm is based on the difficulty of factoring the product of two large prime numbers, which are used to generate the keys.

To encrypt a message using RSA, the sender, Alice in the diagram below,  uses the recipient's public key (Bob's key) to encrypt the message. Once the message is encrypted, only the recipient's private key can decrypt it, ensuring that only the intended recipient can read the message.

[ Insert Image ]

### Advantages of RSA
One of the advantages of RSA is that it provides a high level of security for encrypted messages. The size of the keys used in RSA makes it really hard to break the encryption by trying all the possible keys, or by other means.

Another advantage of RSA is that it can be used for digital signatures, which allow for the verification of the authenticity of a message or document.  We will get to digital signatures later in the lesson.

Despite its strengths, RSA is not perfect and has been subject to attacks over the years. However, these attacks have generally been limited to how the encryption/decryption was implemented in computer code, rather than fundamental flaws in the algorithm itself.

### The RSA encryption mechanism
In the following section we will look at the RSA encryption mechanism. Unfortunately the reason why it is correct requires an in depth understanding of mathematics which is beyond the scope of this course. It is not essential to understand how or why the technique works - but you should develop an appreciation that there is substance behind the technique.

(If you want to appreciate the maths fully, cryptography is a topic which is often studied in a Computer Science degree!)

Let's work through the steps of key generation, encryption and decryption.

#### Key generation

Remember that for RSA there is a private key and a public key. We generate both the public and private parts of the key together. To be able to make a set of keys for use with RSA encryption/decryption we follow the following steps:

1. Choose two large distinct prime numbers  and . A prime number is a number greater than 1 that has no divisors other than 1 and itself. For example 2, 3, 5, 7,11,13,17,19.
2. Compute .
3. Compute . The symbol  is a letter in the Greek alphabet which is commonly used in mathematics, the name of the letter is lambda.  stands for lowest common multiple. This is the smallest number such that it is a multiple of both  and .
4. Choose a value  which is greater than 2, less than , and is coprime to . Two numbers are coprime if they have no common divisors.  The easiest way of choosing  is to select another prime number, less that  and then check that it is coprime with .
5. Compute a value for  such that . This can be done using the extended Euclidean algorithm - this algorithm is normally discussed in a Computer Science degree. There is a tricky bit of notation which you might be unfamiliar with in this set. The "mod" operator is another was of saying "remainder". So what this formula says is that when  is divided by  the remainder should be 1.

The public key is . and the private key is . The public key can be distributed freely with anyone.

### Encryption
To encrypt a message you must have the public key . Let  be an integer such that, , which is an encoding of the message. This might be as simple as the letter's position in the alphabet or its ascii value.

The ciphertext, which we will call , can be computed as;


That is, we raise  to the power of  then divide it by . The remainder of this division is the ciphertext.

### Decryption

To decrypt a ciphertext you must have the public key , and the ciphertext . The plaintext can be computed as;


That is, we raise  to the power of  and then divide it by . The remainder of the division is the plaintext.

## Why is RSA secure? 

The security of RSA relies on selecting large  prime numbers. The larger the prime numbers the better. If an attacker wants to read messages encrypted with RSA then they have to find out the private key. The attacker has access to the public key which comprises , and  is the product of  and . In order to be able to work out the private key the attacker must be able to determine  which is derived from  and .  If the attacker can work out the values of  and  then they would be able to compute , and if the attacker can calculate  then they will be able to calculate  - which is required for decryption. To be able to calculate  and  from  the attacker must factorise  to find two prime numbers that multiple to make . 

This problem is known as the prime factorisation problem. There is currently no known process to solve the prime factorisation problem efficiently using conventional computers. So as long as  and  are large prime numbers, and consequently  will be large also,  it is unlikely that an attacker will be successful in cracking the encryption.

### Next steps

In the next three steps you will have an opportunity to generate an RSA key pair, and then encrypt and decrypt a message.
