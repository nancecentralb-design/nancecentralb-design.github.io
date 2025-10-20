# ❓ FAQ

Find answers to common questions about Binance Central Bank.

## General Questions

<details>

<summary>Was there an IDO or presale?</summary>

BCB had no premine, IDO, ICO, VC allocation, or presale. All tokens are earned through participation in the protocol. This ensures fair distribution and aligns incentives between the team and community.

</details>

<details>

<summary>What prevents Flash Loan attacks?</summary>

Our 2-step minting and redemption mechanism requires separate transactions, making flash loan attacks impossible. Flash loans must be repaid within the same transaction they're borrowed, so attackers can't complete the two-step process needed to mint or redeem tokens.

Learn more in our [Flash Loan Protection](broken-reference) documentation.

</details>

<details>

<summary>Is the protocol audited?</summary>

Yes, our smart contracts have undergone professional security audits. We also maintain an active bug bounty program to continuously improve security. Check our website for current audit reports.

</details>

<details>

<summary>What chains is the protocol deployed on?</summary>

Currently, Binance Central Bank Protocol is deployed on Binance Smart Chain (BSC). We plan to expand to additional L1 ecosystems in the future as we introduce new synthetic assets.

</details>

## Minting & Redeeming

<details>

<summary>I minted xBNB with only BNB but CR was 90%. How?</summary>

The protocol automatically purchases the required BCB from the market using part of your BNB through the Zap feature. This provides a seamless user experience - you don't need to manually acquire BCB before minting.\
\
Step&#x73;**:**&#x20;

1. Provide BNB: you provide 1 BNB.

2) Automatic swap: Protocol automatically swaps (1 - CR) worth to BCB.&#x20;
3) Mint: Protocol mints BNBx using the correct ratio.

</details>

<details>

<summary>How do I redeem xBNB back to BNB?</summary>

You can redeem BNBX anytime through our redemption page. The amount you receive depends on the current Collateral Ratio.

**Example:** At 95% CR, redeeming 100 BNBX returns:

* 95 BNB
* 5 BNB worth of BCB

The redemption is a two-step process for security.

</details>

<details>

<summary>Why does redemption return both BNB and B4NK?</summary>

xBNB is backed by both BNB and B4NK based on the current Collateral Ratio. When you redeem, you receive both types of collateral in the same proportion that backs your xBNB.

If you want only BNB, you can sell the B4NK portion on a DEX after redemption.

</details>

<details>

<summary>Can I cancel a mint or redemption after Step 1?</summary>

No, once you've completed Step 1, you must complete Step 2 to receive your tokens or collateral. This is a security feature to prevent flash loan attacks. However, there's no time limit - you can complete Step 2 whenever you're ready.

</details>

<details>

<summary>What are the fees for minting and redeeming?</summary>

* **Minting Fee**: 0.50% of minted value
* **Redeeming Fee**: 0.50% of redeemed value

All fees are distributed to BCB stakers and lockers, creating value for protocol participants.

</details>

## Farming & Rewards

<details>

<summary>Where are my claimed farming rewards?</summary>

After claiming farm rewards, they automatically enter an 8-week vesting period. You can view them under "BCB in Vesting" on the Staking tab.

Important: Vesting BCB counts as staked and earns BNB platform fees during the vesting period.

</details>

<details>

<summary>Can I access rewards before 8 weeks?</summary>

Yes, but with a 50% penalty. You have two options:

* **Wait 8 weeks**: Receive 100% of your rewards
* **Claim early**: Receive 50% immediately, forfeit 50%

The 50% penalty is distributed to locked BCB holders as additional rewards.

</details>

<details>

<summary>Do vesting tokens earn rewards?</summary>

Yes! Vesting BCB automatically counts as staked and earns BNB platform fees. This means you're earning rewards on your rewards while they vest.

</details>

<details>

<summary>Are there deposit fees on farms?</summary>

No, there are no deposit fees on any of our farms. You can stake and unstake your LP tokens freely. The only protocol fees are on minting (0.50%) and redeeming (0.50%) BNBX.

</details>

<details>

<summary>How often are farm rewards distributed?</summary>

Farm rewards accumulate in real-time based on your share of the pool. You can claim them at any time, though they will enter the 8-week vesting period upon claiming.

</details>

<details>

<summary>What is impermanent loss and how does it affect me?</summary>

**BNBX/BNB Pool:** Minimal impermanent loss since BNBX maintains a 1:1 peg with BNB. This behaves similarly to a stablecoin pair.

**BCB/BNB Pool:** Standard impermanent loss risk since BCB price can fluctuate independently of BNB. However, farm rewards are designed to offset this risk.

</details>

## Staking & Locking

<details>

<summary>Why lock B4NK tokens?</summary>

Locked BCB earns additional rewards compared to staking:

* **Staking:** Earns BNB platform fees only
* **Locking:** Earns BNB platform fees PLUS BCB penalty fees

The 8-week lock commitment is rewarded with higher APR from the additional BCB revenue stream.

</details>

<details>

<summary>Can I unlock my B4NK early?</summary>

