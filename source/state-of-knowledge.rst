=================
MATERIALS STUDIED
=================
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
- gnosis safe 
- `ZeroPass <https://www.zeropass.io/schematics>`_ - recovery based on key splitting. is building a decentralized solution. ZeroPass is building a decentralized password manager.
- `You <https://devpost.com/software/you-k1cb2g>`_ - You are the password. Decentralized password manager. Uses Phone to login.
- https://securekey.com/ - funded by world bank
- https://pillarproject.io/project - "The Wallet is Everything". Building a wallet with identity strage functionality. No details about recovery except they are planing to use hardware wallets and friends. 
- https://rivetz.com/ - recovery. DUAL ROOTS OF TRUST - software wolutions for splitting keys (expl. SIM card + smartphone secure enclave)


Zero Knowledge, privacy
'''''''''''''''''''''''

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
- The Sybil attack in sensor networks: analysis & defenses by 
J. Newsome, E. Shi, D. Song, A. Perrig

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

Other 
'''''
- `Pseudonym_Parties <https://www.researchgate.net/publication/242162818_Pseudonym_Parties_An_Offline_Foundation_for_Online_Accountability_PRELIMINARY_DRAFT>`_