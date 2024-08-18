# Simple ciphers: Polygraphic ciphers
## What is a polygraphic cipher?
A polygraphic cipher is a type of substitution cipher that operates on groups of characters rather than individual characters. In other words, instead of substituting one letter for another, as it is with the Caesar cipher, polygraphic ciphers substitute one group of letters for another group of letters.

The reason for grouping letters together during the encryption process is to counter a common attack which is used against simple substitution called **letter frequency analysis**.

### The Playfair cipher

A common polygraphic cipher is the Playfair cipher. The Playfair cipher is a polygraphic substitution cipher that was invented by Charles Wheatstone in 1854, but was later improved and popularised by Lord Playfair in the 19th century. It was used during World War I and World War II as a secure method of encrypting sensitive military communications.

The Playfair cipher uses a 5x5 grid of letters, typically containing all the letters of the alphabet except for "J". The letters in the grid are arranged randomly, and each letter is used only once. For example, we might use the following grid.

[ Insert Grid ]

To encrypt a message using the Playfair cipher, the plaintext message is first divided into pairs of letters. If there is an odd number of letters, a "Z" or some other uncommon letter is added to the end to create an even number of pairs. Then, each pair is encrypted using a set of rules that determine which letters in the grid to use.

The rules for encrypting each pair of letters are as follows:
1. If the two letters are the same, insert an "X" between them and continue with the next pair.
2. If the two letters are in the same row of the grid, replace each letter with the letter to its right (wrapping around to the left if necessary).
3. If the two letters are in the same column of the grid, replace each letter with the letter below it (wrapping around to the top if necessary).
4. If the two letters are in different rows and columns, replace the first letter with the letter in the same row but in the column of the second letter, and replace the second letter with the letter in the same column but in the row of the first letter.

### A worked example
The resuling pairs of encrypted letters form the ciphertext message. For example if we want to encrypt the word "LEEDS", we first have the "pad" the word to be on an even length because we have to be able to group the characters of the work into pairs. We add the character "Z" as it is uncommon and it is easily removed when the text is decrypted. So we will encrypt the word "LEEDSZ". The pairs of characters we will encrypt as "LE", "ED" and "SZ".

The encrypt the first pair "LE", we look in the table and identify the letters "L" and "E", we then make these letters the corners of a rectangle. We then look at the orther two corners of the rectangle and replace the first character of the pair by the other other character in the rectangle on the same row. Finally we replace the second character of the pair by the other corner character in the rectangle. When we encrypt the character pair "LE" we get the character pair "FB".

[ Insert Grid ]

