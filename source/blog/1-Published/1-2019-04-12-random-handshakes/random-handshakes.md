

# Random handshakes - sybil attack protection mechanism for digital identity system Upala

# Intro 

This is enhanced version of the previous mechanism. It eliminates dolls attack, bot spamming and may work without FOAM proof of location. Phone camera hacks, realistic dools cannot enter.

# In short

Each user has a global and a local reputation. Local means geographically local. 

Users earn local reputation when they meet eachother in person in random pairs. Users confirm they see a real person with the right ID photo. Face recognition algorithm detects sybils. Twins have to prove that they are both real.

Global reputation is calculated by "routing" local user reputation from a small city to the globe. Two cities establish a connection when their citizens travel. The more travelers the more the bandwith of the connection. When reputation is transfered through a connection it loses some points, depending on connection bandwidth.



# Local reputation

There are areas.
~~# In short
Users meet each other in the real world in random pairs. They confirm that they see a real person and take a picture with their phone.~~


## Registration

This will register a new user:
- Make a small registration deposit (it is returned after personhood is confirmed locally - explained further). 
- Take a selfie with the Upala app. This is your ID photo.

In order to confirm that it is you on your ID photo You have to meet several people to confirm it.


## Random local handshake

Each user has a reputation balance. It can be positive or negative. Reputation may be earned only from other users. Users have to meet each other in person to gain reputation. Pairs of users are assigned pseudo randomly by the system. 

The protocol:
- Announce that you are avalable for a meeting. 
The system finds a random user nearby. You cannot see your vis-a-vee's ID. 
- Agree on system-proposed time or disagree (with no punishment).
After the time is chosen the system gives a random nearby location to meet. It is now you responsibility to show up. 
- Meet the other person and confirm:
    + there is a real person acting at own will.
    + the person's ID photo is correct. 
- _Alternatively: take a picture with your phone and let face-recognition nodes deal with the matching._

Approving a user brings this user reputation points. Disapproving a user subtracts points. 


## Reputation propagation

Once the reputation score is recieved by a user it is propagated to his/her closests previously established contacts. 

A number of random contacts is selected by the system. They all get affected by the handshake. If a user gets approval, those who approved her earlier recieve points, those rejectes lose points. And vice versa. If a user gets a rejection, those who approved get rejection, those who rejected get approval. 

Accepting a handshakes thus is like having a share of that user in your own reputation. You don't want a bot in your portfolio, because you'll get negative scores from this contact once in a while. But you'd better not reject real people, because those who approve them will bring you negative scores. 

The system stimulates to approve as many non-malicious people as possible. It also stimulates a user to register early (the earlier - the more reputation from contacts). 

Having a certain local reputation score a user may be considered a human locally. After surpassing this threshold user may chose to continue handshakes to gain even more reputation, thus healing the system. Global reputation score may is different - explained further. 

__Example__ 

Alice have already met two people and recieved 2 points from them. 
Now she is on her third meeting but nobody is showing up. Probably her vis-a-vis had a resaon not to show up, but probably it was a bot. She rejects the handshake. She gets a rejection as well and loses 1 point. Her previous contacts (those who approved her) also lose points. 
But she keeps meeting real people. And eventualy she recieves a good score. With every successful handshake those who approved Alice recieve points and those who rejected lose. Alice also gains points when a real human meets and rejects "her" bot.
But whenever she gets rejected, those who approved her lose and those who rejected gain points. If Alice's bot "meets" another cooperating bot, Alice loses points. 

## Humans vs bots

An area is a geographical outlines of a city or a village. It is within this outlines that a user earns local reputation. 

Under normal conditions this area is densely "populated" with humans. They can easily "downvote" a small botnet. But they cannot withstand a massive botnet attack. The bots will then prevent normal users to even meet each other. And people will only get negative score.

There are two measures to withstand bots: invitation deposit and ability to create a new cluster in the area.

### Invitation deposit

A registering candidate must pay a registration deposit. It is returned as soon as the candidate personhood is confirmed. 

