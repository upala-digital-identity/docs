==================
Anti-Sybil academy
==================

**WARNING!**

This document is under construction. Upala insights are on the way...

..
	Inspiration
	===========
	Blade runners academy

	This section is the collection of our thoughts and insights on antiSybil protection and links to other people's work. This place is for those who is building their own identity system. 

	If you are one of them, please consider using Upala as a base for your system.

	State of knowledge 
..


Basics of digital identity
==========================

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


..
	Examples
	========
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
..


Projects and papers
===================

Links for digital identity enthusiasts. I use this document as personal archive and read-later list. I thought it isworth publishing. It is good source of quality info on digital identity and related topics. 

Identity projects
-----------------

Uniqeness, trust
''''''''''''''''
- `Upala <https://medium.com/six-degrees-of-separation>`_ - reputation that you own, no social graph analysis.
- `BrightID <https://www.brightid.org/>`_ - sybils are detected by analyzing, recovery by friends
- `IDENA <https://idena.io/?view=faq>`_ - sybil protection by meaningful story captcha
- `TrustLines <https://trustlines.network/>`_ - decentralized immutable accounting system for netted IOU balances between trusted parties
- `Pseudonym Pairs <https://panarchy.app/Proof-of-power.pdf>`_ does it in zero degrees of separation.
- `Encointer <https://encointer.org/>`_  personhood through pseudonim pairs. People meet physically simultaneuosly. Incentives through UBI. Own blockchain.
- `Web Of Trust <https://en.wikipedia.org/wiki/Web_of_trust>`_
- `Friend to friend <https://en.wikipedia.org/wiki/Friend-to-friend>`_
- https://tse.bitnation.co/
- https://duniter.org/en/
- https://www.humanitydao.org/ - voting for a new member
- https://www.objectivemoney.org/ - voting for a new member
- `POAP <https://www.poap.xyz/>`_ - The Proof of Attendance Protocol. Allows humans to collect badges in the form of non fungible tokens every time they participate in an activity, in person or remotely.
- `UBIC <https://github.com/UBIC-repo/Whitepaper/>`_ -  Universal Basic Income Currency. Sybil-resistance is based on modern E-Passports. Users join by scanning E-Passport via NFC.
- `Replica by DemocracyEarth <https://github.com/DemocracyEarth/paper/>`_ - Quadratic voting.

Storage and access 
''''''''''''''''''
Mainly concerned with granting access to parts of identity inforamtion.

- `iden3 <https://iden3.io/feature/key-recovery-mechanism>`_ - zknarks, griff nentions. a claim-based model. exmp. A university claims, that a useres has a degree. No social graph. No sybil protection. 
- `Evernym <https://sovrin.org/>`_ - a hyperledger blockchain project
- uPort - ERC-725
- BlockStack todo
- http://selfkey.org 
- https://www.velix.id/ - uses stellar consensus protocol.
- https://www.civic.com/

I categorize project below as ICO-boomers (sorry I may be very wrong):

- https://lynked.world/
- https://trigid.org/
- https://xenchain.io/
- https://www.peermountain.com/
- https://trustcommunity.io/

Recovery
''''''''

- keybase
- gnosis safe - wallet
- `Argent <https://www.argent.xyz/>`_ - wallet
- `ZeroPass <https://www.zeropass.io/schematics>`_ - recovery based on key splitting. is building a decentralized solution. ZeroPass is building a decentralized password manager.
- `You <https://devpost.com/software/you-k1cb2g>`_ - You are the password. Decentralized password manager. Uses Phone to login.
- https://securekey.com/ - funded by world bank
- https://pillarproject.io/project - "The Wallet is Everything". Building a wallet with identity strage functionality. No details about recovery except they are planing to use hardware wallets and friends. 
- https://rivetz.com/ - recovery. DUAL ROOTS OF TRUST - software wolutions for splitting keys (expl. SIM card + smartphone secure enclave)
- `EIP2429 <https://github.com/ethereum/EIPs/blob/5204f606b7634f79ae8c3aabae8a55772aa2d855/EIPS/eip-2429.md>`_ - Secret Multisig Recovery. Social recovery using address book merkle proofs.


Zero Knowledge, privacy
'''''''''''''''''''''''
- `AZTEC protocol <https://medium.com/aztec-protocol/confidential-transactions-have-arrived-a-dive-into-the-aztec-protocol-a1794c00c009>`_- "Being able to prove that you’re part of a group, without revealing who in the group you are".
- https://enigma.co/ -  secure computation protocol, where “secret nodes”  perform computations over encrypted data.
- https://status.im/ - secret messaging check it out

