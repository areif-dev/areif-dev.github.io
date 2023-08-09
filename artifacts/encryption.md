---
layout: default
title: "Artifact 2: Encryption"
---

### Navigation

- [Introduction](/)
- [Artifact 1: Android Inventory](/artifacts/android-inventory)
- **[Artifact 2: Encryption](/artifacts/encryption)**
- [Artifact 3: Fullstack with PostgreSQL](/artifacts/fullstack-with-postgresql)

## Artifact 2: Encryption

## Competency: Algorithms and Data Structures

### Description

This artifact is from CS 405, which I completed during my junior year. Originally, this artifact was intended to demonstrate my ability to implement a very simple cipher to show how encryption can be used to secure data. The original implementation of this artifact was very limited because it was only able to accept input from a very specific file format, and it was also very insecure because the cipher it used only produced a byte-wise xor of the input and a key.

|                   Encryption Command Deomonstration                   |
| :-------------------------------------------------------------------: |
| ![encryption_command_demonstration](/assets/imgs/encryption_demo.png) |

### Justification

Despite the limitations of the original implementation of this artifact, I have chosen to include it in my portfolio because I have turned it into a general purpose command line interface that implements AES-GCM for much more secure symmetric encryption. I have also made the command line interface more useful by allowing users to provide their own key, as well as their own data in any format that they choose.

This project as a whole demonstrates my familiarity with the Rust programming language and the tooling that it provides, such as the Cargo package manager and third party crates. I was able to take existing functionality written in C++ and not only translate it to Rust, but also enhance it by creating a command line interface that people can use to create cryptographically secure messages.

Taking a closer look at the project, functions such as aes_gcm_enc and aes_gcm_dec showcase my knowledge of the advanced encryption standard and specifically the Galois/Counter Mode algorithm for symmetric encryption. In both of these functions as well as simple_cipher, I use data structures such as vectors, slices, and arrays of binary data to create encrypted messages for secure communication.

### Objectives

The primary objective that I hoped to achieve with this project was showcasing a security mindset that anticipates adversarial exploits in software architecture and designs to expose potential vulnerabilities, mitigate design flaws, and ensure privacy and enhanced security of data and resources. I achieved this goal by implementing a cryptographically secure encryption algorithm called Galois/Counter Mode that uses symmetric key encryption as well as a nonce or a Number Used Once to add an extra layer of obfuscation to encrypted messages. I also enhanced security by writing the program in Rust, which improves memory safety by limiting the number of mutable references to a shared memory location to one. This limitation is enforced at compile time, and it helps to mitigate overwriting data or accessing freed memory.

Another objective that I set for this project was to design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and standards appropriate to its solution, while managing the trade-offs involved in design choices. In this project, I was able to solve the problem of needing to send data between two computers securely by using the AES-GCM algorithm. I also designed a command line interface to make calls to this algorithm more intuitively.

### Reflection

The first challenge I faced when working on this project was that I had never made a command line interface in Rust before. I did some research, and I learned about a popular crate called Clap that lets developers define the arguments, options, and documentation for their CLI in basic Rust structs using macros. The documentation for this library also taught me about CLI subcommands, which are arguments passed to a CLI that act like their own CLI inside the main CLI.

The next challenge I faced was trying to write a program that would be able to create messages more securely than the original cipher that I built for CS 405. To overcome this problem, I learned about the Advanced Encryption Standard, which is a specification for creating symmetrically encrypted messages. Symmetric encryption simply means that a message must be decrypted with the same key that it was encrypted with. The specific implementation of AES that I chose for this program was AES-GCM or Galois/Counter Mode. This algorithm adds an extra layer of security over base AES by using a Number Used Once or nonce in addition to the encryption key. The nonce further obfuscates the key so that even two messages with the same content and encrypted with the same key will still encrypt differently as long as they use different nonces. A nonce can also be used to verify the integrity of a message to ensure that nothing was tampered with during transmission.

One final challenge I encountered with this project was UTF-8 encoding. Because the data I was feeding into the program was being encrypted with random keys, the output often was not UTF-8 compliant, which made printing it to std::out and trying to copy and paste it back in as input very difficult. The solution that I came up with for this was to avoid std::out in most cases and just pass raw binary input and output in files, which meant that I also learned how to interact with the filesystem in Rust.
