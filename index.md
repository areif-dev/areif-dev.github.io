---
layout: default
title: Adam's Portfolio
---

### Navigation

- **[Code Review](/)**
- [Artifact 1: Android Inventory](/artifacts/android-inventory)
- [Artifact 2: Encryption](/artifacts/encryption)
- [Artifact 3: Fullstack with PostgreSQL](/artifacts/fullstack-with-postgresqL)

## Code Review

<iframe width="560" height="315" src="https://www.youtube.com/embed/Ykhneko8Hd0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

In this video, I outline 3 projects I worked on in college. I discuss their shortcomings and how I intend to improve them as artifacts for this portfolio.

The first artifact I discuss is an [Android app for managing inventory](/artifacts/android-inventory). It began as a simple table with the ability to manually enter and count products. In my enhancements, I added the ability to scan barcodes to search the web for the description of the product and automatically count the product based on the number of times the barcode was scanned.

The second artifact I created was a very simple [encryption and decryption demo](/artifacts/encryption). The demo only used a xor operation against a random key and the input, which was not very secure, so the first enhancement I made to this program was to use a more secure symmetric encryption algorithm called AES-GCM. I also translated the program from C++ to Rust so the program would benefit from improved memory safety, and I turned the original program into a more general purpose command line app rather than just a one-off demonstration.

The final artifact that I discuss in the video is a [fullstack web application](/artifacts/fullstack-with-postgresql). The main enhancement that I made to this program was to move it from a MongoDB database to a PostgreSQL database to demonstrate my knowledge of relational databases.
