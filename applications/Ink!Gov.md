# Ink!Gov

- **Team Name:** Lakaka Labs
- **Payment Address:** 16d5pX53s9uw3eeFjjLrogsxMBpbTu4cZgApoCvYWEvHWkFV

## Project Overview :page_facing_up:
### Overview

Ink!Gov is a universal governance smart contract built to provide the core building blocks for DAOs within the Polkadot ecosystem, enabling communities to vote with fungible and Nonfungible assets to govern shared resources like treasuries. Ink!Gov aims to fill a crucial gap by providing a dedicated on-chain governance framework for DAOs.

**Category:** Infrastructure.

**Importance:** This project provides essential infrastructure for decentralized coordination and decision making within the ink! ecosystem; while Polkadot's OpenGov offers a robust governance, a flexible equivalent tailored for ink! applications is needed, supplying tools for community ownership, treasury management, and executing contract actions via democratic consensus.

Our interest originates from hands-on experience with comprehensive governance solutions and identifying a corresponding need for such tooling specifically within the ink! smart contract landscape; recognizing the power of on-chain DAO primitives, we aim to bring a versatile and powerful governance system to ink!, incorporating learnings from established frameworks like OpenGov.

### Ink! Ecosystem Impact

Ink!Gov aims to establish a standardized, reusable governance framework by providing a pre-built smart contract and a user interface that developers across the Ink! ecosystem can easily integrate into their projects. This initiative addresses a critical need for consistent, efficient, and accessible governance mechanisms in decentralized applications built with Ink!.

Ink!Gov provides a modular governance standard that simplifies development for Ink!-based teams, allowing them to focus on core innovations rather than rebuilding governance logic. This promotes decentralized governance best practices, and accelerates Ink! adoption within Substrate ecosystems like Polkadot, ultimately fostering innovation, collaboration, and scalability.

### Project Details
Ink!Gov is designed to streamline the creation and management of DAOs, providing developers with modular, reusable tools for decentralized decision-making. The primary goal is to enable seamless integration of governance logic into ink! smart contracts, ensuring full on-chain transparency.

Developing governance systems for DAOs on blockchain poses challenges like double-voting, conflicting executions, and inconsistent states due to distributed participants. InkGov resolves these by providing an ACID-compliant transactional framework, ensuring synchronized asset verification, vote recording, and proposal executions.

Ink!Gov smart contracts will be deployed on the **Polkadot AssetHub** parachain, leveraging its capabilities for handling assets with the `asset pallet` and aligning with parachains utilizing the `revive pallet`.

**Key Benefits**

- **Seamless Connectivity:** Links ink! smart contracts with DAO governance logic.
- **Reliable State Management:** Provides durable storage for DAO configurations, proposals, and votes.
- **Transactional Operations:** Ensures ACID-compliant reads, writes, and executions for consistent governance.
- **Simplified Development:** Offers a modular API for DAO creation, proposal management, and voting.
- **Assethub Integration:** Leverages Polkadot’s AssetHub to support asset-based governance.
- **Authorized Contract Calls:** Secures governance by restricting critical actions to authorized entities, ensuring reliable and tamper-proof DAO decision-making.

**Architectural Diagram**

Ink!Gov smart contracts will be deployed on **Polkadot AssetHub** (for asset-centric logic using the asset pallet). A UI application will interact with these contracts via Substrate RPC calls to create DAOs as well as fungible and non-fungible assets on assethub.

Ink!Gov is divided into:

**Client:** A Rust library integrated within ink! smart contracts.
**API:** Exposed functions for external applications to interact with Ink!Gov contracts.

