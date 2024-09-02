# 💰 Collect

## Overview

Starlicon from a specific epoch can only be collected after the epoch ends. Each miner has its own collect time, which indicates when the $starlicon from that epoch can be collected.

Each miner has 50% of its output protected, which solely belongs to the miner owner and shareholders, divided according to their shares in the miner's upgrades.

The remaining 50% is unprotected and can be collected by any other players (if not collected by the owner, it can be considered as “stolen”). For the unprotected 50%, the quantity that can be collected is based on the user’s role and order:

* The owner can collect 50% of the remaining unprotected $starlicon each time.
* Shareholders can collect 15% of the remaining unprotected $starlicon each time.
* Regular users can collect 10% of the remaining unprotected $starlicon each time.

Collection can continue until the remaining collectible starlicon is less than 1, at which point it will be collected in one go.

## An Example

For example, if a miner's epoch ends at UTC 09:00:00, collection can start at 09:00:01. Suppose the miner produced a total of 10,000 $starlicon in the previous epoch and is at level 100, with 10 levels upgraded by shareholders. Thus, shareholders hold 5% of the total share:

* Protected 50%: 5,000 $starlicon, with 250 for all shareholders and 4,750 for the owner. This portion of $starlicon will always be available for collection by the owner and shareholders, regardless of when they collect.
* Unprotected 50%: This portion can be collected by anyone. If the first user to collect is a regular user, they can collect 10% of the unprotected $starlicon, which is 500. If the second user is a shareholder, they can collect 15% of the remaining unprotected $starlicon (5,000 - 500), which is 675. If the third user is the owner,they can collect 50% of the remaining unprotected starlicon (5,000 - 500 - 675), which is 1,912.5, and so on. The collection process continues until the last player finds that the remaining collectible starlicon is less than 1, in which case they will collect all the remaining starlicon at once.

Regardless of whether the collector is an owner, shareholder, or regular player, they will collect both the protected and unprotected portions in a single transaction when clicking the "Collect" button in the miner Blink user interface.

<figure><img src="../assets/image (12).png" alt="" width="375"><figcaption><p>Different miner links will render different Blink user interfaces. Please ensure that the miner you are about to collect is the one you intend to interact with.</p></figcaption></figure>

## Unprotected Collection Limit

For any users who want to collect (or "steal") the unprotected portion of $starlicon from miners, there is a limit to the amount that can be collected in a single transaction. This limit is influenced by the collector's miner level:&#x20;

$$
UnprotectedCollectionLimit = 10^{MinerLevel}
$$

For example, if your miner is at level 3 and there is a miner with 15,000 unprotected $starlicon, the maximum amount you can collect in one transaction, despite the 10% of 15,000 being 1,500, is limited to 10^3 = 1,000 due to your miner's level as a regular user.