Blockchain social networks
''''''''''''''''''''''''''

- Akasha - соц сеть от Михая todo
- Сикорка - Пруф местоположения на блокчейне ethereum. todo

Other
'''''
- LNTrustChain - Experiment of trust. People passed an ammount of satoshis to those who they trust. 
- https://www.takethetorch.online/Torch
- http://fermat.org/downloads/book-of-fermat.pdf - Person-to-person apps
- BAT - if they pay for ads, how can they tell people apart from bots
- namecoin
- @bloomtoken

KYC-services
''''''''''''
- `Jumio <https://www.jumio.com/>`_- AI-Powered Identity Verification Services

UBI and decentralized landing
'''''''''''''''''''''''''''''

- https://puddle.com - Credit powered by people
- `Circles <https://www.joincircles.net/>`_ - A decentralised Universal Basic Income platform based on personal currencies
- https://www.wetrust.io/ 

-------------------------------------------------------------

Articles
--------

Sybil attack protection in social networks
''''''''''''''''''''''''''''''''''''''''''
- `SybilAttacks in Social Networks <https://arxiv.org/pdf/1504.05522.pdf>`_ - Survey #1
- `Sybil Defense Techniques in Online SocialNetworks <https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=7828091>`_ - Survey #2
- `SybilRank <https://users.cs.duke.edu/~qiangcao/sybilrank_project/index.html>`_- Aiding the Detection of Fake Accounts in Large Scale Social Online Services 
- `Sybil attack on lowest id clustering algorithm in the mobile ad hoc network <https://pdfs.semanticscholar.org/80de/5f955f2532af4622f29da49f02f86513e264.pdf>`_
- `Visualization assisted detection of sybil attacks in wireless networks <https://www.researchgate.net/publication/221325896_Visualization_assisted_detection_of_sybil_attacks_in_wireless_networks>`_
- The Sybil attack in sensor networks: analysis & defenses by J. Newsome, E. Shi, D. Song, A. Perrig


Sybil tolerance 
................
- `Canal <https://people.mpi-sws.org/~gummadi/papers/Canal-EuroSys.pdf>`_

Reputation-based
................
- `Reputation systems <https://github.com/ethereum/wiki/wiki/Problems#12-reputation-systems>`_ - open questions on reputation systems among the list of improtant Problems of Ethereum.
- `Sybilproof Reputation Mechanisms <http://www.eecs.harvard.edu/cs286r/courses/fall08/files/paper-CheFri.pdf>`_ - "...there is no symmetric sybilproof reputation function. conditions for sybilproofness for nonsymmetric functions. (we can easily break symmetry by comput-ing reputation values with respect to some fixed node inthe graph. This may be useful when we can identify sometrusted user, or when each user computes separately thereputations of other users with respect to themselves."
- `Propagation of Trust and Distrust <http://www.shibbo.ethz.ch/CDstore/www2004/docs/1p403.pdf>`_ - todo
- `Ostra: Leveraging trust to thwart unwanted communication <https://www.usenix.org/legacy/event/nsdi08/tech/full_papers/mislove/mislove_html/index.html>`_

