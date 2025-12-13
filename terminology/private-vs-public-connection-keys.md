# Private vs Public connection keys

Holesail has two connection modes, a private mode and a public mode. \
\
We use different terminology for the same:

* Private connection key and Public connection key
* Private mode and a Public Mode

## Private Connection Keys

Private connection keys are what Holesail connection's use by default, you can also specify a custom "key".

**From the custom key we derive a Keypair, that has a Public key and a Private key.** We announce the public key on the P2P [DHT](https://en.wikipedia.org/wiki/Distributed_hash_table) network. This public key is how other users will find you on the network.

On the client side,  When you share your private connection key with someone we will again derive a key pair and use the public key to find the server.

While establishing a connection the client has the same private key as the server and it is sent along the connection. The server will verify the key and allow the connection, if the key is incorrect or there is no key set, the server will not respond at all.

This ensures, that other peer who know about your public key can not connect to you because they do not have the private key.

This process works pretty much like SSH. The public key can be considered your IP address which people know but they can not connect unless they have the private key.

{% hint style="info" %}
Treat Private connection strings how you would treat SSH key, do not share it with anyone you do not trust.\
\
If someone else start a server with your private connection string, they will take over.
{% endhint %}

## Public Connection Keys

With private connection key, we can access our system safely and know that no third party can connect without our permission, but they are only meant for personal use (like SSH) but what if we want to share the connection with a third party?

This is where public connection keys come into play. This time we again generate a random Keypair, discard the private key and announce our public key on the P2P network.

The public key is what becomes your "Public connection key", there is no authentication involved, and you can safely share it with any third party as it is your address itself and not the seed.&#x20;

We like to compare public connection keys with Domains. They exist on the DHT, anyone can find you using it or by scanning the DHT and connect to you.

{% hint style="info" %}
Treat public connection keys like you would treat a domain name on a public server, if there is anything private on it, it is your responsibility to password protect it or use private connection keys instead.
{% endhint %}
