==============
Upala Universe
==============

.. _universe:

**What can be built with Upala.**

The protocol allows groups to **choose any incentives and governance model** as well as many other parameters. A group can pay to its members or to charge them. It can issue a token or it can stick with the DAI. It can decide to be a MolochDAO type or a Token Curated Registry type. Groups are free to choose **everything that is not restricted by the protocol**. Other examples:

- Member entering conditions (e.g. may require payment, an on-chain fact proof, a number of votes from its current members, etc.)
- Profit distribution rules (if the group is profitable)
- Scoring rules (how exactly a group scores its members)
- Exit rules (e.g. define shares refund policy)
- Privacy policy (e.g. visibility of group members to each other and to other groups)
- Score calculation fee for DApps or/and users (e.g. based subscription, lifetime membership, per transaction, free of charge, etc.)
- Governance model
- etc... 

Due to the freedom of options, it is possible to build groups with very different properties. Thus groups can bear different roles within the system. We refer to groups with similar properties as **Group types**. 

Group types
===========
**Score provider.**
A group may or may not provide access to user scores. Some groups may decide to charge users or DApss for the information. 

**For-profit.**
A group may decide to be profitable (or at least try to). Such a group may "tend" to earn from users (through entrance fees) or DApps (score calculation commission).

**Bank with benefits.**
Groups requiring an entrance fee may decide to hold their pool in a bank (like Compound). Members of such groups will receive interest on their fees. Plus the uniqueness score (benefit). A feature like this does not mitigate the risk of bot attack, however, it could speed up onboarding.

**Buffer.**
A philanthropist may decide to bring a group with a small pool and small bot reward into a more expensive group. This person then bears a part of bot attack risks having nothing in return. This way buffer groups can be created to **help bring developing countries** into high-level expensive groups.

**Groups with Fixed Hierarchy Levels.**
There are no leveling constraints per se. The hierarchy is built naturally with initiatives. But one can create a group that allows only subgroups of a particular type to be included as members. A group like this could become a building block of a state ID based identity system (described a little further).

**TCR Group.**
A group may decide to use a Token curated registry to curate its members.

**Score cache.**
A group that caches user scores and saves gas on calculations. 


Dimensions
==========

We can go further and build **whole identity systems** using Upala protocol. We call them **dimensions**. There are two flavors of dimensions: Upala native dimensions and Wraps. The whole set of projects using Upala Protocol is called **The Upala Universe**.


Upala-native dimensions
-----------------------

These dimensions use Upala groups as building blocks. Upala protocol is built-in. Here are a couple of example dimensions:

**Friends based identity system (dimension).** Friends join groups. Groups of friends join larger groups. And so on. Groups of groups will probably form around leaders. A betrayal (bot explosion) is seen by closest friends and naturally rumored around in the real world. A traitor will find it difficult to enter friends based system again. The same is for the group leaders. Everyone is incentivized to allow only trusted people. The hierarchy of groups will reflect the real-world reputation. 

**State ID based identity system (dimension)**. Such a dimension could rely on group types with fixed hierarchy levels. A user is allowed to join only a city-level group. City-level group joins region-level groups. Then come country-level and world-level. Every level with its own entering rules, governance and incentive models. 

**Radical ID**. Set a price for which you are willing to sell your identity to anyone willing to pay. Pay a "tax" relative to the price.

**Reputation tracker**.
Servieces (DApps) give scores to users for interactions. Services are curated via Token Curated Registries. 

Wraps
=====

The Upala protocol may be used to wrap existing identity systems and bring them into Upala Universe as well. A wrap is basically a group that invites members of another system to join. Copy is another way to think of a wrap. Members and scores are copied from an existing system into Upala group(s). Here are examples:

**Humanity DAO Wrap**. Everyone in Humanity DAO is invited to join the wrap (a Upala group). The group smart contract checks if the member is really a Human (in Humanity DAO terminology) and lets them in with 100% score. It may require a fee to fill the group pool with cash. The same procedure may be used to wrap around **Moloch DAO**, **Metacartel**, or other DAOs.

**Random Handshakes Wrap**. The Random Handshakes system was proposed earlier in the Upala blog (todo). It relies on face recognition and the real-world intersection of people. This whole system or its parts (i.e. based on location) can be wrapped with Upala protocol. 

**Layer 2 Analyzers**. A wrap could use several identity systems as inputs (collect data from other dimensions, wraps or existing non-Upala projects) and uniquely calculate user scores. It could use some complicated off-chain graph analysis (like the one that Bright ID does).

Unions
======

A DApp could choose to trust several dimensions to get scores for its users. This is one way of combining dimensions. But it is not very effective because every DApp is responsible for choosing the right (reputable) dimensions. That is to do curation work by itself. We don't want that. 

A better way is to create a group with dimensions as members. It will unite several identity systems (dimensions). Groups like this may be called Unions. A Union group may be a For Profit group and earn by charging DApps for score calculation (or confirmation). 

.. note::

	Group types and dimensions are just paradigms. Neither Group types nor Dimensions are parts of the protocol. These are just sets of **paradigms** with arbitrary names. These paradigms help to understand the possibilities of the protocol. And can be helpful when building on top of Upala. 


.. include:: ./footer.rst

..
	Upala universe
	==============

	Friends
	-------
	This is the essense of Upala. All other dimesions rely on existing identity systems or other constructs. 
	

	DAOs based
	----------
	Assumtion: DAOs members (Moloch DAO, Metacartel, Humanity DAO, etc) are trusted people of ethereum community and they may trust each other. So let's check this assumption.

	Create an Upala group for every DAO on Ethereum.
	Create a Union group to unite all DAO members and make their scores be available from this single group. 
	The Union group will then 

	Let them price the trust. 

	Unite all dao-based groups into one. 

	State ID based
	--------------

	Есть офисы в каждом городе. 
	Они проверяют пасспорта и заключают договор с пользователем. 
	Берут деньги и создают пользователя.

	Как убедиться, что они не генерят хэши паспортных данных? 
	Как убедиться, что они не используют пасспортные данные без участия людей? 

	Можно сделать случайный выбор организации. Пусть пользователь будет обязан раз в год пройти авторизацию. 
	Можно сделать ревизора из вышестоящих групп. 


..