Universal basic income and credit networks UBI
''''''''''''''''''''''''''''''''''''''''''''''
- `Aleeza Howitt <https://ubiresearch.org/category/research/digital-identity>`_
- `Bottom-Up Money <https://ubiresearch.org/wp-content/uploads/2019/05/Bottom-Up-Money-v1.1.pdf>`_    

Game theory 
'''''''''''
- `Deception, identity, and security <https://dl.acm.org/citation.cfm?id=3190836>`_- the game theory of sybil attacks 
- `Robust incentive techniques for peer-to-peer networks <http://www.csl.mtu.edu/cs6461/www/Reading/Feldman04.pdf>`_ - Uses graphs. Simplifies sybil detection. Flow-based reputation. 
- M. Richardson, R. Agrawal, and P. Domingos. Trustmanagement for the semantic web. Flow-based reputation.

Zero-knowledge
''''''''''''''
- `Tutorial: Proving knowledge of a hash preimage <https://zokrates.github.io/sha256example.html>`_ - a good practical example by Zokrates team of zkSNARKS for a quick introduction.
- `Getting Started with zkSnarks on ZoKrates <https://blog.gnosis.pm/getting-started-with-zksnarks-zokrates-61e4f8e66bcc>`_ - great write up by Gnosis team. Step by step guide to implement zero knowledge. 
- `Building Identity-linked zkSNARKs with ZoKrates <https://medium.com/zokrates/building-identity-linked-zksnarks-with-zokrates-a36085cdd40>`_ - an example how a sender's identity could be proven using sender's private key inside snark.
- `Zero-Knowledge Proof-of-Identity <https://arxiv.org/abs/1905.09093>`_ - Sybil-Resistant, Anonymous Authentication on Permissionless Blockchains and Incentive Compatible, Strictly Dominant Cryptocurrencies. TODO study

Password storage, Decentralized file access control
'''''''''''''''''''''''''''''''''''''''''''''''''''
- `Fruitfull Google search <https://www.google.com/search?client=ubuntu&channel=fs&q=grant+access+to+a+file+through+blockchain&ie=utf-8&oe=utf-8>`_
- `Blockchain-Based, Decentralized Access Control for IPFS <https://www.researchgate.net/publication/327034734_Blockchain-Based_Decentralized_Access_Control_for_IPFS>`_
- `Blockchain Based Access Control <https://www.iit.cnr.it/sites/default/files/main_21.pdf>`_

Decentralized unique identity 
'''''''''''''''''''''''''''''
- `Pseudonym_Parties <https://www.researchgate.net/publication/242162818_Pseudonym_Parties_An_Offline_Foundation_for_Online_Accountability_PRELIMINARY_DRAFT>`_
- `Verifying Identity as a Social Intersection <https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3375436>`_ 
- `UniqueID Decentralized Proof-of-Unique-Human <https://arxiv.org/pdf/1806.07583.pdf>`_ - survey of decentralized identity systems


Face-recognition
''''''''''''''''
- `Secure Face Matching Using Fully Homomorphic Encryption <http://hal.cse.msu.edu/assets/pdfs/papers/2018-btas-secure-face-matching.pdf>`_ 
- `Privacy-Preserving Face Recognition <http://homepage.tudelft.nl/c7c8y/SSP/PrivacyPreservingFaceRecognition.pdf>`_ 


Problems of ID in the world
'''''''''''''''''''''''''''
400k people in Europe without IDs - https://apatride.eu
Aadhar India - Aadhaar is a verifiable 12-digit identification number issued by UIDAI to the resident of India for free of cost.

Bonding Curves todo
- https://docs.google.com/document/d/1VNkBjjGhcZUV9CyC0ccWYbqeOoVKT2maqX0rK3yXB20/edit - by Simon 
- Bonding Curves https://yos.io/2018/11/10/bonding-curves/
- Bonding Curves https://medium.com/thoughtchains/on-single-bonding-curves-for-continuous-token-models-a167f5ffef89

.. include:: ./footer.rst


Other (study)
https://identity.foundation/ion/ https://www.w3.org/TR/vc-data-model/