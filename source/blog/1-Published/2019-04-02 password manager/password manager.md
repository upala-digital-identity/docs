

# Plan 

- We cannot build uniquness score -> We can try to build something more useful
- Maybe digital identity? - > Yes, better, but still adoption gap seems to be too wide there is no value. 
Can we deliver value from the start?
As the guy told The problem is recovery.
Digital identity = recovery mechanism + sybil attack protection.
Recovery mechanism = Password manager! 
    + We are half-way through it (we are actualy building it)
    + Challanges
    + Benefits

If we want to build identity we have to solve it. 

We can even lower the ammount of work for the user. 

Digital identity is recovery and sybil protection. With no recovery it is just uniqeness and no adoption. We can do it independently and there is a good reason to do it.


Я попытался представить самую простую версию Upala. 

Но она бы не сработала и вот почему. Однако, я открыл для себя, что система идентификации - это антисивила + восстановление доступа. Дальше думаю... Система восстановления доступа может стать самостоятельной системой, ее можно разрабатывать независимо, она способствует adoption. 


# We cannot build Uniqueness system  (Uniqueness score vs Digital identity)

I tried to imagine a simpler version of Upala. I thought it could only provide some sort of blockchain-native CAPTCHA or provide human uniqueness in some other way, requiring very little of efforts from a user. No deposit, no complicated procedures, no user data stored, uniquness index is comparatively easily gained. Those who lose their acount simply create another one or recovers.

Sounds obscure, but the point is that I tried to redifine the goal of research and lower it. Which is one of invention process techniques, described in this book. (todo)

    Somehow I wanted the whole system to In this it would be sufficient to build a sybil attack protection system: Uniquness score = sybil attack protection.

The adoption concerns however made me quickly abandon the idea. Why should anyone bother to participate in another version of captcha? There is still something to do, but not much of a new value. And why should services participate? The easier it is to recover or to create another account for a user the less trust there is from services. I refused the idea. However I stumbled upon some interesting thoughts...

Considering adoption gap it probably makes more sense to deliver something which is harder to build but easier to adopt. Something more complicated but which brings more benefits.

It made me think again of an alterantive to state ID. The one which allows to take a loan, cast an important vote or order an airplane ticket. The one which is really valuable and trusted.

# What it takes to build a decentralized identity system.

There are Uport (todo link) and some other systems, but they rather provide a storing solution for existing credentials rather than issuing their own. Often sybil atack protection is based on state issued ids.

Garry (todo) noted in his talk that the problem of digital identity is the problem of account recovery. 

Digital identity = recovery mechanism + sybil attack protection.

He believes there is no sane way to solve the problem without forcing users to store their private keys in a bank. Which kinda defeats an idea of building a decentralized identity system.

Let's not be so pessimist. 

    This is a much tougher challange, but there is a lot more value. It is definetelky worth trying to unlock it. 
    It not only helps to overcome adoption gap by providing more value. It can create value so to say in portions and help to start building user base even before digital identity. 

# We can build it in parts.  We can build Password manager and it is cool

Looking at the formula above I realized that there are two completely independent systems in the right part of the equasion. 

Let's drop the sybil attack protection part from it. Then we are left with just a Recovery mechanism. 

If we have a recovery mechanism we can provide an authentication tool for users. And if we can build a decentralized authentication tool, we can build a decentralized password manager and aven a crypto wallet. Which is a holy grail of blockchain adoption! I'm getting too excited as usual. Let us be satisfied with just a password manger for now.

Recovery mechanism = Decentralized password manager

A free opensourse decentralized passoword managaer - sounds great. 100% trusted, 100% available. It would be even better than centralized solutions in terms of security. Due to decentralization there will be no mass database hacks. With a product like that I believe it is quite simple to get a fair user base. 

The problem may become a solution. Everything we will need then is "just" to add a sybil attack protection. We are solving account recovery problem and adoption at the same time. 

