# Liquid Staking - okAlice

- **Team Name:** okAlice LS
- **Payment Address:** 1xgDfXcNuB94dDcKmEG8rE9x9JVoqozCBnnitkN9nAe3Nyx


## Project Overview :page_facing_up:

### Overview

The goal of this project is to create an Ink!-based liquid staking solution for Relay chain native tokens with the following functionality:

- Enable users to participate in securing the network by staking their tokens.
- Provide rewards for the staked tokens.
- Offer a derivative token in exchange for the staked token and thus allowing users to utilize the derivative tokens on other dapps or chains, hence the name "liquid staking."

### Ink! Ecosystem Impact

Our Dapp is designed to bring substantial value to the Ink! ecosystem by implementing this DEFI solution on Astar. We expect that this implementation will attract a new influx of users, promoting growth and active participation within the Ink! community. One of our main goals is to remove the need for users to have technical knowledge about the Dapp's backend processes. Our Dapp will offer a straightforward liquid staking solution that can be completed with just a few clicks to stake the tokens.

To facilitate knowledge sharing and inspire future projects, we are committed to making all our code open-source. Moreover, we intend to document our development process through articles and videos, ensuring transparency and easy access for everyone. Our goal is to create an inspiring point of reference for other projects, complementing the existing smart contracts within the Ink! ecosystem.

### Project Details

#### Architecture 

![image](https://github.com/ok-Alice/Ecosystem-Grants/assets/18469570/249ae6ea-e83a-4765-9137-0fc91cc2b48e)

Runtime Components:

- **XCM CE:** the XCM chain-extension facilitates all contract interactions with the nomination pool on the relay chain. This chain-extension will be utilized during the development phase of the project. In the final release, we plan to leverage the native XCM support in Ink!.

Ink! Contracts:

- **issuer-staker:** Implements an asset with PSP22 interface for the derivative token. It handles staking operations on the nomination pool.
- **Validator Selector:** Provides optimized management of the nomination pool based on the validator statistics published by the *Oracle*.
- **Oracle:** Acts as an Oracle, supplying validator statistics to the *Validator Selector* contract.

## Team :busts_in_silhouette:

### Team members

- Wouter Godefroy - https://github.com/zabuxx
- Michael Assaf - https://github.com/michaelassaf
- Kenneth Verbeure - https://github.com/KennethVrb
- Samuel Yi - https://github.com/s-yi
- Dagmar Duportail - https://github.com/DagieDee

### Contact

- **Contact Name:** Wouter Godefroy
- **Contact Email:** wouter@okalice.dev
- **Website:** www.okalice.dev

### Legal structure
- In process.

### Team's experience

Our team's first project in the Polkadot ecosystem was 'Rooster Dao'. This project won 3 prizes during the Polkadot North-America hackathon in the summer of 2022:

- Winner of the Community Choice award
- First place for the RMRK challenges
- Second place for Dao & Governance

Based on the success of 'Rooster Dao', we were invited by the Astar team to adapt the contract for use on the Swanky node.

In 2023, we participated in the Polkadot EU hackathon with a project called 'Pallet Rent'. This project was awarded the first prize in the NFT category.

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
- **Full-Time Equivalent (FTE):**  1.5
- **Total Costs:** 55

### Milestone 1: Validator Selector

- **Estimated Duration:** 2 months 
- **FTE:**  1.5 
- **Costs:** 22,000 USD 

| Number | Deliverable | Specification |
| ------:| ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | Inline documentation of the code and a basic tutorial on using the Substrate nodes and test transactions |
| **0c.** | Testing and Testing Guide | Comprehensive unit tests and a guide on running these tests |
| **0d.** | Docker | Dockerfile(s) for testing the milestone functionality |
| 1. | XCM CE | Implementation of XCM chain-extension for nomination pool manipulation |
| 2. | Oracle | Implementation of a simple oracle for publishing validator statistics |
| 3. | Oracle prov | Backend scripts for provisioning oracle data |
| 4. | Validator Selector | Contract implementation for optimized selection of nomination pool based on oracle's published statistics |

### Milestone 2: Issuer-Staker

- **Estimated Duration:** 2 months 
- **FTE:**  1.5 
- **Costs:** 22,000 USD 

| Number | Deliverable | Specification |
| ------:| ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | Inline documentation of the code and a basic tutorial on using the Substrate nodes and test transactions |
| **0c.** | Testing and Testing Guide | Comprehensive unit tests and a guide on running these tests |
| **0d.** | Docker | Dockerfile(s) for testing the milestone functionality |
| 1. | Issuer-Staker | Contract implementation providing PSP22 interface for the derivative token and managing staking operations |
| 2. | Staking UI | End-user UI implementation for staking operations | 

### Milestone 3: Bootstrap phase

- **Estimated Duration:** 2 weeks
- **FTE:**  1.5 
- **Costs:** 11,000 USD 

| Number | Deliverable | Specification |
| ------:| ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | Inline documentation of the code and a basic tutorial on using the Substrate nodes and test transactions |
| **0c.** | Testing and Testing Guide | Comprehensive unit tests and a guide on running these tests |
| **0d.** | Docker | Dockerfile(s) for testing the milestone functionality |
| **0e.** | Article | Article explaining the implementation of liquid staking in an Ink! environment |
| 1. | XCM CE | Replacement of the CE with Ink! native XCM functions
| 2. | Deploy | Deployment of the contract on Shibuya (Westend) |
| 3. | Documentation | Online documentation detailing the functioning of the first pool instance |
| 4. | Documentation | Online documentation for deploying your own strategy for managing the pool |
| 5. | Audit | External organization audit of the contract |
| 6. | Deploy | Deployment of the contract on Shiden (Kusama) |
