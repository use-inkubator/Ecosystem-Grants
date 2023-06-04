# Liquid Staking - okAlice

- **Team Name:** okAlice LS
- **Payment Address:** 1xgDfXcNuB94dDcKmEG8rE9x9JVoqozCBnnitkN9nAe3Nyx


## Project Overview :page_facing_up:
### Overview

The goal of this project is to create an Ink! based liquid staking solution with the following functionality:
- Users can participate in securing the network by staking their tokens.
- Receive rewards for their staked tokens.
- Receive a derivative token in exchange for the staked token, which they can use on other dapps or chains, hence the name liquid staking.
- Participate in the validator selection through an on-chain governance.

### Ink! Ecosystem Impact

Regarding the value that the Ink! ecosystem can derive from our Dapp, we plan to deploy it on Astar and hope that it will bring in a whole new wave of users into the Ink! ecosystem. Our aim is to eliminate the need for users to have technical knowledge about the back-end of the Dapp.
We will make all of our code open-source, and we plan to document our development journey through articles and videos. We hope that our Dapp can serve as an inspiration for future projects alongside the existing smart contracts.


### Project Details



![image](https://github.com/ok-Alice/docs/assets/18469570/9d784a76-98f3-4bca-b019-d9358e93c3a7)

Components:

- **XCM CE:** XCM chain-extension for all contract interactions with the nomination pool on the relay chain. This chain-extension will only be used during development phase of the project. We anticipate to use Ink! native XCM support in our final release.
- **issuer-staker:** Implements an asset with PSP22 interface for the derivative token. Manages staking operations on the nomination pool.
- **Validator Selector:** Optimized management of nomination pool based on the validator statistics published by *Oracle.* 
- **Oracle:** Oracle providing validator statistics to the *Validator Selector* contract

**⚠️ okAlice TODO ⚠️**


We expect the teams to already have a solid idea about the project expected final state. Therefore, we ask the teams to submit (where relevant):

- Data models / API specifications of the core functionality
- An overview of the technology stack to be used
- Documentation of core components, protocols, architecture, etc. to be deployed
- PoC/MVP or other relevant prior work or research on the topic
- What your project is _not_ or will _not_ provide or implement
  - This is a place for you to manage expectations and to clarify any limitations that might not be obvious
- Do you need an audit for the contacts? **YES/NO**
(don’t add it as part of Milestones! The auditor will be chosen among Auditor track participants)
- CATEGORY: Infrastructure OR Canary Dapp OR Technical Showcase


Things that shouldn’t be part of the application:
- The (future) tokenomics of your project 
- For non-infrastructure projects—deployment and hosting costs, maintenance or audits
- Business-oriented activities (marketing, business planning), events or outreach


## Team :busts_in_silhouette:

### Team members

- Wouter Godefroy - https://github.com/zabuxx
- Michael Assaf - https://github.com/michaelassaf
- Kenneth Verbeure - https://github.com/KennethVrb
- Samuel Yi - https://github.com/s-yi

### Contact

**⚠️ okAlice TODO ⚠️**

- **Contact Name:** Full name of the contact person in your team
- **Contact Email:** Contact email (e.g. john@duo.com)
- **Website:** Your website

### Legal Structure

**⚠️ okAlice TODO?? ⚠️**

- **Registered Address:** Address of your registered legal entity, if available. Please keep it in a single line. (e.g. High Street 1, London LK1 234, UK)
- **Registered Legal Entity:** Name of your registered legal entity, if available. (e.g. Duo Ltd.)

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

**⚠️ okAlice TODO ⚠️**

- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to building this template,

## Development Roadmap :nut_and_bolt:

![image](https://github.com/ok-Alice/docs/assets/18469570/9d784a76-98f3-4bca-b019-d9358e93c3a7)

Components:

- **XCM CE:** XCM chain-extension for all contract interactions with the nomination pool on the relay chain.
- **issuer-staker:** Implements an asset with PSP22 interface for the derivative token. Manages staking operations on the nomination pool.
- **Validator Selector:** Optimized management of nomination pool based on the validator statistics published by *Oracle.* 
- **Oracle:** Oracle providing validator statistics to the *Validator Selector* contract

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


