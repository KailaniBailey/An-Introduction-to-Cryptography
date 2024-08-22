# Digital signatures

**Digital signatures** are an important part of the internet. Digital signatures are primarily used to verify the authenticity and integrity of digital documents or messages. A digital signature is a mathematical technique used to validate the authenticity of a digital document or message and to ensure that it has not been tampered with during transmission.

Digital signatures are commonly used in electronic transactions and online communications to provide a secure way to verify the identity of the sender and the integrity of the message or document. Digital signatures can also be used to provide non-repudiation, which means that the sender cannot deny having sent the message or document.

Some common applications of digital signatures include:

1. **Online banking**: Digital signatures can be used to sign and verify electronic transactions, ensuring that they are secure and authentic.
2. **Legal documents**: Digital signatures can be used to sign legal documents such as contracts and agreements, providing a secure and tamper-proof way to validate the authenticity of the signature.
3. **Email**: Digital signatures can be used to sign and verify emails, ensuring that they are authentic and have not been tampered with during transmission.
4. **Software**: Digital signatures can be used to sign software applications and updates, ensuring that they are authentic and have not been modified by unauthorised parties.

Consider a world without digital signatures. 

1. Suppose that Alice would like to  send a message to Bob. Alice writes the message and sends it to Bob. During the transmission of the message a third person, Eve, intercepts the message, changes it and then sends the modified message to Bob.
2. When Bob receives the message he has no idea that it has been intercepted and modified.

However, with a digital signature things are different.

1. When Alice wishes to send a message to Bob, Alice writes the message and signs it with her private digital signature and then send the message and the signature to Bob.
2. When Bob receives the message he verifies that the signature is correct and corresponds to the message that Alice sent. If the signature doesn't match the message then Bob should know to discard the message.
3. In the event that Eve wishes to modify the message then, she can. She can intercept the message, modify the message, however Eve will not be able to sign the message with Alice's private signature. So when Bob receives the modified message of Eve he will disregard it, as the signature will not be correct.

The technical details of digitally signing a message relies on a concept that we have seen previously.  It relies on public key cryptography. RSA can be used to sign a message. It is not essential that you understand exactly why this works, it is cool to see another application of RSA keys.

### The mathematics of digital signatures

Suppose that Alice wishes to send a message, let's call it , to Bob. Alice has an RSA key, where the private key is  and the public key is  - these can be generated in the same way as before. Alice writes her message and computes a hash of the message. The hash is then signed with Alice's private key in the following way,


where  is the hash of the message and  is the signature.

When Bob receives the message and the signature he computes the hash of the message. He also computes the following:


If  then the message has not been tampered with and it was signed by Alice. Otherwise, something has gone wrong and the message should be disregarded.

### **Why does this work?**

This works because of a simple exponentiation law. 


When we apply this law to our application we get


This demonstrates an interesting property of RSA keys. A pair of RSA keys can be used for two purposes:

1. You can use the public key to encrypt a message which can only be decrypted by the owner of the private key.
2. You can use the private key to sign a message that can be verified by anyone with access to the public key.

This further compounds the need of ensuring that the private key is kept secret, as the private key can be used to verify the originator of a message.

Much of the technology which you use every day to securely access the internet and send private messages to your family, friends and colleagues relies on public key cryptography to encrypt data and to digitally sign messages.
