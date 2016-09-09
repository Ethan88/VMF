#Voluntary Monetary Fund
##Open source platform for transparent investment vehicles arranged in a nested hierarchy
By joining a VMF platform, you can launch a transparent blockchain-based investment fund in just a few lines of code, with no fees and near-zero overhead. Inter-fund transactions are governed by a fair central bank. For this instance, Iterative Instinct is the central bank; however this software may be licensed to other institutions anywhere in the world who would like to serve in this role. 
###Minimum requirements:
* one (1) intermediate-level coder to deploy the project
* one (1) professional asset manager to run it
* a cheap cloud VPS running a Docker instance
* a community of friends, family, or customers that are willing to invest in you
* six Ethereum addresses

**Introduction:** In essence, this project is a cheap and simple open-source kit for a multi-purpose investment fund made transparent and immutable with underlying blockchain technology. A fund instantiated on this network is not architected to scale to city- or state-size, but rather is intended to support a hard-coded limit of 250 investor-members. The returns from this 250-investor fund are used to back several tiers of bespoke currencies which, like shares, appreciate to reflect the performance of fund management. As more funds are join the platform, these currencies will become the basis for economic activites between fund managers and between member-investors. There are a maximum of 250 funds per VMF network and per central bank, bringing the maximum number of humans in the network to around 62,000.

###Target audience
Both the "parent" central bank daemon (ie., the VMF platform as a whole) and individual "child" Fund daemon are designed to be deployable by anyone with command-line experience, cloud servers, and a little financial know-how.  At first, we expect it will be run by existing brands and membership clubs, replacing rewards systems that use "points" or "miles" with more professionalized financial services. Solo asset managers may also raise and operate various kinds of investment funds using this software. 

###Project Goals
Encourage communities of people to save and grow their money together. 

###Governance
Architected with private business in mind, this system has no governance apparatus for changing itself (i.e., there is no voting, elections, or DAO mechanics). Participation in a given Fund or network of Funds is private, voluntary, and non-exclusive. It is purely an economic system which leaves governance up to the community and the fund managers. Zero data is available to those outside the fund, but member-investors get full visibility into all activity inside their Fund. The central bank may look at all blockchains but cannot move assets on any of them. 

###Approach
Many cryptocurrency maximalists have attempted to build “trustless” global systems where software can somehow isolate bad actors. This belies the natural fact that trust between small groups of humans is foundational to civilization, and that moral hazard cannot be “engineered away.” 

###Solution
The VMF concept proposes a three-level hierarchy for a community monetary "fund of funds" which uses financial and social incentives, as well as immutable ledgers, to keep members and managers honest.

###How it works
The Fund Manager has one basic job: to incorporate citizens into their Fund by issuing them a wallet address. This is the primary responsibility of the managers of a given Fund: to choose who can be in it. Secondarily, they manage the money of those who enter the Fund.

###Management powers
In addition to admitting members, the managers are in charge of active management of their portfolio. They are incentivized to hold and grow the value of the coins they issue in various ways. Fund managers may diversify holdings by trading coins with another Fund community on behalf of their members out of a common pool by incorporating another Fund as a citizen (ie., issuing the outside group a single wallet address). However, inside a Fund it is strictly a one-person, one-wallet address system.

###Trust
When joining a Fund, think of the TSA rules: never let a stranger pack your financial bags. Entering a VMF means you're entrusting value to a human manager who will have freedom to invest as they see fit. If his or her skills as a market-maker are sub-par in the mainstream economy, a Fund will simply lose their money faster. This is a kit for knowledgeable asset managers.

###Impact
Modern fiat instruments, and the banks that hold them, make for poor long-term savings vehicles. Professional wealth management is not available to most people. The Fund model allows groups of individuals to hedge their salaried work in the “mainstream economy” by saving their earnings in an alternative system that is disconnected from bank woes and currency manipulation. More importantly, it allows brands, schools, non-profits, and other small organizations to offer safe, cheap, and transparent financial services to their members.

###Crowdfunding your Fund
* In the Untied States, anybody who has registered a private placement with the SEC under regulation D may crowdsale their VMF in USD from accredited investors (ie., what we did). *With this option, your investors may not withdraw their funds for the length of the fund, essentially behaving like a market-linked certificate of deposit.*
* Anyone can begin a VMF without SEC registration if they raise crowdsale funds paid in BTC, ETC, ETH, or other coins. *The competition amongst unlicensed VMFs will be especially sharp with zero investor lockup!*
* Be sure to comply with local laws when deploying this project outside the US.