**Image 1**: System Architecture
![Figure 1: Overview of InkGov system architecture](https://github.com/Lakaka-Labs/imagestore/blob/main/ink!gov/Architecture.png)

**Image 2:** DAO Creation 
![Figure 2: Flowchart of the DAO creation process](https://github.com/Lakaka-Labs/imagestore/blob/main/ink!gov/Creat%20Dao%20Flow.png)

**Image 3:** Voting Process 
![Figure 2: Flowchart of the Vote process](https://github.com/Lakaka-Labs/imagestore/blob/main/ink!gov/vote%20flow.png)

**Image 4:** Contract Call 
![Figure 2: Flowchart of the Contract Call](https://github.com/Lakaka-Labs/imagestore/blob/main/ink!gov/execute%20flow.png)

**Languages**

- **Smart Contract Library:** Written in Rust using ink! v6.
- **External Interaction:** Compatible with Polkadot.js for TypeScript applications.

**Governance Features**

**1. DAO Creation & Customization:** Supports Multi-Signature Wallets, NFT Community DAOs, and Community Token DAOs, enabling governance rules customization using assets.
**2. Vote Escrowed Tokens (veTokens):** Voting power increases by locking tokens, incentivizing long-term engagement.
**3. Treasury Management:** Facilitates staking, yield-generating activities, and resource allocation through community-driven proposals integrated with Polkadot DeFi platforms.
**4. Customizability:** Offers shared or custom governance instances, with customizable frontend options and branding.
**5. Automatic Contract Calls:** Automatically executes the actions of a proposal on a contract once it’s approved through voting.

## Team :busts_in_silhouette:

### Team members

- **Owolabi Precious**
	- Github: [https://github.com/Pr3c10us](https://github.com/Pr3c10us)
- **Eruja Michael**
	- Github: [https://github.com/Fourthe3rd](https://github.com/Fourthe3rd)
- **Umoh Samuel**
	- Github: [https://github.com/umohsamuel](https://github.com/umohsamuel)
- **Esan Richard**
	- Github: [https://github.com/Richardesan](https://github.com/Richardesan)
- **Adekilekun Abdullah**
	- Github: [https://github.com/Abdul-lah001](https://github.com/Abdul-lah001)

### Contact

- **Contact Name:** Owolabi Precious
- **Contact Email:** owo.pre.eno@gmail.com

### Legal Structure

- **Registered Address:** N/A (We are currently operating as an independent team. If the grant is approved, we intend to register a legal entity in a suitable jurisdiction.)
- **Registered Legal Entity:** Not yet registered. Will be established upon grant approval.

### Team's experience

We are a dedicated team of builders united by our passion for crafting high-quality smart contracts. With diverse experience across both Web2 and Web3, we focus on creating robust, high-performance contract solutions that emphasize security, modularity, and performance optimization.

Our contributions include Gitcoin-funded projects such as [**Aikisend**](https://github.com/aikilabs/aikisend) and [**Aikicloud**](https://github.com/aikilabs/aikicloud), alongside hands-on experimentation with cross-chain technologies including XCM, ISMP, and the POP API.

As alumni of the PBAX program, we’ve been deeply immersed in the technical and cultural landscape of the Polkadot ecosystem. We remain actively engaged in the developer community sharing insights, exploring cutting-edge tools, and collaborating to push the boundaries of what ink! can achieve. With Ink!Gov, we’re channeling this experience into a project aimed at elevating governance standards across the ecosystem.

### Team Code Repos

- [https://github.com/aikilabs/aikisend](https://github.com/aikilabs/aikisend)
- [https://github.com/aikilabs/aikicloud](https://github.com/aikilabs/aikicloud)
- [https://github.com/Lakaka-Labs/Lakaka-Gov](https://github.com/Lakaka-Labs/Lakaka-Gov)

### Team Github Repos

- [https://github.com/Pr3c10us](https://github.com/Pr3c10us)
- [https://github.com/umohsamuel](https://github.com/umohsamuel)
- [https://github.com/Richardesan](https://github.com/Richardesan)
- [https://github.com/Abdul-lah001](https://github.com/Abdul-lah001)
- [https://github.com/Fourthe3rd](https://github.com/Fourthe3rd)

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 6 months
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 41,000 USD

### Milestone 1 - Smart Contract Development

- **Estimated duration:** 3 month
- **FTE:** 2 FTE
- **Costs:** 19,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can deploy the InkGov smart contracts on a local Polkadot node (and demonstrate interactions simulating deployments on AssetHub/POP Network) and interact with them using test transactions to demonstrate governance functionality. |
| **0c.** | Testing and Testing Guide |Core smart contract functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests using Rust’s testing framework. |
| **0d.** | Docker | We will provide a Dockerfile that sets up a complete environment for compiling, testing, and interacting with the Ink! Gov smart contracts. |
| 0e. | Article | We will publish an **article** on Medium that explains what was achieved in this milestone |
| 1. | Smart Contracts: Governance Logic | We will deliver a set of ink! smart contracts that implement proposal creation, voting mechanisms (including weighted voting), and execution of governance decisions based on voting outcomes. |
| 2. | Smart Contracts: Asset Integration | We will develop ink! smart contracts that enable voting with fungible assets and Non Fungible Assets, primarily targeting deployment on AssetHub, ensuring asset interoperability for governance. |


### Milestone 2 - UI Development

- **Estimated Duration:** 2 month
- **FTE:** 2 FTE
- **Costs:** 17,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 4. | UI Component: Dao Interface | We will develop a UI where users can view, create, and manage Daos, as well as creating assets on AssetHub for governance. |
| 5. | UI Component: Proposal Interface | We will develop a UI where users can view, create, and manage governance proposals. |
| 6. | UI Component: Voting Interface | We will create an intuitive interface for users to cast votes using their fungible assets or NFTs, with real-time vote tallying displayed. instructions for voting. |
| 7. | UI Component: Governance Analytics | We will implement analytics tools to visualize voting patterns, proposal outcomes, and participation rates, helping users understand governance trends. |

### Milestone 3 - Debugging & Publicity

- **Estimated Duration:** 1 month
- **FTE:** 1 FTE
- **Costs:** 5,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 8. | Debugging and Polish | We will fix any bugs identified during testing, optimize performance, and enhance the user experience based on feedback from beta testers. |
| 9. | Publicity | We will engage with the Polkadot and ink! communities through forums, social media, and a live demo webinar to promote InkGov and gather feedback. |
| 10. | Final Release | We will deploy Ink!Gov to a live environment (e.g., relevant testnets, then mainnet parachains like AssetHub/POP Network where applicable), making the project publicly available and ready for community adoption. |

## Future Plans
Looking ahead, our roadmap includes several key milestones:

1.  **Ecosystem Integration**: Collaborate with at least five Ink!-based projects by Q4 2025 to integrate Ink! Gov, gathering real-world feedback to refine our solution. Potential partners include DAOs, DeFi protocols, and NFT platforms seeking robust governance.
2.  **Feature Expansion**: Enhance Ink! Gov with advanced governance features, such as quadratic voting, delegated voting, and customizable quorum thresholds, by mid-2026. These additions will cater to diverse use cases and strengthen its utility.
3.  **Community Governance Hub**: Build a standalone platform where Ink!-based projects can showcase their governance setups, share templates, and collaborate on best practices, fostering a self-sustaining community by 2027.
4.  **Sustainability**: Explore a lightweight incentivization model (e.g., optional governance token integration) to ensure long-term maintenance and updates, while keeping Ink! Gov free and open-source.

## Additional Information :heavy_plus_sign:
**How did you hear about the Bounty Program?**

Recommendation from a colleague.
