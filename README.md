# Ork Imperial Guard Fightin' Opinions Log

An on-chain log of how Orks feel about fighting different Imperial Guard regiments.  
Each entry records which regiment the Orks fought, how they reacted, why they felt that way, and what happened in the scrap.  
The community votes whether each opinion is **WAAAGH-approved** or **not proppa'**.

Fully text-based, permissionless, and designed for Warhammer 40K-flavoured world-building on Base.

---

## Contract

Deployed on Base:  
`0x8f7d6c26acd1fd42711f539e01d95cb2339f2f69`  
https://basescan.org/address/0x8f7d6c26acd1fd42711f539e01d95cb2339f2f69#code

Main file: `contracts/OrkGuardFightOpinions.sol`

---

## How it works

Each opinion entry stores:

- `regiment` – Name of the Imperial Guard regiment  
- `reaction` – How the Orks feel about fighting them  
- `reason` – Why the Orks think that  
- `outcome` – What happened in the fight  
- `remark` – Extra Orky comment  
- `approved` / `rejected` – Community votes  

Entry **0** is a built-in example.

---

## Examples

```solidity
recordOpinion(
  "Catachan Jungle Fighters",
  "DASE HUMIES IS DEAD KILLY AN' FUN!",
  "Dey charge right at us wiv big knives an' lots o' shoutin'. Proper scrap!",
  "Da fight lasted all day, lots o' loud booms an' choppin'.",
  "Orks love humies dat don't run away!"
);


voteOpinion(1, true);   // WAAAGH-approved
voteOpinion(1, false);  // Not proppa'


Closing Note
A loud, messy ledger of Orky opinions —
a record of which humies are worth a good scrap, and which are just boring gitz.
