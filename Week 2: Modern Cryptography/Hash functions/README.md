# Hash functions
Sometimes, we need to store data securely. For example, when you create an account on a website you normally set up a password so that you can log in. However, you want the password to be stored securely so that no one can read it, and thus potentially be able to login as you. In these types of circumstances we can use **hash functions**. Rather than storing the password, we can store a value which is related to the password so that if anyone manages to steal the passwords they don't actually get your password, they get the value which is related to your password - but they can't use this value to login. This is a really clever idea!

**Hash functions** are mathematical functions that take in an input (some message or data) of any length and produce a fixed-length output, called a **hash value** or **digest**. The output is related to the input data, and any small change to the input data will result in a vastly different output.

## The SHA-256 function

An example of a hash function is the SHA-256 (Secure Hash Algorithm 256-bit) function, which is widely used in modern cryptography. The SHA-256 function takes an input of any length and produces a 256-bit output, which is almost always unique to that input. For example, if we apply the SHA-256 function to the string "Hello world!", we get the hash value "c0535e4be2b79ffd93291305436bf889314e4a3faec05ecffcbb7df31ad9e51a". If we change even a single character in the input string, we will get a completely different output hash value. The string "hello world!" has the SHA-256 has value of "7509e5bda0c762d2bac7f90d758b5b2263fa01ccbc542ab5e3df163be08e6ca9", the single change of the first character from a uppercase "H" to a lowercase "h" changes the hash value completely.

Hash functions are used in many areas of computer science and cryptography, such as data integrity checking, password storage and digital signatures. They are considered an essential building block in modern cryptography because they provide a mechanism for ensuring the authenticity, integrity, and confidentiality of data. Examples of well-known hash functions include SHA-256, MD5, and BLAKE2.

Hash functions are used for various purposes in computer science and cryptography, including:

- **Data integrity checking**: Hash functions are used to verify the integrity of data. A hash value is calculated for a piece of data, and this value is compared to the hash value of the same data later to check if the data has been modified in transit or storage.
- **Password storage**: Hash functions are used to store passwords securely. Instead of storing the actual password, the hash value of the password is stored in a database instead. When a user enters their password, the hash function is used to generate a hash value, which is then compared to the stored hash value.
- **Digital signatures**: Hash functions are used in digital signatures to ensure the authenticity and integrity of messages. A hash value is calculated for a message, and then the hash value is encrypted using the sender's private key. The encrypted hash value is included in the message, and the recipient can verify the authenticity and integrity of the message by decrypting the hash value using the sender's public key and comparing it to the hash value of the message.
- **Data indexing**: Hash functions can be used to create indexes for databases or search engines. A hash value is calculated for each piece of data, and this value is used as the index for the data. This allows for fast retrieval and searching of data.

The important concept of hash functions is that they are one-way only. That is, if you know the hash of a piece of data then it is not possible to recover the data, so hash functions can be used as proof of ownership of data.

In the example of SHA-256, the output of the SHA-256 hash function is a 64 character sequence. Each position in the sequence can have 62 possible values: it can be any lowercase character from the Latin alphabet (26 characters), it can be any uppercase character from the Latin alphabet (26 characters) and finally any number from 0-9 (10 characters) - in total 62 possibilities. With a little bit of careful counting there are  possible hash values.

Although this is a very large number of hash values, it is considerably smaller than the number of potential messages that could be hashed. The consequence of this (two input values producing the same hash value) is what is known as a hash collision.

## Hash collisions

A **hash collision** occurs when two different input values produce the same output hash value from a hash function. In other words, the hash function maps two different inputs to the same output, which can create security vulnerabilities in some applications.

For example, in the illustration below, we can see that the keys "Edmund" and "Alice" are hashed to the same value, "CxC8Jg14Fj". Also, the keys "Debra" and "Eve" are hashed to the same value, "W72FD000jP5".

[ Insert Image ]

In general, hash collisions can be problematic because they can allow attackers to create fake data with the same hash value as legitimate data. This can lead to various security vulnerabilities, such as data integrity violations or forged digital signatures. Therefore, hash functions are designed to minimise the probability of hash collisions occurring, such as using larger hash values or more sophisticated hash algorithms.

We will see an application of hash functions in the next section when we look at digital signatures.
