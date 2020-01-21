.. _bots:

===============
How Upala works
===============


Groups
======
Users join groups. Groups join larger groups (groups of groups). Larger groups join even larger groups. And so on. This creates a hierarchy with massive groups at the top and users at the bottom.

A group sets scores to its members (users or lower-standing groups). The score means an amount of trust and is expressed in percents from 0 to 100.

A **user score** is calculated relative to a group and relies on all the scores down the hierarchy. 

Say Alice has a 90% score in group A, group A has a 80% score in group B. Group B has a 70% score in group C. 

Alice score in group B is then: 0,90 x 0,80 x 100=72%. 

And Alice's score in group C is: 0,90 x 0,80 x 0,70 x 100=50,4%

Users are allowed to join multiple groups and leave a group at any time. The same applies to groups (similar to MolochDAO rage quit feature).

The process of group creation is completely decentralized. The hierarchy grows naturally in a bottom-up direction. Thus several top-level groups could emerge with millions (or even billions) of users in their subgroups. 

A DApp may decide to trust any group and estimate user scores relative to that group. A DApp may choose a number of groups to trust. 

.. image:: /img/groups-1.jpg

Explosive bots
==============
Every group has a pool of money (DAI). Every group member has a share in the group's pool (not necessary, simplified here).

Every user has an option to attack any group. That is to steal a portion of the group's pool. The amount of theft depends on the user score in that group. The attack affects all groups along the path from the user to the attacked group.

If Alice decides to attack group C, that would also affect groups B and A. 

A user performing such an attack is considered a bot. A bot is effectively stealing from other users because the value of their shares drops. Presumably, there is no way for this same user remains friends with. The act of stealing is immediately followed by self-destruction. Thus the name exploding bots. 

.. image:: /img/bots-1.jpg

Pools and Upala Timer
=====================
Changes to the group pool, users' scores and anything that may affect bot reward are delayed. The delay prevents group owners from front-running bot attacks. The delay also allows for bot-net attacks. 

The Upala Protocol (bot explosion protocol)
===========================================
Users may be represented by simple Ethereum addresses or wallets. Groups are Ethereum smart contracts using Upala Protocol (experimental code is `here <https://github.com/porobov/upala/tree/master/contracts/>`_).

The contract defines **bot explosion rules** - the only rules necessary for compatibility with other contracts:

- maintain a pool of money
- provide member scores
- reward an exploding bot with a portion of a pool (and get locked for not doing so)

**That's it! The rest is out of protocol.** A group may choose any behavior as long as it can pay bot rewards in DAI.


Conclusion
=============

**Bots train the network**

The Explosive bots feature allows trading reputation for money. Bot rewards show how expensive it is for a bot to gain the same reputation again. It incentivizes participants to carefully select who they trust so that they will inspect candidates more thoroughly next time. 

**Users scores are staked**

The bot reward is a signal of user quality:

	- How much trust a group puts in its users (or subgroups).
	- How expensive it is to create a unique identity (the same amount of trust or score) again. Or how high users price themselves. 
	- How safe it is for a DApp to rely on the user's uniqueness. 

.. 
	**Simple hierarchy**
	The protocol provides incentives to build a hierarchy. Or rather it provides a tool to build incentives models and unite. Hierarchy simplifies social graph. 

	It moves game on chain. 
	What is better: a group with 10000 members, $1000 pool and $100 bot reward or the same group but with 
	Will you send 5 dollars to every user that values identity for 1 dollar?

	However it is the strength of the system. It shows how Upala can unite different systems. 
..

Future work
===========

**Bots statistics** The idea of explosive bots appeared first here (todo link to Bot black market). We hope to develop a system with some Zero Knowledge magic, able to count bots without revealing them. This most probably will require to specify account type (bot or human) at creating once and forever. The actual implementation is to be discovered as well as its effect on the existing game. 

**Standard, layer or protocol**
How to position the system better. Should be a ERC20-like standard of smart contracts. A Uniswap-like contract factory or something different. 

**System sustainability**
As of writing we believe the system will work without a specific token or any other point of centralization or income funnel. It looks like a standard for contracts. Unfortunately, there is no reliable funding scheme in sight. So please consider donating right now (todo link)

**Bot attack details**
How exactly the bot reward is shared among the members of the attack path

**Privacy**

**Score intersection**
What if a group combines say two lower groups. A user has a score in those groups. How is the score combined? Best score? Then there is another thing to consider when joining a top level group - are there any "higher score" groups so that adding a group giving lower scores is suicidal for the lower group.

**Tokens** Native token: Eth, dai, own token? Burn tokens for bot explosion. A way for each group to have it's own token (e.g. hard-coded penalty for braking bot reward obligations)


**Next, human, have a look at** :ref:`the Upala Universe (all the things you can build with Upala)<universe>`.

.. include:: ./footer.rst