# Ideas to solve sibyl attack problem

Goal
Share ideas
A don't know the ideas
B have ideas, inspired

- reminder
- what is sibyl problem
- ideas
- conclusion 


I'm developing a new identity proof system. It's purpose is to distingush people from bots and clones (people with multiple IDs). It is based on six degrees of separation idea. It is a huge goal. To get there I started a series of posts (https://airtable.com/shrNQ0VClgqBiHmkL), showing my developement process. I will then transform these posts into whitepaper.

# Sync with me - video with bubbles 



# What is a sibyl attack problem

We want every ID to represent a unique human. But in a voluntery system it is very hard to notice anyone splitting into two. We don't have everybody in the system to notice there is a lishnii popping out of nowhere.

While I was writing this post Markus Knecht (https://medium.com/@tawarien) commented my previous post. He gave this simple explanation of the problem.

The following situations are completely indistinguishable:
1: Two people living in the same flat: one is out in the morning and home in the afternoon, the other is out in the afternoon and home in the morning meeting different people when they are out but never the same ones and they never invite other people to their home.
2: A single person with two phones each with another account going out in the morning with phone 1 and in the afternoon with phone 2 and does never meet the same people in the morning as in the afternoon and does never invite people into its home.

It is impossible to catch these clones by just analyzing the connections. Another mechanism is needed. 

But there may be other examples: generating bots, copying the existing clusters of people to mimic real connections.


# Existing solutions

The only working solution for now is a state ID. 

    By the way if you have it, you probably underestimate how lucky you are. Have a look at this article (todo).

uPort, Akasha, ERC-725, keybase, pgp/gpg, Web Of Trust, Bouillon project don't deal with uniqueness. These are either for identity storage or for trust networks (or related). Trust is not uniqueness. As in many cases you may trust two IDs and you may not care, that these are the same person. 

I came accross two projects, which are trying to provide uniqueness. These are Bright ID (https://www.brightid.org/) and Pseudonim pairs (https://panarchy.app/Proof-of-power.pdf). Bright ID seems to be focusing on network analysis and Pseudonim pairs on random pairs validation. And it seems to me they havent's solved the puzzle yet. Please, authors forgive me if I'm wrong.

I'm looking only at titles. Currently I'm keeping myself away from papers. I want to preserve my fresh and "naive" view and share it.

This post has no solvution to the puzzle of course. I'm just throwing a bit more pieces (ideas and questions). I haven't seen these ideas anywhere, so I hope it will be helpful.


# Ideas

I explore friends, location-proof and face recognition.

# Locals and friends

I like the idea of collaborating friends. We should somehow benefit from trust between friends. Imagine small groups. Communities, small villages, multistortied houses, schools, campuses.

# State ID hash, issuing own IDs 

We can "invite" our friends into system by typing in their state ID on our phone. The app will encrypt it, search for duplicates and create a new record, if there were no duplicates.

State ID is a unique reliable number. But there are drawbacks. The most important one - not everyone in the world has a reliable ID.

I refused an idea of using state ID. But maybe there are clues here anyway. Let's leave limits of resources, time and morale behind:

    Why the state ID works at all? Because it is forced, and everyone is in the system. Everyone is monitored since birth. But it is just a photo and a number. Can we issue a papper ID for developing countries? Can we start from birth? The state ID system is relatively young. How it was built? What is the prosedure of reissuing a lost ID? How reliable state it is?


# FOAM. Proof of location. Proof of space-time. Proof of movement. 

Consider FOAM. It is a blockchain-based location service. Unlike GPS it will allow to reliably prove device location. With FOAM releazed we will be able to prove a real-world physical handshake. 

We can use it for additional overhead for bots and other new mechanics:
- Our app ask for a random meeting. There everyone confirms the number of people they see and their photos.
- Everytime you use the app, your location gets recorded (and encrypted) for further analysis.
- The app may require an inviter and invitee to be at the same location.
- We can ask an ID to be at a certain place at a __certain time__. Space-time overhead, 
- Proof of movement. Move together for 1 km to create an account.
- Human runs.
- Untill FOAM is in developement, we can take pictures of known landmarks with current block hash to confirm location. 

Friends can easily meet each other, bots and clones can't.

    There are many simularities with FOAM. We both need to spread the network all around the world to make it usefull. Let's draw more parallels. What if we think of connections as coordinates? Am I just a set of coordinates? Forget about nodes. A connection confirms two people at the same time. 


# Two-to-one (peer-to-peers). Triad - is the building block.

What if we use a triad of nodes instead of a single node to be the smallest indivisible part of the system? What if in order to register an ID the app would require two existing IDs to witness the new one (confirm photo, ID, humanness, location, etc.).

- It is simple to split oneself into two. Triads will require a more sophisticated consiracy. 
- A triad could form a police unit (blade runners), which checks if a person or other triad exists.
- Triads could be used to start a new communities (clusters). As oposed to BrightID's seeds.
- A triad could share responsibility for life - chose your friends wisely. 
- __No, third person is a random set of validators from around the world who stake on the new connection__ 

Friends can easily form triads - bots and clones cannot.

    Independently organized clusters are invisible for each other. How could we connect two independent clusters of triads? Community Detection in the Network of German Princes in 1225: a Case Study (Dahmen, 2017) https://www.researchgate.net/publication/312157420_Community_Detection_in_the_Network_of_German_Princes_in_1225_a_Case_Study



# Initiatives

# Vote is chaper than fraud. 

There is probably no solution to sybil problem in a voluntary identification system. Meaning the overall accuracy will be significantly lower than that of a state ID. But we can use  accuracy with probability. Every ID will have a probability of uniqueness. 

Still keeping sybils in mind how would you calculate this probability? Analyzing connection is not enough or too comlicated.

An answer may be in game theory as for the many blockchain projects. With a staking sytem are we gonna be able to measure a probability of uniqueness for everyone or only for the whole sytem? 

Even if we only have an overall probability there the system may be usefull for services where vote is cheaper than fraud. Vote price is a threshold. It will not be used for goverment elections, but will be good enough for social networks registration or some not so important voting.

    What is the right incetive to keep one's social graph tight? How expensive alter egos are? The tighter my graph is, the more reputation/money I get. Keep yourself and your friends away from a slippery slope of graph splitting.



# UBI. A pyramid-like scheme. Laggards sponsor early birds.

We can introduce a commision of joining the network. Let it be very low. Participants invite others and form a pyramid. The payments from newcomers are split up the chain of handshakes. This way early birds get return of investment (probably huge). Those in the middle join for free. And it is only the laggard who acually have to pay for the service. In other words early birds recieve universal basic income. 

# Horizontal connections. Reputation. Stake.

In the scheme above there are no horizontal connections, no reputation. Even worse it endorses to invite profiteers who will invite even more profiteers (hope I'm using the right word). But we'd rather endorse bringing friends and trust to the network.

Probably mechanics of "Laggards sponsor early birds" could be used to stake on "humanness" or trustworhtyness of anybody in the system. The earlier the stake, the higher the returns. 

    Invert the pyramid. Pay it forward. 


# Investors, buyers, advertisers 

We can try to get rid of commision by introducing some external source of money. 
- sell uniquness data. 
- use affeliate marketing campaigns to drive growth. 
- establish a fund to bootstrap further growth (big companies, goverments?).

    Can we sell People (token)? What is the token utility? A vote? Can an identity uniqueness be a byproduct of a campaign? Is there any business entity (or antities) interested in investing to a platform like this? Are we even "allowed" to have a profit?




# Devices and algorythms 

# Face recognition

It is impossible to search a face with a perfect match in a Database. But it is possible to find similar faces. Here try searching my photo http://searchface.ru/. The very first are mine! This appeared 12 february and will probably be shutdown soon. 

Here is how we can use face recognition: 
- When registering a new user take a picture of a newcoming user through the 6handshakes app.
- The app stores the photo on users devices and uploads it to some open storage encrypted with a special key (generated in ceremony like ZCash's - so that nobody knows it).
- The key is available to the face recognition algorithm. The algorithm searches for clones suspects. 
- If there is a suspected clone, the clone and our new user are asked to upload a new photo within a determined time interval (with current block hash and proof of location by FOAM). 
- Random validators confirm they see two different (maybe very similar) people at different loactions. 

    At this point I started to write a new article on a more detailed solution of sybil problem. 


# Devices 

We can introduce a notary or a validator entity, equipped with some device or app on their phone (a smart phone is a special equipement too - not everyone in the world has it). 

The same way FOAM is planning to use beacons (LoRa Wifi devices) we can incentivse people to buy fingerprits and eye scanners, face-recognition apps, DNA-tests, chip implanters! Notaries (or validators) will earn money for building, updating or helaing the network (register people and hunt replicants for bounty!)






================
I don't like an idea of analyzing clusters. 




=============================
DO NOT READ THIS ENTIRELY
=============================
I bolded all the important keywords. Scroll to something that catches your attention. Share your thoughts. 



===================
I like to start imaginig how the system works as many clusters forming independently around the world.


===========
I've seen Bright ID is talking about seeds. I woud like clusters to start forming independently.