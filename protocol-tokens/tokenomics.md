# 📊 Tokenomics

## Tokenomics

Our emission model features a carefully designed decay schedule that rewards early participants while ensuring long-term sustainability.

### Emission Schedule

<table><thead><tr><th width="250">Period</th><th>Emission Rate</th></tr></thead><tbody><tr><td><strong>First 2 months</strong></td><td>Strong decay, reaching 49.6% of initial emissions</td></tr><tr><td><strong>Month 3+</strong></td><td>5% monthly decay</td></tr></tbody></table>

### Why This Model?

{% hint style="success" %}
**Early Adopter Advantage**: This model rewards early liquidity providers with higher emission rates.
{% endhint %}

#### Benefits of Decay Schedule

**Incentivise Early Adoption**\
Higher initial emissions attract early liquidity providers who help bootstrap the protocol.

**Long-Term Sustainability**\
Gradual decay ensures the protocol doesn't over-emit tokens, preserving long-term value.

**Predictable Supply**\
The decay schedule is transparent and predictable, allowing users to model their expected returns.

### Emission Distribution

B4NK emissions are distributed to liquidity providers based on pool allocation:

| Pool                                 | Allocation |
| ------------------------------------ | ---------- |
| **xBNB/BNB LP** (stable/pegged pair) | 60%        |
| **B4NK/BNB LP**                      | 40%        |

The xBNB/BNB pool receives higher allocation because it's the core stable pair that maintains the protocol's primary synthetic asset peg.

### Supply Mechanics

{% tabs %}
{% tab title="Minting" %}
**B4NK is Burned**

When users mint **xBNB**, the **B4NK** portion of collateral is burned, removing tokens from circulation.

This creates deflationary pressure during periods of net xBNB minting.
{% endtab %}

{% tab title="Redeeming" %}
**BCB is Minted**

When users redeem BNBX, new B4NK is minted to return collateral.

This creates inflationary pressure during periods of net BNBX redemption.
{% endtab %}

{% tab title="Net Effect" %}
**Dynamic Supply**

B4NK supply adjusts based on protocol usage:

* Growing protocol (more minting) → Deflationary
* Contracting protocol (more redemption) → Inflationary

This mechanism naturally balances token supply with protocol demand.
{% endtab %}
{% endtabs %}

### Fair Launch

{% hint style="info" %}
**No Premine, No Presale**

B4NK had no premine, IDO, ICO, VC allocation, or presale. All tokens are earned through participation in the protocol.
{% endhint %}

***

**Next Steps**: Learn about staking and locking your B4NK tokens
