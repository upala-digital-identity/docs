===============
How Upala works
===============

.. _bots:

Explosive bots protocol
=======================
No summary yet... The full description below is already readable though.

..
	The main ideas are the notions of groups and explosive bots.
	Gives quantitative measure of personhood
	High-level incentives protocol.
..

Groups
======
Users join groups. Groups join larger groups (groups of groups). Larger groups join even larger groups. And so on. This creates a hierarchy with massive groups at the top and users at the bottom.

A group sets scores to its members (users or lower-standing groups). The score means an amount of trust and is expressed in percents from 0 to 100.

A **user score** is calculated relative to a group and relies on all the scores down the hierarchy. Say Alice has 90% score in group A, group A has 80% score in group B. Group B has 70% score in group C. Alice score in group B is then 
0,90 x 0,80 x 100=72%. 
Alice's score in group C is 
0,90 x 0,80 x 0,70 x 100=50,4%

The process of group creation is completely decentralized. The hierarchy grows naturally in bottom-up direction. Thus several top-level groups could emerge with millions (or even billions) of users in their subgroups. 

A DApp may decide to trust any group and assess its users relative to that group. A DApp may chose a number groups to trust. 

Users are allowed to join multiple groups and leave a group at any time. The same applies to groups. Similarly to MolochDAO rage quit feature.


Explosive bots
==============
Every group has a pool of Ether (more on token economy here - todo link). Every group member has a share in the group's pool. More on entering conditions of a group - todo link.

Every user has an option to attack any group. That is to steal a portion of group's pool. The amount of the theft depends on user score in that group. The attack affects all groups along the path from user to the group under attack. If Alice decides to attack group C, that would also affect groups B and A. 

A user performing such an attack is considered a bot. Such an attack is effectively steals from other users, because the value of their shares drop. Presumably there is no way for this same user remains friends with. The act of stealing is immediately followed by self-destruction. Thus the name exploding bots. 

A User is an Ethereum address or a wallet.  

The only thing which is necessary is to follow the **bot explosion rules**. That is a group is supposed to maintain a pool, bot explosion reward and member scores, bot explosion feature and exit feature are the only necessary parameters of a group. The rest is optional. There is no token economy and no governance model.

**That's it! The rest is out of protocol.** However it is the strength of the system. It shows how Upala can unite different systems. 

.. A group may chose any currency as long as it can pay bot reward in DAI. There is a penalty for not doing so. 

.. _universe:

The Upala Universe
==================

The protocol allows groups to **choose any incentives and governance model** as well as many other parameters. A group can pay to its members or to charge them. It can issue a token or it can stick with DAI. It can decide to be a MolochDAO type or a Token curated registry type. Groups are free to choose **everything that is not restricted by the protocol**. Other examples:

- Member entering conditions (e.g. my require a payment, an on-chain fact proof, a number of votes from its current members, etc.)
- Profit distribution rules (if the group is profitable in any way)
- Scoring rules (how exactly a group scores its members)
- Exit rules (e.g. define shares refund policy)
- Privacy policy (visibility of group members to each other and to other groups)
- Score calculation commission for DApps or users (subscription, lifetime membership, per transaction, free of charge, etc.)
- Commission for super-groups to allow inclusion (todo). 
- Governance model
- etc... 

Due to the freedom of options it is possible to build groups with very different properties. Thus groups can bear different roles within the system. We refer to groups with similar properties as **Group types**. 

Group types
-----------
**Score provider**
A group may or may not provide access to user scores. Some groups may decide to charge users or DApss for the information. 

**For profit**
A group may decide to be profitable (or at least try). Such a group may "tend" to earn from users (through entrance fees or score calculation commission) or from DApps.

**Bank with benefits**
Groups requiring an entrance fee may decide to hold their pool in a decentralized bank (like Compound). Members of such groups will receive interest on their fee. Plus a uniqueness score (benefit). A feature like this does not mitigate the risk of bot attack, however it could speed up onborading.

**Buffer**
A philanthropist may decide to bring a group with a small pool and small bot reward into a more expensive group. This person is then bears a part of bot attack ricks having nothing in return. This way buffer groups can be created to **help bring developing countries** into high level expensive groups.

**Groups with Fixed Hierarchy Levels**
There is no leveling constrains per se. The hierarchy is built naturally with initiatives. But one can create a group which allows only subgroups of particular type to be included as members. A group like this could become a building block of a state ID based identity system (described a little further).

**TCR Group**
A group may decide to use Token curated registry to curate it's members.