#Software components
0. Central bank node daemon overseeing a VMF network (it has admin/root permissions)
1. Fund node daemon which can instantiate and administer a child Fund (roll our own with Eris Industries tools)
2. Wallet mobile application (iOS/Android)
3. Fund management web interface that our central bank, i2, built for our particular VMF (Flux Trade)
 
In the VMF platform architecture, there is one main chain shared by all funds in the network. This is the liquid tier chain, also known as the L-tier chain or Lisa chain. This chain is generated by the central bank, in this case Iterative Instinct. The central bank is also responsible for building a mobile wallet for its ecosystem, and building a Fund Admin iterface. They may also tell their fund managers to use Flux Trade and Flux wallet applications, if they are unwilling to build their own; however, they must host instances of these applications themselves.

All Iterative Instinct applications (such as the Flux mobile wallet for member-investors, the Flux CLI daemon/node for fund managers, and the Flux trade web app) run nodes on the main Lisa chain that connects every fund in this VMF network run by i2. However, each fund has its own chain which is private and permissioned to their member-investors. This chain runs on the fund's Docker nodes, as well as on the wallet mobile apps of their members, as well as on some central bank nodes owned by Iterative Instinct.

##Specification for Fund node daemon ("Flux node")
This CLI node can be deployed on a **Docker instance** (required for ErisDB) and connects to our initial peers at Iterative Instinct. 

###Creating a fund
Once connected to the network, the CLI node allows fund administrators to setup their fund as follows:
* New fund manager can use the CLI to instantiate a new wallet address on the liquid-tier chain (nickname: Lisa chain) which is shared by all funds. Anyone on earth may obtain a Lisa wallet address with the Flux mobile app. 
  * Next, the fund manager must enter his information. This Lisa address will turn into a Fund Manager object containing attributes: six ethereum addresses from an existing Mist wallet, labeled for the six actively managed tiers A0, A1, A2, R, R0, and R1; plus name, company, URL, keybase key, address, phone, email, user@handle, SSN/EIN, and image URL
  * Fund manager must then create a password
  * Fund manager must enable two-factor phone number authentication (use Eth proof of phone project?)

###Requesting permission from central bank
Now with a Lisa-chain wallet address, fund manager may send a zero-coin transaction to Iterative Instinct's central bank Lisa address, which indicates a request to start a new fund.
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

#Fund composition and coin issuance
Now that you have a fund and some investors, you'll need to take their money and give them back shares in your fund. These shares are represented by coins: the six actively managed tiers, corresponding with the types of wallet addresess you created: A0, A1, A2, R, R0, and R1. There are seven different kinds of coins for each fund, each representing a different level of risk. (The seventh, LX..., represents an average of the value of all.) 

As a fund manager, you may issue whatever combination number and type of coins you like right in the command line, representing whatever business activity you like for each tier -- just remember to sort them by risk. LX coins are held in contract, and exchangeable only for underlying A/R coins (See the table below, and contract details further down.)

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
    <td>Lx0...</td>
    <td>Stable-coin specific to this fund, and redeemable for the above tiers. Gets its value from the sum total basket average. Value shown in Lisa.</td>
    <td>Risk average of entire fund</td>
  </tr>
  <tr>
    <td>Lisa</td>
    <td>Stable-coin usable across all the L-chain which connects all funds in this VMF instance. Value pegged to XDR.</td>
    <td>Low</td>
  </tr>
</table>

####Note on fungibility
Funds cannot exchange A0, A1, A2, R, R0, and R1 coins with one another. Because each fund's chain is not connected to any other, the only way that funds may do business is by trading their Lx0... instrument for a Lisa coin, and then doing a transacton in Lisa. The Lisa coin is the lingua franca in a given VMF platform network, and its value is pegged to the XDR; thus 100 lisa = 100 xdr. Central banks may not do business with one another except by trading with each other in underlying assets. **Lisa chains are not connected.**