But just like there is a threshold to be considered a human within an area, there is a negative threshold to be considered a bot. 

When a bot is confirmed it's deposit is payed to those who had (or rather hadn't) handshakes with it. 

    When FOAM is delivered. Invitation deposit can be (partly) raplaced with location proof. This makes it harder for bot-farms to maintain their army of bots. They have to move around a lot.

### Clusters

It is expensive for bots to bother a "human" cluster. But what if bots populated an area first? Real people will lose their stake when they try to register in their own city. 

There is an opportunity for them to create a new cluster in the area. They will then start collecting people there. Pairs for handshakes will be chosen only wihin that cluster. Whether there emerges several human clusters they may chose to merge.

This will create two instances of a location, which don't trust each other: humans and bots. This is what we want. We will then distinguish them from the outside.

    There is a very high incentive for a human cluster to separate itself from bot-nets. But there is no incentive to create too many clusters in the area. A single densly interconnected human cluster is easier to reach from the outside than a set of small ones. 





## Sybil detection

The mechanism above allows only humans with correct photo to enter the system. It confirms personhood and location. But it cannot recognize the same human entering multiple times. Uniqueness is proved by face recognition.

When user takes a selfie with the Upala app. The app guides her to take several photos from different angles. It helps increase accuracy. 

There are roughly 0,5% of people that have an identical twin (https://www.bbc.com/news/magazine-22813345). And we can only try to predict how many people will be suspected as a twin. I bet it won't be higher that 5%. 

But let's assume everybody has at least one twin somewhere (or the algorith is giving us false positives). So that everyone should expect to do aditional work sometime after they registered. 


__Uniqueness proof procedure__

Once a new candidate is registered and algorithm find a twin for him. The twin gets notified. When the candidate proves his global reputation, they both need to undergo uniqueness proof procedure. 

Related twins or similar people from the same area may chose to appear together at a handshaek. The third person confinrms there are really two similary lokng people.

Twins from different parts of the world need to appear in different places of the world within an interval too short to travel from one place to another. 

In both cases twins just need to request a handshake and agree on time. And there are penalties for delaying the procedure. So they both incentivised to cooperate.

    On privacy: 
    - Photos are stored as a search index only.
    - There is no information attached to a photo except location (we will try to detach it too).
    - The contacts are random so there is no way to deanonymise you by deanonymising your friends.
    - Additionally for every uploaded photo the system may generate a number of fakes.





# Global reputation

There are local and global user reputation scores. Local is the user's reputation in a local community (area). Global reputation represents how much of user's local reputation is "visible" to the global community.

The visibility depends on how well the user's location is connected to the global community. 

Any two locations can have a connection. These connections are established by traveling users. Every connection has a bandwidth. 

To calculate user's global reputation his local reputation is routed through  best bandwith to the global level. Reputation points are lost along the way on low bandwidth connections. Thus global reputation is always lower or equal to local.


### Conections between cities 

The network is hierarcial. 

Developers are at the top level. 

    There might be a different definition of what is global depending on the incetive model we chose. But for now let's use "developers" as the global level for the sake of simplicity.

Then come major world cites. Or rather citites with the largest Upala communities. They are well interconnected and a group of Upala developers have a lot of random connections in these cities. Local and global reputation are equal here.

Then come big cities, small cities, villages. 

Every pair of cities has two connections in either way, both with their own bandwidth. Bandwidths can be negative or positive. 


###  Establishing a connection, connection weight

Connections can be established only by users. We call them ambassadors. Anybody can become an ambassador. A user just needs to go into another area and request a handshake.

A handshake establishes a connection. Succesfull handshakes add __weight to the connection__. If the ambassador cannot find a human, he rejects handshakes. Rejections subtracts from the connection. This way the connection from ambassador's native location (A) to the new one (B) is established and weighted.

Future ambassadors from the same location (A) also add or subtract weight to the connection (A -> B). Previous ambassadors are punished or rewarded for their judgement. Majority punishes minority. 

Ambassadors also recieve scores (negative or positive) from their journey handshakes through reputation propagation mechanism (as described above). Rewards and punishments are higher than within the local area. The further the distance the higher the multiplier. 


__Example__

New York, Hartford and Providence all have high internal interconnectedness and all of them has a lot of global trust level. 

Springfield had a massive bot attack so that it citizens decided to separate into their own cluster. Now there are two Springfields in the same place. The humans Springfield turned out to be the same same size as the bots Springfield. But nobody can tell yet, which is which. 

Someone from Providence decides to visit Springfield. The abassador performs 12 random handshakes and approves only those belonging to Springfield 1. It creates a connection between Springfield 1 and Providence. But it's weight is too small to create any practical bandwith among the cities (concerning their population).

Now more people are visiting Springfield. Some come from Providence others from Hartford. But they all reject Sprigfield 1 and approve Springfield 2 citizens during their random handshakes. The visits result in downvoting connection weight to Sprinfield 2 into negative number. 

Eventualy good bandwith is established to Sprigfield 2 from both Providence and Hartfort. Those who approved Sprigfield 1 gets punished. 




###  Connection bandwidth

Every connection also has a bandwidth which depends on city population, density of local connections, distance between locations, ambassadors and locals reputation. 

So that two big cities need a connection with a lot of weight to get good bandwidth. A small village can be visited by a few ambassadors with high score to get good bandwidth to the big city. 



### From local to global reputation score

In order to calculate the global score the local score is router to the global level through connections between cities. 

Reputation score points are lost on every connection. The lower the bandwidth the more points are lost. System choses the route with the best bandwidth. Connections with negative bandwidth are ignored.

Bot clusters cannot earn connectivity to anywhere. 


### Example 

Alice have heard that her hometown Springfield has now at least some connection to the global setting. And now she would like to apply for universal basic income experiment using her Upala ID. 

She had 20 handshakes, 2 of which were rejected. Her local reputation score is 18 (scoring parameters may differ in production). 

Springfield had a lot of visits from Providence and Hartford. The weights of connections are quite high which resulted in bandwiths of 56 and 70% respectively. Good enough for the local score to be visible from the global level.

Providence to New York has 90% bandwidth, Hartford to NewYork - 89%, NewYork to global - 99%.

The best bandwidth would be 0,99*0,89*0,70 = 0,62 (bandwidth calculation may differ in production).

Alice global score is 18 * 0,62 = 11,16. This is higher than personhood threshold which is for now 6. Alice is considered a human. Greetings, Alice!


# Benefits
- Local communities can be initiated independently and included in global setting afterwards.
- Local communities can benefit even before inclusion to the global setting. 
- No complicated algorytms. We are on the path to an auditable system. So that probability of personhood can be calculated deterministicaly by anybody.
- Small number of interactions needed for a person to be confirmed as a human (random connections have more value than trusted connections).


# Further research
- Incentives. Why would a user want to earn more reputation than it is needed to be considered a human?
- Incentives. How face-recognition nodes earn?
- Incentives. The protocol discriminates people that cannot walk, blind people.
- Attacks. Two real twins can create an army of clones.
- Attacks. A skillful makeup artist can try to create multiple personalities by cheating both humans (at handshake) and face-recognition algorythm. 
- Attacks. As a consequence a skillful makeup artists can try to spam a victim with an evil twins army.







========================================

# Reputation system (7,5 bln cryptocurrencies)

Each user has a reputation balance. Reputation is like own coin. It is unique for every user in the system. However a user doen't "store" any of his coins. Instead the user's current reputation balance is only the course of his coin. And it can be positive or negative. 

A user stores only other people's tokens. His own reputation balance then is the 

When users meet eachother, they exchange their coins. But each of them has an option to decline the other person's coin.

Own reputation is a number, your reputation in other person's portfolio is the number of coins * course. 

Each of them decides if they want to a coin from their vis-a-vee.  

they can decide to accept a handshake or not. Accepting handshake means the 

is like having a share of that user in your own reputation. 

Reputation is a sum of reputation of every other person they ever had handshakes with within the system. 



