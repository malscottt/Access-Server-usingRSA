# Access Server using RSA ( Asymmetric Encryption )

This project demonstrates a secure access server implementation utilizing the RSA encryption algorithm. RSA is a widely used asymmetric encryption method that employs a pair of cryptographic keys: a public key for encryption and a private key for decryption.


## How It Works?


A public-private key pair is generated.
The private key is shared with clients, while the public key is securely stored on the server.


## How Client can Access?:

The client will using the server's private key to gain access.


## Server Decryption:

The server will store public key so when it matches with client's private key, the server will allow clients to access the server.


## Secure Access:

The server validates the client request and grants/denies access based on encrypted credentials.


## Tools

Before we start, we need 2 essential tools which is:

  - Rocky Linux or any preferred UNIX platform

  - VMware Workstation to activate Unix platform

  - PuTTY for remote access

  - OpenSSL for generating private key and public key


When these tools is already installed, now we can start with our project.