###Take investment
Once the Fund Manager has decided which tiers to issue, he must next decide how many to issue at each tier. The total number of coins issued at all tiers must equal at least 20,000 and at most 999,999,999. What number you choose really comes down to the ETH amount you plan to raise, since people don't like using tiny decimals. In the CLI, the Fund Manager:
  * Enters proportion of coins for each tier (out of 100 percent)
  * Enters the size of the total coin pool (at least 20,000)
  * Enters the face value of each coin in ETH (same value for all)
  * "Fundraising exchange" contact address is generated
   * This contract listens for deposits in your six ethereum addresses labeled A0, A1, A2, R, R0, and R1 and returns a message over RPC to look for the txn.sender address among the member-investor objects
    * If/when found, give the appropriate amount of coins from that tier to that member-investor

#The Central Bank
VMF structure is loosely modeled on the IMF, its [Special Drawing Rights](https://en.wikipedia.org/wiki/Special_drawing_rights) basket, and its XDR instrument. The model has been modified to suit a different purpose: stable appreciation, rather than just *prima facie* stability. This new model creates many of the benefits of the Petrodollar (debts shrink; savings grow) without the (quantitative) inflation and subsequent price inflation in the small business arena. Transparency in all ways is what makes this whole thing work, hence the blockchain (ie., immutability as a backstop for fund managers). We believe it is the ultimate safe haven network. 

## Elements of the Central Bank role versus Fund Manager role
* Structured like the other funds, in six tiers, the Central Bank (parent fund) has six of its own wallet addresses for its own A0, A1, A2, R, R0, and R1 activities. These obey the same rules as all other funds (the 250-address limit, for example, limits every central bank to 250 funds, just as every fund is limited to 250 members). 
* It also has its own LX coin representing the average value of its other tiers, and may issue its LX... addresses to other funds, just like any other fund.
### The Fund LX Exchange Contract
All funds in a VMF, including the central bank, have their own LX Exchange Contract. This contract address receives A/R tier coins from their own Fund investors, holds it in escrow, and lends out that fund's LX coins for the sender to use and circulate within the Fund (or to any external group that has been given a fund address by this Fund's manager.) 

## How the central bank (parent fund) is different
The central bank does two things:
 1. Initializes the **Lisa Exchange Contract.** At the genesis of a VMF, the parent fund (central bank) issues a hard-coded number of 100,000,000 Lisa, which is held 100 percent in an "exchange contract" and tradeable for each fund's LX, plus 100 percent collateral in R-tier coins.
  * This exchange contract address is available to the entire Lisa chain, even the central bank itself
  * Upon receiving LX from any one of the 250 funds in its network, this contract sends back the equivalent amount of Lisa and holds that fund's LX in escrow
   * If the value of the Fund's LX coins decrease against the Lisa while they are held in contract, the amount is debited from the R-tier collateral and held by the contract; if the value of the fund's LX goes up against the Lisa, the amount is credited back.

####Notes
* Fund managers may issue other funds wallet addresses with same info above
* Central bank will need to deploy a bunch of its own Docker instances for seeds (initial peers to connect to. e.g. "addr1:46656,addr2:46656") to secure the Lisa chain, and secure all 250 fund chains

#Member-investor wallet & blockchain explorer mobile application (Nickname: "Flux wallet")
* Runs a full node on a smartphone
For each Fund a member-investor joins....
* Get a text invitation to join a fund; download Flux wallet and confirm number
 1. Enter KYC info; create password; turn on 2FA
 2. View the six ETH wallet addresses for this fund, and send in your Ether
 3. Get coins in your new Flux wallet, hooray
* User’s profile contains: 7 wallet addresses per fund; name, photo, @handle, keybase, website, address, SSN, EIN, and all other KYC information 
* Reputation system t.b.d.
* User can see a dashboard for all his or her Fund, and their performance
 * For each Fund user is member-investor in, they can view
  * View all 7 tier coin prices change for this fund last 1h, 3h, 6h, 12h, 1d, 3d, 7d, 10d, 14d, 21d, 1m, 3m, 6m, 9m, 1y, 2y, 3y (...) and YTD. 
* User can see blockchain explorer for each Fund they’re a member of
* User can use contracts
 * Convert A/R coins to LX using the Fund LX Exchange Contract; the A/R coins are held in escrow
 * Convert LX coins to Lisa using the central bank's Lisa Exchange Contract
* User can enter a chat room with other Fund members (use ethTweet?)

#Flux Trade
