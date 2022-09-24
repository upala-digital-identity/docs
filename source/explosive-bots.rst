.. _bots:

===============
How Upala works
===============

Check out this `4 min video on how Upala works <https://youtu.be/9ekWCMQcdbc>`_ if you prefer.


Warning
===========
Docs moved `here <https://www.notion.so/upalahq/How-Upala-works-draft-79bd03181dc045009e727bc902a8835b>`_

	
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