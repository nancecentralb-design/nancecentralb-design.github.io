# ↪️ Minting and Redeeming

## Minting & Redeeming

Learn how to mint new xBNB tokens and redeem them back to collateral.

### Minting xBNB

Create new xBNB tokens by depositing collateral based on the current Collateral Ratio.

#### Minting Formula

To mint 1 xBNB:

* **BNB Required**: CR × 1 BNB
* **B4NK Required**: (1 - CR) × 1 BNB worth

#### Example Calculations

{% tabs %}
{% tab title="CR = 90%" %}
**To mint 1 xBNB:**

* BNB needed: 0.90 BNB
* B4NK needed: 0.10 BNB worth of B4NK

**To mint 100 xBNB:**

* BNB needed: 90 BNB
* B4NK needed: 10 BNB worth of B4NK
{% endtab %}

{% tab title="CR = 75%" %}
**To mint 1 xBNB:**

* BNB needed: 0.75 BNB
* B4NK needed: 0.25 BNB worth of B4NK

**To mint 100 xBNB:**

* BNB needed: 75 BNB
* B4NK needed: 25 BNB worth of B4NK
{% endtab %}

{% tab title="CR = 95%" %}
**To mint 1 xBNB:**

* BNB needed: 0.95 BNB
* B4NK needed: 0.05 BNB worth of B4NK

**To mint 100 xBNB:**

* BNB needed: 95 BNB
* B4NK needed: 5 BNB worth of B4NK
{% endtab %}
{% endtabs %}

#### Minting Process

{% stepper %}
{% step %}
#### Check Current CR

View the current Collateral Ratio on the minting page.
{% endstep %}

{% step %}
#### Prepare Collateral

Ensure you have the required amount of BNB and B4NK in your wallet.

{% hint style="info" %}
**Pro Tip**: Use the Zap feature if you only have BNB - it will automatically purchase the required B4NK for you.
{% endhint %}
{% endstep %}

{% step %}
#### Initiate Minting (Transaction #1)

Submit first transaction to deposit collateral and initiate minting.
{% endstep %}

{% step %}
#### Collect xBNB (Transaction #2)

Submit second transaction to collect your newly minted xBNB tokens.
{% endstep %}
{% endstepper %}

#### Minting Fees

* **Fee**: 0.50% of minted value
* **Collected in**: BNB
* **Distributed to**: Staked and locked B4NK holders

#### What Happens to Collateral?

When you mint xBNB:

* **BNB portion**: Held in protocol treasury as collateral
* **B4NK portion**: Burned, removing tokens from circulation

### Redeeming xBNB

Convert your xBNB back to collateral at any time.

#### Redeeming Formula

When redeeming 1 xBNB:

* **BNB Returned**: CR × 1 BNB
* **B4NK Returned**: (1 - CR) × 1 BNB worth

#### Example Calculations

{% tabs %}
{% tab title="CR = 90%" %}
**Redeeming 1 xBNB returns:**

* BNB: 0.90 BNB
* B4NK: 0.10 BNB worth of B4NK

**Redeeming 100 xBNB returns:**

* BNB: 90 BNB
* B4NK: 10 BNB worth of B4NK
{% endtab %}

{% tab title="CR = 75%" %}
**Redeeming 1 BNBX returns:**

* BNB: 0.75 BNB
* BCB: 0.25 BNB worth of BCB

**Redeeming 100 BNBX returns:**

* BNB: 75 BNB
* BCB: 25 BNB worth of BCB
{% endtab %}

{% tab title="CR = 95%" %}
**Redeeming 1 BNBX returns:**

* BNB: 0.95 BNB
* BCB: 0.05 BNB worth of BCB

**Redeeming 100 BNBX returns:**

* BNB: 95 BNB
* BCB: 5 BNB worth of BCB
{% endtab %}
{% endtabs %}

#### Redemption Process

{% stepper %}
{% step %}
#### Check Current CR

View the current Collateral Ratio to know what you'll receive.
{% endstep %}

{% step %}
#### Initiate Redemption (Transaction #1)

Submit first transaction to burn your xBNB and initiate redemption.
{% endstep %}

{% step %}
#### Collect Collateral (Transaction #2)

Submit second transaction to collect your BNB and B4NK collateral.
{% endstep %}
{% endstepper %}

#### Redemption Fees

* **Fee**: 0.50% of redeemed value
* **Collected in**: BNB
* **Distributed to**: Staked and locked B4NK holders

#### What Happens During Redemption?

When you redeem xBNB:

* **xBNB**: Burned, removing tokens from circulation
* **BNB portion**: Released from protocol treasury to you
* **B4NK portion**: Newly minted and sent to you

### Two-Step Security

{% hint style="danger" %}
**Flash Loan Protection**

Both minting and redeeming require two separate transactions. This prevents flash loan attacks since flash loans must be repaid within the same transaction.
{% endhint %}

#### Why Two Steps?

**Security**: Prevents attackers from exploiting the protocol with flash loans

**Time Lock**: Collateral is time-locked between transactions

**User Safety**: Additional confirmation step prevents accidental large transactions

### Frequently Asked Questions

<details>

<summary>Can I mint xBNB with only BNB?</summary>

Yes! Use the Zap feature on the minting page. The protocol will automatically purchase the required B4NK amount from the market using part of your BNB.

</details>

<details>

<summary>How long between the two transactions?</summary>

You can complete the second transaction immediately after the first confirms. There's no required waiting period, but you must complete both transactions.

</details>

<details>

<summary>What if I only complete the first transaction?</summary>

Your collateral will be held in the contract. You can complete the second transaction at any time to collect your minted xBNB or redeemed collateral.

</details>

<details>

<summary>Can I cancel after the first transaction?</summary>

No, once you've completed the first transaction, you must complete the second to receive your tokens. This is a security feature.

</details>

<details>

<summary>Do fees apply to both transactions?</summary>

The 0.50% protocol fee is applied during the first transaction. The second transaction only costs gas fees.

</details>

***

**Next Steps**: Learn about the collateral ratio used in B4NK mechanics
