#The Voluntary Monetary Fund
## "Crypto-economy in a box"
**DESCRIPTION**: *An open source system for administering a group of transparent, interactive, immutable investment vehicles.*

**Introduction.** Asset managers of all types must use banks and software tools to make trades and hold their capital. Banks, funds, and family offices today pay handsomely for software tools and platforms to do this, in addition to counterparties, contract attorneys, underwriters, accountants, data scientists, and other expensive personnel. Many of these positions exist purely to make estimated guesses where good economic or price data simply is not available, or to craft legal contingencies for events not forseeable without such data. This cost is passed on to investors in the form of enormous fees.

The nascent blockchain economies couldn't be more different. Discrete data about one's ecosystem is free and voluminous for businesses built on blockchains: that is to say, the protocol is "fat" and provides a lot of valuable shared functionality for all businesses at an underlying level. The blockchain "application" layer, operated by people, can thus be very thin -- paper thin, in fact, which actually makes the name "smart contract" seem apt. 

For financial services, this means an incredible shrinkage on Wall Street. Banks that were once thousands of people could now be administerd by six or seven. But the mainstream economy already uses all those *other* kludgey systems. How could an asset manager in 2017 create an investment vehicle from scratch, entirely in blockchain software?

The solution would look something like: "a transparent blockchain-based investment fund in just a few lines of code," with all the value and promise of no-hacking, no-corruption, low-fees for "thin" software applications, and lower human capital costs. But immediately there are problems.

First, it's important to remember what software does well: it scales, and it disintermediates. So this would be a one-man bank that could get very big, very fast: Fat cat bankers like Lloyd Blankfein fundraising directly from millions of average Americans, all by himself. It would be Madoff 2.0. 

This absurd scenario makes light of the fact that financial technology problems -- unlike the rest of humanity's problems -- do not improve as the software scales. In fact, the better the software gets at scaling, the bigger the moral hazard gets.

This makese sense with what science knows about the biological limits to scale in our social networks. Dunbar's Number is around 250: the maximum number of human souls you can conceivably love and understand as three-dimensional beings. A good crypto-financial system would accomodate this biological handicap without encouraging tribalism; a great crypto-financial system would allow groups to interact, trade, and compete with one another under the aegis of a provably fair referee.

###The role of UX in this solution
Today, banks organize themselves in ways that are convenient for them, and force customers to manage the complexity. Having different types of accunts forces you to deal with different "units" of the bank, or be "transferred" to another "department" which is probably running an entirely separate set of databases. 

A private, permissioned blockchain-based financial institution can use the same interfaces as its customers, and its databases so they get the same visibility into transaction data. And thanks to the Merkle Root algorithm, assets can be marked to market in real time. In a pure software bank, everything is transparent -- much too transparent. Behind a walled garden this might be fine; say within a few dozen members of a family. But your friends and relatives aren't exactly an "economy" in and of themselves.

###Approach to a solution
Many cryptocurrency maximalists have attempted to build “trustless” global systems where software can somehow isolate bad actors. This belies the natural fact that trust between small groups of humans is foundational to civilization, and that moral hazard cannot be “engineered away."

The VMF platform uses incentives and disincentives both social and monetary to create a scalable system for transparent investment funds. We begin by imagining an "economy" comprised of many "child funds" all on equal footing. Each Fund has a Fund Manager, one human being with a fiduciary duty to the friends, family, and colleagues who let him manage their money; this person has a legal entity in the "real world" and is regulated. But he keeps his assets, and all customer funds, on a private blockchain hard-coded limit of 250 wallet addresses, so that his investors can see their positions at all times. The value of his positions are updated by oraclized endpoint, whether from a crypto-wallet, crypto-bank such as Uphold, or for mainstream equities, a traditional portal like the ETrade API.

### Wallet Issuance
Each private chain ("Fund") has room for 250 entities. The Fund Manager's duty is to invite 250 solvent, responsible, and wealthy individuals to the Fund. The wallet addresses may be issued to discrete human beings; a head of household or some other such trustee; or another Fund Manager. Because these wallet addresses are preferential, we will call them "wallet-passports," in that they confer similar "value" of being a member of a privileged, private economic group. 

