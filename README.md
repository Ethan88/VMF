#Voluntary Monetary Fund
##Open source platform for transparent investment vehicles arranged in a nested hierarchy
By joining the VMF platform, you can launch a transparent blockchain-based investment fund in just a few lines of code, with no fees and near-zero overhead. Intra- and inter-VMF transactions are governed by a fair central bank. For this instance, Iterative Instinct is the central bank; however this software may be licensed to other institutions who would like to serve in this role. 
###Minimum requirements:
* one (1) entry-level coder to deploy the project
* one (1) professional asset manager to run it
* a cheap cloud VPS running a Docker instance
* a community of friends, family, or customers that are willing to invest in you
* six Ethereum addresses

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
0. Central bank node daemon overseeing a VMF network (it has admin/root permissions)
1. Fund node daemon which can instantiate and administer a child Fund (roll our own with Eris Industries tools)
2. Wallet mobile application (iOS/Android)
3. The central Lisa chain to which all VMFs under this central bank connect
 
In the VMF platform architecture, there is one main chain shared by all funds in the network. This is the liquid tier chain, also known as the L-tier chain or Lisa chain. This chain is generated by the central bank, in this case Iterative Instinct. All Iterative Instinct applications (such as the Flux mobile wallet for member-investors, the Flux CLI daemon/node for fund managers, and the Flux trade web app) all run nodes on the Lisa chain. However, each fund has its own chain which is private and permissioned to their member-investors. This chain runs on the fund's Docker nodes, as well as on the wallet mobile apps of their members, as well as on some central bank nodes owned by Iterative Instinct.

##Specification for full node daemon (Nickname "Flux node") deliverable Q4 2016
This CLI node can be deployed on a **Docker instance** (required for ErisDB) and connects to our initial peers at Iterative Instinct. 

###Creating a wallet address with the daemon
Once connected to the network, the CLI node allows fund administrators to setup their fund as follows:
* New fund manager can use the CLI to instantiate a new wallet address on the liquid-tier chain (nickname: Lisa chain) which is shared by all funds
  * Next, the fund manager must enter his information. This Lisa address will turn into a Fund Manager object containing attributes: six ethereum addresses from an existing Mist wallet, labeled for the six actively managed tiers A0, A1, A2, R, R0, and R1; plus name, company, URL, keybase key, address, phone, email, user@handle, SSN/EIN, and image URL
  * Fund manager must then create a password
  * Fund manager must enable two-factor phone number authentication (use Eth proof of phone project?)

###Request permission from i2 "central bank" to start a fund
Now with a Lisa-chain wallet address, fund manager may send a zero-coin transaction to Iterative Instinct's Lisa address, which indicates a request to start a new fund.
  * If rejected, return "rejected; for help email help@iterativeinstinct.com"
  * If this address already submitted, return "already submitted"
  * If request is approved by Iterative Instinct human operators, human operator generates seed peers for one (1) new Fund chain with no wallet addresses. Next, the fund manager's Docker instance connects to this new chain, and generates seven wallet addresses (A0, A1, A2, R, R0, R1, and LX) and associating them with the Lisa wallet address that sent the new fund request. These addresses are now all part of the new Fund Manager object, sitting on the new Fund chain.
    * Next, require the Fund Manager to enter a wallet address -or- API endpoint & key to create price oracles for all six actively managed tiers (A0, A1, A2, R, R0, R1; the value of LX must be auto-calculated.) These wallet addresses and endpoints are required to display fund's balance of positions, crypto and otherwise. (eg., using the Fidelity API or E-Trade API)
     * Return "successfully started your chain and created your wallet! Please backup your keys."
     * Return also fund manager's seven new Fund Chain wallet addresses, six of which are associated with the ethereum addresses he entered earlier; and remind him his Lisa address
  * Private keys for all Fund manager wallet addresses are held on Fund Manager's Docker server which requested them (as per ErisDB)
  * End of fund setup process!

###Getting Investors
Now that your chains are up and running, you may enlist up to 250 member-investors. First, get their mobile phone numbers.
* To invite a new member-investor to the system, use the CLI to create a new user associated with the person's phone number (eg., `new.user = 2123002020`)
* Tell the new member-investor to download the Flux mobile app. The app will auto-generate an L-tier wallet address for them
 * New member-investors must add KYC information and *matching phone number* to the invitation. Phone verification security code involved; rest of mobile app spec is below)
 * With the app, member-investors send a zero-coin transaction to Fund Manager's Lisa address from their new Lisa address to request membership
    * If waitlisted, return "waitlist"
    * If rejected, return "rejected"
    * If accepted by fund managers, instantiate A0, A1, A2, R, R0, R1, and LX wallet addresses on the Fund chain, and associate them with the Lisa wallet address that made the request, along with the KYC info the member-investor entered. These are the attributes of the "Member-Investor object." 
     * Save the private keys for this users 7 addresses to the member-investor's mobile device.
     * Tell them to back up their damn private keys

