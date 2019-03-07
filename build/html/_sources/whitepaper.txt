===========
LIGHT PAPER
===========

Main features
-------------
- Proof of uniqueness
- Data on demand
- No password




Sybil attack protection
-----------------------

**The sibyl attack problem**

Imagine two situations:

1: Alice and Bob are twins. They live in the same flat. Alice is out in the morning and home in the afternoon. Bob is out in the afternoon and home in the morning. They meet different people when they are out but never the same ones. They never invite guests.

2: Isabel is diagnosed with dissociative identity disorder. She has two phones. One has an account registered with her real name. And the other is registered with her alter ego — Sibylla. Isabel is out in the morning and home in the afternoon. There she changes her pale pink standard waitress uniform for a stunning evening gown and goes to a luxurious cocktail party. She gracefully grabs the phone registered for Sibylla. Isabel and “Sibylla” meet different people and never invite anybody to “their” home.

Here Isabel is performing a sibyl attack. We need to “punish” Isabel and “reward” Alice and Bob.

**The sibyl attack problem solution**

Sybils are detected at the entrance to the system. 

Components:

- Upala smart-phone app
- Face recognition server
- FOAM’s proof of location service

Here is how registering a new user looks like in short:

1. Take a picture of a registering user using Upala app
2. Detect twins with face-recognition algorithm
3. If twins are detected they need to take selfies simultaneously in different places (proof of location)
4. Random validators confirm that the new selfies depict the same people as their ID photos

The solution is described in detail `this blog post <https://medium.com/six-degrees-of-separation/a-solution-to-sibyl-attack-problem-for-upala-identity-proof-system-ca924202ab8f>`_ . It is still a draft though. The final solution will be added as a separate section to this documentation.

**Proof of location using known landmarks**

Known landmarks can be used to confirm location until FOAM is released. Registering a new user or confirming a twin will require putting an object available through Google street view on the background. Validators confirm landmarks on photos.

**Starting communities independently**

The presented sibyl attack protection mechanism provides an additional benefit. It allows starting communities independently in different parts of the world. Clusters of people don’t need to be intersected to trust each other.

Account recovery
----------------


Incentives
----------