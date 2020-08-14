.. _bots:

===============
How Upala works
===============

Check out this `4 min video on how Upala works <https://youtu.be/9ekWCMQcdbc>`_ if you prefer.

Groups
======
Users join a group. They put their depostis in a pool (DAI). And the group assigns scores to all of its users.

.. image:: /img/deck/groups.png

Explosive bots
==============

Notice that the score is higher than the deposit. This is where Explosive bots concept comes in. It ensures that anyone can delete their ID at any time and grab an amount of money corresponding to their score.

.. image:: /img/deck/bots.png

Here a malicious user is able to get $10 from the pool. 

Sure enough other members will feel betrayed. And they will not let this person in again. 

A user performing such an attack is considered a bot. The act of stealing is immediately followed by self-destruction. Thus the name Exploding bots.

Stacking
========

The same way users join groups, groups gather into hierarchies. Superior groups may require deposits from its subgroups. And in return they add extra scores to their users (the same scores will be paid as a reward to an exploding attacker).

.. image:: /img/deck/stacking.png

Paths
=====

Both an attacker or a good user need a membership path through the group hierarchy to prove their score.

.. image:: /img/deck/membership_paths.png

These are the only constraints in the protocol. The rest is arbitrary.

Multiple membership
===================
Users and groups may join any number of superior groups. The process of group creation is completely decentralized. The hierarchy grows naturally in a bottom-up direction. Thus many top-level groups could emerge with millions (or even billions) of users in their subgroups. 

.. image:: /img/deck/multiple_membership.png

DApps
=====

A DApp may decide to trust any group and use user scores relative to that group. DApps may approve any number of groups as their score providers.

Groups may decide to charge DApps for providing user scores. Or they may earn interest on their pools. Or they may chose some other economic model.

They may chose any governance model as well.

.. image:: /img/deck/dapps.png

Best path
=========

A **user score** is calculated relative to a group and relies on all the scores down the hierarchy. There could be several authorization paths. It is practical for the user to select the path, that collects the maximum score.

.. image:: /img/deck/best_path.png

Market
======

Everyone is free to chose. But. DApps need large and trusted score providers. Groups need large low-explosion-risk audiencies. And users need the highest scores for the lowest investment of money or reputation.

.. image:: /img/deck/market.png

A market similar to insurance emerges. But instead of trading coverage for premium, in Upala scores are traded for deposits. And the risk here is the risk of explosion. It is meausered by user's reputation and the efforts spent on solving CAPTCHAS (pseudonym parties, empathy tests, etc).

.. image:: /img/deck/insurance.png

The market makes the score to be roughly equal to the cost of acquiring such a score. Which in other words is the price of forgery. And it is a very reliable metrics for DApps to assess human uniqueness with.


Flexibility
===========

A variety of identity systems can be built with Upala. Like the one based on friendship.

.. image:: /img/deck/friends_dimension.png

An identity system using DAO membership as an entry test.

.. image:: /img/deck/membership_dimension.png

.. 
	wrap
	.. image:: /img/deck/wraps.png
..

Upala can wrap over multiple identity systems and communities.

.. image:: /img/deck/multiple_dimensions.png

Here scores may be higher than a blackmarket cost of a state ID. This is a way for Upala to become a subsitute for state IDs.

Explosion window
================
Any changes to the group pool, users' scores or anything that may affect bot reward are delayed for a certain ammount of time. The delay prevents group owners from front-running bot and bot-net attacks. If any changes, that hurt bots rights are made, bots have enough time to decide and to explode.

Users and groups entities
=========================
Users may be represented by simple Ethereum addresses or wallets. Groups may be represented by Ethereum smart contract or by a single manager. Both users and groups have a permanent ID in Upala which they can control. 

Conclusion
=============

**Bots train the network**

The Explosive bots protocol allows trading deposit, reputation and work for score. Bot rewards show how expensive it is for a bot to gain the same reputation again. It incentivizes participants to carefully select who they trust so that they will inspect candidates more thoroughly next time. 

**Users scores are staked**

The bot reward is a signal of user quality:

	- How much trust a group puts in its users (or subgroups).
	- How expensive it is to create a unique identity (the same amount of trust or score) again. Or how high users price themselves. 
	- How safe it is for a DApp to rely on the user's uniqueness. 


Future work
===========

**Standard, layer or protocol**
How to position the system better. Should be a ERC20-like standard of smart contracts. A Uniswap-like contract factory or something different. 

**System sustainability**
As of writing we believe the system will work without a specific token or any other point of centralization or income funnel. It looks like a standard for contracts. Unfortunately, there is no reliable funding scheme in sight. So please consider donating right now (todo link)

**Privacy**
The idea of explosive bots appeared first here (todo link to Bot black market). We hope to develop a system with some Zero Knowledge magic, able to count bots without revealing them. This most probably will require to specify account type (bot or human) at creating once and forever. The actual implementation is to be discovered as well as its effect on the existing game. 

**Tokens** Native token: Eth, dai, own token? Burn tokens for bot explosion. A way for each group to have it's own token (e.g. hard-coded penalty for braking bot reward obligations)

**Next, human, have a look at** :ref:`the Upala Universe (all the things you can build with Upala)<universe>`.

.. include:: ./footer.rst