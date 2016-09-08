#Voluntary Monetary Fund
##Productizing transparent micro-finance
Launch a bank or investment fund with just a few lines of code. Build a cheap, sustainable crypto-economy on top of your fund and invite [Dunbar's Number] of your friends. Trade investment products with other micro-economies. Save and grow your wealth. 
###By the time this project is done, anyone on Earth will only need a few things to enrich their community: 
* one (1) entry-level coder to deploy the project
* one or two (1-2) professional asset managers to run it
* several cheap cloud VPSs to get started
* some friends and family with money (and smartphones) to join
* the trust and confidence of these people

**Introduction:** Today, working people around the world get paid in a single local currency. All too often, this currency is inflated by their central bank for political ends, destroying the savings of the middle class, putting small business goods on a never-ending price-hike against corporate goods, and encouraging people to borrow even at punitive rates of interest. It should be easier for people everywhere to save the hard-earned value of their work product.

The proposed solution is a cheap and simple open-source kit for a cryptographically-enabled market making (ie., hedge) fund. This fund is not architected to scale to city- or state-size, but rather is intended to support a small community hard-coded to a limit of 250 individuals (a smartphone or computer required to be a member-investor). The returns from this 250-investor hedge fund are used to back several tiers of bespoke currency which appreciate to reflect the performance of fund management. These currencies become the basis for further group economic activity, most notably financial services.

The VMF project is designed to be deployable by anyone with command-line experience, cloud servers, and a little financial know-how.  At first, we expect it will be run by existing local officials, community leaders, and bankers on behalf of friends and family. Eventually amateurs may rise through the ranks and gain notoriety for their performance, creating an active “staking” market wherein smaller fund managers stake their lots with top fund managers.

###Project Goals
This library will enable anyone with basic web development skills to spin up a cheap, simple, and low-maintenance crypto-economic wealth management / market-making fund that can help a community save and grow their money. 

###Governance
This system is simple: it has no governance apparatus for changing itself (i.e., there is no voting, elections, or DAO mechanics). Participation in a given VMF is private, voluntary, and non-exclusive. It is purely an economic system which leaves governance up to the community using the open source library.

###Approach
Many cryptocurrency maximalists have attempted to build “trustless” global systems where software can somehow isolate bad actors. This belies the natural fact that trust between small groups of humans is foundational to civilization, and that moral hazard cannot be “engineered away.” 

###Solution
The VMF concept proposes a community monetary fund which uses financial and social incentives, as well as immutable ledgers, to keep members honest.

###How it works
The VMF has one basic purpose: to incorporate citizens in the VMF by issuing them a wallet address. This is the primary responsibility of the managers of a given VMF: to choose who can be in the VMF. VMFs don’t necessarily expire, but i2’s first deployment will end after 7 years.

###Management powers
In addition to admitting members, the managers are in charge of active management of their portfolio. They are incentivized to hold and grow the value of the coins they issue in various ways. Fund managers may trade coins with another VMF community on behalf of their members out of a common pool by incorporating another VMF as a citizen (ie., issuing an outside VMF group a single wallet address). However, when inside a VMF it is strictly a one-person, one-wallet address system.

###Deployment
Based on the Tendermint protocol, a VMF can be deployed cheaply on widely-available cloud VPSs or local machines. All VMFs use the same open source mobile wallet application, but a given fund manager could make a custom wallet if they choose. 

###Trust
When joining a VMF, think of the TSA rules: never let a stranger pack your financial bags. Entering a VMF means you're entrusting that cryptocurrency to a human manager who will have freedom to invest as they see fit. If his or her skills as a market-maker are sub-par in the mainstream economy, a VMF will simply lose their money faster. However, with a trained investment professional and an entry-level coder combined, performance for the VMF members will be stellar.  

###Impact
Modern fiat instruments, and the banks that hold them, make for poor long-term savings vehicles. Professional wealth management is not available to most people. The VMF allows groups of individuals to hedge their salaried work in the “mainstream economy” by saving their earnings in an alternative system that is disconnected from bank woes and currency manipulation. 

###Crowdfunding your VMF
* In the Untied States, anybody who has registered a private placement with the SEC under regulation D may crowdsale their VMF in USD from accredited investors (ie., what we did). *With this option, your investors may not withdraw their funds for the length of the fund, which for us is 7-10 years.*
* Anyone can begin a VMF without SEC registration if they raise crowdsale funds paid in BTC, ETC, ETH, or other coins. *The competition amongst unlicensed VMFs will be especially sharp with zero investor lockup!*
* Be sure to comply with local laws when deploying our project outside the US

#Components
0. Full node daemon running Tendermint, to be used on Ubuntu VPS nodes (with Eris Industries tools)
1. Smart contract library in Solidity
2. Wallet mobile application (iOS/Android)
3. Web app / desktop application (Mac/Windows/Linux)

**1. Full node daemon (Nickname "Flux node")** // Sept-Nov 2016
* Compile from source
* Private chain w/ hard-coded limit to 250 wallet addresses (ie., limit of Dunbar’s Number)
* Fund managers may issue one wallet address per member (ie., a “passport-wallet”)
* Fund managers may issue a single wallet address to another VMF

**2. Smart contract library (Nickname: "Flux services")** // Sept - Nov 2016
* One-time minting of the coin pool; 100% unsold coins held in contract (no giveaways!)
* A-tier and R-tier transfer contracts for converting coins between tiers 
* Brokerage contract for supervised A-tier / R-tier transfers between members
* Wallet desktop app contracts for L0 instrument services between members (eg., escrow, layaway, collateralized loan)

**3. Member wallet mobile application (Nickname: "Flux wallet")** // Nov 2016 - March 2017
* Runs a full node on a smartphone
* User’s profile contains: wallet address, name, photo, @handle (reputation system t.b.d.)
* User can see a dashboard for all his or her VMFs, and their performance
* User can see blockchain explorer for each VMF they’re a member of
* User can use P2P banking contracts between members (may include escrow, layaway, collateralized loans, and other types of common contracts)
* User can enter a chat room with other VMF members (use ethTweet?)

**4. Full GUI node for Web/Mac/Win/Linux (Nickname: "Flux trade"; screenshots of web version in repo)** // June 2017
* As of 9/16 we have web-based prototype with trading interface
* Will have same features as the mobile wallet
* Will also run a full node
* Contains existing trading interface, plus coin inventory management, blockchain explorer, and issuances interface
* In sum, user can launch and manage his own VMF from this desktop application

*Read next: Fund Composition document*
