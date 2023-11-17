# ink! War Games

- **Team Name:** SO/DA zone
- **Payment Address:** 12NsfdvxfCTAfAvMRxYQewgxhihqkY3UsKxp1tDrCfW8xf62

## Project Overview :page_facing_up:

### Overview

ink! War Games is a system to help developers learn about secure practices for ink! smart contracts through war game challenges.

A decentralized application (dapp) presents participants with a list of available challenges and provides information about the current participant status in the game. From this interface, participants can select a challenge to solve and access the challenge information and war game tools within its context. All data regarding challenges and achievements is available on chain.

### ink! Ecosystem Impact

The project aims to educate smart contract developers about security practices in a gamified manner. It also serves as a means to engage the developer community through mechanisms such as rewards, leaderboard, new challenge announcements, and more.

### Project Details

The system comprises a set of ink! smart contracts and a decentralized web application. It serves as an equivalent to [Ethernaut](https://ethernaut.openzeppelin.com/) for Substrate networks.

#### Smart Contracts

The system consists of two base contracts, Games Hub and Challenge, which provide the essential functionality for managing and instantiating challenges, as well as tracking player participation and outcomes.

Each specific challenge will have its own contract implementation.

**Games Hub (WOPR[¹])**

This set of contracts are responsible for registering new challenges, instantiating them for players, submitting challenge completions, and tracking game statistics.

[¹]: War Operation Plan Response, pronounced "whopper", see [WarGames](https://en.wikipedia.org/wiki/WarGames)

**Challenge**

This interface provides methods for instantiating a specific challenge and verifying successful completion by a player.

**Specific Challenges**

For this grant, we will port the Ethernaut levels that are applicable to ink! and do not require attacker contract logic (e.g., Token, Instance, Fallback, etc.).

We will investigate in detail which Ethernaut levels are applicable to ink! and can be ported. We will verify our findings with OpenZeppelin and ink! team before implementation.

We have decided to utilize the concept of challenges to enable the association of multiple challenges with a single level or any other relevant tag. This approach will facilitate more engaging reward mechanisms, such as awarding points based on the level of the challenge completed.

### Decentralized Web Application

The web application will show players the challenges that are registered in the `Game Hub`, along with their associated source code and multimedia content. The multimedia content includes the challenge description, hero images, and challenge metadata. The app should  support the localization of assets.

Players will be able to instantiate a challenge within the app using their wallet account and verify that it has been successfully completed.

We aim to create an engaging and immersive game experience by designing a visually appealing user interface. Here is a screenshot showcasing the concept design:

![ink war games - concept screen](https://drive.google.com/uc?id=1T_9wdCMl3LjExIvrnkviKXyULqcLTdlp)

You can also find a video demo of the concept [here](https://www.loom.com/share/42b308968a6f41f3a3911dcb6d824380)

When considering Ethernaut as a reference, we found its user experience to be somewhat lacking, particularly with the reliance on the integrated browser console as the main _hacking_ tool. To address this, we plan to avoid using the integrated browser console and instead implement an integrated terminal emulator within the browser. This will be achieved by utilizing [xterm.js](http://xtermjs.org/) and a custom ink! shell, as demonstrated in the concept screenshot.


### Technology Stack

**Smart Contracts**
- :squid: ink!

**Decentralized Web App**
- Typescript + React.js
- xterm.js

We will also assess and utilize appropriate tools and libraries within the ink! and Substrate ecosystem.

For implementing contracts with features such as upgradeability, access control, and administration, we will employ the [OpenBrush](https://github.com/Brushfam/openbrush-contracts) contract library.

To interact with the contracts and user wallets, we will make use of [Polkadot.js](https://github.com/polkadot-js/) and, potentially, [useink](https://github.com/paritytech/useink) hooks.

## Team :busts_in_silhouette:

### Team members

- Marc Fornós
- Xueying Wang

### Contact

- **Contact Name:** Xueying Wang
- **Contact Email:** frozen.pomelo@gmail.com
- **Website:** https://soda.zone/

### Legal Structure

N/A

### Team's experience

**Marc Fornós** has been designing and implementing software systems for 20 years. He is an expert in the area of distributed systems and data-intensive applications. His experience ranges from warehouse automation with radio-frequency terminals, to being the technical director of an airline post-sale revenue optimization software-as-a-service platform, generating millions in incremental revenue during eight years of operation. In the recent past, he was in charge of evolving a commercial Ethereum block explorer and bootstrapping an explorer for Substrate-based networks focused on the contracts pallet and ink! smart contracts.

**Xueying Wang** pivoted to software development after completing an MSc. in Aerospace Engineering and has been in the industry for the past eight years. During this time, she pioneered conversational AI assistants for airlines, counting more than 20 assistants in production covering ten languages for customer service, FAQ and in-chat purchases. She also built a scalable publish-subscribe system to trigger actions on flight feed events for the automated agents. She participated in designing a composable Solid POD/RDF data browser and bootstrapping an explorer for Substrate-based networks focused on the contracts pallet and ink! smart contracts.

We applied for, implemented and delivered the following Web3 Foundation grants under our previous employer:

**Wasm contracts explorer**
<br />
[Application](https://github.com/w3f/Grants-Program/blob/master/applications/epirus_substrate_explorer.md)
<br />
[Delivery](https://github.com/w3f/Grant-Milestone-Delivery/pull/527)

**ink! verifier service**
<br />
[Application](https://github.com/w3f/Grants-Program/blob/master/applications/epirus_substrate_phase_2.md)
<br />
[Milestone 1 Delivery](https://github.com/w3f/Grant-Milestone-Delivery/pull/652)
<br />
[Milestone 2 Delivery](https://github.com/w3f/Grant-Milestone-Delivery/pull/742)


### Team Code Repos

- https://github.com/mfornos
- https://github.com/XY-Wang
- https://github.com/frozenpomelo (shared account)

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 6.5 months
- **Full-Time Equivalent (FTE):**  1.5 FTE
- **Total Costs:** 97,500

### Milestone 1 - Smart Contracts

In this milestone we will implement the contracts for Games Hub, Challenge and Specific Challenges as defined in [Smart Contracts](#smart-contracts).

- **Estimated duration:** 2.5 months
- **FTE:**  1.5
- **Costs:** 37,500 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0  |
| **0b.** | Documentation | We will provide both inline documentation of the code and a basic guide on how to set up the game. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests. In the guide, we will describe how to run these tests. |
| 1. | Games Hub implementation | We will implement the set of contracts required for managing the game and collecting statistics. |
| 2. | Challenge interface implementation | We will implement the Challenge contract interface |
| 3. | Specific challenges implementation | We will port the applicable Ethernaut levels to ink! |
| 4. | Deployment to a test network | We will deploy the contracts on a development network for easy testing. |


### Milestone 2 - Decentralized Web Application

In this milestone we will build the web application for users to interact with the contracts implemented in the first milestone.

- **Estimated Duration:** 2 months
- **FTE:**  1.5
- **Costs:** 30,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0  |
| **0b.** | Documentation | We will provide both inline documentation of the code and a basic guide on how to run the application. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile and Docker Compose file(s) to ease deployment. |
| 1. | Web UI  | We will implement the UI as described in [Decentralized Web Application](#decentralized-web-application), including English content. |
| 2. | Public instance | A public instance of the application connected to the development network where game contracts are deployed in Milestone 1. |


### Milestone 3 - Internationalization and Further Gamification

In this milestone we will enhance the game's reach and engagement by implementing support for internationalization and introducing a scoring system. The scoring system will enable us to showcase a global leaderboard, as well as display high scores for each challenge factoring in points per difficulty and the time to complete.

- **Estimated Duration:** 2 months
- **FTE:**  1,5
- **Costs:** 30,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0  |
| **0b.** | Documentation | We will provide both inline documentation of the code and a guide on how to set up the game. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile and Docker Compose file(s) to ease deployment of the UI. |
| 1. | Points system | We will implement the points system in the core Games Hub contracts set. |
| 2. | Updated UI | Internationalization support and multi-language content. We will also add a global leaderboard and high scores for each challenge in the UI. |
| 3. | Public instance | We will update the public instance and deployed contracts to include internationalization and the scoring system. |


## Future Plans

As part of our future plans we aim to implement the following features:
1.  Deploy in additional Substrate testnets that implement the contracts pallet.
2.  NFT badges for completing levels or discovering easter eggs: Similar to the concept of badges on platforms like Github, we will introduce NFT badges that users can earn by successfully completing levels or uncovering hidden easter eggs within the game. These badges will serve as unique digital rewards, enhancing the overall gaming experience.
3.  Points system and leaderboard for challenge proposers: we will implement a points system where challenge proposers can earn points based on the popularity and success of their challenges. These points will contribute to their ranking on a leaderboard, fostering a sense of achievement and recognition among the community.
4.  Duels/Moshpit - Challenge other players to solve challenges faster: We plan to introduce a multiplayer feature where players can engage in duels or participate in a "moshpit" mode. In these modes, players can challenge each other to solve specific challenges and compete against one another to complete them in the shortest amount of time. This feature will add a competitive element to the gameplay and provide an avenue for players to showcase their skills against others.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Personal recommendation from Michael and Hernando from the ink! team.
