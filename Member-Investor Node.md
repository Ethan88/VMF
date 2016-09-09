
# Member-Investor Node
## Underpins the Flux Mobile Wallet app
This app is intended for two groups of users. The first, logged-out users, may just want to create a Lisa wallet to receive (and hold, and send) some Lisa coins from a friend. Logged in users have access to all their Iterative Instinct investments, marked to market in 1-second intervals (ie., the blocktime of the Tendermint consensus engine).

### Functional Spec
* Runs a full Lisa chain & A/R chain nodes on a smartphone
* Even logged out, members can create a Lisa wallet address with zero balance and **receive** Lisa, which they can then send to others.
 
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
  * NB that KYC info includes an ETH address, full legal name, company, URL, keybase key, address, phone, email, user@handle, SSN/EIN, and image URL.

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
* Deposit ETH. Be sure to deposit ETH only from the address you added to your profile during signup.
 * (This view shows the six QR codes for the six ETH addresses of your fund, representing each risk tier)
 * The six QR codes are labeled A0, A1, A2, R, R0, and R1.
 * Once ETH is deposited in once of these QR codes, 
* Savings Account (LX wallet)
* Misc. Settings 
 * Account transfer (multi-sig required, including fund managers and two random member-investors, who must personally verify individual's desire to transfer account to a new owner).
