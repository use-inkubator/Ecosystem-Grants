# Decentralized Oracles

> This document will be part of your agreement and therefore needs to contain all the required information about the project. Don't remove any of the mandatory parts presented in bold letters or as headlines (except for the title)! Lines starting with a `>` (such as this one) should be removed. Please use markdown instead of HTML (e.g. `![](image.png)` instead of `<img>`). 
>
> See the [Grant Program Process](https://github.com/smart-contract-bounty/Wasm-Bounty-01#pencil-process) on how to submit a proposal.
- **Team Name:** Lucky Team
- **Payment Address:** 5FsPMucWPWHGaKD6TiHV2fpbd1497m5sgA7drbBtYic6rhsK.

> :exclamation: *The combination of your GitHub account submitting the application and the payment address above will be your unique identifier during the program. Please keep them safe.*

## Project Overview :page_facing_up:
### Overview

We would like to bring decentralized and trustless oracles for ink! smart contracts.
Now that phat contracts are live on Khala and Phala Networks, we are able to provide decentralized oracles for any ink! smart contracts deployed on the Polkadot ecosystem.
This project will focus to build two oracles:
 - VFR
 - Graph Api Oracles

### Project Details

Recently the Phala team released the Lens Api Oracle.
https://medium.com/phala-network/lensapi-oracle-supercharge-your-web3-social-app-a413c936df2b

This oracle is built on offchain rollup request-response for evm smart contracts.
https://github.com/Phala-Network/phat-bricks/tree/master/phat/contracts/action_offchain_rollup

Our team is applied to the Phala builder program to develop the offchain rollup request-response for ink! smart contracts.

When this milestone will be completed, we would like to use this offchain rollup request-response model to build:
 - VRF Oracle. It should generate cryptographically secure random numbers for ink! smart contracts
 - Graph API Oracle that : 
 -  - accesses SubQuery/SubSquid via an uri
 -  - transform and format the response wia the JS engine developed by the Phala team
 -  - send the output to the ink! smart contract

For both oracle, we will provide:
 - the phala offchain rollup to compute the VRF or access SubQuery/SubSquid
 - the ink! smart contracts to interact with the offchain rollup
 - a UI to test and play with these smart contracts. For the Graph API Oracle, we will index the data from the dApps Staking on Astar and returns the information about the stakers.
 - a documentation to use these oracles

## Team :busts_in_silhouette:

### Team members

- GuiGou is application architect in Web 2 (Java technology) and progressively work more and more in web3. 
As technical ambassador for Astar and ambassador for Phala, I already write some tutorials to build ink! smart contracts (https://polkaverse.com/11143) and reply about the technical questions on ink! smart contracts via the Astar's discord.

- Arno is web developer and ambassadors for Polkadot, Phala, Acala and Talisman Sentinel


### Team's experience

We developed the dApp Lucky.
Lucky is a dApp built on top of dApp Staking in Astar Network. If the user stakes on the Lucky dApp, he will still receive the rewards from the dApp Staking, and furthermore, he will have a chance to win extra rewards. It’s a no-loss lottery!
The dApp is built with several ink! smart contracts, a subquery indexer, and off-chain workers (scheduled jobs). We plan to replace the scheduled jobs with phat contracts to improve decentralization and demonstrate the interoperability between ink! smart contracts (Shiden/Astar) and ink! phat contracts (Khala/Phala).

The dApp is already live in Shiden.
https://portal.astar.network/shiden/dapp-staking/dapp?dapp=x6ykus6l6ch4eozitzsyjscxh2agk2ky9g6a2xeu1w9fftp

Website:
https://lucky.substrate.fi/

Documentation:
https://polkaverse.com/11201/introducing-the-d-app-lucky-37998

The dApp was awarded in the Polkadot Hackathon Europe Edition, in the category ink! Smart Contracts.


### Team Code Repos

GitHub accounts of team members:
  https://github.com/GuiGou12358
  https://github.com/arnobase

GitHub for the smart contracts used in the dApp Lucky:
  https://github.com/GuiGou12358/lucky-contracts


## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):**  1 FTE
- **Total Costs:** 14,000 USD

### Milestone 1  — VRF

- **Estimated duration:** 1 month
- **FTE:**  1 FTE 
- **Costs:** 7,000 USD

|  Number | Deliverable                                             | Specification                                                                                                                                                                                                                               |
|--------:|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                                                 | Apache 2.0                                                                                                                                                                                                                                  |
| **0b.** | Documentation                                           | We will provide documentation that explains how a user can use these oracles and test them                                                                                                                                                  |
| **0c.** | Testing and Testing Guide                               | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests.                                                                             |
|      1. | Phat contract: VRF Oracle                               | We will deliver the phala offchain rollup to compute the VRF                                                                                                                                                                                |
|      2. | Library: crate to connect the client and the VRF Oracle | We will deliver a rust library to allow the developers to integrate easily the VRF Oracle into the ink! smart contracts. The crate will contain the traits and a default implementation for these traits following the OpenBrush standards. |
|      3. | Ink! smart contract: vrf client                         | We will deliver an ink! smart contracts to test the VRF Oracle                                                                                                                                                                              |
|      4. | UI                                                      | We will deliver an simple UI to test and play with the delivered smarts contracts                                                                                                                                                           |


### Milestone 2 — Graph Api Oracle

- **Estimated duration:** 1 month
- **FTE:**  1 FTE
- **Costs:** 7,000 USD

|  Number | Deliverable                                    | Specification                                                                                                                                                                                                                                     |
|--------:|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                                        | Apache 2.0                                                                                                                                                                                                                                        |
| **0b.** | Documentation                                  | We will provide documentation that explains how a user can use these oracles and test them                                                                                                                                                        |
| **0c.** | Testing and Testing Guide                      | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests.                                                                                   |
|      1. | Phat contract: Graph Api Oracle                | We will deliver the phala offchain rollup to query SubQuery/SubSquid                                                                                                                                                                              |
|      2. | Library: crate to develop easily the client    | We will deliver a rust library to allow the developers to integrate easily the Graph Api Oracle into the ink! smart contracts. The crate will contain the traits and a default implementation for these traits following the OpenBrush standards. |
|      3. | Ink! smart contract: Graph Api Oracle client   | We will deliver an ink! smart contracts to test the Graph Api Oracle                                                                                                                                                                              |
|      4. | UI                                             | We will deliver an simple UI to test and play with the delivered smarts contracts                                                                                                                                                                 |



## Future Plans

We will help other teams to use these oracles and we will provide the help to customize them in function of their business.

We will deploy these oracles as phat bricks to allow the developers to deploy custom, no-code oracles in few minutes!

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Personal recommendation of the Phala Team.

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
We already build the library to query and call ink! smart contracts inner phat contracts:
https://github.com/GuiGou12358/phala-blockchain/commits/master/crates/pink-libs/subrpc/src/lib.rs

- If there are any other teams who have already contributed (financially) to the project.
We are applied in the Phala Builder Program
