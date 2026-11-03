# ReservistenCoin Core 25.2.0 – "ASERT with Shears StallGuard"

**Upgrade required before block 26,500.** Older versions stop following the chain at that block.

From block **26,500** the difficulty uses **ASERT with Shears StallGuard** (replacing the anchored ASERT of 25.1.0):

1. **Step-by-step ASERT** (aserti3-2d maths from Bitcoin Cash, by Mark Lundeberg and Jonathan Toomim):
   each block's difficulty follows how long the previous block took, with a **1-hour half-life**.
   There is no fixed timetable, so a quiet spell is not followed by a burst of "catch-up" blocks.
   The switch-over block carries on from the previous difficulty – no jump.
2. **Shears StallGuard:** if no block has been found for **2 hours**, the next block may be easier –
   the difficulty halves for every further **30 minutes** of waiting. A big miner leaving can no
   longer freeze the chain.
3. **A floor of difficulty 10,000** – however quiet the chain is, it never becomes cheaper than this.
4. From block 26,500, **block times may be at most 10 minutes in the future** (2 hours before), so
   StallGuard cannot be triggered early with fake timestamps.

The target block time stays at 10 minutes; rewards and all other rules are unchanged.

## Upgrading
Back up your wallet, stop the old node/wallet, start 25.2.0. Data folder and wallets are used as they are.
Keep your computer clock set automatically.

## Credits
ASERT: Mark Lundeberg and Jonathan Toomim (Bitcoin Cash Node). StallGuard and the floor: Shears Mining.
ReservistenCoin: the ReservistenCoin developers.