**Score cache**
A group that caches user scores and saves gas on calculations. 


Branches
--------

We can go further and build **whole identity systems** using Upala protocol. We call them **branches**. There are two flavors of branches: Upala native branches and Wraps. The whole set of projects using Upala Protocol is called **The Upala Universe**.


**Upala-native branches**

This branches use Upala groups as building blocks. Upala protocol is built-in. Here are a couple of example branches:

*Friends based branch.* Friends join groups. Groups of friends join larger groups. And so on. Groups of groups will probably form around leaders. A betrayal (bot explosion) is seen by closest friends and naturally rumored around in the real world. A traitor will find it difficult to enter friends based system again. Same is for the group leaders. Everyone is incentivezed to admit only trusted people. The hierarchy of groups will reflect the real-world reputation. 

*State ID based branch*. Such a branch could rely on group types with fixed hierarchy levels. A user is allowed to join only a city-level group. City-level group joins region-level group. Then come country-level and world-level. Every level with its own entering rules, governance and incentives models. 


**Wraps**

The Upala protocol may be used to wrap existing identity systems and bring them into Upala Universe as well. A wrap is basically a group that invites members of another system to join under some conditions. Copy is another way to think of a wrap. Members and scores are copied from an existing system into Upala group(s). Here are examples:

*Humanity DAO Wrap*. Everyone in Humanity DAO are invited to join the wrap (group). The group smart contract checks if the member is really a Human (in Humanity DAO terminology) and lets them in with 100% score. It may require a fee to fill the group pool with cash. The same procedure may be used to wrap around Moloch DAO, Metacartel and other similar DAOs.

*Random Handshakes Wrap*. The Random Handshakes system was proposed earlier in the Upala blog (todo). It relies on face recognition and real-world intersection of people. This whole system or its parts (i.e. based on location) can be wrapped with Upala protocol. 

*Layer 2 Analyzers*. A wrap could use several systems as inputs (branches, wraps or existing non-Upala projects) and calculate user scores in a unique way. It could use some complicated off-chain graph analysis (like the one Bright ID does). 

**Unions**

A DApp could chose to trust several branches to score its users. This is one way of combining branches. But it is not very effective because every DApp is responsible of choosing the right (reputable) branches. That is to do curation work by itself. We don't want that. 

A better way is to create a group with branches as members. A group that will unite several identity systems (branches). Groups like this may be called Unions. A Union group may be a For Profit group and earn by charging DApps for score calculation (confirmation). 


Group types and branches are just paradigms
-------------------------------------------

Neither Group types nor Branches are parts of the protocol. These are just sets of **paradigms** with quite arbitrary names. These paradigms help to understand the possibilities of the protocol. And can be helpful when building on top of Upala. 

Conclusion
=============

**Graph analysis**
The protocol provides incentives to build a hierarchy. Or rather it provides a tool to build incentives models and unite. Hierarchy simplifies social graph. 

A DApp can use a score of a whole group (for whatever reason).

**Bots train the network**
the Explosive bots feature gives an opportunity to trade reputation for money. It incentivizes participants to carefully select who they trust. Moving game on chain

The measure of how hard it is to create a new human account in that particular system. 

Anyone can chose whether to gain reputation or to trade it for cash (and lose chance to enter those groups again). 

на какую сумму оценивает себя их пользователь

With this we are going to build our own types of Upala branches. 


Future work
===========

**Counting bots** The idea of explosive bots appeared first here (todo link to Bot black market). We hope to develop a system with some Zero Knowledge magic, able to count bots without revealing them. This most probaly will require to specify account type (bot or human) at creating once and forever. The actual implementation is to be discovered as well as its affect on the existing game. 

**Standard, layer or protocol**
How to position the system better. Should be a ERC20-like standard of smart contracts. A Uniswap-like contract factory or something different. 

**System sustainability**
As of writing we believe the system will work without a specific token or any other point of centralization or income funnel. It looks like a standard for contracts. Unfortunately there is no reliable funding scheme in sight. So please consider donating right now (todo link)

**Authorization commission**
The way a group can earn on authorization

**Bot attack details**
How exactly the bot reward is shared among the members of attack path

**Privacy**

**Score intersection**
What if a group combines say two lower groups. A user has a score in those groups. How is the score combined. Best score? Than there is another thing to consider when joining a top level group - are there any "higher score" groups so that adding a group giving lower scores is suicidal for the lower group.

**Burn tokens for bot explosion**

**Native token**
Eth, dai, own token?

**Multiple tokens**
Is there a way for each group have it's own token