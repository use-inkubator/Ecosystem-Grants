# Using Verifiable Offchain Computing in ink! smart contracts

- **Team Name:** Lucky Team
- **Payment Address:** 14ogWEsaFHYk1rDcRMLVApekUd3np4e1ker81tBF6odd39Q9

## Project Overview :page_facing_up:
### Overview

On-chain computation capabilities are inherently limited by blockchain design, which affects all smart contract platforms including ink!. Our project aims to complement ink! smart contracts by providing verifiable off-chain computing capabilities through Phala Cloud's Trusted Execution Environment (TEE), enabling developers to build more complex applications while maintaining blockchain security guarantees.

This solution bridges the gap between blockchain's security and off-chain computational power through:

1. A Professional SDK Suite
   - Enterprise-ready toolkit for seamless smart contract integration
   - Built-in ACID compliance for reliable state management
   - Production-grade security with TEE protection

2. Production-Ready Oracle Suite
   - Price Feed Oracle: Real-time market data integration from CoinGecko
   - VRF Oracle: Cryptographically secure random number generation
   - Graph API Oracle: Universal indexer connectivity (SubQuery, Subsquid, The Graph, ...)

3. Next-Generation AI Integration
   - Full Eliza OS integration for advanced AI capabilities
   - Direct LLM connectivity through Phala Cloud
   - Interactive proof-of-concept with Tic-Tac-Toe game

Each component is designed with enterprise-grade reliability and seamless integration capabilities, deployed on Phala Cloud's secure computing platform.

### Ink! Ecosystem Impact

Verifiable Offchain Computing is crucial for ink! smart contracts because it enables complex computations to be executed off-chain while ensuring their integrity and verifiability on-chain. Here's why it matters:

1. Interoperability with External Systems
   - Smart contracts often need to access external APIs, databases, and oracles.
   - Verifiable Offchain Computing ensures that off-chain data used in smart contracts is correct and tamper-proof.

2. Verifiable Computation
   - To ensure the integrity of off-chain computations, Remote Attestations are generated and Phala L2 Explorer tools simplify trustless verification.

3. Use Cases
   - Rollups: Off-chain execution with verification.
   - Oracles: Retrieve and verify off-chain data for smart contracts.
   - AI: Use AI/LLM in your ink! smart contracts

In summary, Verifiable Offchain Computing provides many benefits and use cases for dApps developed with ink! smart contracts.

### Project Details

#### SDK Details

The SDK will be designed to simplify the connection between smart contracts and dApps deployed on Phala Cloud. 
Its primary goal is to enable transactional and atomic cross-blockchain operations, ensuring seamless integration and interaction.

##### The Challenge
Developing dApps that interact with blockchains can be a common but challenging task, especially when it comes to handling concurrency issues in off-chain programs. 
Without a proper synchronization mechanism, this may end up conflicting between the contracts and dApp deployed on Phala Cloud.

Consider a real-world scenario: a smart contract distributes computation tasks to workers. These workers compete with each other when claiming tasks from the blockchain. Ideally, each task should only be claimed once. However, without coordination among the workers, they might send transactions simultaneously to claim the same task, resulting in inconsistent smart contract states.

Consistent state management is crucial when developing an application that communicates with a blockchain. Developers need a reliable and transactional way to perform operations, where read and write tasks are combined into a single unit and executed atomically on the blockchain. This approach aligns with the ACID principle found in transactional database management systems.

The sdk is here to simplify development by providing a stable, ACID-compliant connection with ink! smart contracts. This eliminates concurrency issues and enables a request-response programming model for seamless interaction between the workers and on-chain smart contracts.

##### Key Benefits
- Seamless connectivity between ink! smart contracts and workers
- Reliable KV-store on blockchains for durable state management
- Transactional (ACID) on-chain KV-store designed for stateful dApps deployed on Phala Cloud
- ACID-compliant read, write, and contract call operations for consistent data handling
- Request-response programming model that simplifies interactions between worker and on-chain smart contracts

