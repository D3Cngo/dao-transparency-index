The DAO Transparency Index (WIP)
===
Measuring a Decentralized Organization's Transparency: A Proposed Framework to Develop a Transparency Index

Part of an ongoing effort to create a more transparent future at ShapeShift DAO, as well as a contribution to Covalent's DAO Transparency Dashboard challenge. Because of the time restraints of the due date for Covalents challenge, development of the MVP platform will begin right away, taking priority over the completion of this document. The core ideas are however explained and a proposed solution offered. This paper, the solutions, and methodologies are all WIP and live documents that will constantly change.

![Vision.gif](https://gateway.pinata.cloud/ipfs/QmfMLd2XFhSqNdULhXfHSMkpL6g9F9uyeBgh56c1GXVttM)

**Disclaimer: this "lightpaper" is not representative of anyone or any organization's views and beliefs, except my own.**

## Table of Contents

[TOC]

## Foreword: The Inspiration

In order to create a DAO transparency dashboard that actually gives the DAO value, we must first set some boundaries and definitions. This is especially hard to do since the term "DAO" has in recent months become muddied with misconceptions and misrepresentations. At the same time, the very nature and core concept of DAOs does not permit anyone to judge or try to impose "their way" on others. 

Many are calling 2022 "The Year of the DAOs," and the industry is eagerly watching to see what the new year will usher in with innovations, breakthroughs, new unicorns, and of course, dramas, scandals, and rug pulls. 

With the space evolving so quickly, there will certainly be more fadening of what the industry had tried to associate, define, and judge on what makes a respectable DAO. Since the early days of _The DAO_ until just last year, DAOs were almost universally seen as a group of extremely forward thinking engineers that were almost seen as public servents, working on a service or protocol that would ultimately provide tremendous value in the proliferation of the decentralization movement. 

This—perhaps unfair—preconceived notion that we have imposed on DAOs for so long has already begun its inevitable evolution, and there is an odd, almost eery feeling in the air, that somethings about to explode. DeFi was revolutionary for those who already had assets on hand to experiment with, but let's admit it: the party was (and is, and will continue to be) life-changing, but something feels off... as if we had forgotten to invite someone important. ***Oh shit, we forgot to invite the people that the party was thrown for— the unbanked and the oppressed.***

Whereas DeFi revolutionized the way that hard earned assets can be invested and spent, DAOs are beginning to revolutionize the way that wealth and ownership is distributed to collective goal-aligned workers. In doing so, DAOs are also spreading the 'crypto gospel' around the world at an unprecedented pace. This revolution is breaking the molds of perhaps one of the longest standing form of systematic oppression, which had affected every civilization and era that came before us. The idea of work, jobs, careers, fruits of labor (or therelackof), and freedom have captivated the minds of philsophers as far back as the beginning of recorded human history.

We are yet again on the verge of another paradigm shift in the blockchain space -- but this time theres an eerly feeling in the air. Re-defining the meaning of work, how it is conducted, and how the fruits are distributed is a mind-blowing, dangerous, and yet liberating concept that could be the change of course of the direction of our species that we so desparately needed. The economic playing field for the first time would be trending to a more fair and level direction, reversing the milleniums' old trend of the latter. And this is why DAO transparency is so crucial in these early times. It is almost certain that regulators are taking notice, and history has shown that that means the general public at large are not that far off from taking notice as well. This revolution can not fully happen without mainstream adoption, and the mainstream adoption of DeFi can not fully happen without the power and numbers of the world's workforce.

To protect the DAO space we must take it upon ourselves to protect both investors and workers by beginning to explore areas such as DAO Transparency, and ways of equipping knowledge and tools that will allow future DAO frens to do their own research and make their own decisions. The spirit of free innovation and experimentation is how the space got this far, and no one has the right to try and hinder a DAO's growth regardless of how radical or silly its ideas might seem to be. There will certainly be criminal organizations that take the form of a DAO, but web2 has shown the world the terrifying power of angry communities and their capabilities in taking entire organizations down -- and I believe that spirit will continue on to web3.


## Abstract

How does one define something that shouldn't be limited by a definition? Rhetorical questions can be annoying, but there are times when it must be asked. This entire project will be conducted with no pre-concieved, rigid definition of what a DAO is and should be doing, and thus will constantly be evolving over the years as we get a clearer picture of the projected direction and impact of DAOs. 

The ideal outcome is to use the power of data to make it obvious without having to blatantly announce it whether or not a DAO is trustworthy, or even a DAO at all. Since data requires parameters and values, almost all DAOs will ultimately "generally defined" under the same or similar frameworks which will be used to 1) Assign a transparency index score; 2) Show areas in which the DAO could improve on; 3) Shine light on areas that the DAO is excelling at. 

It is proposed that transparency consists of three interrelated principles: 

1. Metric A: **Finance** (i.e., financial health, token liquidity, revenue streams and debts, etc.)
2. Metric B: **Governance** (i.e., degree of decentralization, token holder participation, consolidation of power, smart contract execution, etc.)
3. Metric C: **Communication** (i.e., financial disclosures, internal communications, social and press/media prescence, etc.). 

Independently, all three principles of transparency are necessary but not sufficient for information to be considered transparent. Further, all three principles have major components that can be tracked on-chain and off-chain. 

The three proposed principles are also measured in overlapped sections that give an even clearer, segmented view of the inner workings of a DAO.

A depiction of the proposed principles of transparency is offered in Figure 1.

![](https://i.imgur.com/atV4hjw.png)

### A. Financial

#### **Tokenomics: Smart Contract Level**

| Contract| Description| Importance |
| --------------------- | ---------------------------------------------- | ---------- |
| **ERC20 Contract**    | Is the DAO using a standardized ERC20 implementation? If not, has the contract source been verified and viewable for the public on Etherscan or a similar service? | Critical   |
| **Audit**    | If not using a standard ERC20 token standard (i.e. openzeppelin presets), has the contract been audited? | Critical   |
| **Distribution**  | During the initial token mint, were the tokens distributed contractually? Are there any undisclosed wallets (not in control of the DAO) that received significant amounts?| Critical |
| **Minting** | Can new tokens be minted at will without a cap? If so, does the minter role belong to a sole address or a governed multi-sig address? | Critical |
| **Restriction**| Can tokens be frozen or restricted? If so, does the pauser role belong to a sole address or a governed multi-sig address? | High |
| **Circulation & Supply Cap** | What percentage of the set max supply (if set) has been minted and is in public circulation?| High |
| **Locked Supply** | If all tokens minted, is there a contract controlling the release of a set steady stream? If not, are the tokens not in circulation in a safe contract held by the DAO? | High |

Because of the unforgiving nature of smart contracts, it is crucial that a proper contract was used when minting or designing the release schedule of the token, and every transparency check in this section is rated critical or high. Most token mints are conducted utilizing standard, battle-tested, meticulously audited smart contract templates and interfaces provided by organizations like OpenZeppelin and ConsenSys. A non-standard ERC20 implementation may be a potential red flag and should be investigated -- however, there may be a perfectly legitimate reason for the developers' decision.

**Tokenomics: Market Data**

#### AB. Financial Governance

#### AC. Financial Disclosure (Communication)

### B. Governance

#### BC. Disclosure of Governance Processes and Proposals/Changes

### C. Communication

### Data Collection Methodology

### Edge Cases and Use of a Weighted Scale

### Transparency Dashboard for DAOs and Researchers

--- 

## License

Apache License, Version 2.0
 
## Contributing

TBA after Covalent's Challenge.

## Changelog 

- 0.0.1