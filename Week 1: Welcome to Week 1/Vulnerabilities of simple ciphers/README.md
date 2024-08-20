# Vulnerabilities of simple ciphers
All of the simple ciphers that we have considered so far are not safe to use as a cipher in modern times. This is because it is too easy to work out the **key**, which would allow anyone who wanted to to decrypt the ciphertext.

All ciphers rely on the idea that you can transform the plaintext into the ciphertext easily, however it is hard to recover the plaintext from the cipher text without an additional piece of information -  the **key**. Discovering the key used to encrypt a cipher is called **cracking** the cipher. If you are determined enough, it is always possible to crack a cipher. However,  it might be impractical and typically ciphers are safe because it would take too long to recover the key.  

The simple ciphers that we have discussed so far were typically used until the invention of the electronic/mechanical computer around 1920. Prior to the invention of the computer, any attempt to decrypt a message would have to be done by a human, and the computational throughput of a human is limited, therefore even the simple ciphers were reasonably effective. However, with electronic computers these ciphers are vulnerable.

As technology advances, the amount of computation power increases and this means that as time progresses the ciphers have to develop to prevent them from becoming vulnerable to advances in technology.

## Keyspace

In this step we will look at some common methods of recovering the key used to encrypt the plaintext using one of the simple ciphers.

Before we start looking at the technical detail, it is important to understand the concept of the **keyspace**. The keyspace refers to the set of all possible keys that can be used with a particular cipher.

## Caesar cipher vulnerabilities

An an illustration, let's look again at the Caesar cipher. This cipher is vulnerable to a brute force attack, which is where the attacker (the person trying to crack the cipher) keys each key in turn.

For example, they try out each key, decrypting the ciphertext, and then checking to see if the decrypted message can be read. If the text is not readable then the key was incorrect. However, if the key was correct then the text will be readable.

This is where the keyspace is important. The smaller the keyspace, the more vulnerable the cipher is to a brute-force-attack.

For the Caesar cipher, the keyspace is fixed and there is no opportunity to expand it. The keyspace for the Caesar cipher is 25, that is, there are only 25 possible keys. With a key space of this size, it is almost practical for a human to crack the code without the assistance of a computer, just by using trial and error.  And with a computer the keyspace is far too small and is vulnerable to a brute force attack.

As time has progressed most ciphers increase the size of the key to make the keyspace larger which makes brute force attacks impractical. 

## Using character frequency analysis to crack the code

A slightly more efficient way of cracking the Caesar cipher is using character frequency analysis. This idea relies on an interesting fact that the average frequency of each letter in a language is different. This can be exploited, with high probability, to find the key without having to employ a brute-force-attack approach.

The letter frequency of the English language is in the table below.

[ Insert Table ]

These statistics are gathered by taking large quantities of text written in English and calculating the percentage of frequency of each character. If we are presented with a long enough text we would expect to see a roughly equivalent letter frequency distribution. Looking at the frequency distribution to determine the key is called **frequency analysis**.

When we perform frequency analysis on ciphertext which has been encrypted using the Caesar cipher we would expect to see a similar letter frequency distribution, only the peaks in the distribution would be elsewhere. When we use this idea to crack a cipher, we calculate the frequency analysis over the cipher text and look for the most frequent letter. We then formulate the hypothesis that this most frequently occurring letter corresponds to the character "E", as this is the most frequently occurring character in the English language. From this we can deduce the key used to offset the alphabet. This approach is a marginal improvement over using the brute force approach.

## Next steps

You have covered a lot of ground in this lesson - time for a quiz to check your understanding!
