# McEliece-Cryptosystem

## Introduction
The McEliece Cryptosystem is a code-based cryptographic system that has the potential to withstand potential quantum attacks. This project is a simulation of the McEliece Cryptosystem, a post-quantum public key encryption system. Unlike RSA and ECC, which are vulnerable to quantum attacks, McEliece is built on error-correcting codes—a problem that remains hard even for quantum computers. This implementation is written in Python and SageMath, taking advantage of SageMath’s algebraic tools to generate keys, encrypt, and decrypt messages.

## Importance of the McEleice Cryptosystem
* Quantum Resistance
  - The McEliece Cryptosystem is believed to withstand attacks from quantum computers
* Fast encryption and Decryption
  - The cryptosystem is based on matrix-vector multiplication

## Encryption and Decryption Process
### Key Generation  
1. Generate a **random Goppa code** using a **random binary generator matrix**.  
2. Apply a **random permutation matrix** and an **invertible scrambling matrix** to obscure the structure of the code.  
3. Publish the transformed **generator matrix** as the **public key**.  
4. Keep the **Goppa code** and **secret transformations** as the **private key**.  

### Encryption  
1. Encode the **plaintext message** into a **binary vector**.  
2. Multiply the message vector by the **public key matrix**.  
3. Introduce a small **random error vector** (within the code’s error correction capability).  

### Decryption  
1. Use the **private key** to remove the **permutation** and recover the original **Goppa code** structure.  
2. Apply **error correction** to retrieve the **original message**.  