At this stage in the thought experiment, leave aside in your mind the issue of which cryptocurrency is being exchanged; that will be addressed below. Assume it is an ideal, perfectly stable asset; we'll solve the problem of volatility separately below.

## How "child funds" Interact
Because one Fund Manager can issue another Fund Manager a wallet-passport, Funds may take positions in one another as a hedge against their own management skills. This is good, because it encourages pro-social investment from one community in another; a more-zero sum solution might end up with one group arming to rob (whether by 51 percent attack, or physical means) the blockchain bank of another group. 

Our utopia seems to be struggling. For one thing, each Fund must be sound and solvent or the whole system will come crashing down. And for another, we haven't solved the issue of whose coins to trade in. Why? Because none of us want to hold huge amounts of savings in bitcoin or ether, owing to its volatility. So we have to solve three big problems:

1. What coin would 250-person crypto-economies use to trade with one another?
2. How could these 250 people "save" their money or do any financial planning in a crypto-economy when public-chain currencies like BTC/ETH are so volatile? 
3. How do we tell a "good" Fund from a bad one?

### Sweet home USD
The USD is a managed currency, albeit horribly mismanaged, that offers some attractive features *prima facie.* Because of its constant, soul-sucking, savings-destroying (quantitative) inflationary tendencies, it makes debt shrink, and in some small way (though not to the extent Keynesians would have us believe) this does encourage people to invest their money in something worthwhile instead of letting it sit. 

We believe these features of a currency are attractive enough to pursue cryptographically, but only if we can find another price mechanism unlike the extortative Petrodollar recycling scheme (that combined with T-bond sales) props up the price of the USD today.

Such a currency would need to be administered by a provably fair referee: a central bank that would hold assets in reserve, backing some common coin that Funds could pass around as units of account. Importantly, this coin would need to have a one-time issuance and some guarantee of no further issuance; in practical, these are the rules of an open source protocol in the making, so that licensing a given "economy" means consenting to certain hard coded-rules, such as the 250-member limit on member-investors. 

If a central banker can manage his reserves responsibly, the liquid coin used by his funds will appreciate. This principle is also true of child funds; good management of the underlying assets means any coins a fund issues will appreciate to reflect the improved value of the underlying, plus some premium for demonstrably good management. Now we are getting somewhere! 

But we still haven't solved problems our three problems. And let's be real -- there are lots of other obstacles to creating an economy, so let's hammer through the rules of the system in more specific terms. 

###How it works
The Central Banker has one job: get good Fund Managers on the platform. The Fund Manager, in turn, has one basic job: to incorporate wealthy and honest citizens into their Fund by issuing them a wallet address. This is the primary responsibility of the managers of a given Fund: to choose who can be in it. Secondarily, they manage the money of those who enter the Fund, and try to grow its value in various ways.

Each private fund has its own permissioned blockchain with the ascribed 250 wallet addresses. Each fund is also connected to the Central Bank's main chain, where it can exchange the liquid coin issued by the Central Bank with other funds. Superficially, this is a solution to problem #1, whose coin Funds should trade in. That's because it removes the possibility that coins backed by one Fund might become valueless if that Fund made bad investments and subsequently collapses. An economy where you can't trust the currency your neighbor pays you is not a stable economy. 

We are hitting on the bedrock of problem #2: people need to trade in a stable currency, managed by some trustworthy entity they know isn't quantiatively easing the money supply and thus destroying peoples' savings, incentivizing debt at interest, and inflating the prices of small business goods and services. 

However, there is good news: in our parent fund / child fund architecture, if we solve the problem for one, we solve it for all. Let's begin with who gets into a VMF, which is a catch-all term to describe a crypto-economy as deployed using our tools, under one person who begins by capitalizing the Central Bank. 

