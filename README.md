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

| Contract| Description| Importance (1-5) |
| --------------------- | ---------------------------------------------- | ---------- |
| **ERC20 Contract**    | Is the DAO using a standardized ERC20 implementation? If not, has the contract source been verified and viewable for the public on Etherscan or a similar service? | 5 - Critical   |
| **Audit**    | If not using a standard ERC20 token standard (i.e. openzeppelin presets), has the contract been audited? | 5 - Critical   |
| **Distribution**  | During the initial token mint, were the tokens distributed contractually? Are there any undisclosed wallets (not in control of the DAO) that received significant amounts?| 5 - Critical |
| **Minting** | Can new tokens be minted at will without a cap? If so, does the minter role belong to a sole address or a governed multi-sig address? | 5 - Critical |
| **Restriction**| Can tokens be frozen or restricted? If so, does the pauser role belong to a sole address or a governed multi-sig address? | 4 - High |
| **Circulation & Supply Cap** | What percentage of the set max supply (if set) has been minted and is in public circulation?| 4 - High |
| **Locked Supply** | If all tokens minted, is there a contract controlling the release of a set steady stream? If not, are the tokens not in circulation in a safe contract held by the DAO? | 4 - High |

Because of the unforgiving nature of smart contracts, it is crucial that a proper contract was used when minting or designing the release schedule of the token, and every transparency check in this section is rated critical or high. Most token mints are conducted utilizing standard, battle-tested, meticulously audited smart contract templates and interfaces provided by organizations like OpenZeppelin and ConsenSys. A non-standard ERC20 implementation may be a potential red flag and should be investigated -- however, there may be a perfectly legitimate reason for the developers' decision.

#### **Tokenomics: Market Data, Asset Performance, Sentiment**

| Metric                    | Description                                  | Importance |
| ------------------------- | -------------------------------------------- | ---------- |
| Distribution of tokens    | Distribution of tokens -- essentially the power to influence a DAOs elections and direction -- has the potential to become a massive problem especially for DAOs that have not adopted quadratic voting. A more in-depth description will be provided in section *B - Governance.*                                  | 5 - Critical |
| Number of token holders   | The growth or decrease in the number of token holders is a generally a good indicator of the market sentiment of the DAO. However, it is important to note that this metric is inapplicable for newer DAOs that have opted to airdrop tokens to kick off the decentralization process, for obvious reasons. Ideally, after the initial sell-off of the tokens for uninterested receipents, the number of token holders should somewhat stabilize. In cases where the DAO's governance token also serves as a utility token, a rapid or even exponential growth in the number of token holders is possible, and indicates excellent sentiment or utility.     | 4 - High |
| Token holders to active participants ratio     | A high participation rate in the day to day operations and decisions of the DAO show that the stakeholders, regardless of how big or how small their voting influence is, is a big indicator of the DAO stakeholders' commitment to see the long-term success of the DAO. This metric should be measured in relativity to similar DAOs of similar size, as governance participation rates, understandably, been low across the board.  | 4 - High |
| Token Liquidity   | Liquidity is an important factor to consider as it most DAOs are looking to lower the barrier to entry in the participation of their organization. Multi-chain liquidity is ideal, as it is an undeniable fact that many users become relectant to exchange assets on the Ethereum network when gas fees are on the higher side. | 3 - Medium |
| Token Resiliency                    | It's no secret that the entire market can get extremely volatile when Bitcoin becomes moody. The correlation of price with the token and BTC is easily measurable and is useful in guaging not only the resiliency of the token and its holders, but also for getting a very primitive estimate on the influence of arbitrage bots on the token's price action (more problematic for tokens listed on CEXs).         | 2 - Low |
| Token value/price over time           | Asset performance and price movement is absolutely important to many, but for the most part short term price action has shown the industry many times that it is not a reliable indicator of a project's health. The performance is also relative to each holder -- some may be up 30,000% while others are holding at a 50% loss. However, if a token has been on a downtrend for a prolonged period of time -- especially during a bull market -- then it is something definitely worth investigating. | 2 - Low |
| Token trading volume | Self-explanatory; a token's trading volume is not completely indicitive of a DAOs health or its direction. On the other hand, a TV of near-zero might be a red flag that something is awry.                                   | 2 - Low |



- Token value/price over time
- Token holder growth over time
- Token liquidity among different networks
- Token trading volume
- No. of holders to governance participants

#### AB. Financial Governance

![image](https://user-images.githubusercontent.com/16395727/153219361-4408d49b-6851-4e22-84ef-0dca569f3211.png)


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