#Fund composition and coin issuance
Now that you have a fund and some investors, you'll need to take their money and give them back shares in your fund. These shares are represented by coins: the six actively managed tiers, corresponding with the types of wallet addresess you created: A0, A1, A2, R, R0, and R1. There are seven different kinds of coins for each fund, each representing a different level of risk. (The seventh, LX..., represents an average of the value of all.) As a fund manager, you may issue whatever combination number and type of coins you like, representing whatever business activity you like for each tier -- as long as you sort them by risk. LX coins are held in contract, and exchangeable only for underlying A/R coins (See the table below.)

##Choose your fund's risk profile
Consult the tables below. Whatever business activities are creating your profits, rank them by riskiness into one of the categories below. Then decide what percentage of your total funding will go to each activity; that is, what mixture of coins you'd like to issue. Some people may only issue one tier of coins, while others will be active in all six tiers.

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
     <td>Lisa</td>
    <td>Stable-coin usable across all the L-chain which connects all funds in this VMF instance. Value pegged to XDR.</td>
    <td>Low</td>
  </tr>
</table>

####Note on fungibility
Funds cannot exchange A0, A1, A2, R, R0, and R1 coins with one another. Because each fund's chain is not connected to any other, the only way that funds may do business is by trading their Lx0... instrument for a Lisa coin, and then doing busines in Lisa. The Lisa coin is the lingua franca in the VMF platform network, and its value is pegged to the XDR; thus 100 lisa = 100 xdr. Central banks may not do business with one another. **Lisa chains are not connected.**

###Take investment
Once the Fund Manager has decided which tiers to issue, he must next decide how many to issue at each tier. The total number of coins issued at all tiers must equal at least 20,000 and at most 999,999,999. What number you choose really comes down to the ETH amount you plan to raise, since people don't like using tiny decimals. In the CLI:
  * Enters proportion of coins for each tier (out of 100 percent)
  * Enters the size of the total coin pool (at least 20,000)
  * Enters the face value of each coin in ETH (same value for all)
  * "Fundraising exchange" contact address is generated
   * This contract listens for deposits in your six ethereum addresses labeled A0, A1, A2, R, R0, and R1 and returns a message over RPC to look for the txn.sender address among the member-investor objects, and if found, give the appropriate amount of coins from that tier to that member-investor

###Taking investment  
Investment should be rendered to you, the Fund Manager, in ETH sent to the same addresses you entered when you created the Fund Manager object. The "Fundraising exchange" contract watches for deposits to this address, from member-investor addresses, and automatically
  * Contract address which accepts ether from a known address and sends back fund coins to that member's wallet


#The Central Bank
From an investor perspective, the purpose of a VMF network of funds is to serve as a high-return safe haven. VMF structure is loosely modeled on the IMF and its [Special Drawing Rights](https://en.wikipedia.org/wiki/Special_drawing_rights) basket and its XDR instrument, but modified to suit a different purpose: stable appreciation, rather than just stability. This creates many of the benefits of the Petrodollar (debts shrink; savings grow) without the (quantitative) inflation and subsequent price inflation in the small business arena. Transparency in all ways is what makes this whole thing work, hence the blockchain (ie., immutability as a backstop for fund managers).

##Elements of the central bank role
* Structured like the other funds, in six tiers, and has six of its own wallet addresses for its own A0, A1, A2, R, R0, and R1 activities. These obey the same rules as all other funds (the 250-address limit, for example, limits every central bank to 250 funds, just as every fund is limited to 250 members). It also has its own Lx... coin representing the average value of its other tiers, and an Lx address for these coins, and may issue its Lx... addresses to other funds, just like any other.
* Also connected to the Lisa chain, like all funds; has its own Lisa address; it must also trade with other funds in Lisa.
* A central bank may transact with another central bank (ie., someone who deployed the project themselves) using ether. 

##How the central bank is different
Besides its obvious privilege and obligation to vet new funds and permit them on the platform, the "parent" fund is unlike child funds in the following ways:
 1. The parent fund holds all 7 wallet addresses for **every single fund** equaling 1,750 wallet addresses for all 250 child funds
 2. The parent fund creates one issuance of 100,000,000 Lisa, held 100 percent in an exchange contract
 3. This exchange contract address is available to the entire Lisa chain
  * When it receives Lisa from a Fund Manager address











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
