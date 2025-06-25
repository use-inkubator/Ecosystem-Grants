# ZUNNO

- **Team Name:** ZUNNO & [Edgetributor SubDAO](https://x.com/Edgetributors)
- **Payment Address:** 14XNJmoUzkvmh9cYoqG4axBRR4BWzWRbnFP79oiZgKu7V9bz

## Project Overview :page\_facing\_up:

### Overview

ZUNNO is a multiplayer digital adaptation of the classic UNO game. ZUNNO leverages Polkadot's scalability, interoperability, and customization to deliver a transparent, fair, and engaging gaming experience. ZUNNO will be deployed on the AssetHub parachain, utilizing PolkaVM-compatible ink\! v6 smart contracts for its backend logic. The proposed development falls into the ‘An Innovative Game’ sub-category of ‘Technical Showcase’ category.   
Traditional online card games often suffer from trust issues, lack transparency, and are vulnerable to manipulation. ZUNNO addresses these concerns by implementing core game logic on-chain, ensuring verifiable and tamper-proof gameplay. Privacy is maintained through a commit-and-reveal scheme, enhanced with cryptographic randomisation, to keep players' hands and the deck hidden, preventing unfair advantages. The choice of the AssetHub parachain allows us to leverage the direct utility of DOT and cross chain assets to deliver the best possible user experience.

### Ink\! Ecosystem Impact

Utilising ink\! v6, ZUNNO will leverage deployment on AssetHub‘s pallet-revive/ PolkaVM, demonstrating future-proofing for the post-JAM ecosystem spectrum. This approach also aligns with the strategy of minimizing cross-chain hops.   
ZUNNO has the potential to attract new users to the Polkadot ecosystem while also promoting community engagement within the web2/web3 gaming space, adding more utility to DOT and contributing to the growth of the AssetHub parachain and indirectly the whole ecosystem. In-game fact popups of how ink\! powers ZUNNO and provide additional benefits over other smart contract languages will subliminally promote ink\! to the players.

### Project Details

- Technology stack & functionality document: [https://drive.google.com/file/d/12cNgTdyWKQiOjA0jQwbLga0m3Ii\_22le/view?usp=sharing](https://drive.google.com/file/d/12cNgTdyWKQiOjA0jQwbLga0m3Ii_22le/view?usp=sharing)

- ZUNNO will be developed with the following core components/ features:  
  * **Decentralized Gameplay:** Core game logic (card shuffling, dealing, turn management) implemented on-chain.

  * **Game State Management:** On-chain management of game state synced across clients via websockets for real-time consistency.

  * **Action Validation:** Off-chain validation of player actions replicated on-chain to ensure adherence to game rules.

  * **State Reconstruction and Verification:** Ability for any participant to reconstruct and verify the game state using the blockchain transaction history.

  * **Optimistic client rollup:** Build an optimistic UI that gathers transactions and submits it on chain as one transaction after a certain number of transactions have already happened.

  * **Confidential Hands and Decks:** Privacy layer to ensure only the cardholder can view their hand.

  * **Game Features:** Implementation of multiple game rooms, various UNO rules, and point systems.

  * **Cryptographic Operations:** Use of hashing and encryption/decryption for data security and privacy.

  * **Deck Shuffling:** Cryptographically secure deck shuffling to ensure randomness.

  * **Deployment on AssetHub Parachain:** ZUNNO's backend, built with v6 ink\! smart contracts, will be deployed on the AssetHub parachain`s PolkaVM.

  The architecture comprises frontend components (Web UI, Wallet Connection, State Manager, Merkle Tree Manager), blockchain components (Smart Contract, Merkle Tree Storage, Game State \- residing on the AssetHub parachain), and backend services (P2P Sync Service, Card Service). The smart contract will be written in ink\!.  
  - Do you need an audit for the contacts? **NO**  
  - CATEGORY: Technical Showcase  
  - Business model:   
    - Players need to stake DOT/gDOT/vDOT on hydration to get in-game points to play.   
    - Players will earn or lose points based on the outcome of the games.  
    - Random airdrops to the point holders.   
  - Target market:  
    - Solo players looking to play UNO digitally  
    - DeFi farmers  
  - Future production plans and growth strategy:  
    - Tentative DeFi derivative to generate income stream  
    - Protocol income can be utilised to host campaigns and as an income stream for the treasury/ink\! bounty. 

## Team :busts\_in\_silhouette:

### Team members

- Parth Mittal: PBA grad and Polkadot Hackathon winner.  
- Krishanu Dhar: Full stack and smart contract developer.  
- Ayush kumar Singh: Full stack developer and UniDAO core member.  
- Nikhil Shrivas: Ace designer and frontend developer with 4+ years in Marketing  
- Saurabh Shetty: Developer relations professional.

### Contact

- **Contact Name:** Saurabh Shetty
- **Contact Email:** sauraj9290@gmail.com
- **Contact Email for operations:** shankar@edgeware.community
- **Website:** [https://zkuno.xyz/](https://zkuno.xyz/)

### Legal Structure

- **NA**

### Team's experience

The ZUNNO team have members from diverse backgrounds and are experienced hackathon winners at ETHIndia (4x) and EncodeClub London. They worked with top companies/projects like Oracle, Dell EMC, Mina, Arbitrum, Midnight protocol, etc. One of the team members, Parth also graduated from the PBA Singapore edition with distinction.

### Team Code Repos

- [https://github.com/thezunno](https://github.com/thezunno)

GitHub accounts of all team members:

- [https://github.com/mittal-parth](https://github.com/mittal-parth)  
- [https://github.com/ronykris](https://github.com/ronykris)  
- [https://github.com/ayush4345](https://github.com/ayush4345)  
- [https://github.com/nshri1609](https://github.com/nshri1609)  
- [https://github.com/Saurus9290](https://github.com/Saurus9290)

### Team LinkedIn Profiles

- [https://www.linkedin.com/in/mittal-parth/](https://www.linkedin.com/in/mittal-parth/)  
- [https://www.linkedin.com/in/krishanu-dhar](https://www.linkedin.com/in/krishanu-dhar)  
- [https://www.linkedin.com/in/ayush45](https://www.linkedin.com/in/ayush45)  
- [https://www.linkedin.com/in/nikhilshrivass](https://www.linkedin.com/in/nikhilshrivass)  
- [https://www.linkedin.com/in/saurabhshettyofficial](https://www.linkedin.com/in/saurabhshettyofficial)

## Development Status :open\_book:

- NA, idea stage.

## Development Roadmap :nut\_and\_bolt:

### Overview

- **Total Estimated Duration:** 2.5 months  
- **Full-Time Equivalent (FTE):** 1.84
- **Total Costs:** 39500

### Milestone 1 — Development, Early Testing and Refinement stage

- **Estimated duration:** 1.5 month  
- **FTE:**  2  
- **Costs:** 24000 USD

| Number | Deliverable | Specification |
| ----: | :---- | :---- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1\. | Complete game development  | The core logic development will consist following phases: Game Initialisation Sequence Game Play Sequence State Synchronisation Sequence  |
| 2\. | Substrate wallet access management | The development of universal wallet integration will serve following purpose: Connector for all existing ecosystem wallets.  Access management of the users’ profiles/ progress. |
| 3\. | Contracts deployment on testnet | We will deliver a set of PolkaVM-compatible/ v6 ink\! smart contracts that will serve as the backend of the game which will feature following component: Automated rules Fair rewards distribution engine |
| 4\. | Launch beta | Launch of beta version on either of AssetHub testnets (Paseo PAssetHub or Westend AssetHub). |
| 5\. | Community engagement campaigns on testnet | Launch of engagement campaigns to stress-test the beta release. |
| 6\. | Gather feedback on beta release | Collection of feedback through an engagement campaign task. |
| 7\. | Enhance privacy layer | Improve/optimise the core privacy layer which operates via the commit-and-reveal scheme |
| 8\. | Revamp and finalise UI | Switch from functionality-oriented UI to production level UX. |

### 

### Milestone 2 — Strategic Launch & DOT’s Utility Integration

- **Estimated duration:** 1 month  
- **FTE:**  1.375  
- **Costs:** 11000 USD

| Number | Deliverable | Specification |
| ----: | :---- | :---- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains the gameplay as well as the development process and the ink\!ubator bounty experience for the grant. |
| 1\. | Points system launch for the DOT holders/stakers | Introduce DeFi-oriented gamification via points which can be procured by staking DOT/vDOT/gDOT etc. |
| 2\. | Implement ongoing campaigns for retention, and develop an ecosystem rewards program. | Reward points holders from the gamified DeFi yield. |
| 3\. | Expand gameplay features | Add new modes, tournaments, custom decks, etc. |
| 4\. | Official launch with targeted marketing | Deploy ZUNNO on AssetHub mainnet, followup announcements and social media marketing. |

### 

### Milestone 3 — DevOps, operations and advisory by Edgetributor SubDAO

- **Estimated duration:** 2.5 months  
- **FTE:** 0.225  
- **Costs:** 4500 USD

| Number | Deliverable | Specification |
| ----: | :---- | :---- |
| 1\. | DevOps | Guiding and assisting the ZUNNO team with system architecture and integration with AssetHub Parachain. |
| 2\. | Operations | Periodic feedback collection, review strategies, progress reports for the bounty and the Polkadot community. |
| 3\. | Advisory | Introducing the ZUNNO team to the Polkadot ecosystem and bounty quirks/steps, along with the curation of the development scope/proposal. |

...

## Future Plans

- Tentative integrations with JAM services based on the post-JAM ecosystem spectrum.

## Additional Information :heavy\_plus\_sign:

**How did you hear about the Bounty Program?**  
Radha from Web3 Foundation suggested us to apply for the ink\!ubator bounty.
