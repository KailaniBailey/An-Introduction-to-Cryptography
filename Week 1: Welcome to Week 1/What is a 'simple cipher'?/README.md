# What is a 'simple cipher'?
A cipher is a method used to encrypt or encode a message in order to make it unreadable by unauthorised parties. Ciphers have been used throughout history to protect sensitive information, such as military secrets or private communications.

The process of encrypting a message (sometimes called the **plaintext**) using a cipher involves substituting or scrambling the original text using a specific set of rules or mathematical functions. The resulting output, or **ciphertext**, appears to be random and unintelligible to anyone who does not know the secret key (or algorithm) used to create it.

The goal of a cipher is to ensure that only the intended recipient, who has access to the secret key (or algorithm), can decrypt the message and read its original content. 

Different ciphers use different techniques and strategies to achieve this goal, and they can vary in terms of their level of security and the amount of computing power needed to break them. 

## A history of ancient ciphers
The history of cryptography dates back to ancient civilisations, where cryptographic systems were used to protect sensitive information from unauthorised access. Two of the most well-known examples of cryptographic systems used by ancient civilisations are the systems used by the Greeks and Romans.

### Scytale ciphers
The Greeks developed several cryptographic systems, including the **scytale**. It is a type of **transposition cipher**, which means that it does not replace individual letters or symbols, but instead rearranges them in a particular order.

The scytale, pictured below, consisted of a long and narrow wooden rod, around which a strip of parchment or leather was wound. The message to be encrypted was written lengthwise along the parchment or leather. When the parchment or leather was unwound from the rod, the letters of the message would be scrambled, making it difficult to read without rewinding it onto a rod of the same diameter.

The intended recipient would have a matching rod of the same diameter, which could be used to wrap the parchment or leather around it, aligning the letters of the message in their original order, and thus decrypting the message.

The security of the scytale system relied on the fact that the diameter of the rod was known only to the sender and the intended recipient. This meant that anyone intercepting the message would not be able to read it unless they also had access to the correct rod.

The scytale encryption system was used extensively by the Spartans during their military campaigns, as it provided a secure method of communicating sensitive information. However, the scytale system was relatively simple, and it was eventually replaced by more sophisticated encryption systems that were more difficult to crack.

Despite its limitations, the scytale remains an important part of the history of cryptography and an interesting example of how even the most straightforward encryption methods can be effective when used correctly.

### The Caesar cipher
The Romans also used several cryptographic systems, and the Caesar cipher, also known as the shift cipher, is one of the simplest and most widely known encryption systems in history. It was named after Julius Caesar, who is believed to have used this system to encrypt his messages.

In the Caesar cipher, each letter of the plaintext message is shifted a certain number of places down the alphabet. The number of places shifted is determined by a key, which is a number between 1 and 25. For example, if the key is 3, the letter "A" would be replaced by the letter "D", "B" would become "E", and so on.

The Caesar cipher is a type of **substitution cipher**, meaning that each letter in the plaintext is replaced with another letter according to a fixed rule. In this case, the rule is a simple shift of the alphabet by the amount set out in the key.

### The problem of the Caesar cipher
While the Caesar cipher was effective in Julius Caesar's time, it is not a secure encryption system by today's standards. It is vulnerable to several attacks, including so-called **brute force attacks**, where an attacker simply tries every possible key until the correct one is found (more on brute force attacks later).

So, although limited, both the Greek and Roman cryptographic systems were simple but effective in providing a basic level of security to messages that needed to be kept confidential. These systems paved the way for the development of more sophisticated cryptographic systems, which are still used today to protect sensitive information and ensure secure communication.

### Try it!
In the next step, have a go with a simple cipher we have created, based on the Caesar cipher.
