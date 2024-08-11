# Simple ciphers: Substitution ciphers
The Caesar cipher is a form of **substitution cipher**, so called because each letter is substituted for another. There are other types of cipher which we will focus on a little later in the lesson, but let's stick with substitution ciphers for now.  

## Substitution ciphers
As you saw with the Ceaser cipher,  a substitution cipher is a way to turn a message or a word into a secret code. In this cipher, each letter is replaced by a different letter.

For example, let's say we have a message that says "HELLO". In a simple substitution cipher, we might replace each letter with the next letter in the alphabet, so "H" would become "I", "E" would become "F", and so on. Our secret code for "HELLO" would then be "IFMMP".

In Ancient Rome, the person encrypting the message in the Caeser cipher had a table containing which letter should be substituted for each letter. The table is constructed by shifting each letter a set number of items to the right in the table. Any letters that "fall out" the end of the table wrap around to the beginning on the left hand side. 

### Example of a Caesar cipher table
The table below is an example of a Caesar cipher table where all of the characters are shifted right by three positions.
[ Table must be inserted. ]

### An example of encryption
The words "University of Leeds" can be encrypted by taking each character in the words, one at a time, and looking the character up in the top row of the table above. Then, replace that character by the character in the second row. For example:
[ Table must be inserted. ]

## Try it yourself
Now it's your turn:  

- Using the table above, decrypt this: f dp fohyhu
- What is the key in this table?
- The answers are at the bottom of this step.

## The problem of the Caesar cipher
The Caesar encryption is very simple and is very easy to undo. As there are only 25 Caesar encryption tables it doesn't take a human very long to discover the key which has been used to encrypt a message (and it takes even less time for a computer to find the key). We will look at how a computer can discover the key for a Caesar cipher later in the lesson.

Caesar ciphers should not be used for anything where security is important. There are more complicated substitution ciphers which have more available keys, such as the [Vigenère cipher](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher).

## Try it yourself: Answers
- I am clever
- 3

## Optional exercise
- Create a table like the one above where the key is 8. (ie. shift the the lower row of letters in the table 8 steps to the right).
- Decrypt the words kzgxbwozixpg qa i zmittg kwwt bwxqk bw abclg

## Additional resource
The British Broadcasting Corporation (BBC) have a great activity where you can make a Caesar cipher wheel which is great for encrypting and decrypting message. Why not have a go? Head over to the [Caesar cipher page](https://www.bbc.co.uk/bitesize/articles/z6pcg7h) and have a go.