##### Note
In 2023, our team built the [Phala's offchain rollup anchor](https://github.com/Phala-Network/phat-offchain-rollup) implementation for ink! smart contracts in the context of Phala Builder.
Even if this sdk is still used in mainnet, it was built with ink! v4, OpenBrush and Phat Contracts. OpenBrush is now deprecated. Phat Contracts are replaced by Phala Cloud. 
The main goal is to provide the same features as [Phala's offchain rollup anchor](https://github.com/Phala-Network/phat-offchain-rollup) but with the latest technologies (ink! v5 or ink! v6 and Phala Cloud compatibility)

##### Languages
The library/crate used in ink! smart contracts will be written in Rust and the latest released ink! version.
The library used in the worker deployed on Phala Cloud will be written in TypeScript and will use the latest version of Polkadot.js api.

#### Price Feed Oracle, VRF Oracle, Graph Api Oracle

In the previous cohort, we released the [decentralized oracles](https://github.com/use-inkubator/Ecosystem-Grants/blob/master/applications/decentralized_oracles.md) built with Phala's offchain rollup anchor.
We want to build the same oracles with the new SDK to ensure the robustness of the new SDK and provide concrete and functional usage examples.
- Price Feed Oracle. The Oracle will read the data from CoinGecko and feed the data in ink! smart contracts
- VRF Oracle. It will generate cryptographically secure random numbers for ink! smart contracts
- Graph API Oracle that: The Oracle will query a SubQuery/SubSquid endpoint and send the output to the ink! smart contract

For both oracles, we will provide:
- The worker to be deployed on Phala Cloud
- The ink! smart contracts to interact with the worker
- A UI to test and play with these smart contracts
- For the Graph API Oracle, we will index the data from the dApps Staking on Astar and return the information about the stakers
- The documentation to use these oracles

The smart contracts will be deployed on testnet.

#### AI Integration in ink! smart contract

We will release a version with the ElizaOS lib to provide AI/LLM into ink! smart contracts.

We will deploy a dApp implementing the Tic-Tac-Toe game with an AI/LLM integration. 
The user will be able to discuss with OpenAI and play some games against the AI even if the LLM is not optimized to play this kind of games.

## Team :busts_in_silhouette:

### Team members

- GuiGou   
  - Discord: guigou12358
  - X: https://twitter.com/GuiGou12358
- Arno
  - Discord - Arno8443
  - X: https://twitter.com/test_ut

- Lucky Team:
  - Discord: https://discord.gg/R8VvUajBGv
  - X: https://twitter.com/LuckyDapp 

### Team's experience

Team Lucky is a passionate group of developers and blockchain enthusiasts focused on building decentralized applications (dApps) that bring the power of blockchain to real-world use cases. 

GuiGou, a developer with over 20 years of experience, joined the web3 space in 2020 and quickly became involved with the Polkadot ecosystem. Initially an ambassador for Astar Network, he later transitioned to developer roles, contributing to various projects in the ecosystem. GuiGou is the creator of the [Lucky dApp](https://lucky.substrate.fi/astar), which was rewarded in the ink! Hackathon (European edition) and is also part of the Ink!ubator program and Phala Builder program. He specializes in ink! smart contract development, with a strong focus on interoperability, decentralized applications, and blockchain security.

Arno, with his 20 years of experience in web2 development and a deep involvement in the web3 ecosystem since 2021, has worked as an ambassador for Polkadot, Acala, Talisman, and Phala Network. Arno brings a strong background in ecosystem engagement and developer education. He has been instrumental in building user interfaces to interact with smart contracts, integrating EVM and Substrate wallets, optimizing decentralized hosting via IPFS, and ensuring real-time synchronization of the UI with blockchain states.

Together, the Lucky team has deployed the Lucky dApp on both [Astar](https://lucky.substrate.fi/astar) and [Shiden](https://lucky.substrate.fi/shiden), the Lotto dApp on [Astar](https://lucky.substrate.fi/lotto/astar) and [Soneium](https://lotto-evm.netlify.app/), a decentralized and multi-chain Lottery.

- Lucky
   - Lucky dApp on [Astar](https://lucky.substrate.fi/astar)
   - [Lucky dApp Presentation](https://youtu.be/hW4OcKYC3YM)
- Lotto
  - Lotto dApp on [Astar](https://lucky.substrate.fi/lotto/astar) and [Soneium](https://lotto-evm.netlify.app/)
  - [Lotto dApp Presentation](https://youtu.be/r3iTKy5NOg4)
  - [Smart Contracts Interaction](https://youtu.be/jwdbL1Mynw8)

### Team Code Repos

- https://github.com/LuckyDapp
- https://github.com/LottoDapp
- https://github.com/decentralized-oracles

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/GuiGou12358
- https://github.com/arnobase


## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 7 months
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** 69,000 USD

### Milestone 1 - SDK Implementation

- **Estimated duration:** 2.5 months
- **FTE:**  1 FTE
- **Costs:** 25,000 USD

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

|  Number | Deliverable                            | Specification                                                                                                                                                                            |
|--------:|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                                | Apache 2.0                                                                                                                                                                               |
| **0b.** | Documentation                          | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide              | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests.                          |
| **0d.** | Docker                                 | We will provide Dockerfile and smart contract artifacts that can be used to test all the functionality delivered with this milestone.                                                    |
|      1. | Library for ink! smart contract        | We will deliver a rust crate to use in ink! smart contract to communicates with workers/dApps deployed on Phala Cloud                                                                    |
|      2. | Library for worker/dApp on Phala Cloud | We will deliver a Typescript library to use in worker/dApp to communicates with ink! smart contract                                                                                      |


### Milestone 2 — Price Feed Oracle

- **Estimated Duration:** 1 month
- **FTE:**  1 FTE
- **Costs:** 8,000 USD

|  Number | Deliverable               | Specification                                                                                                                                                                            |
|--------:|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                   | Apache 2.0                                                                                                                                                                               |
| **0b.** | Documentation             | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests.                          |
| **0d.** | Docker                    | We will provide the Dockerfile to set up the Price Feed Oracle on Phala Cloud                                                                                                            |
|      1. | Smart contract            | We will deliver the ink! smart contracts that will receive data from the oracle                                                                                                          |
|      2. | UI                        | We will deliver a user interface (UI) to interact with the dApp seamlessly                                                                                                               |


### Milestone 3 — VRF Oracle

- **Estimated Duration:** 1 month
- **FTE:**  1 FTE
- **Costs:** 8,000 USD

|  Number | Deliverable               | Specification                                                                                                                                                                            |
|--------:|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                   | Apache 2.0                                                                                                                                                                               |
| **0b.** | Documentation             | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests.                          |
| **0d.** | Docker                    | We will provide the Dockerfile to set up the VRF Oracle on Phala Cloud                                                                                                                   |
|      1. | Smart contract            | We will deliver the ink! smart contracts that will receive data from the oracle                                                                                                          |
|      2. | UI                        | We will deliver a user interface (UI) to interact with the dApp seamlessly                                                                                                               |


### Milestone 4 - Graph API Oracle

- **Estimated Duration:** 1 month
- **FTE:**  1 FTE
- **Costs:** 8,000 USD

|  Number | Deliverable               | Specification                                                                                                                                                                            |
|--------:|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                   | Apache 2.0                                                                                                                                                                               |
| **0b.** | Documentation             | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests.                          |
| **0d.** | Docker                    | We will provide the Dockerfile to set up the Graph API Oracle on Phala Cloud                                                                                                             |
|      1. | Smart contract            | We will deliver the ink! smart contracts that will receive data from the oracle                                                                                                          |
|      2. | UI                        | We will deliver a user interface (UI) to interact with the dApp seamlessly                                                                                                               |


### Milestone 5 - AI Integration with chat message and Tic-Tac-Toe game

- **Estimated Duration:** 2 months
- **FTE:**  1.5 FTE
- **Costs:** 20,000 USD

|  Number | Deliverable               | Specification                                                                                                                                                                            |
|--------:|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                   | Apache 2.0                                                                                                                                                                               |
| **0b.** | Documentation             | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests.                          |
| **0d.** | Docker                    | We will provide the Dockerfile to set up the AI agent on Phala Cloud                                                                                                                     |
|     0e. | Article                   | We will publish an **article** that explains what was done/achieved as part of the grant                                                                                                 |
|      1. | Smart contract            | We will deliver the ink! smart contracts that will communicate with the AI agent                                                                                                         |
|      2. | UI                        | We will deliver a user interface (UI) to interact with the dApp seamlessly                                                                                                               |


## Future Plans

When the sdk will be released, we plan to migrate our current dApps, Lucky and Lotto, on the new sdk.

## Additional Information :heavy_plus_sign:

We participated in the first cohort.
