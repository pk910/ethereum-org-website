---
title: Staking withdrawals
description: Page summarizing what staking push withdrawals are, how they work, and what stakers need to do to get their rewards
lang: en
template: staking
image: ../../../assets/staking/leslie-withdrawal.png
alt: Leslie the rhino with her staking rewards
sidebarDepth: 2
summaryPoints:
  - The Shanghai upgrade brings staking withdrawals to Ethereum
  - Validator operators must provide a withdrawal address to enable
  - Rewards are automatically distributed every few days
  - Validators who fully exit staking will receive their remaining balance
---

<UpgradeStatus dateKey="page-upgrades-withdrawals">
  Staking withdrawals will be enabled through the Shanghai/Capella upgrade. This Ethereum network upgrade is expected to take place in the first half of 2023. <a href="#when">More below</a>
</UpgradeStatus>

The Shanghai/Capella upgrade enables **staking withdrawals** on Ethereum, allowing people to unlock ETH staking rewards. Reward payments will automatically and regularly be sent to a provided withdrawal address linked to each validator. Users can also exit staking entirely, unlocking their full validator balance.

Note to validator operators: If a withdrawal address was not set during the initial deposit, validators will need to enable withdrawals by submitting a withdrawal credential change. For details on how and when to make this change, see [Staking Launchpad](https://launchpad.ethereum.org/withdrawals).

## Staking rewards {#staking-rewards}

Rewards payments are automatically processed for active validator accounts with a maxed out effective balance of 32 ETH, who are accumulating rewards.

Any balance above 32 ETH earned through rewards does not actually contribute to principle, or increase the weight of this validator on the network, and is thus automatically withdrawn as a rewards payment every few days. Aside from providing a withdrawal address one time, these rewards do not require any action from the validator operator. This is all initiated on the consensus layer, thus no gas (transaction fee) is required at any step, nor do withdrawals compete for existing block space.

### How did we get here? {#how-did-we-get-here}

Over the past few years Ethereum has undergone several network upgrades transitioning to a network secured by ETH itself, instead of energy-intensive mining as it once was. Participating in consensus on Ethereum is now known as "staking", as participants have voluntarily locked up ETH, placing it "at stake" for the ability to participate in the network. Following the rules rewards users, while attempts to cheat can be penalized.

Since the launch of the staking deposit contract in November 2020, some brave Ethereum pioneers have voluntarily locked funds up to enable "validators", or accounts that have the right to formally attest to and propose blocks, following network rules.

Before the enabling of staking withdrawals, none of the funds staked had any ability to be unlocked and used elsewhere. With the addition of staking withdrawals, staked ETH no longer requires an unknown lock-up period. Liquid rewards will automatically be deposited into the provided account, and stakers can unlock and withdrawn their entire balance at any time.

### How do I prepare? {#how-do-i-prepare}

<WithdrawalsTabComparison />

### Important notices {#important-notices}

Providing a withdrawal address is a required step for any validator account before it will be eligible to have ETH withdrawn from its balance.

<InfoBanner emoji="⚠️" isWarning>
  <strong>Each validator account can only be assigned a single withdrawal address, one time.</strong> Once an address is chosen and submitted to the Beacon Chain, this cannot be undone or changed again. Double-check ownership and accuracy of the address provided before submitting.
</InfoBanner>

There is <strong>no threat to your funds in the meantime</strong> for not providing this—only the loss of opportunity. Failure to add withdrawal credentials will simply leave the ETH locked in the validator account as it has been until a withdrawal address is provided.

## Exiting staking entirely {#exiting-staking-entirely}

Providing a withdrawal address is required before _any_ funds can be transferred out of a validator account balance.

Users looking to exit staking entirely and withdraw their full balance back must also sign and broadcast a "voluntary exit" message with validator keys which will start the process of exiting from staking. This is done with your validator client and submitted to your beacon node, and does not require gas.

The process of a validator exiting from staking takes variable amounts of time, depending how many others are exiting at the same time. Once complete, this account will no longer be responsible for performing validator network duties, is no longer eligible for rewards, and no longer has their ETH "at stake". At this time the account with be marked as fully “withdrawable”.

Once an account is flagged as "withdrawable", and withdrawal credentials have been provided, there is nothing more a user needs to do aside from wait. Accounts are automatically and continuously swept by block proposers for eligible exited funds, and your account balance will be transferred in full during the next sweep (also known as a "full withdrawal").

## When are staking withdrawals enabled? {#when}

Withdrawal functionality will be enabled through a two-part simultaneous network upgrade, **Shanghai + Capella**.

<ShanghaiCapella />

## How do withdrawal payments work? {#how-do-withdrawals-work}

Once a validator account has a withdrawal address registered, rewards payments for eligible ETH will happen automatically.

Instead of requiring stakers to manually submit a transaction requesting a particular amount of ETH to be withdrawn, withdrawals are designed to automatically transfer out any amount of ETH that is not actively at stake—**no gas required**.

### Validator "sweeping"

With each block, the proposing validator must include a list of withdrawals to process. Each validator is evaluated for possible withdrawals in order, evaluated as follows:

| Decision                                     | Yes                                   | No                                                     |
| -------------------------------------------- | ------------------------------------- | ------------------------------------------------------ |
| 1. Has a withdrawal address been provided?   | Proceed to #2                         | **No** withdrawal will be processed, validator skipped |
| 2. Is the validator still active?            | Proceed to #3                         | **Full** withdrawal will be processed                  |
| 3. Is the effective balance maxed out at 32? | **Rewards payment** will be processed | **No** withdrawal will be processed, validator skipped |

A maximum of 16 withdrawals can be processed in a single block. At that rate, 115,200 validator withdrawals can be processed per day (assuming no missed blocks). As noted above, validators without eligible withdrawals will be skipped, decreasing the time to finish the sweep.

## Frequently asked questions {#faq}

<ExpandableCard title="Once I have provided a withdrawal address, can I change it to an alternative withdrawal address?">
No, the process to provide withdrawal credentials is a one-time process, and cannot be changed once submitted.
</ExpandableCard>

<ExpandableCard title="What if I participate in liquid staking derivatives or pooled staking">
<p>If you are part of a <a href="/staking/pools/">staking pool</a> or hold liquid staking derivatives, you should check with your provider for more details about how staking withdrawals will affect your arrangement, as each service operates differently.</p>
<p>In general, users will likely have nothing they need to do, and these services will no longer be limited by the inability to withdrawal rewards or exit validator funds after this upgrade.</p>
<p>This means that users can now decide to redeem their underlying staked ETH, or change which staking provider they utilize. If a particular pool is getting too large, funds can be exited and redeemed, and re-staked with a <a href="https://pools.invis.cloud">smaller provider</a>. Or, if you’ve accumulated enough ETH you could <a href="/staking/solo/">stake from home</a>.</p>
</ExpandableCard>

<ExpandableCard title="Do rewards payments (partial withdrawals) happen automatically?">
<p>Yes, as long as your validator has provided a withdrawal address. This must be provided once to enable any withdrawals, then rewards payments will be automatically triggered every few days with each validator sweep.</p>
</ExpandableCard>

<ExpandableCard title="Do full withdrawals happen automatically?">
<p>No, if your validator is still active on the network, a full withdrawal will not happen automatically. This requires manually initiating a voluntary exit.</p>
<p>Once a validator has completed the exiting process, and assuming the account has withdrawal credentials, the remaining balance will <em>then</em> be withdrawal during the next validator sweep.</p>
</ExpandableCard>

<ExpandableCard title="How can I withdrawal a custom amount?">
<p>Withdrawals are designed to be pushed automatically, transferring any ETH that is not actively contributing to stake. This includes full balances for accounts </p>
<p>It is not possible to manually request specific amounts of ETH to be withdrawn.</p>
</ExpandableCard>

<ExpandableCard title="I operate a validator, where can I find more information on preparing?">
<p>Validator operators are recommended to visit the <a href="https://launchpad.ethereum.org/withdrawals/">Staking Launchpad Withdrawals</a> page where you'll find more details about how to be prepared, timing of events, and more details about how withdrawals function.</p>
</ExpandableCard>

## Further reading {#further-reading}

- [Staking Launchpad Withdrawals](https://launchpad.ethereum.org/withdrawals)
- [EIP-4895: Beacon chain push withdrawals as operations](https://eips.ethereum.org/EIPS/eip-4895)
- [Ethereum Cat Herders - Shanghai](https://www.ethereumcatherders.com/shanghai_upgrade/index.html)
- [PEEPanEIP #94: Staked ETH Withdrawal (Testing) with Potuz & Hsiao-Wei Wang](https://www.youtube.com/watch?v=G8UstwmGtyE)
- [PEEPanEIP#68: EIP-4895: Beacon chain push withdrawals as operations with Alex stokes](https://www.youtube.com/watch?v=CcL9RJBljUs)