=======================================================
PALE BLUE PAPER (outdated, please refer to Medium Blog)
=======================================================

**WARNING!**

This document is outdated. The most recent information is `here <https://medium.com/six-degrees-of-separation/what-is-upala-all-you-need-to-know-updated-regularly-21e585f20c43/>`_.

**WARNING!**

Greetings human!
----------------
Upala is here to help you distinguish humans from bots. 

Upala main features
-------------------
- Proof of uniqueness. One person — one ID.
- Disclosure on demand. Decide which pieces of information to share.
- Friends recover each other's accounts. 

About this document
-------------------
This document as well as the Upala itself is under development. It originates from the series of blog posts and discussions `listed here <https://airtable.com/shrNQ0VClgqBiHmkL/>`_. Everyone is welcome to join. The document is meant to be short and easy to understand, with no technical details. 

Main challenges
---------------
**Sybil attack**. How to prevent a malicious actor from creating multiple accounts?

**Account recovery**. Relying on password is not enough. Managing private keys or mnemonics is too complex. Hardware tokens are rare. We need to build a secure system for the unskilled, the absent-minded and the naive.

**Incentives**. Until widely adopted one cannot call it an identity system. We need a lot of businesses and a lot of users. But why would anybody participate?

It does matter who you are, where you are and who you friends with. We will often use this as a metaphor to shape our thinking when solving these problems. 

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

Registering a new user:

1. Take a picture of a registering user using Upala app
2. Detect twins with face-recognition algorithm
3. If twins are detected they need to take selfies simultaneously in different places (proof of location)
4. Random validators confirm that the new selfies depict the same people as their ID photos

The solution is described in detail `this blog post <https://medium.com/six-degrees-of-separation/a-solution-to-sibyl-attack-problem-for-upala-identity-proof-system-ca924202ab8f>`_ . Which is still a draft though. The final solution will be added as a separate section to this documentation.

**Proof of location using known landmarks**

Known landmarks can be used to confirm location until FOAM is released. Registering a new user or confirming a twin will require putting an object available through Google street view on the background. Validators confirm landmarks on photos.

**Starting communities independently**

The presented sibyl attack protection mechanism provides an additional benefit. It allows starting communities independently in different parts of the world. Clusters of people don’t need to be intersected to trust each other.

Account recovery
----------------

It does matter who you are, where you are and who you friends with. The 3 unique features are used to identify a person: face, location and friends. What if you want to recover your account:

1. Search the account. Take a selfie with the Upala app.
2. Select the one which belongs to you. You can't see any photos or names. Type your real name to select your account.
3. Meet with some of your friends physically (with location proof) to unlock your account.

Account recovery process is another incentive to connect (within the system) with trustworthy friends.


Incentives
----------

No bots in social networks, no spam (as spammers will not be able to abuse single account too much), no CAPTCHA. These are some of the benefits and incentives both for users and services. 

This is probably not enough for the start. Needs more research. 