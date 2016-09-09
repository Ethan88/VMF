#The Voluntary Monetary Fund
## "Crypto-economy in a box"
**DESCRIPTION**: *An open source system for administering a group of transparent, interactive, immutable investment vehicles.*

By joining a VMF platform, you can launch a transparent blockchain-based investment fund in just a few lines of code, with no fees and near-zero overhead. Inter-fund transactions are governed by a fair Central Bank. For this instance, Iterative Instinct is the central bank; however this software may be licensed to other institutions anywhere in the world who would like to serve in that role. 
###Minimum requirements:
* one (1) intermediate-level coder to deploy the project
* one (1) professional asset manager to run it
* a cheap cloud VPS running a Docker instance
* a community of friends, family, or customers that are willing to invest in you
* six Ethereum addresses 
* $10,000 USD minimum or 10 percent of fund assets AUM in ETH to be held in escrow contract as stake (fully refundable)

**Introduction:** In essence, this project is a cheap and simple open-source kit for a multi-purpose investment fund made transparent and immutable with underlying blockchain technology. A fund instantiated on this network is not architected to scale to city- or state-size, but rather is intended to support a hard-coded limit of 250 investor-members. The returns from this 250-investor fund are used to back several tiers of bespoke currencies which, like shares, appreciate to reflect the performance of fund management. As more funds are join the platform, these currencies will become the basis for economic activites between fund managers and between member-investors. There are a maximum of 250 funds per VMF network and per central bank, bringing the maximum number of humans in a given VMF network to around 62,000.

###Target audience
Both the "parent" central bank daemon (ie., the VMF platform as a whole) and individual "child" Fund daemon are designed to be deployable by anyone with command-line experience, cloud servers, and a little financial know-how.  At first, we expect small brands, startups, and small asset managers to join our Iterative Instinct VMF. Quickly thereafter, we expect our Central Bank daemon will be run by large brands, hotels, airlines, membership clubs, and other organizations looking to replace or amplify rewards systems that use "points" or "miles" and realize the increased revenue from more professionalized financial services.

###Project Goals
Encourage communities of like-minded people to save and grow their money together. Secondarily, to bootstrap coins into circulation between these people for goods, services, and debts.

###Governance
Architected with private business in mind, this system has no governance apparatus for changing itself (i.e., there is no voting, elections, or DAO mechanics). Participation in a given Fund or network of Funds is private, voluntary, and non-exclusive. It is purely an economic system which leaves governance up to the community and the fund managers. Zero data is available to those outside the fund, but member-investors get full visibility into all activity inside their Fund by viewing its blockchain explorer inside their mobile app. (Addresses are pseudonymous, but hardly anonymous.) The central bank may look at all Fund blockchains within its VMF, but has no power to move assets in any of them. 

###Approach
Many cryptocurrency maximalists have attempted to build “trustless” global systems where software can somehow isolate bad actors. This belies the natural fact that trust between small groups of humans is foundational to civilization, and that moral hazard cannot be “engineered away.”

The VMF concept proposes a three-level hierarchy: the central bank, the funds, and the member-investors of those funds. In sum, this network is a community monetary "fund of funds" which uses financial and social incentives, as well as immutable ledgers, to keep members and managers honest, and to grow everyone's wealth.

###How it works
The Central Bank has one job: get good Fund Managers on the platform. The Fund Manager, in turn, has one basic job: to incorporate wealthy and honest citizens into their Fund by issuing them a wallet address. This is the primary responsibility of the managers of a given Fund: to choose who can be in it. Secondarily, they manage the money of those who enter the Fund, and try to grow its value in various ways.

###Management powers
In addition to admitting members, the managers are in charge of active management of their portfolio. They are incentivized to hold and grow the value of the coins they issue in various ways. Fund managers may diversify holdings by trading coins with another Fund community on behalf of their members out of a common pool by incorporating another Fund as a citizen (ie., issuing the outside group a single wallet address). However, inside a Fund it is strictly a one-person, one-wallet address system.

###Trust
When joining a Fund, think of the TSA rules: never let a stranger pack your financial bags. Entering a VMF means you're entrusting value to a human manager who will have freedom to invest as they see fit. If his or her skills as a market-maker are sub-par in the mainstream economy, a Fund will simply lose their money faster. This is a kit for knowledgeable asset managers.

###Impact
Modern fiat instruments, and the banks that hold them, make for poor long-term savings vehicles. Professional wealth management is not available to most people. The Fund model allows groups of individuals to hedge their salaried work in the “mainstream economy” by saving their earnings in an alternative system that is disconnected from bank woes and currency manipulation. **More importantly, it allows brands, schools, non-profits, developing governments, and other small organizations to offer safe, cheap, and transparent financial services to their members.**

