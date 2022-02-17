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

---

#### AB. Financial Governance

Financial governance refers to the way a company collects, manages, monitors and controls financial information. Financial governance includes how companies track financial transactions, manage performance and control data, compliance, operations, and disclosures[^1]. 

Sounds like a perfect use-case for blockchain -- blockchain being giant, immutable, transparent ledgers. Unfortunately, at the moment it is not as simple as opening up a company ERP and querying the financial data that's needed. In fact, as the blockchain space continues to grow and evolve, it is arguable that financial transparency within the scope of DAOs, smart contracts, dApps, etc., is harder than ever for the average user. It's not as simple as tracking incoming and outgoing transactions and checking balances. Many DAOs are diversified in liquidity pools, taking out decentralized loans, participating in DAO2DAO collaborations and swaps, issuing bonds, and the list goes on and on.

Even a *visual* guide of how GnosisSafe, the multisig ~~wallet~~ protocol of choice for many DAOs, utilizes smart contracts under the hood can look quite indimidating. 

![image](https://user-images.githubusercontent.com/16395727/153219361-4408d49b-6851-4e22-84ef-0dca569f3211.png)

For the sake of time, I will keep this section short and to the point. The key transparency measurements will be based on the following questions:

- Is the DAO's treasury secured under an audited, respected, battle-tested protocol or contract?
- If the DAO's treasury is controlled by a multisig wallet, are there safeguards in place to allow the DAO to regain control of the treasury in a catestrophic event (death, natural disasters, alien abduction, etc)?
- Can DAO funds be accessed via a permitted, governance approved smart contract call? (i.e. can the DAO operate without human middlemen having to sign off on governance-passed proposals and initiatives)
- Is the DAO intentionally involved in any shady or illegal financial practices ultimately designed to benefit from others' losses?

The SEC has made it clear that it will not meddle with DeFi and decentralized protocols as long as laws, which we are all fully aware of, are not broken and investors are not being punked.

> I recognize it is not the SEC’s role to prevent all investment losses.  It is also not my goal to restrict investor access to fair and appropriate opportunities.  But it is my job to demand that investors have equal access to critical information so they can make informed decisions whether to invest and at what price.  I am similarly committed to ensuring markets are fair and free from manipulation. 

For the first time in possibly my life, I stand by and commend the SEC for their seemingly renewed stanced and enthusiasm for the blockchain industry. I go more into the significance of this more in-depth at the [end.](#SEC-calls-for-more-transparency)

---

#### AC. Financial Disclosure

This portion will be separated into three segments: on-chain financials, off-chain financials, and proactive disclosure reports.

**On-Chain**

- Can the DAOs financial holdings, assets, and debts be easily queried?
- Are all DAO holdings, including LP tokens, interest bearing assets, assets on other chains, etc., publicly known?
- Essentially, are all DAO-owned wallets and addresses publicly known?
- Is there a somewhat clear record of incoming transactions and outgoing transactions (cash inflow/outflow)
- Is the DAO treasury only used for governance-passed or DAO-approved transactions?

**Off-Chain** (if applicable, so far nearly all DAOs deal mostly with digital assets)

- Did the DAO ever receive compensation or investment from a third-party? If so, are the terms of the investment public knowledge?
- Is the DAO committed to any deals, promises, or contract with another entity, decentralized or conventional? If so, are the terms public knowledge?
- If the DAO is generating fiat revenue into a bank account, are third party auditors welcome for review? 

**Proactiveness**

- Does the DAO put in an effort to keep the stakeholders well informed of its financial health?
- How often does the DAO put out financial reports, if any?
- Is the DAO actively engaged in treasury and financial discussions?

---

### B. Governance

This section will be filled in more in-depth at a later date. Governance is an interesting and very important topic but the current time restraints leave me no choice but to focus on development again.

**Key concepts to be explored:**

- The Theory of the Calculus of Voting by William H. Riker and Peter C. Ordeshook
- The Mathematics and Statistics of Voting Power by Andrew Gelman, Jonathan N. Katz and Francis Tuerlinckx
- Banzhaf power index vs Shapley–Shubik power index
- Lewin's equation in what determines behavior
- Quadratic voting

To put it simply, too much concentrated power from a few holders = potentially bad. 

#### BC. Consistent Governance Process and Inclusion of Stakeholders

##### Edge Cases and Use of a Weighted Scale


### C. Communication

Transparency has historically been measured along two primary dimensions; one which considers the controllable factors inherent in strategic information sending to be the extent of its measurability[^4], and another that considers the duality and complexity of relationships, meaning making and understanding to be at the core of its application[^5]. Both are related, but both are very different ends to apply to the same construct.

---

## The Dashboard 

The dashboard at its current state is pretty barebone looking on the outside, but underneath I am putting constnat thought into the foundational structure so that any DAO can easily input, modify, remove, components and pages as they see fit. Organization is not a strong suit of mine, so I hate to admit that it did take a large portion of the development time. 

### Data Collection Methodology

**Because of the time restraints I am currently stressing over,** the initial submission will use cached versions of real API calls made to awesome data providers like Covalent, Infura, Moralis, etc. Proper CORS, caching, API credentials,  CDN networks, IPFS, are all very important parts of any platform, but again, for the sake of time, the demo data will be from the folder `.static/data/mock`

Although an attempt was made to keep most data points as objective as possible, there are certain data points that are simply not able to be queried, scraped, or assigned automatically through software. This in itself is not a bad thing, but prevents a large scale industry-wide scoring assignments of DAOs. 

The dashboard was designed and being built with in mind that it should be useful for all involved parties, from DAO leaders to investors, to researchers *_*ahem*_* regulatory bodies to bounty hunters and degens.

ShapeShift DAO was chosen as the DTI test guineu pig for several reasons:

- It's where I am currently emplyoed full-DAO time.
- It holds a special place in my heart as an organization that got me excited once more in the blockchain field
- As one of the oldset blockchain organizations still in operation today, the decision to decentralize its entire operations was a bold one -- definitely not an easy feat. But somehow, we're DAOin it, and I believe that ShapeShift can be a very good case study for future entities wishing to decentralize.


--- 

## Clarifications of this project and a Plea for Support

The plans and basic work for the DAO transparency project began in mid-2021, long before the posting of the bounty by Covalent. That being said, I wnat to thank Covalent for pushing me to research the topic even further -- I truly hope that this project will continue for years to come, eolving and adapating to the inevitable changes of the landscapes. My passion and desire to continue this project has been renewed and rekindled upon reading the SEC's statement regarding DeFi and what needs to change in order for them to allow the space to grow and innovate without interference. tl;dr: contributors? yes please! Contact me as you wish. 

### SEC Calls for More Transparency


The SEC, in a surprisingly non-threatening tone, released a statement[^2] just a few months prior in Nov. 2021:

> Whether in the news, social media, popular entertainment, and increasingly in people’s portfolios, crypto is now part of the vernacular.  But what that term actually encompasses is broad and amorphous and includes everything from tokens, to non-fungible tokens, to Dexes to Decentralized Finance or DeFI. For those readers not already familiar with DeFi, unsurprisingly, definitions also vary.  In general, though, it is an effort to replicate functions of our traditional finance systems through the use of blockchain-based smart contracts that are composable, interoperable, and open source 

>... DeFi presents a panoply of opportunities.  However, it also poses important risks and challenges for regulators, investors, and the financial markets.  While the potential for profits attracts attention, sometimes overwhelming attention, there is also confusion, often significant, regarding important aspects of this emerging market.

>...While DeFi has produced impressive alternative methods of composing, recording, and processing transactions, it has not rewritten all of economics or human nature.  Certain truths apply with as much force in DeFi as they do in traditional finance: 
> - Unless required, there will be projects that do not invest in compliance or adequate internal controls;
> - when the potential financial rewards are great enough, some individuals will victimize others, and the likelihood of this occurring tends to increase as the likelihood of getting caught and severity of potential sanctions decrease; and
> - absent mandatory disclosure requirements, information asymmetries will likely advantage rich investors and insiders at the expense of the smallest investors and those with the least access to information.

While claiming to have jurisdiction over DeFi, most likely realizing that it is not something one can simply regulate, went as far to offer a hand:

> As an SEC Commissioner I have a duty to help ensure that market activity, whether new or old, operates fairly, and offers all investors a level playing field.  I would expect this goal to be one DeFi market participants also support. To do this, the SEC has a variety of tools at its disposal ranging from rulemaking authority, to various exemptive or no action relief, to enforcement actions.  Importantly, if DeFi development teams are not sure whether their project is within the SEC’s jurisdiction, they should reach out to our Strategic Hub for Innovation and Financial Technology (“FinHub”), or our other Offices and Divisions, all of which have experts well-versed in issues relating to digital assets. It is my understanding that FinHub has never refused a meeting, and their engagement is meaningful.

But it's not all flowers and rainbows, she did go on to say the SEC had to flex its muscles and settle an enforcement on DMM[^3] for "failing to register their offering, which raised $30 million, and misled their investors while improperly spending investor money on themselves." 

People will have opinions and I might have already ruffled some feathers, but the SEC has made it crystal clear that fundraising securities on American soil and to American citizens undoubtedly illegal -- half a decade ago. In the end, they got a slap on the wrist, and was ordered to pay about half of the $30mil raised in penalties. Whether or not they were involved in fradulent activity is not for me to judge, but just as I was thinking to myself "that's why we need more transparency in the space!" lo and behold, straight from the horses mouth:

> I recognize it is not the SEC’s role to prevent all investment losses.  It is also not my goal to restrict investor access to fair and appropriate opportunities.  But it is my job to demand that investors have equal access to critical information so they can make informed decisions whether to invest and at what price.  I am similarly committed to ensuring markets are fair and free from manipulation.  Given this, it seems that there are two specific structural problems that the DeFi community needs to address: Lack of Transparency and Pseudonymity.

While I do not fully agree with the Pseudonymity portion, this excerpt from the Lack of Transparency section showed some level-headed thinking and rationale that I can get behind:

> First, although transactions often are recorded on a public blockchain, in important ways, DeFi investing is not transparent.  I am concerned that this lack of transparency contributes to a two tier market in which professional investors and insiders reap outsized returns while retail investors take more risks, get worse pricing, and are less likely to succeed over time.  Much of DeFi is funded by venture capital and other professional investors.  It is unclear to me how well known this is in the DeFi retail investor community, but the underlying funding deals often grant professional investors equity, options, advisory roles, access to project team management, formal or informal say on governance and operations, anti-dilution rights, and the ability to distribute controlling interests to allies, among other benefits.  Rarely are these arrangements disclosed, but they can have a significant impact on investment values and outcomes.  Retail investors are already operating at a significant disadvantage to professional investors in DeFi, and this information imbalance exacerbates the problem. 

> Some contend that DeFi is, in fact, more egalitarian and transparent because much of the activity is based on code that is publicly available. However, only a relatively small group of people can actually read and understand that code, and even highly-qualified experts miss flaws or hazards.  Currently the quality of that code can vary drastically, and has a significant impact on investment outcomes and security.  If DeFi has ambitions of reaching a broad investing pool, it should not assume a significant portion of that population can or wants to run their own testnet to understand the risks associated with the code on which their investment prospects rely.  It is not reasonable to build a financial system that demands investors also be sophisticated interpreters of complex code. 

If I had known that the *SEC* out of all organizations had already written the beginning portion of this section, Financial Governance, I could've saved an hour with a simple copy and paste. On a more serious note, if we want true decentralization, we must take ownership and take responsibilities. And for now it appears the SEC has given the green-light to continue -- let's not screw it up. 

### License

Apache License, Version 2.0
 
### Contributing

TBA after Covalent's Challenge.

## Changelog 

- 0.0.1 Initial commit, a lot of internal thinking into how to proceed with this task
- 0.0.2 Boilerplate Nuxt/VueJS dashboard ready and organized for anyone to deploy (client side and SSR both supported)
- 0.0.3 Integration of both Bootstrap and TailwindCSS for future users to select, or even use both at the same time. 



[^1]: Wolters Kluwer N.V. 
[^2]: Statement on DeFi Risks, Regulations, and Opportunities: https://www.sec.gov/news/statement/crenshaw-defi-20211109#_ftn19
[^3]: SEC Proceeding File No. 3-20453: https://www.sec.gov/litigation/admin/2021/33-10961.pdf
[^4]: Carl E. Walsh, Journal of Money, Credit and Banking Vol. 35, No. 5 pp. 829-849
[^5]: Mueller, Elisabeth, British Journal of Management, Towards a Theory of Network Facilitation: A Microfoundations Perspective on the Antecedents, Practices and Outcomes of Network Facilitation.