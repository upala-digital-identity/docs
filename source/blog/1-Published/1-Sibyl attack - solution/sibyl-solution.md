# A solution to sibyl attack problem

Goal
Share ideas
A don't know the ideas
B have ideas, inspired

- reminder
- in short
- in detail
- conclusion.


I'm developing a new identity proof system Upala. It's purpose is to distingush people from bots and clones (people with multiple IDs). It is a huge goal. To get there I started a series of posts (https://airtable.com/shrNQ0VClgqBiHmkL), showing my thinking process. I will then transform these posts into whitepaper.

While brainstorming ideas to solve the sibyl attack problem in the previous post (todo link), I came to a solution. In this post I will describe it detail. While it still lacks incetives of the users and some other parts I do believe this is a working one.


# Greetings human!
Sync with me! Video with Blade runner theme.

# The sybil attack problem 
I used an illustrasion proposed by Markus Knecht and added just a bit of a drama. The following situations are completely indistinguishable:

1: Alice and Bob are twins. They live in the same flat. Alice is out in the morning and home in the afternoon. Bob is out in the afternoon and home in the morning. They meet different people when they are out but never the same ones. They never invite guests.

2: Isabel is diagnosed with dissociative identity disorder. She has two phones. One has an account registered with her real name. And the other registered with her alter ego - Sibilla. Isabel is out in the morning and home in the afternoon. There she changes her pale pink standerd waitress uniform for a stunning evening gawn and goes to a luxurious cocktail party. She gracefully grabs the phone registered for Sibilla. Isabel and "Sibilla" meet different people and never invite anybody to "their" home.

Here Isabel is perfoming a sybil attack. We need to "punish" Isable and "reward" Alice and Bob. It is impossible to do by only analyzing social connections.


# A solution

Components: a smart-phone app, a face recognition server (todo), the FOAM's proof of location. It also presumes that we've figured out the incetives for the users to do the work.

__Here is how registering a new user will look like in short:__
- Take a picture of new user to sign him or her up
- AI detects sibyls
- Sybils take pictures simultaneously in different places
- Random validators confirm they see two different people

Now to details.

# Take a picture of new user
Two friends meet. One is in the system (Bob), the other (Alice) wants to recieve a new shiny decentralized censorship-free unique id. 

- Alice installs the __Upala__ app (I never mentioned the projects name before. Will soon devote a post to it too).
- Bob takes a picture of Alice using the new app on her phone (The app guides Bob to shoot the right perspective, face size, light, etc.)
- The app creates an ID for Alice.
- The app's indexes the Alice's face features, adds block hash, encrypts it and uploads it to a face recognition server. The features are assigned an id hash, not the id itself. So that face-recognition server cannot identify Alice.
- Bob and Alice confirm their "handshake" in their apps.
- Bob takes a picture together with Alice. The app constructs a picture for validation - adds their ID photos to the scene.
- Random validators confirm (by staking tokens) that they see 2 different people and that each of them has the right ID photo. Validators cannot see IDs. They only see photos associated with IDs.


# Face recognition server detects twins

Now let's check Alice. 

Face recognition server using Alice's face features looks for Alice in its database. If there is no suspicion for a twin Alice is considered a unique person and gets a high score.

If the algorytm suspects a sybil attack. Some additional work should be done. What if Alice has a twin from another part of the world - Sally.


# People looking alike (twins) confirm their uniqueness

In order to confirm we are dealing with twins we need to see them together (same time, same place, same photo). The other way is to see them __at the same time, but in different places.__ 

Here is where FOAM may be hepfull. - todo. What is FOAM. 

Alice and Sally will have to undergo another verification process:
- They decide on the interval they both are able to take photos. The allowed length of the interval is calculated depending on their timezones.
- Withinin the allowed interval they take pictures through the Upala app. Every picture has the latest block hash, person's ID hash, location-proof data (FOAM).
- Both photos are validated by a random set of validators. Validators only need to confirm the new photos correspond to the ones that were used to create Alice's and Sally's IDs. The fact that the photos were taken almost at the same time in different parts of the globe confirm the people are different.

A failure to do this procedure would mean we have a sybil attack.


# Components 

Do we need all this complexity: friends handshake, location proof and face recognition? Can we get rid of some of the componetnts?

I like the I came up with mantra in my previous post: __it does matter who you are, where you are and who you friends with.__ I think I'll use it my future developement a lot. For now let's use it for ordering the componetns. 


# It does matter who you are. Face recognition.
Without face recognition we will have to compare every newcomer with every existing user. This is practically impossible. Face allows us to lower the ammount of work to a practical level. The system will only ask to confirm the suspected twins. I believe it is the most crucial part of the sybil attack protection.

Face recognition works really well. Try using my photo to find me among 100 million (https://www.similarweb.com/website/vk.com) of active users of Russian social network vk.com. Remember we can adjust the "suspicion score" on the go balancing between accuracy and ammount of work.

The face recognition system will probably be from a 3-rd party. Thus we need to make sure that this 3-rd party will have no access to user's credentials. I thought of some zkSnarks cryptography, a private key generated in a multi-party computation procedure similar to the one used by ZCash (https://z.cash/blog/completion-of-the-sapling-mpc/). But I cannot assemble it in my head right now. Let me just blatantly declare that it is possible and drop this uncommented sheme below as a prove.


# It does matter where you are. FOAM's proof of location service. 
In order to prove that we are dealing with twins we either need to photograph them together or take two photos simultaneously in different locations (or within an interval equal to a flight time). To prove that pictures are taken at the same time at different places we need location proof. 

__Do we have to wait untill FOAM releases their proof of location service?__
Well, I believe, for a state of the art system - yes we need FOAM. But we can start small. We can use known landmarks to confirm location. Take pictures with something available on Google street view on the background, validators will confirm. 

__Can we do without lacation proof at all?__
I can't imagine any other realistic way except some sophisticated biometry: DNA tests, cornea, fingerprints, palm vein scanners, etc. I'd say palm vein scanners would be a realistic approach but with an addition of notary entities and the right incentives for them. I see it as palm vein scanners cost VS FOAMs release date question.
https://commons.wikimedia.org/wiki/File:Computerised_Corneal_Topography.jpg


# It does matter who you are friends with.
Why would Alice need Bob? What if anyone just takes a selfie and registers in the system? The mechanizm above will work just fine with invitation procedure. But there are some problems:

- What if malicious Alice will start registering every day? She breakes the face recognition algorithm, makes a realistic doll and starts spamming Sally. Sally's uniqueness score will go down. 
- What if lazy Sally doesn't want to cooperate and confirm her uniqueness. This time Alice will have an unfairily low score.
- What if Bob will pay people from the street to register them in the system and then use their IDs.

These problems seems to me unsolvable without a reputation system. That's why we need friends. The mechanism to replicate trust between friends is yet to be found - hopefully one of the following posts will be on that. 


# Conclusion

A sybil attack protected system like this posseses an additional and not so obvious benefit. It allows starting communities independently in different parts of the world. Clusters of people don't need to be intersected. 

The mechanism has a good chance of becoming a part of a system which will provide human uniqueness.

