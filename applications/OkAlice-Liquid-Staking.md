# Liquid Staking - okAlice

- **Team Name:** okAlice LS
- **Payment Address:** 1xgDfXcNuB94dDcKmEG8rE9x9JVoqozCBnnitkN9nAe3Nyx


## Project Overview :page_facing_up:
### Overview

The goal of this project is to create an Ink! based liquid staking solution with the following functionality:
- Users can participate in securing the network by staking their tokens.
- Receive rewards for their staked tokens.
- Receive a derivative token in exchange for the staked token, which they can use on other dapps or chains, hence the name liquid staking.

### Ink! Ecosystem Impact

Regarding the value that the Ink! ecosystem can derive from our Dapp, we plan to deploy it on Astar and hope that it will bring in a whole new wave of users into the Ink! ecosystem. Our aim is to eliminate the need for users to have technical knowledge about the back-end of the Dapp.
We will make all of our code open-source, and we plan to document our development journey through articles and videos. We hope that our Dapp can serve as an inspiration for future projects alongside the existing smart contracts.


### Project Details

#### Architecture 

![image](https://github.com/ok-Alice/Ecosystem-Grants/assets/18469570/249ae6ea-e83a-4765-9137-0fc91cc2b48e)

Runtime Components:

- **XCM CE:** XCM chain-extension for all contract interactions with the nomination pool on the relay chain. This chain-extension will only be used during development phase of the project. We anticipate to use Ink! native XCM support in our final release.

Ink! Contracts:

- **issuer-staker:** Implements an asset with PSP22 interface for the derivative token. Manages staking operations on the nomination pool.
- **Validator Selector:** Optimized management of nomination pool based on the validator statistics published by *Oracle.* 
- **Oracle:** Oracle providing validator statistics to the *Validator Selector* contract

## Team :busts_in_silhouette:

### Team members

- Wouter Godefroy - https://github.com/zabuxx
- Michael Assaf - https://github.com/michaelassaf
- Kenneth Verbeure - https://github.com/KennethVrb
- Samuel Yi - https://github.com/s-yi

### Contact

- **Contact Name:** Wouter Godefroy
- **Contact Email:** wouter@okalice.dev
- **Website:** www.okalice.dev

### Team's experience

Our first project that we built in the Polkadot ecosystem was ‘Rooster Dao’. The project [won 3 prizes](https://devpost.com/software/rooster-dao?utm_campaign=winner_email&utm_content=submission_won&utm_medium=tweet&utm_source=twitter) during the Polkadot North-America hackathon in the summer of 2022:
- Winner of the community choice
- First place for the RMRK challenges
- Second place for Dao & Governance
Based on this project we have been invited by the Astar team to adapt the Rooster Dao’ contract to be usable on Swanky node.
In 2023 we participated in the Polkadot EU hackathon with a project called ‘Pallet Rent’. The project won the first prize in the NFT category.


### Team Code Repos

- https://github.com/ok-Alice
- https://github.com/RoosterDao

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/kenneth-verbeure-2b151571/
- https://www.linkedin.com/in/michael-assaf/
- https://www.linkedin.com/in/woutergodefroy/
- https://www.linkedin.com/in/dagmar-duportail-50919150/
- https://www.linkedin.com/in/samuel-yi-54796b141/
- https://www.linkedin.com/in/am-prajwal/



## Development Status :open_book:

## Development Roadmap :nut_and_bolt:

### Overview 

- **Total Estimated Duration:** 5 months
- **Full-Time Equivalent (FTE):**  1,5
- **Total Costs:** 55

### Milestone 1 Validator selector

- **Estimated duration:** 2 month 
- **FTE:**  1,5 
- **Costs:** 22,000 USD 


| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | XCM CE | We will write the XCM chain-extension allowing nominationpools manipulating |
| 2. | Oracle | Implement simple oracle that allows publication of validator statistics |
| 3. | Oracle prov | Implement backend scripts for provisioning oracle of data |
| 4. | Validator Selector | Implement contract for optimized selection of nomination pool based on the validator statistics published by *Oracle.* |


### Milestone 2 Issuer-Staker

- **Estimated duration:** 2 month 
- **FTE:**  1,5 
- **Costs:** 22,000 USD 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Issuer-Staker | Implement contract to provide PSP22 interface to an asset for the derivative token and managing staking operations |
| 2. | Staking UI | Implement end-user UI for staking operations | 

### Milestone 3 Bootstrap phase

- **Estimated duration:** 2 weeks
- **FTE:**  1,5 
- **Costs:** 11,000 USD 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains how liquid staking was implemented in an Ink! environment |
| 1. | XCM CE | Replace the CE with Ink! native XCM functions
| 2. | Deploy | We will deploy an instance of the contract on Shibuya(Westend) |
| 3. | Documentation | We will provide online documentation detailing functioning of first pool instance |
| 4. | Documentation | We will provide online documentation for deploying your own strategy for managing pool |
| 5. | Audit | We will have an external organisation audit the contract |
| 6. | Deploy | We will deploy an instance of the contract on Shiden(Kusama) |