#The Central Bank
VMF structure is loosely modeled on the IMF, its [Special Drawing Rights](https://en.wikipedia.org/wiki/Special_drawing_rights) basket, and its XDR instrument. The model has been modified to suit a different purpose: stable appreciation, rather than just *prima facie* stability. This new model creates many of the benefits of the Petrodollar (debts shrink; savings grow) without the (quantitative) inflation and subsequent price inflation in the small business arena. Transparency in all ways is what makes this whole thing work, hence the blockchain (ie., immutability as a backstop for fund managers). We believe it is the ultimate safe haven network. 

## Fund of funds
* Structured like the other funds in six tiers, the Central Bank (parent fund) has six of its own wallet addresses for its own A0, A1, A2, R, R0, and R1 activities. These obey the same rules as all other funds (the 250-address limit, for example, limits every central bank to 250 funds, just as every fund is limited to 250 members). 
* It also has its own LX coin representing the average value of its other tiers, and may issue its LX wallet addresses to other funds, just like any other fund.
* The central bank must also contribute to the stake pool equaling at least $10,000 USD or 10 percent of its AUM, whichever is larger, just like **every other fund in a VMF.** This covers outstanding LX and Lisa instruments in circulation, as explained below.

## The Fund A/R Exchange Contract
All funds in a VMF, including the central bank, have an A/R Exchange Contract which will turn A-tier coins into the equivalent value of their own R-tier coins, and visa-versa. These coins are not transmissable outside a given fund, but may be sold and exchanged between member-investors within a Fund. 

Why would anyone exchange A-tier coins for R-tier coins? Because R-tier coins are the only ones allowed to back a fund's LX instrument, which is the "index" coin that tracks the performance of that particular fund. Of course, every member-investor of a fund gets an LX address upon signup and acceptance. But Fund Managers may also choose to issue LX addresses to other funds. Even so, these LX coins have yet larger uses: read on!

## The Fund LX Exchange Contract
All funds in a VMF, including the central bank, have their own LX Exchange Contract address. Every fund also has LX coins issued and held 100 percent in-contract when its blockchain begins. This contract address will release these LX coins if sent collateral. Let's look at how this works. 

The LX Exchange Contract for this fund receives an R (bitmetal reserve) coin, which should be relatively price stable, and places it in escrow. In turn, it automatically lends out that fund's LX (index) coins to whomever the `msg.sender` of the R coin was. This LX may be then be sent as payment to other member-investors, or held by another Fund as an investment. Another common use will be in backing Lisa coins, in the contract below.

### How Lisa Coins Are Issued
At the genesis of a VMF, the parent fund (Central Bank) issues a hard-coded number of 100,000,000 Lisa, which is held 100 percent in an "exchange contract." Both Funds and the Central Bank must send ~100 percent (+/-1) collateral in R-tier coins to the LX contract to borrow Lisa and put those coins into circulation.
  * This exchange contract address is available to the entire Lisa chain, even the central bank itself
  * Upon receiving LX from any one of the 250 funds in its network, this contract sends back a request for 100 percent (+/-1) in R-tier coins
  * The user must reply by sending that amount of R-tier coins as collateral; both the R-tier collateral and the LX coins are held in escrow by the contract
  * The contract returns a "redemption address" where the member-investor can send their Lisa when they're done, releasing their LX coins, and the R-tier coins being held as collateral
   * If the value of the Fund's LX coins decrease against the Lisa while they are held in contract, the amount is debited from the R-tier collateral and held by the contract; if the value of the fund's LX goes up against the Lisa, the amount is credited back.

## The Lisa Exchange Contract 
In order to trade with one another universally, Fund Managers will probably use Lisa coins. (Fund Managers who know each other, and have formed a syndicate, might issue one another's Funds a wallet address in their own fund's LX coin, and those pass LX coins back and forth.) But the Lisa coin will be most commonly circulated, itself "backed into" circulation by someone's LX and R-tier collateral, plus the value of their stake in the ETH stake pool.

## Limits on Outstanding LX and Lisa
A scenario might arise where a member-investor sends another member-investor some Lisa as payment for an item. Suddenly and without warning, the value of the LX being held in escrow for the outstanding Lisa plummets in value! No worry, that's what the 100 percent collateral, held in any of the trusty R-tier coins, is there to insure against. But then, the value of those R-tier coins drops as well. What happens then?

Should the value of voth the R-tier coins and the LX coins stay below 10 percent of earlier value for more than 96 hours, then the LX and R-tier coins being held in the LX Exchange Contract are joined in escrow by the equivalent amount of ETH from the stake pool. This situation remains, marked to market every 24 hours, until the value of the underlying LX and R-tier asset returns.

For this reason -- to ensure the price stability of the Lisa -- the value of outstanding LX for any given Fund may not exceed the value of their initial stake (either $10,000 USD in ETH or 10 percent of AUM, whichever is larger) that they submitted when launching their fund, and which is being held in the stake contract.

###Crowdfunding a new Fund on a VMF platform
* In the Untied States, anybody who has registered a private placement with the SEC under regulation D may crowdsale their VMF in USD from accredited investors (ie., what we did). *With this option, your investors may not withdraw their funds for the length of the fund, essentially behaving like a market-linked certificate of deposit.*
* Anyone can begin a VMF without SEC registration if they raise crowdsale funds paid in BTC, ETC, ETH, or other coins. *The competition amongst unlicensed VMFs will be especially sharp with zero investor lockup!*
* Be sure to comply with local laws when deploying this project outside the US.

#Software components
0. Central bank node daemon overseeing a VMF network (it has admin/root permissions)
1. Fund node daemon which can instantiate and administer a child Fund (we're rolling our own with Eris Industries tools)
2. Wallet mobile application (iOS/Android)
3. Fund management web interface that our central bank, i2, built for our particular VMF (Flux Trade)
 
In the VMF platform architecture, there is one main chain shared by all funds in the network. This is the liquid tier chain, also known as the L-tier chain or Lisa chain. This chain is generated by the central bank, in this case Iterative Instinct. The central bank is also responsible for building a mobile wallet for its ecosystem, and building a Fund Admin iterface. They may also tell their fund managers to use Flux Trade and Flux wallet applications, if they are unwilling to build their own; however, they must host instances of these applications themselves.

All Iterative Instinct applications (such as the Flux mobile wallet for member-investors, the Flux CLI daemon/node for fund managers, and the Flux trade web app) run nodes on the main Lisa chain that connects every fund in this VMF network run by i2. However, each fund has its own chain which is private and permissioned to their member-investors. This chain runs on the fund's Docker nodes, as well as on the wallet mobile apps of their members, as well as on some central bank nodes owned by Iterative Instinct.

##Specification for Fund node daemon ("Flux node")
This CLI node can be deployed on a **Docker instance** (required for ErisDB) and connects to our initial peers at Iterative Instinct. 

###Creating a fund
Once connected to the network, the CLI node allows fund administrators to setup their fund as follows:
* New fund manager can use the CLI to instantiate a new wallet address on the liquid-tier chain (nickname: Lisa chain) which is the chain shared by all funds. (Anyone on Earth may obtain a Lisa wallet address with the Flux mobile app.)
  * Next, the fund manager must enter his information. This Lisa address will turn into a Fund Manager object containing attributes: six ethereum addresses from an existing Mist wallet, labeled for the six actively managed tiers A0, A1, A2, R, R0, and R1; full legal name, company, URL, keybase key, address, phone, email, user@handle, SSN/EIN, and image URL
  * Fund manager must then create a password
  * Fund manager must enable two-factor phone number authentication (use Eth proof of phone project?)

###The stake pool contract
In order to launch a fund, you'll need to add collateral (ETH) to to a stake pool contract. This is to protect the price of Lisa in the event that your fund collapses while it has LX and/or Lisa coins backed by its assets in circulation amongst other funds. The amount of this stake in ETH should be equivalent to $10,000 USD minimum or 10 percent of fund assets AUM in ETH to be held in escrow contract as stake (fully refundable). Contact partners@iterativeinstinct.com for more information on staking, and to get the stake pool contract address for the Iterative Instinct VMF.

###Requesting permission from a central bank
Now with a Lisa-chain wallet address, fund manager may send a zero-coin transaction to Iterative Instinct's central bank Lisa address, which indicates a request to start a new fund. **This should be done only after you have transferred your stake to the stake contract.** 
  * If rejected, return "rejected; for help email help@iterativeinstinct.com"
  * If this address already submitted, return "already submitted"
  * If request is approved by Iterative Instinct human operator, he generates seed peers for one (1) new Fund chain with no wallet addresses. Next, the fund manager's Docker instance connects to this new chain, and generates seven wallet addresses (A0, A1, A2, R, R0, R1, and LX) and associating them with the Lisa wallet address that sent the new fund request. These addresses are now all part of the new Fund Manager object, sitting on the new Fund chain.
    * Next, require the Fund Manager to enter Flux Trade API key
     * Oraclize the Flux Trade account balances endpoint so the network can calculate the value of this Fund's holdings for all tiers (A0, A1, A2, R, R0, R1; the value of LX must be auto-calculated.) This is required for the member-investor dashboard to see how their investment is performing.
    * Return "successfully started your chain and created your wallet! Please backup your keys."
    * Return also fund manager's seven new Fund Chain wallet addresses, six of which are associated with the ethereum addresses he entered earlier; and remind him his Lisa address
  * Private keys for all Fund manager wallet addresses (I think) are held on Fund Manager's Docker server which requested them (as per ErisDB docs)
  * Fund setup process complete!

###Getting Investors
Now that your fund is up and running, you may enlist up to 250 member-investors. First, get their mobile phone numbers.
* To invite a new member-investor to the system, use the CLI to create a new user associated with the person's phone number (eg., `new.user = 2123002020`)
* Tell the new member-investor to download the Flux mobile app. The app will auto-generate an L-tier wallet address for them
 * New member-investors must add KYC information and *matching phone number* to the invitation. Phone verification security code involved; rest of mobile app spec is below
 * With the app, member-investors send a zero-coin transaction to Fund Manager's Lisa address from their new Lisa address to request membership
    * If waitlisted, return "waitlist"
    * If rejected, return "rejected"
    * If accepted by fund managers, instantiate A0, A1, A2, R, R0, R1, and LX wallet addresses on the Fund chain, and associate them with the Lisa wallet address that made the request, along with the KYC info the member-investor entered. These are the attributes of the "Member-Investor object." 
     * Save the private keys for this users 7 addresses to the member-investor's mobile device.
     * Tell them to back up their damn private keys
*Lastly, have them send ETH to any or all of your six fund ETH addresses that you (as Fund Manager) entered upon when you created your fund. Remember to tell your investors that these ETH addresesses for A0, A1, A2, R, R0, and/or R1 correspond to risk level!

# Fund composition and coin issuance
Now that you have a fund and some investors, you'll need to take their money and give them back shares in your fund. These shares are represented by coins: the six actively managed tiers, corresponding with the types of wallet addresess you created: A0, A1, A2, R, R0, and R1. There are seven different kinds of coins for each fund, each representing a different level of risk. (The seventh, LX, represents an "index," or moving average, of the value of all.)

## A/R Tier Issuance
As a fund manager, you may issue whatever combination number and type of coins you like right in the command line, representing whatever business activity you like for each tier -- just remember to sort them by risk. 

##LX Issuance
Your fund may issue as many LX coins as it likes, with the same minimums and maxiumums as the other tiers. The difference is that **all LX coins are held in contract** and are put in circulation only once R-tier coins have been put up as collateral (See the table below, and more contract details and limits further down.)

##Choose your fund's risk profile
Whatever business activities are creating your profits, rank them by riskiness into one of the categories below. Then decide what percentage of your total funding will go to each activity; that is, what mixture of coins you'd like to issue. Some people may only issue one tier of coins, while others will be active in all six tiers.

<table>
  <tr>
    <td>Coin</td>
    <td>Layer Description</td>
    <td>Risk Profile</td>
  </tr>
  <tr>
    <td>A0</td>
    <td>Misc. Day Trading</td>
    <td>High</td>
  </tr>
  <tr>
    <td>A1</td>
    <td>Commercial Operations</td>
    <td>High</td>
  </tr>
  <tr>
    <td>A2</td>
    <td>Interval Trading</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>A3</td>
    <td>Arbitrage</td>
    <td>Medium</td>
  </tr>
</table>

Reserve Tier coins **must equal at least 34 percent** of total coin issuance

<table>
  <tr>
    <td>Coin</td>
    <td>Layer Description</td>
    <td>Risk Profile</td>
  </tr>
  <tr>
    <td>R</td>
    <td>Precious metals</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>R0</td>
    <td>Long positions</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>R1</td>
    <td>Staking Nodes</td>
    <td>Medium</td>
    </tr>
  <tr>
    <td>R2</td>
    <td>Fiat Reserves</td>
    <td>Very Low</td>
  </tr>
</table>


### Liquidity Tier 

<table>
  <tr>
    <td>Coin</td>
    <td>Description</td>
    <td>Risk Profile</td>
  </tr>
  <tr>
    <td>LX</td>
    <td>Stable-coin specific to this fund, and redeemable for the above tiers. Gets its value from the sum total basket average. Value shown in Lisa/XDR.</td>
    <td>Risk average of entire fund</td>
  </tr>
  <tr>
    <td>Lisa</td>
    <td>Stable-coin usable across all the L-chain which connects all funds in this VMF instance. Value pegged to XDR.</td>
    <td>Low</td>
  </tr>
</table>

####Note on fungibility
Funds cannot exchange A0, A1, A2, R, R0, and R1 coins with one another. Because each fund's chain is not connected to any other, the only way that funds may do business is by trading their LX instrument for a Lisa coin, and then doing a transacton in Lisa. The Lisa coin is the lingua franca in a given VMF platform network, and its value is pegged to the XDR; thus 100 lisa = 100 xdr. Central banks may not do business with one another except by trading with each other in underlying assets. **Lisa chains are not connected.**

###Take investment
Once the Fund Manager has decided which tiers to issue, he must next decide how many to issue at each tier. The total number of coins issued at all tiers must equal at least 20,000 and at most 999,999,999. What number you choose really comes down to the ETH amount you plan to raise, since people don't like using tiny decimals. In the CLI, the Fund Manager:
  * Enters proportion of coins for each tier (out of 100 percent)
  * Enters the size of the total coin pool (at least 20,000)
  * Enters the face value of each coin in ETH (same value for all)
  * "Fundraising exchange" contact address is generated
   * This contract listens for deposits in your six ethereum addresses labeled A0, A1, A2, R, R0, and R1 and returns a message over RPC to look for the txn.sender address among the member-investor objects
    * If/when found, give the appropriate amount of coins from that tier to that member-investor

#### Notes
* Fund managers may issue other funds wallet addresses with same info above
* Central bank will need to deploy a bunch of its own Docker instances for seeds (initial peers to connect to. e.g. "addr1:46656,addr2:46656") to secure the Lisa chain, and secure all 250 fund chains

# Flux wallet mobile app (to be built separately)
The end-user experience (aka, member-investor) for wallet & blockchain explorer
* Runs a full node on a smartphone
* Even logged out, members can create a Lisa wallet address with zero balance and **receive** Lisa, which they can then send to others.
* User may login to all their Funds. 
* User may add new Funds. For each Fund a member-investor joins....
* Get a text invitation to join a fund; download Flux wallet and confirm number
 1. Enter KYC info; create password; turn on 2FA
 2. View the six ETH wallet addresses for this fund, and send in your Ether
 3. Get coins in your new Flux wallet, hooray
* User’s profile contains: 7 wallet addresses per fund; name, photo, @handle, keybase, website, address, SSN, EIN, and all other KYC information 
* Reputation system t.b.d.
* User can see a dashboard for all his or her Funds, and their performance
* User can see aggregate of all their Funds holdings in this wallet
 * For each Fund user is member-investor in, they can view
  * View all 7 tier coin prices change for this fund last 1h, 3h, 6h, 12h, 1d, 3d, 7d, 10d, 14d, 21d, 1m, 3m, 6m, 9m, 1y, 2y, 3y (...) and YTD. 
* User can see blockchain explorer for each Fund they’re a member of
* User can use contracts
 * Convert A/R coins to LX using the Fund LX Exchange Contract; the A/R coins are held in escrow
 * Convert LX coins to Lisa using the central bank's Lisa Exchange Contract
* User can enter a chat room with other Fund members (use ethTweet?)

#Flux Trade (built separately; launching end of September 2016)
This open-source level 2 tool combines 10 crypto exchanges in one price ladder and order book to make day trading, interval trading, and accumulating long positions easy. Bonus: it's extra easy to get out of tight trades without slippage. But Flux Trade has a more important feature when it comes to the larger fund.

**The Flux Meta Wallet**

Flux Trade has a meta wallet based on Uphold Bank. It keeps reserves safely there, while conducting limited market operations, specifically arbitrage (automated) and trading (manual, by humans). This Meta Wallet serves as the source for price data that member-investors see in their mobile app. As Flux Trade develops, we will add other equities and FX trading to the tool so that market makers of all types can operate funds in our network.

#Licensing Fees
Generally speaking, the VMF project is shockingly cheap to deploy for everyone involved, even not considering the unspeakable waste of existing banks that serves as comparison. However, there are fees to maintain and further the development of this software, and to meagerly enrich its creators.

In a given VMF, each Fund pays an annual tithing to the Central Bank to the tune of **0.009** percent per annum of a moving average of AUM **payable in ETH only.** This payment is remitted in 12 intallments, or monthly, each year. Payment is made manually by Fund Managers -- it is not auto-deducted.  

For other VMFs licensing this software to operate as their own Central Banks, a licensing fee of **4.4** percent of their total fee haul per annum, to be paid in 12 installments and **also remitted in ETH.**

Flux Trade introduces a **0.01** percent fee per trade, per exchange.
