#Voluntary Monetary Fund: a platform for transparent investment funds
Launch a transparent blockchain-based investment fund in just a few lines of code.
###What you'll need:
* one (1) entry-level coder to deploy the project
* one or two (1-2) professional asset managers to run it
* several cheap cloud VPSs to get started
* a community of friends, family, or customers that are willing to invest in you

**Introduction:** In essence, this project is a cheap and simple open-source kit for a multi-purpose investment fund made transparent and immutable with underlying blockchain technology. This fund is not architected to scale to city- or state-size, but rather is intended to support a hard-coded limit of 250 investor-members. The returns from this 250-investor fund are used to back several tiers of bespoke currencies which, like shares, appreciate to reflect the performance of fund management. As more funds are join the platform, these currencies will become the basis for economic activites between fund managers and between member-investors.

###Target audience
The VMF project is designed to be deployable by anyone with command-line experience, cloud servers, and a little financial know-how.  At first, we expect it will be run by existing brands and membership clubs, replacing rewards systems that use "points" or "miles" with more professionalized financial services. Solo asset managers may also raise and operate various kinds of investment funds using this software. 

###Project Goals
Encourage communities of people to save and grow their money together. 

###Governance
Architected with private business in mind, this system has no governance apparatus for changing itself (i.e., there is no voting, elections, or DAO mechanics). Participation in a given VMF is private, voluntary, and non-exclusive. It is purely an economic system which leaves governance up to the community and the fund managers. Zero data is available to those outside the fund, but member-investors get full visibility into all activity inside their VMFs.

###Approach
Many cryptocurrency maximalists have attempted to build “trustless” global systems where software can somehow isolate bad actors. This belies the natural fact that trust between small groups of humans is foundational to civilization, and that moral hazard cannot be “engineered away.” 

###Solution
The VMF concept proposes a community monetary fund which uses financial and social incentives, as well as immutable ledgers, to keep members and managers honest.

###How it works
The VMF has one basic job: to incorporate citizens in the VMF by issuing them a wallet address. This is the primary responsibility of the managers of a given VMF: to choose who can be in the VMF. Secondarily, they manage the money of those who enter the VMF. VMFs don’t necessarily expire, but i2’s first deployment will expire after 10 years.

###Management powers
In addition to admitting members, the managers are in charge of active management of their portfolio. They are incentivized to hold and grow the value of the coins they issue in various ways. Fund managers may diversify holdings by trading coins with another VMF community on behalf of their members out of a common pool by incorporating another VMF as a citizen (ie., issuing an outside VMF group a single wallet address). However, inside a VMF it is strictly a one-person, one-wallet address system.

###Deployment
Based on the Tendermint no-mining consensus protocol, a VMF can be deployed cheaply on widely-available cloud VPSs or local machines. All VMFs use the same open source mobile wallet application, but a given fund manager could make a custom wallet if they choose. All VMFs share consensus with one another, so even a very small VMF can take advantage of the security of the overall system.

###Trust
When joining a VMF, think of the TSA rules: never let a stranger pack your financial bags. Entering a VMF means you're entrusting value to a human manager who will have freedom to invest as they see fit. If his or her skills as a market-maker are sub-par in the mainstream economy, a VMF will simply lose their money faster. This is a kit for knowledgeable asset managers.

###Impact
Modern fiat instruments, and the banks that hold them, make for poor long-term savings vehicles. Professional wealth management is not available to most people. The VMF allows groups of individuals to hedge their salaried work in the “mainstream economy” by saving their earnings in an alternative system that is disconnected from bank woes and currency manipulation. More importantly, it allows brands, schools, non-profits, and other small organizations to offer safe, cheap, and transparent financial services to their members.

###Crowdfunding your VMF
* In the Untied States, anybody who has registered a private placement with the SEC under regulation D may crowdsale their VMF in USD from accredited investors (ie., what we did). *With this option, your investors may not withdraw their funds for the length of the fund, essentially behaving like a market-linked certificate of deposit.*
* Anyone can begin a VMF without SEC registration if they raise crowdsale funds paid in BTC, ETC, ETH, or other coins. *The competition amongst unlicensed VMFs will be especially sharp with zero investor lockup!*
* Be sure to comply with local laws when deploying this project outside the US.

#Components
0. Full node daemon (roll our own with Eris Industries tools)
1. Smart contract library in Solidity
2. Wallet mobile application (iOS/Android)
 
