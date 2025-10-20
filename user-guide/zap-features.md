# ⚡ Zap Features

## Zap Features

One-click actions for improved user experience and simplified DeFi interactions.

### What are Zaps?

Zaps allow you to perform complex multi-step operations in a single transaction, saving time, gas fees, and reducing the complexity of interacting with DeFi protocols.

### Available Zaps

<table data-header-hidden><thead><tr><th width="200"></th><th></th></tr></thead><tbody><tr><td><strong>Minting Page</strong></td><td>Simplified xBNB creation with automatic token swaps</td></tr><tr><td><strong>Farming Page</strong></td><td>Direct LP addition and staking in one transaction</td></tr></tbody></table>

### BNB-Only Zapping

The most powerful feature of our Zap system: complete farming setup with only BNB.

#### How It Works

{% stepper %}
{% step %}
#### Start with BNB

You only need BNB in your wallet - no need to acquire xBNB or B4NK first.
{% endstep %}

{% step %}
#### Automatic Purchases

The Zap automatically:

* Swaps portion of BNB for required xBNB or B4NK
* Maintains optimal ratio for liquidity provision
{% endstep %}

{% step %}
#### Add Liquidity

Zap adds liquidity to your chosen pool on PancakeSwap and receives LP tokens.
{% endstep %}

{% step %}
#### Stake LP Tokens

LP tokens are automatically deposited to farms, immediately earning rewards.
{% endstep %}
{% endstepper %}

#### Supported Pools

You can use BNB-only zapping for:

* **xBNB/BNB LP Pool**
* **B4NK/BNB LP Pool**

### Minting Zap

Simplify xBNB minting with automatic collateral management.

#### Standard Minting (Without Zap)

1. Calculate current Collateral Ratio
2. Acquire correct amount of BNB
3. Acquire correct amount of B4NK
4. Approve both tokens
5. Mint xBNB
6. Collect minted tokens (separate transaction)

#### With Minting Zap

1. Input desired xBNB amount
2. Provide BNB (Zap calculates and swaps for B4NK automatically)
3. Confirm single transaction
4. Collect minted tokens (separate transaction)

{% hint style="success" %}
**Benefits**: Saves multiple transactions, no need to calculate ratios, automatic slippage protection
{% endhint %}

### Farming Zap

Go from single token to earning farm rewards in one click.

#### Traditional Process (Without Zap)

1. Swap BNB for xBNB or B4NK
2. Add liquidity on PancakeSwap
3. Receive LP tokens
4. Approve LP tokens
5. Stake in farm

#### With Farming Zap

1. Select pool and amount
2. Confirm single transaction
3. Start earning immediately

### Gas Optimisation

Zaps are optimised to save gas costs:

* **Fewer Transactions**: Multiple operations bundled into one
* **Optimised Routing**: Smart routing finds best swap paths
* **Batch Approvals**: Combines approvals where possible

### Safety Features

{% hint style="info" %}
**Slippage Protection**

All Zaps include customisable slippage tolerance to protect against unfavourable price movements during execution.
{% endhint %}

{% hint style="info" %}
**Transaction Preview**

Before confirming, you'll see exactly what tokens you'll receive and at what rates.
{% endhint %}

### When to Use Zaps

#### Use Zaps When:

* You're new to DeFi and want simplified interactions
* You want to save time and gas fees
* You only have BNB and want to start farming quickly
* You want to avoid manual calculations

#### Consider Manual Approach When:

* You already have the exact tokens needed
* You want to optimise for absolute minimum slippage
* You prefer to control each step of the process

***

**Next Steps**: Learn about main protocol token, B4NK
