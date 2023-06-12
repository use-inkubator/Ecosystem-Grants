# Counter.ink

- **Team Name:** stated.tech
- **Payment Address:** 14HhananesXW9VXWpiw4SKmTZ9zAuPaRryk7Fk1Y4a7R436U

## Project Overview :page_facing_up:
### Overview

A PoC for a smart-contract based OTC desk built with the ink! framework on the Azero blockchain, focused on permissionlessness and privacy. This OTC desk will be a v1 and a proof of concept for further development on Liminal, and deployment of a matching engine for DotSama by using parathreads and XCM.

### Project Details

We plan to build and deploy this OTC smart contract on Azero, which will enable cross-contract peer-to-peer trading for experienced traders as well as early supporters of newly issued projects. Users will be able to create and execute trades without the need for any DEX listing or existing liquidity. We will use the ink! framework to build this smart contract, and partial fill for enhanced liquidity.

## Team :busts_in_silhouette:

### Team members

- David Germain (Product Manager)
- Matthieu Moreau (Blockchain Developer)
- JS Full Stack Developer (external)
- UI/UX designer (external)

### Contact

- **Contact Name:** stated.tech
- **Contact Email:** stated.tech@proton.me
- **Website:** http://www.stated.tech/

### Legal Structure

- **Registered Address:** Avenue Edouard Michelin Tours, 75 RUE DE LONGCHAMP 75116 PARIS.
- **Registered Legal Entity:**  MATTHIEU MOREAU (French Siret : 889280939), DAVID GERMAIN 

### Team's experience

Our team has extensive experience in blockchain development, particularly on the Substrate framework. Our Substrate Blockchain Framework Expert Matthieu has done the Polkadot Academy in Buenos Aires in February and David has worked with parachain teams to act as a Product Manager, notably around Kabocha Network on Kusama. We also have worked on EVM smart contract based DeFi projects, particularly with derivatives such as perps and options protocols.

### Team Code Repos

- https://github.com/stated-tech/
- https://github.com/Matthiewm23

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/david-germanowicz-57151a236
- https://www.linkedin.com/in/matthiew23/


## Development Status :open_book:

- We already have a prototype ready to be implemented (90% finished): https://www.figma.com/proto/Q10yEXOp0rha3dlY1T7Qt0.
- A first version of our smart contract (not finalized and not tested) can be found here (70% finished): https://github.com/stated-tech/Counter.ink. This is the main logic that our smart contract will be based on. We will need to finalize it with all features, test it in order to make sure no attack is possible and integrate it to the front end.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):**  3 FTE
- **Total Costs:** 30 000 USD

### Milestone 1 Maker contract — Trade setup

- **Estimated duration:** 1.5 month
- **FTE:**  2
- **Costs:** 15,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains how we created the Maker Contract for trade setup, with a step-by-step guide on how to setup your own OTC trade or add a contract by its address. |
| 0f. | Article | We will publish an article/workshop that explains the taking offer or making counter-offer functionality implemented in the Taker Contract. The article will be aimed at developers and will describe the technical aspects of the implementation. |
| 1. | Smart Contract : Maker Contract | We will create an ink! smart contract that will allow users to create trade offers with specific terms and conditions, such as price, quantity, and expiration date. The Maker Contract will store this information on-chain and emit events for trade creation. We will allow users to register the assets they want to trade. The user will have the possibility to accept partial fill|
| 2. | Substrate module: Asset Registery | Users will be able to register the assets they want to trade. |
| 3. | Smart Contract : Taker Contract | We will then allow takers to take offers or make counter-offers. |
| 4. | Smart Contract : Partial Fill | If the maker accepted the partial fill, the taker will have the opportunity to accept only a percentage of the trade (e.g the maker sell 10ETH for each 2000 USDT and the taker will only take 5ETH. |
| 5. | Tests and testnet : | We will implement testing procedures to ensure there are no vulnerabilities present. Initial testing will be conducted on the testnet for optimal security assurance.|

### Milestone 2 UI and TSX (React) development

- **Estimated Duration:** 1.5 month
- **FTE:**  4
- **Costs:** 15,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article |We will publish an article/workshop that explains the taking offer or making counter-offer functionality implemented in the Taker Contract. The article will be aimed at developers and will describe the technical aspects of the implementation. |
| 1. | Figma module: UI Design | We will design a user-friendly and intuitive UI for the Maker and Taker contracts. Mockups and wireframes will be made on Figma. We will propose filters to make the user interface more efficient. |
| 2. | React module: Front-end Development | We will develop the front-end of the platform using React, including all necessary components and interactions with the smart contracts. |

## Future Plans

Our team has several exciting plans for the future development of our platform. Here are some of our top priorities:

- Incubation by Azero ecosystem development incubator: This incubation will provide us with valuable resources, mentorship, and networking opportunities to accelerate our development and growth.

- Developing on Liminal for enhanced privacy features: We plan to explore the capabilities of Liminal and develop our smart contract to utilize its privacy features for our users. This will provide an added layer of security and privacy for our users, which is especially important in the world of decentralized finance.

- Add batch transactions for multi-assets OTC trades and NFT support.

Our long-term goal is to build a Parachain on DotSama (or use parathreads) that enables peer-to-peer OTC trades using XCM and ink!. This will create a decentralized and trustless platform for OTC trading, which is currently dominated by centralized exchanges. We may also explore the possibility of integrating with EVM with Shiden/Astar, when cross VM will be enabled. We're planning for this parachain/parathread to build a matching engine to aggregate orders and build a native orderbook dex that grows organically from OTC trades to aggregated orderbook-inspired liquiddity pools.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Medium / Twitter / Element / Announcement by another team / personal recommendation / **All of the above.** We already are strong supporters of Substrate technology and want to contribute to this ecosystem by providing useful and simple usecases ready for adoption.

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done: see development status.
- If there are any other teams who have already contributed (financially) to the project: none.
