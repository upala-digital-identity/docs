=======================
EXPLOSIVE BOTS PROTOCOL
=======================
High-level incentives protocol (layer).

How Upala works
===============

The main ideas are the notions of groups and explosive bots.
Gives quantitative measure of personhood

Groups
------
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
--------------
Every group has a pool of Ether (more on token economy here - todo link). Every group member has a share in the group's pool. More on entering conditions of a group - todo link.

Every user has an option to attack any group. That is to steal a portion of group's pool. The amount of the theft depends on user score in that group. The attack affects all groups along the path from user to the group under attack. If Alice decides to attack group C, that would also affect groups B and A. 

A user performing such an attack is considered a bot. Such an attack is effectively steals from other users, because the value of their shares drop. Presumably there is no way for this same user remains friends with. The act of stealing is immediately followed by self-destruction. Thus the name exploding bots. 

A User is an Ethereum address, a wallet.  


Money flows. Incentive models. 
==============================
Pool size, bot explosion reward and member scores, bot explosion feature and exit feature are the only necessary parameters of a group. The rest is optional. Though this little constrain let build and unite a veriety of different systems. 

Groups are allowed to choose:
- Entering conditions (e.g. may require payment, an on-chain fact proof, a number of votes from current members, etc.)
- Profit sharing rules (if the group is profitable in any way)
- Member scoring rules
- Member exit rules (e.g. will the shares be returned)
- Privacy policy (visibility of group members to each other and other groups)
- Receive payments for user score confirmation. 


A group can pay to its members. Group can be a bank. It can issue a token. It can decide to be a MolochDAO-type or a TokenCurated registry type. Собственные тарифы на авторизацию пользователей для приложений (подписка, единовременный платеж за членство, платеж за каждую авторизацию или бесплатно. The only thing which is necessary is to follow the bot reward rules. 



Ivitation - payment from top. 


Groups can decide to chose different economy models. 

From bottom and from top. 
The system allows to build any incentive model. 


No token economy
----------------
No global economy. No way to close the circuit for own token. Allows to be a cross standard to unite different systems. 




Paradigms
====================
Simple building block to build complex systems. Many network designs could be used. This is a standard to connect them all. Can create different systems. Even better it can be used to unite different systems into one. 

Build
-----
Friends
State ID based system
A group of types may emerge. For State issued ID there may be types as follows. A city group type may accept only user as members. A group of type region accepts only cities, a country type accepts only 

Wrap
----
Wrapping other blockchain identity systems
Random handshakes
Humanity DAO
Provide lacking incentives layer

Layer 2 analyzers
-----------------

Unite
-----
Unite different identity systems

Buffer
-----
(Support of developing countries)


Conclusion
=============

Graph analysis
----------------------
The protocol provides incentives to build a hierarchy. Or rather it provides a tool to build incentives models and unite. Hierarchy simplifies social graph. 

A DApp can use a score of a whole group (for whatever reason).

Bots train the network
----------------------
the Explosive bots feature gives an opportunity to trade reputation for money. It incentivizes participants to carefully select who they trust. Moving game on chain

The measure of how hard it is to create a new human account in that particular system. 

Anyone can chose whether to gain reputation or to trade it for cash (and lose chance to enter those groups again). 

на какую сумму оценивает себя их пользователь

With this we are going to build our own types of Upala branches. 


Future work
===========

Counting the bots
-----------------
The idea of explosive bots appeared first here (todo link to Bot black market). We hope to develop a system with some Zero Knowledge magic, able to count bots without revealing them. This most probaly will require to specify account type (bot or human) at creating once and forever. The actual implementation is to be discovered as well as its affect on the existing game. 

Standard, layer or protocol
---------------------------
How to position the system better. Should be a ERC20-like standard of smart contracts. A Uniswap-like contract factory or something different. 

System sustainability
---------------------
As of writing we believe the system will work without a specific token or any other point of centralization or income funnel. It looks like a standard for contracts. Unfortunately there is no reliable funding scheme in sight. So please consider donating right now (todo link)

Authorization commission
------------------------
The way a group can earn on authorization

Bot attack details
------------------
How exactly the bot reward is shared among the members of attack path

Privacy
-------

Score intersection
------------------
What if a group combines say two lower groups. A user has a score in those groups. How is the score combined. Best score? Than there is another thing to consider when joining a top level group - are there any "higher score" groups so that adding a group giving lower scores is suicidal for the lower group.

Burn tokens for bot explosion
-----------------------------

Native token
------------
Eth, dai, own token?

Multiple tokens
------------
Is there a way for each group have it's own token