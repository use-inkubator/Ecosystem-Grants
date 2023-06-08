# Counter.ink

- **Team Name:** stated.tech
- **Payment Address:** Polkadot payment address.

## Project Overview :page_facing_up:
### Overview

A PoC for a smart-contract based OTC desk built with the ink! framework on the Azero blockchain, which is focused on privacy using zero-knowledge proof. This OTC desk will be a v1 and a proof of concept for further development on Liminal, and deployment of a matching engine on DotSama.

### Project Details

We plan to build this OTC smart contract on Azero, which will enable cross-contract peer-to-peer trading between parties. Users will be able to create and execute trades without the need for any DEX listing or existing liquidity. We will use the ink! framework to build this smart contract, and enable counter-offers for takers.

## Team :busts_in_silhouette:

### Team members

- David Germain (Product Manager)
- Matthieu Moreau (Blockchain Developer)
- JS Full Stack Developer (external)

### Contact

- **Contact Name:** stated.tech
- **Contact Email:** stated.tech@proton.me
- **Website:** http://www.stated.tech/

### Legal Structure

- **Registered Address:** Address of your registered legal entity, if available. Please keep it in a single line. (e.g. High Street 1, London LK1 234, UK)
- **Registered Legal Entity:** Name of your registered legal entity, if available. (e.g. Duo Ltd.)

### Team's experience

Our team has extensive experience in blockchain development, particularly on the Substrate framework. Our Substrate Blockchain Framework Expert Matthieu has done the Polkadot Academy in Buenos Aires in February and David has worked with parachain teams to act as a Product Manager, notably around Kabocha Network on Kusama. We also have worked on EVM smart contract based DeFi projects, particularly with derivatives such as perps and options protocols.

### Team Code Repos

- https://github.com/stated-tech/

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/<team_member_1>
- https://github.com/Matthiewm23

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/<person_1>
- https://www.linkedin.com/in/matthiew23/


## Development Status :open_book:

- A first version not finalized and not tested can be found here : https://github.com/Matthiewm23/OTC_ink. This is the main logic that our smart contract will be based on. 
- We will need to finalize it with all features, test it in order no attack is possible and integrate it to the front end. 

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):**  2 FTE
- **Total Costs:** 30 000

### Milestone 1 Maker contract — Trade setup

- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains how we created the Maker Contract for trade setup, with a step-by-step guide on how to setup your own OTC trade or add a contract by its address. |
| 1. | Substrate module: Maker Contract | We will create a Substrate module that will allow users to create trade offers with specific terms and conditions, such as price, quantity, and expiration date. The Maker Contract will store this information on-chain and emit events for trade creation. |
| 2. | Substrate module: Asset Registery | We will create an ink! smart contract that will allow users to register the assets they want to trade. |
| 3. | Smart contracts | We will integrate the Maker Contract and Asset Registry smart contracts to enable the creation of trade offers using registered assets. |

### Milestone 2 Taker contract — Taking offer or making counter-offers

- **Estimated Duration:** 1 month
- **FTE:**  2
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article |We will publish an article/workshop that explains the taking offer or making counter-offer functionality implemented in the Taker Contract. The article will be aimed at developers and will describe the technical aspects of the implementation. |
| 1. | Substrate module: Taker Contract | We will create a new ink! smart contract that allows takers to take offers or make counter-offers. |
| 2. | Substrate module: Integration | We will integrate the Taker contract with the Maker contract from Milestone 1. |

### Milestone 3 UI and JS (React) development

- **Estimated Duration:** 1 month
- **FTE:**  3
- **Costs:** 12,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article |We will publish an article/workshop that explains the taking offer or making counter-offer functionality implemented in the Taker Contract. The article will be aimed at developers and will describe the technical aspects of the implementation. |
| 1. | Figma module: UI Design | We will design a user-friendly and intuitive UI for the Maker and Taker contracts. Mockups and wireframes will be made on Figma. |
| 2. | React module: Front-end Development | We will develop the front-end of the platform using React, including all necessary components and interactions with the smart contracts. |

## Future Plans

Our team has several exciting plans for the future development of our platform. Here are some of our top priorities:

- Incubation by Azero ecosystem development incubator: This incubation will provide us with valuable resources, mentorship, and networking opportunities to accelerate our development and growth.

- Developing on Liminal for enhanced privacy features: We plan to explore the capabilities of Liminal and develop our smart contract to utilize its privacy features for our users. This will provide an added layer of security and privacy for our users, which is especially important in the world of decentralized finance.

- Add batch transactions for multi-assets OTC trades and NFT support.

Our long-term goal is to build a Parachain on DotSama that enables peer-to-peer OTC trades using XCM and ink!. This will create a decentralized and trustless platform for OTC trading, which is currently dominated by centralized exchanges. We may also explore the possibility of integrating with the EVM with Shiden. We're planning for this parachain to build a matching engine to aggregate orders and build a native orderbook dex that grows organically from OTC trades to aggregated liquiddity pools.

We are excited to continue working on our platform and bringing these plans to fruition.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Medium / Twitter / Element / Announcement by another team / personal recommendation / **All of the above**

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
