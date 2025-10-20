# 🛡️ Flash Loan Protection

## Flash Loan Protection

Our protocol employs a robust 2-step mechanism to prevent flash loan attacks and ensure user safety.

### What are Flash Loans?

Flash loans are uncollateralised loans that must be borrowed and repaid within a single blockchain transaction. While useful for legitimate purposes like arbitrage, they can also be exploited to attack DeFi protocols.

#### Common Flash Loan Attack Vectors

**Price Manipulation**\
Attackers can use flash loans to manipulate token prices on DEXes, then exploit protocols that rely on those prices.

**Collateral Exploits**\
Large flash loans can be used to mint excessive amounts of synthetic assets, then default, draining protocol reserves.

**Governance Attacks**\
Flash loans can temporarily grant voting power to pass malicious proposals.

### Our 2-Step Protection

{% hint style="success" %}
**Complete Protection**

By requiring two separate transactions, we make it impossible for flash loan attacks to succeed, since flash loans must be repaid within the same transaction.
{% endhint %}

#### How It Works

<table><thead><tr><th width="150">Action</th><th>Step 1 (Transaction #1)</th><th>Step 2 (Transaction #2)</th></tr></thead><tbody><tr><td><strong>Minting</strong></td><td>Deposit collateral and initiate mint</td><td>Collect minted xBNB tokens</td></tr><tr><td><strong>Redeeming</strong></td><td>Burn xBNB and initiate redemption</td><td>Collect BNB and B4NK collateral</td></tr></tbody></table>

### Why This Prevents Attacks

#### Flash Loan Constraints

Flash loans **must** be repaid in the same transaction they're borrowed. This is enforced at the smart contract level and cannot be bypassed.

#### Our Defense

Since our minting and redemption processes require **two separate transactions**:

1. Attacker borrows flash loan (transaction begins)
2. Attacker completes Step 1 (deposit collateral or burn xBNB)
3. Transaction ends - flash loan **must** be repaid now
4. Step 2 cannot be completed because it requires a new transaction
5. Attack fails - attacker cannot collect minted tokens or redeemed collateral

#### Example Attack Scenario (Prevented)

```
❌ Attempted Flash Loan Attack:

1. Borrow 10,000 BNB via flash loan
2. Mint massive amount of xBNB (Step 1 completes)
3. Try to collect xBNB (Step 2) ← FAILS - requires new transaction
4. Must repay flash loan without receiving xBNB
5. Attack fails, attacker loses gas fees
```

### Additional Security Benefits

#### Time-Locked Collateral

Collateral deposited during Step 1 is locked until Step 2 is completed by the same address that initiated Step 1.

**Benefits:**

* Prevents collateral theft
* Ensures only legitimate users can complete the process
* Creates clear audit trail

#### Address Validation

The protocol verifies that:

* Step 2 is called by the same address that called Step 1
* The transaction parameters match the original mint/redeem request
* No unauthorized modifications occur between steps

#### Economic Disincentive

Even if attackers try the two-step process normally:

* They must provide real collateral (Step 1)
* They must wait for transaction confirmation
* They pay gas fees for both transactions
* They gain no advantage over normal users

### User Experience Trade-off

While the two-step process adds a small inconvenience for users, the security benefits far outweigh this minor friction:

{% tabs %}
{% tab title="Security Gained" %}
**Complete Flash Loan Protection**

* No risk of protocol drainage
* No price manipulation attacks
* No governance exploits via flash loans

**User Fund Safety**

* Your collateral is always safe
* No risk of sudden protocol insolvency
* Predictable and secure operations
{% endtab %}

{% tab title="User Cost" %}
**Minimal Inconvenience**

* One additional transaction per mint/redeem
* \~10-30 seconds additional time
* Small additional gas cost

**Easy to Complete**

* Clear UI guidance through both steps
* Automatic reminders if Step 2 incomplete
* Can complete Step 2 anytime (no rush)
{% endtab %}
{% endtabs %}

### Technical Implementation

#### Smart Contract Logic

```solidity
// Simplified example of two-step minting

// Step 1: Initiate mint
function mintStep1(uint256 amount) external {
    // Transfer collateral from user
    // Record pending mint
    // Lock collateral
    pendingMints[msg.sender] = amount;
}

// Step 2: Collect minted tokens (must be separate tx)
function mintStep2() external {
    require(pendingMints[msg.sender] > 0, "No pending mint");
    uint256 amount = pendingMints[msg.sender];
    delete pendingMints[msg.sender];
    // Mint and transfer xBNB to user
}
```

#### Key Security Features

* `pendingMints` mapping prevents double-claiming
* `msg.sender` check ensures only initiator can complete
* State changes are atomic within each step
* No way to combine both steps in single transaction

### Industry Recognition

The two-step minting/redemption pattern is increasingly recognized as a best practice for synthetic asset protocols and has been successfully used by multiple DeFi projects to prevent flash loan attacks.

{% hint style="info" %}
**Battle-Tested Security**

This protection mechanism has been proven effective across multiple DeFi protocols and has successfully prevented numerous attempted attacks.
{% endhint %}
