[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/W7xCJoxq)
# CSCY 3765 - Secure Programming - Lab #4

## Team
- **Team Member #1**: *your name here*
- **Team Member #2**: *your name here*

## Team
- *DEADLINE*: **_Tuesday, November 7, 11:59 PM_**

## Goals
- This lab focuses on furher implementation of the confidentiality of information embedded in a multithreading environment. 

## Overall Description
- A Client/Server application is given for relaying messages between two parties through a centralized server.
- The Cliente/Server communications is channel-encrypted. In other words, communication between the server and the client is encrypted. 
- However, messages relayed between parties (A) and (B) can be easyly read in the server side. 
- Your **mission** is to use **end-to-end encryption** using **RSA**, so if messages are leaked on the server, they cannot be read. 

## Repository Structure
- `Client` folder has an IntelliJ Project to run the client. *You must open the `Client` folder as the project, not src.*
    - This folder includes channel encryption as well as the configuration to successfully run the client. 
- `MsgSrv` folder has an IntelliJ Project to run the server. *You must open the `MsgSrv` folder as the project, not src.*
    - This folder includes channel encryption as well as configuration to run successfully the server.
- `README.md`: this file with the instructions.

## Guidelines
- Add in the server a print of every message, so you can see that the messages can be read. 
    - Later this should not be the case.
- Each client will have its own Private/Public Key pairs. 
    - Public Keys are shared with other clients. You don't need to implement this in the program, you can just copy the public key file (.pub)
    - Keys are names as `<username>` and `<username>.pub` for private and public keys respectively. 
    - You can use any tool to create PKI. You can use this [website](https://www.devglan.com/online-tools/rsa-encryption-decryption) as well. 
- When sending a message, encrypt the message using `<target_user>.pub`.
- When decrypting the message, use the user private key `<username>`.
- Keep in mind that only the message should be enciphered, and not the entire package. 


## Using PKI to Encipher/Decipher 
- You will need to use the package `import java.security.*;`.
- [This post](https://stackoverflow.com/questions/34454531/java-how-can-i-generate-privatekey-from-a-string) has information on how to read the private/public key into a `PrivateKey`/`PublicKey` objects
- [This post](https://aws.plainenglish.io/how-to-use-rsa-asymmetric-encryption-and-decryption-in-java-a4d7c3ad8236) has a good tutorial on how to encipher/decipher using Java. [pdf](./rsa.java.pdf)

## Resources
- The internet is open for this Lab. 
    - However, **AI tools**, like *ChatGPT*, **are NOT permitted**.

## Submission
- After Implementing and Testing End-To-End Encryption, just **Commit** and **Push** your repository.