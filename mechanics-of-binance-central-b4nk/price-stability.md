# ⚖️ Price Stability

## Price Stability Mechanism

xBNB maintains its 1:1 peg to BNB through market-driven arbitrage opportunities combined with dynamic collateral ratio adjustments.

### How Price Stability Works

The protocol doesn't rely on direct interventions or oracles to maintain the peg. Instead, it creates natural economic incentives for arbitrageurs to keep xBNB at 1:1 of BNBs value.

### Under Peg Scenario

**When 1 xBNB < 1 BNB** (e.g., 1 xBNB = 0.98 BNB)

#### Arbitrage Opportunity

```
Buy 1 xBNB at 0.98 BNB → Redeem for 1 BNB value → Profit 0.02 BNB
```

#### Market Response

{% stepper %}
{% step %}
#### Arbitrageurs Buy xBNB

When xBNB trades below peg, arbitrageurs buy cheap xBNB from the market.
{% endstep %}

{% step %}
#### Buying Pressure Increases

This buying activity pushes xBNB price upward toward 1 BNB.
{% endstep %}

{% step %}
#### Redeem for Full Value

Arbitrageurs redeem xBNB for its full value (1 BNB worth of collateral).
{% endstep %}

{% step %}
#### Profit Realised

The difference between purchase price and redemption value is the arbitrageur's profit.
{% endstep %}
{% endstepper %}

#### Protocol Response

When xBNB is consistently under peg:

* Collateral Ratio **increases** hourly by 0.1%
* Higher CR makes redemptions return more BNB
* More attractive redemption terms strengthen the peg recovery

### Over Peg Scenario

**When 1 xBNB > 1 BNB** (e.g., 1 xBNB = 1.02 BNB)

#### Arbitrage Opportunity

```
Mint 1 xBNB for 1 BNB value → Sell at 1.02 BNB → Profit 0.02 BNB
```

#### Market Response

{% stepper %}
{% step %}
#### Arbitrageurs Mint xBNB

When xBNB trades above peg, arbitrageurs mint 1 new xBNB at 1 BNB cost.
{% endstep %}

{% step %}
#### Sell at Premium

They immediately sell the minted xBNB on the market at above-peg prices.
{% endstep %}

{% step %}
#### Selling Pressure Increases

This selling activity pushes xBNB price downward toward 1 BNB.
{% endstep %}

{% step %}
#### Profit Realised

The difference between minting cost and selling price is the arbitrageur's profit.
{% endstep %}
{% endstepper %}

#### Protocol Response

When xBNB is consistently over peg:

* Collateral Ratio **decreases** hourly by 0.1%
* Lower CR makes minting cheaper (less BNB required)
* Easier minting increases xBNB supply, bringing price down

### Key Advantages

#### Decentralised

No reliance on centralised price feeds or governance decisions. Market forces naturally maintain the peg.

#### Capital Efficient

Arbitrageurs don't need large capital reserves. Small price deviations create profitable opportunities.

#### Self-Correcting

The combination of arbitrage + dynamic CR creates a robust, self-correcting system.

#### Permissionless

Anyone can participate in arbitrage, ensuring the mechanism works 24/7.

### Peg Tolerance

Minor price deviations are normal and healthy:

{% hint style="success" %}
**Typical Range for 1 xBNB**: 0.99 - 1.01 BNB

Small deviations allow for:

* Natural market making spreads
* Transaction costs for arbitrageurs
* Short-term supply/demand imbalances
{% endhint %}

{% hint style="warning" %}
**Significant Deviation for 1 xBNB**: < 0.95 or > 1.05 BNB

Larger deviations trigger stronger arbitrage incentives and faster CR adjustments.
{% endhint %}

### Real-World Example

#### Scenario: 1 xBNB Trading at 0.97 BNB

**Arbitrageur's Action:**

1. Buy 100 xBNB for 97 BNB on DEX
2. Redeem 100 xBNB for 100 BNB value in collateral
3. Profit: \~3 BNB (minus gas fees and 0.50% redemption fee)

**Market Impact:**

* Buying 100 xBNB increases demand
* Price moves from 0.97 toward 1.00
* Other arbitrageurs see opportunity and also buy
* Peg is restored through collective action

### Fee Considerations

Remember that protocol fees apply:

* **Minting Fee**: 0.50%
* **Redeeming Fee**: 0.50%

These fees create a small buffer zone (approximately 0.99 - 1.01) where arbitrage may not be immediately profitable, which is healthy for reducing unnecessary trading volume.

***

**Next Steps**: Learn about staking and locking B4NK