In the VMF platform architecture, there is one main chain shared by all funds in the network. This is the liquid tier chain, also known as the L-tier chain or Lisa chain. This chain was generated by Iterative Instinct. All Iterative Instinct applications (such as the Flux mobile wallet for member-investors, the Flux CLI daemon/node for fund managers, and the Flux trade web app) all run nodes on the Lisa chain. However, each fund has its own A-tier and R-tier chains which are private and permissioned to their member-investors. These chains run on the fund's Docker nodes, as well as on the wallet mobile apps of their members.

##Full node daemon (Nickname "Flux node") // Q4 2016
This CLI node can be deployed on a **Docker instance** (required for ErisDB) and connects to our initial peers at Iterative Instinct. Once connected to the network, the CLI node allows fund administrators to setup their fund as follows:
* Instantiate a new wallet address on the liquid-tier chain (nickname: Lisa chain) which is shared by all funds
  * Associate this Lisa address with fund manager object containing attributes: bitcoin address, ether address, name, company, URL, keybase key, address, phone, email, user@handle, SSN/EIN, and image URL
  * Fund manager must create a password
  * Fund manager must enabled two-factor phone number authentication (use Eth proof of phone project?)
* Now with a Lisa-chain wallet address, fund manager may send a zero-coin transaction to Iterative Instinct's Lisa address: requesting to start a fund
  * If put on wait-list, return "waitlisted: we will contact you"
  * If rejected, return "rejected; for help email help@i2.vc"
  * If this address already submitted, return "already submitted"
  * If approved, Iterative Instinct spins up new A-tier and new R-tier chains in a Docker instance, to serve as seed peers. Once fund manager's Docker instance connects to these new chains, it will generate A-tier and R-tier addresses and associate them with the L-tier wallet address that sent the request
    * Return "successfully started your A-tier and R-tier chains!"
    * Return fund manager's new A-chain and R-chain wallet addresses, which are now added to the Fund manager object as attributes
  * Private keys for all Fund manager wallet addresses are held on Fund manager's Docker server which requested them (as per Eris)
  * End of fund setup process!

###Getting Investors
Now that your chains are up and running, you may enlist up to 250 member-investors. First, get their mobile phone numbers. To join, they will download the Flux mobile app and get an L-tier wallet address (phone number security code involved; entire mobile app spec is below) after they enter their KYC information (same as above)
  * With the app, member-investors use their Lisa wallet address to send a zero-coin transaction to your fund's Lisa wallet to request membership
    * If waitlisted, return "waitlist"
    * If rejected, return "rejected"
    * If accepted by fund managers, instantiate a new wallet addresses on the A-tier and R-tier chains, associated with this Lisa wallet address. Save the private keys for L-, A-, and R-tiers to the mobile device (more details on mobile app below).

#Fund composition and coin issuance
Now that you have a fund and some investors, you'll need to take investment and give them back shares in your fund. These shares are represented by coins. There are six different kinds of coins for each fund, each representing a different level of risk. As a fund manager, you may issue whatever combination number and type of coins you like, representing whatever business activity you like for each tier -- as long as you sort them by risk. (See the table below.)

##Choose your fund's risk profile
Consult the tables below. Whatever business activities are creating your profits, rank them by riskiness into one of the categories below. Then decide what percentage of your total funding will go to each activity; that is, what mixture of coins you'd like to issue. Some people may only issue one tier of coins, while others will be active in all six tiers.

<table>
  <tr>
    <td>Coin</td>
    <td>Proportion of issuance i2 chose</td>
    <td>Number of coins i2 chose to mint</td>
    <td>Number sold (as of 9.2016)</td>
    <td>Layer Description</td>
    <td>Risk Profile</td>
    <td>Returns</td>
  </tr>
  <tr>
    <td>A0</td>
    <td>14%</td>
    <td>5,600</td>
    <td>5.6</td>
    <td>Day Trading</td>
    <td>High</td>
    <td>High</td>
  </tr>
  <tr>
    <td>A1</td>
    <td>16%</td>
    <td>6,400</td>
    <td>6.4</td>
    <td>Arbitrage Pool</td>
    <td>Low</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>A2</td>
    <td>30%</td>
    <td>12,000</td>
    <td>12</td>
    <td>Interval Trading</td>
    <td>Medium</td>
    <td>High</td>
  </tr>
  <tr>
    <td>A3</td>
    <td>6%</td>
    <td>2,400</td>
    <td>2.4</td>
    <td>Tangible Operations</td>
    <td>Medium</td>
    <td>High</td>
  </tr>
</table>


### Reserve Tiers equal the other 34 percent of the fund

