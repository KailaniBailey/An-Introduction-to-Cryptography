# Simple ciphers: Permutation ciphers
## What is a permutation cipher?
A permutation cipher is a special type of transposition cipher. In a permutation cipher we take blocks of characters from the plaintext and permute them. The word "permute" means to change the order or arrangement of a set of items or elements. It refers to the act of rearranging the items or elements of a collection in a specific order or pattern.

In mathematics, permutation refers to the arrangement of objects in a specific order or pattern. For example, if you have a set of three letters "A", "B", and "C", then there are six possible permutations: ABC, ACB, BAC, BCA, CAB, and CBA.

## An example of a permutation cipher
As an example of a permutation cipher, we could change the order of the characters in the following way:
- Let's take the characters from the plaintext in blocks of five symbols at a time.
- Let us represent these characters by the variables x1, x2, x3, x4, and x5.
- We could rearrange the character into the following order x3x1x4x5x2.
- In the permutation the third character of the plaintext becomes the first character of the ciphertext, the first character of the plaintext becomes the second character of the ciphertext, the fourth character of the plaintext becomes the third character of the ciphertext, the fifth character of the plaintext becomes the fourth character of the ciphertext, and the second character of the plaintext becomes the fifth character of the ciphertext.
- If the plaintext contains more than five characters we simply repeat the same process for the next set of five characters.

Clearly, for this cipher to work the length of the plaintext has to be a multiple of the length of the transposition block. If we apply this permutation to the plaintext "University of Leeds" then we would get the following:

[ Insert Table ]

### Your turn!
Now you have a try: decrypt the ciphertext "MPRWUITTAOINC PSHRE QERSLIPME". The ciphertext is encrypted using the transposition where x1x2x3x4x5 is transposed as x4x1x3x2x5.

## How does this compare to the Caesar cipher?
There are lots of ways of permuting the characters in the plaintext. Comparing this to the Caesar cipher that we introduced earlier, where there were only 25 keys, transposition ciphers have more keys and more ways of rearranging the letters. For example, using the transposition scheme that we have introduced earlier, if the transposition block has length n there are n! (read as "n factorial") transposition. If you haven't encountered n! before, don't worry, it is easy, n! = n x (n-1)x ... x 1. The factorial function grows very fast. Below is a table showing you how many transpositions there are for different left transposition blocks.

[ Insert Table ]

As a result of the number of permutations being very large as the transposition block length increases, if you wanted to decrypt a message and didn't know what the transposition was then you would have to try a lot of possible permutations. This makes it not very practical for a human to do it by hand, however by using cryptanalysis techniques a computer can easily discover the transposition and decrypt a ciphertext.

## A famous permutation cipher: The Engigma machine
The [Enigma machine] is a famous machine used by the National Socialists in Germany in World War II to encrypt military messages. The efforts of the code breakers, including Alan Turig, at Bletchley Park helped to crack the Enigma. The Enigma machine at its foundation is a substitution cipher, only the substitution key changes for every character encrypted. It took a lot of effort, and some of the brightest minds of the time, to crack Enigma and it wouldn't have been possible without the developments of specialized electromechanical computers.