No, locked BCB cannot be withdrawn before the 8-week period ends. This is by design to ensure stability and reward long-term holders. Make sure you're comfortable with the lock duration before locking.

</details>

<details>

<summary>What happens to my staked B4NK during vesting?</summary>

Vesting BCB is automatically considered staked, so it earns BNB platform fees during the entire vesting period. You don't need to take any action - it happens automatically.

</details>

<details>

<summary>Can I have both staked and locked B4NK?</summary>

Yes! You can split your BCB holdings between:

* Some tokens staked (flexible, lower rewards)
* Some tokens locked (8 weeks, higher rewards)
* Some tokens in farms (earning emissions)

This allows you to balance liquidity needs with reward optimization.

</details>

<details>

<summary>When do I receive my staking/locking rewards?</summary>

Rewards are distributed at the end of each 7-day epoch (Monday to Sunday). After an epoch ends, rewards become available for claiming in the following epoch.

</details>

## Technical Issues

<details>

<summary>Ledger + Metamask mint issue?</summary>

If you're experiencing issues minting with Ledger + Metamask, enable "Display Contract Data (debug data)" in your Ledger device settings.

Open Ledger appOpen Binance Smart Chain app on Ledger.Go to SettingsGo to Settings.Enable display contract dataEnable "Display Contract Data".RetryTry minting again.

This resolves the "blind signing" error that some users encounter.

</details>

<details>

<summary>Transaction failed - what happened to my funds?</summary>

If a transaction fails:

* Your funds are safe and remain in your wallet
* You only lose the gas fee for the failed transaction
* Check error messages for details
* Common issues: insufficient gas, slippage too low, insufficient balance

If you completed Step 1 of minting/redeeming but Step 2 failed, your collateral is safely held in the contract. Simply retry Step 2.

</details>

<details>

<summary>Why is my transaction pending so long?</summary>

BSC transaction times depend on network congestion and gas price:

* **Low gas price:** Slower confirmation (5-30 seconds typical)
* **Standard gas price:** Normal confirmation (3-5 seconds typical)
* **High gas price:** Fast confirmation (1-3 seconds typical)

If stuck for more than 2 minutes, the transaction may have failed. Check BSCScan using your transaction hash.

</details>

<details>

<summary>How do I check my transaction status?</summary>

Copy tx hashCopy your transaction hash from Metamask.Visit BSCScanVisit BSCScan.com.Paste and searchPaste transaction hash in search.View statusView status: Success, Failed, or Pending.

You can also click on transaction notifications in Metamask to open BSCScan directly.

</details>

## Tokenomics & Economics

<details>

<summary>What happens to B4NK during minting and redeeming?</summary>

**During Minting:**

* BCB portion of collateral is burned
* Removes BCB from circulation
* Creates deflationary pressure when protocol grows

**During Redeeming:**

* New BCB is minted to return as collateral
* Adds BCB to circulation
* Creates inflationary pressure when protocol contracts

This dynamic supply mechanism balances BCB supply with protocol usage.

</details>

<details>

<summary>How does the Collateral Ratio affect my returns?</summary>

CR affects returns in several ways:

**Lower CR (e.g., 75%):**

* More BCB required for minting → Higher BCB demand
* Less BNB returned when redeeming → More BCB exposure
* Potentially better for BCB bulls

**Higher CR (e.g., 95%):**

* More BNB required for minting → Lower BCB demand
* More BNB returned when redeeming → Less BCB exposure
* Potentially better for BNB maxis

The CR adjusts automatically based on BNBX price, so you don't need to time it manually.

</details>

<details>

<summary>Where does the yield come from?</summary>

Protocol yield comes from multiple sources:

* **Minting fees (0.50%)** → Stakers and lockers
* **Redeeming fees (0.50%)** → Stakers and lockers
* **Early exit penalties (50%)** → Lockers only
* **Farm emissions** → Liquidity providers

All yield is generated from real protocol activity and user interactions.

</details>

## Safety & Security

<details>

<summary>Is my collateral safe when minting xBNB?</summary>

Yes, your collateral is secured in audited smart contracts. The two-step minting process and flash loan protection ensure that collateral can only be accessed through legitimate redemptions.

Key safety features:

* Time-locked collateral
* Flash loan protection
* Professional audits
* Bug bounty program
* Battle-tested mechanisms

</details>

<details>

<summary>What if the protocol gets hacked?</summary>

We've implemented multiple security measures:

* Battle Tested Contracts
* Flash loan protection mechanisms
* Two-step transaction processes
* Active bug bounty program ($50,000)
* Continuous security monitoring

While no protocol can guarantee 100% safety, we've implemented industry best practices to minimize risks.

</details>

<details>

<summary>Can the team rug pull?</summary>

No. The protocol is designed to be decentralised:

* No premine or team allocation
* Smart contracts are immutable for core functions
* Governance is controlled by BCB holders
* All fees go directly to users, not team
* Time-locked admin functions where needed

</details>

## Still Have Questions?

Can't find the answer you're looking for?

* Join our community channels
* Check our [documentation](broken-reference)
* Contact our [support team](broken-reference)

***

_Last Updated: October 2025_