<table>
  <tr>
    <td>Coin</td>
    <td>Proportion</td>
    <td>Number of coins minted</td>
    <td>Number rendered (9.2016)</td>
    <td>Layer Description</td>
    <td>Risk Profile</td>
    <td>Returns</td>
  </tr>
  <tr>
    <td>R0</td>
    <td>10%</td>
    <td>4,000</td>
    <td>4</td>
    <td>Long positions</td>
    <td>Medium</td>
    <td>High</td>
  </tr>
  <tr>
    <td>R1</td>
    <td>7%</td>
    <td>2,800</td>
    <td>2.8</td>
    <td>Staking Nodes</td>
    <td>Low</td>
    <td>Low</td>
  </tr>
  <tr>
    <td>R2</td>
    <td>7%</td>
    <td>2,800</td>
    <td>2.8</td>
    <td>Fiat Reserve</td>
    <td>Low</td>
    <td>Low</td>
  </tr>
  <tr>
    <td>R3</td>
    <td>10%</td>
    <td>4,000</td>
    <td>4</td>
    <td>Bit-metals</td>
    <td>High</td>
    <td>High</td>
  </tr>
</table>


### Liquidity Tier 

<table>
  <tr>
    <td>Coin</td>
    <td>Number of coins minted</td>
    <td>Number rendered</td>
  </tr>
  <tr>
    <td>L0</td>
    <td>1,200,000</td>
    <td>0</td>
  </tr>
</table>

  * Enter proportion of coins for each tier (out of 100 percent)
  * Contract address which accepts bitcoin/ether from a known address and sends back fund coins to that member's wallet
* Enter a URL and API key to oraclize one or more external wallet addresses (to display fund's balance of crypto-positions)
  * Also oraclize one or more API endpoints (to display fund's balance for non-crypto positions, eg., the Fidelity API or E-Trade API)

From an investor perspective, the purpose of a VMF fund is to serve as a high-return safe haven. VMF structure is loosely modeled on the IMF’s [Special Drawing Rights](https://en.wikipedia.org/wiki/Special_drawing_rights) basket, but modified to suit a different purpose: stable appreciation, rather than just stability. This creates many of the benefits of the Petrodollar (debts shrink; savings grow) without the (quantitative) inflation and subsequent price inflation in the small business arena. This fund architecture is codified entirely in open source software; transparency in all ways is what makes this whole thing work, hence the blockchain (ie., immutability as a backstop for fund managers). 


####Important Legal & Logistical Notes
* VMFs may interact by trading their L0 instruments only
* In a privately-placed VMF, the Actively Managed Tier (A-Tier) is fully redeemable for USD after ~10 years
* Member-investors holding A- and R-tier coins may sell them to other member-investors, brokered by the fund managers
* In a "public" (crypto-crowdsale) VMF, fund managers may choose their own lockup period, after which A- and R-tier coins would presumably be made redeemable in one of the underlying crypto-assets (eg., ether or bitcoin).

  
####Notes
* Fund managers may issue other VMFs wallet addresses with same info above
* We will need to deploy a bunch of our own Docker instances for seeds (initial peers to connect to. e.g. "addr1:46656,addr2:46656") to secure the Lisa chain
* We may require fund managers to operate several Docker instances

**2. Smart contract library (Nickname: "Flux services")** // Sept - Nov 2016
 Multi-sig contract addresses allow managers to broker trades within their group:
  * Exchanging between A- and R-tier coins, to adjust an investor's risk profile
  * Redeeming the liquid tier (L) for A-Tier/R-tier coins
  * Buying, selling, or trading coins of any tier between members
  * 
* One-time minting of the coin pool; 100% unsold coins held in contract (no giveaways!)
* A-tier and R-tier transfer contracts for converting coins between tiers 
* Brokerage contract for supervised A-tier / R-tier transfers between members
* Wallet desktop app contracts for L0 instrument services between members (eg., escrow, layaway, collateralized loan)

**3. Member wallet mobile application (Nickname: "Flux wallet")** // Nov 2016 - March 2017
* Runs a full node on a smartphone
* Accept an invitation to join a VMF; creates a wallet and private key on this device
* User’s profile contains: wallet address, name, photo, @handle (reputation system t.b.d.)
* User can see a dashboard for all his or her VMFs, and their performance
* User can see blockchain explorer for each VMF they’re a member of
* User can use P2P banking contracts between members (may include escrow, layaway, collateralized loans, and other types of common contracts)
* User can enter a chat room with other VMF members (use ethTweet?)

*Read next: Fund Composition document*