###Management powers and responsibilities 
In addition to admitting members, the Fund Managers are in charge of active management of their portfolio. In a crypto-fund, any asset or position can be represented by a coin issued by the Fund. In our architecture, all Funds -- including the Central Bank -- are architected in six (6) tiers of assets. Anyone who licenses our software may choose to create and capitalize their own central bank, or deploy a Fund under the aegis of an existing Central Banker. That interaction, agreement, and vetting process must happen in the meatspace, just as these individuals need to file proper fund formation documents in the real world. 

Fund Managers and Central Bankers are incentivized to hold and grow the value of the coins which may represent literally any underlying asset or activity on Earth. (As long as there's an API endpoint we can oraclize to get a balance, we can inventory it in on the blockchain. Though admittedly the joys of real-time marking-to-market are only available for native crypto-assets such as DGD, for precious metals, for appcoins and altcoins, and to a lesser extent for Fx.)

###Trust
When joining a Fund as a member-investor, or by starting a Fund under a Central Banker, think of the TSA rules: never let a stranger pack your financial bags. Entering a VMF means you're entrusting the value of your hard work to a human manager who will have freedom to invest as they see fit. If his or her skills as a market-maker are sub-par in the mainstream economy, a crypto-asset instrument will simply lose their money faster. The kit specified below is designed for knowledgeable asset managers but requires only basic programming skills.

#The Central Bank
To solve the problem of a stable Central Bank issue currency, we draw especially on the IMF, its oddly named [Special Drawing Rights](https://en.wikipedia.org/wiki/Special_drawing_rights) basket, with the accompanying SDR/XDR instrument. The model has been modified to suit a different purpose: stable appreciation, rather than just stability. This new model creates many of the benefits of the Petrodollar (debts shrink; savings grow) without the (quantitative) inflation and subsequent price inflation in the small business arena. Transparency in all ways is what makes this whole thing work, hence the blockchain.

## Just like any other Fund
Every fund including the central bank issues 7 of its own coins, while participating communally in the 8th, which is issued by the central bank but backed by assets managed by all or most of the participating Funds. How this reserve system functions will become apparent further below. For now, we'll focus on the structure of a Fund. Both the Central Bank and the 250 Funds it governs are structured the same way.
* Every Fund including the Central Bank has six tiers of "assets" representing an arbitrary sorting of activities and assets by risk, from least risky to most risky. Thus, each Fund and Central Bank has its own wallet addresses for its own A0, A1, A2, R, R0, and R1 coins, representing its own underlying activities. The A- and R- designations are purely risk stratfications. 
* It is up to the Fund Managers (and the Central Banker, for the assets under his management) to decide what investment or commercial activity to engage in, and how to categorize their risk level. 
* It is up to Fund Managers how many coins to issue, and at which tiers. They can issue 100,000,000 coins at just one tier, or 100,000 evenly across all six tiers. Whether their actual investment activity lines up to the API endpoint that marks their asset-value to market is a question not of trust, but of verification, as Oraclized endpoints can be cryptographically matched to the server that issued the API key for that given equity trading account. This provides insurance the Fund Manager actually owns the accounts and wallet addresses he claims to.
* It is up to the sales skills and trustworthiness the face value of the coins he will be able to sell to investors to represent a share of his asset management activities. Inexperienced asset managers may not be successful at raising funds to capitalize a Fund or Central Bank without demonstrable success in a related discipline.
* Each Fund including the Central Bank also has its own LX coin ("index coin") representing the average value of its other tiers, and may issue its LX wallet addresses to other funds, just like any other fund. This coin is backed by redeemable assets and may only be circulated when underlying assets are held in escrow in a smart contract, as detailed below.


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

For the rest of this explanation, a "Fund" will serve to mean both a Fund and/or its Central Bank. A "VMF" means a group of Funds under a provably fair Central Bank.

## The Fund A/R Exchange Contract
Remember that A- and R-tier coins may represent any activity, for example, trading, arbitrage, the holding of precious metals, altcoins, and the holding of equities and assets both mainstream and crypto. All Funds share a common challenge in turning these investments and activites into a backable currency which they can then exchange with one another. 

Thus, all Funds in a VMF have an A/R Exchange Contract which will turn A-tier coins into the equivalent value of their own R-tier coins, and visa-versa. These coins are not transmissable outside a given fund, but may be sold and exchanged between member-investors within a Fund.

### Backing coins with R-tier
Why would anyone exchange A-tier coins for R-tier coins? Because R-tier coins are the only ones allowed to be held as collateral for a fund's LX instrument, which is the "index" coin that tracks the performance of that particular fund. This has the fringe benefit of isolating Fund Managers who issue Of course, every member-investor of a fund gets an LX address upon signup and acceptance. But Fund Managers may also choose to issue LX addresses to other funds. Even so, these LX coins have yet larger uses: read on!

## The Fund LX Exchange Contract
All Funds in a VMF deploy a standard LX Exchange Contract address. Every fund also has LX coins issued, and held 100 percent in this contract, when its blockchain begins. This contract address will release these LX coins if sent the proper collateral. Let's look at how this works. 

The LX Exchange Contract for this fund only receives an R-coin (bitmetal reserve) which should be relatively price stable, and places it in escrow. The endpoint deliering the value of the asset underlying this asset must provably be metals; for example, a balance of gold held in Uphold, or some DGD in an Ethereum wallet address. 

When this contract receives an R-coin to hold, it automatically sends out that fund's LX (index) coins to whomever the `msg.sender` of the R coin was. This LX may be then be sent as payment to other member-investors, or held by another Fund as an investment who was issued a wallet address for the Fund. Another common use will be in backing the common "liquid-tier" coin which allows Funds to do business with each other. 

### How the Central Bank's common currency works
At the genesis of a VMF, the parent fund (Central Bank) issues a hard-coded number of 100,000,000 liquid-tier coins we will affectionately call "lisa," a nice bastardization of "lira." The 100,000,000 lisa coins are held 100 percent in an "exchange contract." Both Funds and the Central Bank must send ~100 percent (+/-1) collateral in R-tier coins to the LX contract to borrow Lisa and put those coins into circulation. Here is the actual contract flow:
  * An exchange contract address is made available to the entire Lisa chain (both Fund Managers and regular Member-Investors) when the Central Bank starts the chain
  * Upon receiving an arbitrary amount of LX coins to hold, in escrow, from any one of the Funds or Member-Investors in its network, the contract then sends back a request for 100 percent (+/-1) in R-tier coins
  * The user must reply by sending that ~100 percent collateral in R-tier coins; now 200% the value of the issued Lisa coins are held, both R-tier collateral and LX coins, in escrow by the contract
  * The contract returns a "redemption address" where the member-investor can send their Lisa when they're done, releasing their LX coins and R-tier coins back to their wallet
   * If the value of the Fund's LX coins decrease against the Lisa while they are held in contract, the contract debits the amount is debited from the R-tier collateral and held by the contract; if the value of the fund's LX goes up against the Lisa, the amount is credited back.

# Why are we doing this again?
At last, we have the beginnings of a stable instrument that Funds can transfer between one another. Again, this isn't foolproof: if a Central Banker lets in crappy Fund Managers, it only takes one or two to scuttle an entire VMF. So as sophisticated as smart contracts might sound, they are not, and never will be, a replacement for good sense or other oldies-but-goodies such as the English Common Law system. This system of private crypto-economies is intended to serve purely as a kit, deployable by any individuals, for rescuing their wealth from mainstream or fiat instruments of all kinds.

Luckily customers won't see any of this complexity, or the true state of pending economic crisis that warrants the invention of this system. Comforting people during this time of transition is just as essential as empowering them to become their own bank and take ahold of their wealth for themselves, by entrusting its management to a series of Fund Managers they trust, perhaps even Funds managed under different Central Bankers.

As you'll see below, comfortable UX plays into the way we daisy chain these contracts to behave just like the currencies and banking systems that we're used to. In fact, as you'll notice from the contract above, the exchange is a fairly manual process. We don't believe people are ready for auto-debit contracts that perform complex conversions. We're dealing with real value here -- peoples' savings and retirements -- so this system purposely seeks to replicate a select few of the useful conventions of old-fashioned savings and loan banking.

## The importance of the Lisa Exchange Contract and its Stake Pool
In order to trade with one another universally, Fund Managers inside a VMF will probably use the Lisa coins of that VMF. Lisa coins are not fungible between VMFs. Fund Managers who know each other, and have formed some sort of syndicate either inside a single VMF or across VMF boundaries, might issue one another's Funds a wallet address in their own fund's LX coin, and those pass LX coins back and forth as a way of investing in an "index" of that Fund. But the Lisa coin will be most commonly circulated among member-investors, itself "backed into" circulation by someone's LX and R-tier collateral, plus the value of their stake in the ETH stake pool.

All Funds including the Central Bank must contribute to the stake pool equaling at least $10,000 USD or 10 percent of its AUM, whichever is larger. This covers outstanding LX and Lisa instruments in circulation, as explained below.

## Stake Pool Contract, and limits on outstanding LX and Lisa
A scenario might arise where a member-investor sends another member-investor some Lisa as payment for an item. Suddenly and without warning, the value of the LX being held in escrow for the outstanding Lisa plummets in value! No worry, that's what the 100 percent collateral, held in any of the trusty R-tier coins, is there to insure against. But then, the value of those R-tier coins drops as well; perhaps the price of gold has randomly plummeted. What happens then?

Should the value of voth the R-tier coins and the LX coins stay below 10 percent of earlier value for more than 96 hours, then the LX and R-tier coins being held in the LX Exchange Contract are joined in escrow by the equivalent amount of ETH from the stake pool. This situation remains, marked to market every 24 hours, until the value of the underlying LX and R-tier asset returns.

For this reason -- to ensure the price stability of the Lisa -- the value of outstanding LX for any given Fund may not exceed the value of their initial stake (either $10,000 USD in ETH or 10 percent of AUM, whichever is larger) that they submitted when launching their fund, and which is being held in the stake contract.

##How Central Banks do business
As described above, Funds might do business with other Funds in either LX or Lisa coins, depending on the arrangement. But how do Central Banks do business? In BTC, ETH, ETC, Monero, or any other public chain. In all likelihood, they'll already have these coins as part of a long crypto-position inside their fund. But more importantly, both Central Bankers and Funds must buy ether and send it to an address in order to instantiate a new Fund or Central Bank.

We believe in the Federal system of government, despite its degradation at the hands of the Federal Reserve. We believe in privacy, but not total anonymity, which creates incentives for bad actors. Wallet-passports tie real names and KYC information held on-chain by Fund Managers, but names are not associated publicly with wallet addresses. So while **all member-investors can see all transactions inside their Fund(s) they will probably not know which addresses belong to which individuals** unless they have done business with that wallet address directly.

Outside of a Fund, there is zero visibilty inside. Only a Central Banker and Fund Manager can see which wallet addreses belong to which individuals, but they are powerless to move anyone's funds without their permission.

From here, this guide increases in specificity as it turns into a tutorial. This tutorial is also a functional spec for our development team.

#Software components
0. Central Bank CLI daemon/node (free and open source)
1. Fund node CLI daemon/node (free and open source)
2. Member-investor node (free and open source; becomes the core of mobile application for iOS/Android)
3. Trading Account / API Mesh for 10 exchanges (free and open source; becomes the core of Flux Trade)
 
###Minimum requirements:
* one (1) intermediate-level coder to deploy the project
* one (1) professional asset manager to run it
* a cheap cloud VPS running a Docker instance
* a community of friends, family, or customers that are willing to invest in you
* six Ethereum addresses 
* $10,000 USD minimum or 10 percent of fund assets AUM in ETH to be held in escrow contract as stake (fully refundable)

In the beginning, an aspiring central banker instantiates a VMF by running the Central Bank daemon. This generates the main chain shared by all funds in this new VMF network. It is the liquid tier chain, also known as the L-tier chain or Lisa chain. In so doing, this newly-minted banker is agreeing to the terms of the license  set forth in this Github project; namely the GNU Affero License. 

Next, they must deploy their capital and begin managing their positions. How they do that is entirely up to them. The Central Bank daemon will ask them for the API endpoints and private keys of those endpoints, in order to represent wallet balances. It also provides endpoints for these balances, which a mobile wallet (for example) might be able to poll. All the interfaces (both customer and Fund Manager) must be built custom by the Central Banker. 

Once up and running the Central Banker must recruit entrepreneurial Fund Managers who want to join the platform. Once he has gotten a Fund Managers to agree to raise a fund under his VMF, the new Fund Manager may do this by running the Fund Daemon and instantiating a new fund. This Fund exists on its own blockchain, but is also connected to the Lisa chain started by the Central Bank.

##Specification for Central Bank and Fund Nodes
This CLI node can be deployed on a **Docker instance** (required for ErisDB) and connects to initial peers set by the Ur-Central-Bank, also known as Iterative Instinct, the creators of this project. This architecture is built on the Tendermint protocol with Eris Industries open source tools. 

###Creating a Central Bank
Once you've fired up the Central Bank Daemon on your VPS, it will connect with seed peers at Iterative Instinct and begin a new Lisa chain. Then the CLI node allows fund administrators to setup their fund as follows:
* The new Central Bank will be issued the first Lisa wallet address.  
* Next, the fund manager must enter his information. This Lisa address will turn into a Fund Manager object containing attributes: six ethereum addresses from an existing Mist wallet, labeled for the six actively managed tiers A0, A1, A2, R, R0, and R1; full legal name, company, URL, keybase key, address, phone, email, user@handle, SSN/EIN, and image URL
  * Fund manager must then create a password
  * Fund manager must enable two-factor phone number authentication (use Eth proof of phone project?)
  * After this is done, proceed to "the stake pool contract" below.

###Creating a Fund under an existing Central Bank (similar)
Once connected to the network, the CLI node allows fund administrators to setup their fund as follows:
* New fund manager can use the CLI to instantiate a new wallet address on the liquid-tier chain (nickname: Lisa chain) which is the chain shared by all funds. *The Central Bank is responsible for creating a mobile wallet app to hold its Lisa coins. Lisa coins are not transferrable between VMFs. People doing business with strangers outside their VMF should transact in ether, bitcoin, monero, or another public chain coin.*
  * Next, the fund manager must enter his KYC information. This Lisa address will turn into a Fund Manager object containing attributes: six ethereum addresses from an existing Mist wallet, labeled for the six actively managed tiers A0, A1, A2, R, R0, and R1; full legal name, company, URL, keybase key, address, phone, email, user@handle, SSN/EIN, and image URL
  * Fund manager must then create a password
  * Fund manager must enable two-factor phone number authentication (use Eth proof of phone project?)
  * After this is done, proceed to "the stake pool contract" below.

###Sending ether to the stake pool contract
In order to launch a Central Bank or a new Fund, you'll need to add collateral (ETH) to to a stake pool contract. This is to protect the price of Lisa in the event that your fund collapses while it has LX and/or Lisa coins backed by its assets in circulation amongst other funds. The amount of this stake in ETH should be equivalent to $10,000 USD minimum or 10 percent of fund assets AUM in ETH (whichever is more) to be held in escrow contract as stake (fully refundable). Contact partners@iterativeinstinct.com for more information on staking, and to get the stake pool contract address for the Iterative Instinct VMF.

###For Central Banks: get your wallets
Once your stake is received, assuming it is the appropriate amount, your Central Bank daemon will generate seven wallet addresses (A0, A1, A2, R, R0, R1, and LX) and associate them with the Lisa wallet address created for this new Central Bank just a minute ago. These addresses are now all part of the new Central Bank Manager object, sitting on the Central Bank's own A/R tier chain. As Funds join your VMF, wallet addresses for their LX coin will be added to your Central Bank Manager object attributes. Now go out and recruit some Funds on your platform!

###Getting people into your economy
Whether you started a Central Bank or a Fund in an existing VMF, you may enlist up to 250 wallet-address holders to join your platform. For Funds, this means 250 humans, which in VMF terms are known as "member-investors." For Central Banks, this means up to 250 Funds. 

For Central Banks, this process is passive. Go out and speak to asset managers you like and respect, and encourage them to download the Fund daemon and get started. Once they have, you'll see their request, and you may approve it once they've sent in stake.

###For Funds: request permission from your Central Bank
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

###How Funds onboard member-investors
First, get their mobile phone numbers, and give them back a password. 
* To invite a new member-investor to the system, use the CLI to create a new user associated with the person's phone number (eg., `new.user = 2123002020`). Then generate a temporary passcode for each phone number (account) and give it to the person by hand, on paper. 
* Tell the new member-investor to download the Flux mobile app. The app will auto-generate an Lisa wallet address for them
 * New member-investors must etner *matching phone number and temporary password* to the invitation. Phone verification security code involved; reset password to something user sets. Rest of mobile app spec is in another doc in this repo.
 * With the app, member-investors send a zero-coin transaction to Fund Manager's Lisa address from their new Lisa address to request membership. This is done in person, with QR codes.
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
Whatever business activities are creating your profits, rank them by riskiness into one of the categories in the tables laid out in the sections above. Then decide what percentage of your total funding will go to each activity; that is, what mixture of coins you'd like to issue. Some people may only issue one tier of coins, while others will be active in all six tiers.

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

###Impact
Modern fiat instruments, and the banks that hold them, make for poor long-term savings vehicles. Professional wealth management is not available to most people. The Fund model allows groups of individuals to hedge their salaried work in the “mainstream economy” by saving their earnings in an alternative system that is disconnected from bank woes and currency manipulation. **More importantly, it allows brands, schools, non-profits, developing governments, and other small organizations to offer safe, cheap, and transparent financial services to their members.**

####The 250 entity limit
If 250 investors sounds like a tiny bank or fund by present day standards, consider that the account-to-human ratio is about to reverse. That is to say: today, banks require *at least* one account per customer. In fact, many customers have several accounts with one bank (savings, checking, money market, business checking, and so on) which all represent different lines of business for the bank: different departments. In a VMF, it's much more likely that family members (parents and kids; spouses; entire families) will all operate inside the same VMF for simplicty's sake (ie., they can pay each other in the same Lisa coin). 

Consider also that, for legal reasons, initial deposits into a Fund must be made in ETH, which most people are not carrying around each day. One family member or friend can give a relative USD to invest in one big ETH purchase without fear they won't see their money come back -- simply by creating a smart contract denominated in Lisa coins in which the relative pays them out an evenly-divisble balance over `i` payments in a loop where `p` equals the principle `for (i = 0; i > (p / i); i--);`. Such contracts will be available off the shelf in the mobile wallet app. This one is called an "annuity contract." For more common contracts, see the Member-Investor node spec document in this Github project.

With such a smart contract, family trust issues are removed, and they can each funnel dollars to the Fund Manager through the same "head of household" who buys the ETH outright. 

#Licensing Fees
Generally speaking, the VMF project is shockingly cheap to deploy for everyone involved, even not considering the unspeakable waste of existing banks that serves as comparison. However, there are fees to maintain and further the development of this software, and to meagerly enrich its creators.

In a given VMF, each Fund pays an annual tithing to the Central Bank to the tune of **0.009** percent per annum of a moving average of AUM **payable in ETH only.** This payment is remitted in 12 intallments, or monthly, each year. Payment is made manually by Fund Managers -- it is not auto-deducted.  

For other VMFs licensing this software to operate as their own Central Banks, a licensing fee of **4.4** percent of their total fee haul per annum, to be paid to Iterative Instinct (the Ur-bank) in 12 installments and **also remitted in ETH.**

Fund Managers and Central Bankers may use our Flux Trade level 2 tool to manage their positions. This tool introduces a **0.01** percent fee per trade, per exchange.
