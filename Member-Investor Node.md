
# Member-Investor Node
## Underpins the Flux Mobile Wallet app for ANDROID
This app is intended for two groups of users. The first, logged-out users, may just want to create a Lisa wallet to receive (and hold, and send) some Lisa coins from a friend. Logged in users have access to all their Iterative Instinct investments, marked to market in 1-second intervals (ie., the blocktime of the Tendermint consensus engine).

### Functional Spec
* Runs a full Lisa chain & A/R chain nodes on a smartphone
* Even logged out, members can create a Lisa wallet address with zero balance and **receive** Lisa, which they can then send to others.

 ## LOGGED OUT
 Opening screen
 * Generate seed mnemonic (ie., a list of 12 random words the user must write down on paper)
 * Generate Lisa wallet address and private key
 * Backup the private key by downloading it (Android)
 * View Lisa Balance and QR code
  * Send (QR)
  * Receive (QR)
  * My Transaction Log
  * Automated Payments (QR with contracts)
    * Annuity contract between 1:n addresses
    * Escrow (ie., sale & transfer of goods) contract
    * Recurring remittance 
  * Verify phone number... (next user flow)
 
 ## VERIFICATION
 * User may "log in" by entering their phone number and temporary password they got from the fund manager in person. Then they get a confirmation code by SMS. The user must then reset the password to something they choose.
  * Once code is entered, this brings up all their funds and wallets to which this phone number is associated. 
  * Check for KYC info and 2FA; if either are absent, prompt user to finish filling out "passport" KYC info and turn on 2FA
  * NB that KYC info includes an ETH address, full legal name, company, URL, keybase key, address, phone, email, user@handle, SSN/EIN, and image URL.

## LOGGED IN
* Complete Keybase verification flow

## LONG TERM PERFORMANCE TAB
* Fund list breakout with Balances for each Fund you're in
  * View each Fund's performance all seven tiers over time
  * View total fund holdings
  * View, sort, and search all fund transsactions over time
* Passport info, Wallets and Balances for each wallet address
  * View performance of your specific holdings over time

## TRANSACTIONS TAB
* My Transaction Log

## CONTACTS TAB
* List of all my Contacts passport entries
* Save anyone I do a transaction with

## CHECKING TAB
* Write Check to another LX addressholder of this Fund (1:n)
 *  This effectively converts A/R --> LX using contract, and sends the LX to the recipient
 1. Send (QR or select someone from Contact Book)
 2. Receive (QR and Contact Book)
 3. Request (QR and Contact Book)
 4. Automated Payments (QR with contracts)
    * Annuity contract between 1:n addresses
    * Escrow (ie., sale & transfer of goods) contract
    * Recurring remittance ] 

## CASH TAB
* Get Cash in your Lisa wallet (convert LX --> Lisa using contract)
* Show Lisa ("cash") balance in USD and XDR
*  Transfer "cash" from Lisa wallet
 1. Send (QR and Contact Book)
 2. Receive (QR and Contact Book)
 3. Request (QR and Contact Book)
 4. Automated Payments (QR with contracts)
    * Annuity contract between 1:n addresses
    * Escrow (ie., sale & transfer of goods) contract
    * Recurring remittance 
    
## INVEST TAB
Invest view shows the balance/value of the A-tier coins you hold in your three A-wallets (A0, A1, A2) in USD/XDR
* Deposit: this feature involves depositing more ETH into the Fund. Be sure to deposit ETH only from the address you added to your profile during signup.
 * (This view shows the six QR codes for the six ETH addresses of your fund, representing each risk tier)
 * The six QR codes are labeled A0, A1, A2, R, R0, and R1, from top to bottom. Top (A0) is riskiest, bottom (R1) is least risky.
 * Once ETH is deposited in once of these QR codes, a deposit of coins to the corresponding wallet (A0, A1, A2, R, R0, or R1) will occur; user should be notified of this
 
## SAVINGS TAB
Savings Account shows the Rerserve (R-tier) coins you hold in your three R-wallets (R, R0, R1)
 * Show R-tier balance in USD and XDR
 * Transfer from Savings (these four sets of functions appear in several places in the app)
 1. Send (QR and Contact Book)
 2. Receive (QR and Contact Book)
 3. Request (QR and Contact Book)
 4. Automated Payments (QR with contracts)
    * Annuity contract between 1:n addresses
    * Escrow (ie., sale & transfer of goods) contract
    * Recurring remittance 

## SETTINGS 
* Edit Passport --> changes some contact info; some can't be changed/removed (eg., name, phone, an email address) 
* Account transfer (multi-sig required, including fund managers and two random member-investors, who must personally verify individual's desire to transfer account to a new owner).