# But is it possible at all to build a decentralized password manager? 
Without a central server and banks we have to rely on friends and biometry. Biometry seems to be prone to hacking. I believe we can do without biometry, but we cannot do without friends (You see, bockchain is like real life, you can loose your face, but if there are friends to suuport you, you are fine). Our social connections are as unique as our biometry. In my opinion in a set up like this we will have to share our responsibility of keeping an account with our trusted ones. Here are some facts that make me hopefull, that it is possible.

__Social responsibility works.__ Not quite direct comparasion, but social responsibility works fine in microfinance. (todo wiki)

__Facebook is already doing it.__ Facebook can recover your account with 3 friends out 5 confirming it is you. A working example from a centralized world. 

__ZeroPass is building a decentralized solution.__ ZeroPass is building a decentralized password manager. https://www.zeropass.io/schematics. 

__Gnosis Safe is building a Etehreum-based solution.__ Gnosis Safe in my current unserstanding they provide a framework to build a decentralized account recovery mechanism (todo)

# Challanges

Keeping aside the fact, that we will have to invent a decentralized password manager first... 

If we are about to use biometry or friends we'd have to remember that we are exposing our users to unfamaliar attacks. Instead of database hacks and stolen passwords we'd then have to deal with dolls, makeups and masks when someone tries to trick biomentry. And even worse - bribery and blackmail when someone tries to pass through our friends and notaries. 

We are moving threat from hackers to performers (ransoms and social hacking). Responsibility from coders to users and to those who teaches them security. 

# Conclusion
There is no identity system without authentication and recovery. But there is an authentication and recovery without identity system.

1. It is simpler to build an alternative to state ID than an alternative to CAPTCHA. 
2. Digital identity = Decentralized password manager + sybil attack protection.
3. It makes sense to start with a Decentralized password manager as an independent project, build user base and attach sybil attack protection afterwards. Helps to jump over the adoption gap.












https://github.com/BlockProject/b-lock
https://blockvault.site/











# Mechanism
It does matter, who you are, where you are and who you are friends with. In other words it a combination of person's name, biometry (face-recognition), location and friends. 

# How can we do it Implementation
Skip this section if you are not interested. These are some super-draft ideas of how it may work in a decentralized world.

We have a login, password and second factor. Let's try to imagine an alternative to this. Before we start try to think differently of login. If it is kept secret, it adds to security a lot. Authentication and recovery can be split into two stages: find and unlock. We will think of login-password as find and unlock. We also assume that unlock is a chastnyy sluchay of unlocking.

This is just an illustration of how it may look like. Point is - there is some job for a user to be done. 

## FOAM
Replace login-password pair with face-recognition, proof of location, person's name and friends approval.

Find
1. Find account with face recognition
2. Type name to select account (or register as a new user)

Unlock
When sybil attack is detected
3. Ask a number of friends to confirm recovery

Use location as password. When planning a trip - make sure to put checkpoints.

##  Notaries (gates)
Ask one random notary to start a procedure of recovery.
The other random notary finishes the procedure. All other steps are in between. This may cost money. Friends pay.

1. Ask a random notary to register again (no need to tell about recovery)
2. Sybil attack warning -> select account recovery.
3. Friends confirm new account - take pictures through their apps. Meet physically.
4. Give all tokens to the old account. Freeze for a couple of days.

These are some super-draft ideas of how it may work in a decentralized world. They do have flaws. But it is just to start a conversation. And just to give a gimpse that it is possible. But it is a lot of job and not what is accustomed too. Will this be adopted?


# Register
- Take a selfie 
- Type name
- Point to 3 friends for recovery (enforced)


# Use 


Get a seed phrase. 


Face, name, friends, location, secret? 

# Attack 
Doll 

# Recover
Accounts are forever. Append an existing account to a device. 

1. Ask a random notary to register again (no need to tell about recovery)
2. Sybil attack warning -> select account recovery.
3. Friends confirm new account - take pictures through their apps. Meet physically.
4. Give all tokens to the old account. Freeze for a couple of days. 




Notaries can revoke approval.
Access is regained gradually
Old account can cancel at any time?
