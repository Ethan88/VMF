
# Member-Investor Node
## Underpins the Flux Mobile Wallet app
**Functional spec**
This mobile application runs a full Flux node on a smartphone
* Even logged out, members can create a Lisa wallet address with zero balance and **receive** Lisa, which they can then send to others.
* User can SEND, RECEIVE, and REQUEST funds from anyone in their wallet address book using QR codes (no address book if logged out; QR code scan only)


Depositing Funds
 1. View the six ETH wallet addresses for this fund, and send in your Ether
 2. Get coins in your new Flux wallet, hooray (this is the Fund Exchange Contract in action)
 
 NOTES
 
 LOGGED OUT
 Opening screen
 * Generate seed, mnemonic, back it up, etc
 * Generate Lisa wallet address and private key
 * Backup/restore flow TBD
 * View Lisa Balance and QR code
  * Send (QR)
  * Receive (QR)
  * My Transaction Log
  * Automated Payments (QR with contracts)
    * Annuity contract between 1:n addresses
    * Escrow (ie., sale & transfer of goods) contract
    * Recurring remittance * Verify phone number... (next user flow)
 
 VERIFICATION
 * User may "log in" by entering their phone number and temporary password they got from the fund manager in person. Then they get a confirmation code by SMS. The user must then reset the password to something they choose.
  * Once code is entered, this brings up all their funds and wallets to which this phone number is associated. 
  * Check for KYC info and 2FA; if either are absent, prompt user to finish filling out "passport" KYC info and turn on 2FA

LOGGED IN
* Complete Keybase verification flow
* Fund list breakout with Balances for each Fund you're in
  * View each Fund's performance all seven tiers over time
  * View total fund holdings
  * View, sort, and search all fund transsactions over time
* Passport info, Wallets and Balances for each wallet address
  * View performance of your specific holdings over time
* [Same Automatic Payments as Logged Out user, see above]
* My Transaction Log
* My Contacts
* Send (QR and Contact Book)
* Receive (QR and Contact Book)
* Request (QR and Contact Book)
* Write Check (1:n)
* Get Cash (Lisa withdrawl; this uses A/R --> LX contract; then LX --> Lisa contract)
* Deposit ETH (this shows the six addresses of your fund, for each risk tier)
* Savings Account (LX wallet)
* Misc. Settings 
 * Account transfer (multi-sig required, including fund managers and two random member-investors, who must personally verify individual's desire to transfer account to a new owner).
