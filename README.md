# VMF: Voluntary Monetary Fund Project
##An open source system for community wealth management.
=======

**Introduction:** In 2016, people around the world work hard and get paid in a single local currency. Often this currency is inflated by their central bank, destroying their savings and encouraging them to borrow at interest. It should be easier for people everywhere to save.

The proposed solution is a cheap and simple open-source kit for a cryptographically-enabled market making fund. The returns from this fund are used to back a sound money and bootstrap a small crypto economy of less than 250 individuals.

This project is designed to be deployable by anyone with command-line experience, cloud servers, and a little financial know-how.  At first, we expect will be run by existing local officials, community leaders, and bankers on behalf of friends and family. Eventually amateurs may rise through the rank, creating an active “staking” market wherein smaller fund managers stake their lots with top fund managers.

###Project Goals
This library will enable anyone with basic web development skills to spin up a cheap, simple, and low-maintenance crypto-economic wealth management / market-making fund that can help a community save and grow their money. 

###Governance
This system is simple: it has no governance apparatus for changing itself (i.e., there is no voting, elections, or DAO mechanics). Participation in a given VMF is private, voluntary, and non-exclusive. It is purely an economic system which leaves governance up to the community using the open source library.

###Approach
Many cryptocurrency maximalists have attempted to build “trustless” global systems where software can somehow isolate bad actors. This belies the natural fact that trust between small groups of humans is foundational to civilization, and that moral hazard cannot be “engineered away.” 

###Solution
The VMF concept proposes a community monetary fund which uses financial and social incentives, as well as immutable ledgers, to keep members honest.

###How it works
The VMF has one basic purpose: to incorporate citizens in the VMF by issuing them a wallet address. This is the primary responsibility of the managers of a given VMF: to choose who can be in the VMF. VMFs don’t necessarily expire, but i2’s first deployment will end after 7 years. The length, size, scope, and investors in a given VMF will need to comply with local laws when deploying our project. (Our fund is a private placement regulated under US SEC Regulation D.)

###Management powers
In addition to admitting members, the managers are in charge of active management of their portfolio. They are incentivized to hold and grow the value of the coins they issue in various ways. Fund managers may trade coins with another VMF community on behalf of their members out of a common pool by incorporating another VMF as a citizen (ie., issuing an outside VMF group a single wallet address). However, when inside a VMF it is strictly a one-person, one-wallet address system.

###Deployment
Based on the Tendermint protocol, a VMF can be deployed cheaply on widely-available cloud VPSs or local machines. All VMFs use the same open source mobile wallet application, but a given fund manager could make a custom wallet if they choose. 

###Impact
Modern fiat instruments, and the banks that hold them, make for poor long-term savings vehicles. Professional wealth management is not available to most people. The VMF allows groups of individuals to hedge their salaried work in the “mainstream economy” by saving their earnings in an alternative system that is disconnected from bank woes and currency manipulation. 

===================

####Components of the VMF SDK
Tendermint blockchain running on VPS nodes (use Eris Industries tools?) Benson
Smart contract library Chris D.
Wallet mobile application (iOS/Android) C. White / Frederico
Documentation (legal and technical) Chris

**1. Community-oriented blockchain**
Private chain w/ hard-coded limit to 250 wallet addresses (ie., limit of Dunbar’s Number)
Fund managers may issue one wallet address per member (ie., a “passport-wallet”)
Fund managers may issue a single wallet address to another VMF
VMFs may interact by trading their L0 instruments only
Any fund manager may host their own instance of a VMF

**2. Smart contract library**
One-time minting of the coin pool; 100% unsold coins held in contract (no giveaways!)
Issuance of new wallet addresses to new member-investors
A-tier and R-tier transfer contracts for converting coins between tiers 
Brokerage contract for supervised A-tier / R-tier transfers between members
Wallet desktop app contracts for L0 instrument services between members (eg., escrow, layaway, collateralized loan)

**3. End-user wallet mobile application**
User’s profile contains: wallet address, name, photo, @handle (reputation system t.b.d.)
User can see a dashboard for all his or her VMFs, and their performance
User can see blockchain explorer for each VMF they’re a member of
Twitter-style chat forum for each VMF on its own blockchain (we could use this project)
GUI for using P2P banking contracts between members (may include escrow, layaway, collateralized loans, and other types of common contracts)

**4. Documentation T.B.D.**
Boilerplate private placement
Partner agreement
Legal Instructions
Technical deployment documents

*Read next: Fund Composition document*
