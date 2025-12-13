# Connection Keys

## The Connection Key

A **connection key** is what you need to connect to someone with Holesail.&#x20;

The QR code has connection key stored in it for easy sharing.

Connection keys are automatically generated but you can specify custom connection keys. They should be at least 32 chars long for security purpose and custom connection keys can not be equal to exactly 64 chars.

### The Key and Keypair

Custom Keys act as a **seed** for generating a Keypair. This keypair is used to announce yourself on the peer-to-peer network and for authentication.

The keypair has a public key and a private key. We announce the public key on the network and that is what becomes your address, other peers will find you through this public key.

Private key on the other hand is a method for authentication. More on public and private keys in the next section.



