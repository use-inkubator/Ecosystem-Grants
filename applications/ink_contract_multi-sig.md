# Ink! Contract Multi-Sig
- **Team Name:** Altoros LLC (dba Protofire DAO)
- **Payment Address:** Polkadot Relay Chain: 14YXgiAqian6PWkABXGVhKB43tmbqMwscHLdhHi1qQVBeVQM

## Project Overview :page_facing_up:
### Overview

To onboard developers, blockchain networks must provide developers with a set of essential building blocks. We call them a “Minimum Viable Infrastructure.” Without offering essential services, the unique capabilities of the Smart Contract Pallet are not accessible to consume. We identified this on any chain implementing contracts pallet.
At Protofire, we specialize in removing blockers that prevent developer ecosystem organic growth. 
In this proposal, we will address one of these blockers: the lack of a multi-sig wallet that could be edited without changing its address, providing a smooth workflow and a desirable user experience. 
It is an essential tool for: 
 - DAOs and individuals to manage cryptocurrency assets 
 - Interacting with Smart Contracts in a secure manner 

We have already implemented the Gnosis Safe multi-sig wallet in Astar. Still, that functionality has a narrow scope because is constrained to the EVM Pallet. So, we intend to bring similar functionalities to any substrate chain that supports Contract Pallet by implementing an Ink! smart contract with a user interface focused on the user experience.

### Project Details

After conducting research into the [Native Multisig](https://wiki.polkadot.network/docs/learn-account-multisig), we have concluded that for an address generated crytpographically there are some serious limitations such as:
  1. Fixed threshold. 
  2. Owners of the multisig cannot be added or removed.
  3. User needs to reserve tokens to pay for transaction storage.
 
We plan to implement our approach through a series of steps:

#### <a name="step1"></a>1.- Discovery & Proof of Concept (PoC) phase 

We will initiate the project with a thorough Discovery & Proof of Concept phase. At this stage, we will delve into the existing implementations and explore how we can enhance their value. The primary objective of this phase is to create a basic ink! smart contract that can interact with other contracts on behalf of the owners. During this phase, we expect to detect potential challenges. However, we are confident that our experienced team will be able to find the best strategies to overcome them, which can only be fully understood when the project has been initiated.

By undertaking this approach, we aim to gain a comprehensive understanding of the current landscape and identify the areas where we can introduce innovative solutions. This will facilitate the development of a robust and effective smart contract that can fulfill the project's requirements.

One of the major limitations we highlighted in the proposal is the inability to add or remove owners of the multisig wallet once it is created. To address this, our design will incorporate methods in the smart contract that allows this flexibility.

Our ink! multisig smart contract will maintain an array of wallet owners and a threshold number that will be used to validate the transactions. When a proposal to add or remove an owner is created, owners of the wallet will have to confirm the change. If the number of confirmations crosses the defined threshold, the change will be committed.

#### <a name="step2"></a>2.- Multi-sig Mininimum Viable Product (MVP)

As a next step, we will combine the insights gained from our research with our experience in implementing multi-sig solutions in EVM environments. Drawing on our expertise in multi-sig architecture and lessons learned from building on top of Safe, we aim to develop an MVP that not only incorporates multi-sig logic in an ink! smart contract, but also provides an exceptional user experience through a well-designed user interface.

In considering the requirements of large multi-sig contracts, we will also evaluate the need for a backend that reduces transaction costs and improves user interactions. Through this approach, we are confident that we can develop a robust, user-friendly multi-sig solution that meets the project's goals and provides value to its users.

#### UI Wireframes
>Note: These are just wireframes, the final UI design will be done by our UI/UX designer.

- Select type of contract call

![type](https://github.com/protofire/Ecosystem-Grants/blob/assets/assets/image0.png)

---

- Provide address and metadata

If you choose to interact with a custom contract you have to provide the following:

![metadata](https://github.com/protofire/Ecosystem-Grants/blob/assets/assets/image1.png)

---

- Choose the method and provide parameters

![method](https://github.com/protofire/Ecosystem-Grants/blob/assets/assets/image2.png)

---

To summarize, what we will do:

- Build an ink! smart contract-based multi-sig that interacts with the Contract Pallet. 
- Develop a user-friendly front-end for interacting with the smart contract.
- Evaluate the need for a backend to reduce transaction costs and improve user interactions in large multi-sig contracts, presenting a report with pros and cons of it.

- Technology stack: Ink!, Rust, React, NextJS, TypeScript 



## Team :busts_in_silhouette:

### Team members

- Diego Torres (Team leader / Product Owner)
- Marina Munilla (Project Manager)
- Gabriel Gonzalez (Rust Engineer)
- Luca Auet (Rust Engineer)
- Nickolai Zhiltsov (Consultant Safe Engineer)
- Agustin Longoni (UI/UX Designer)
- Henry Palacios (Front-end engineer)
- Matias Dastugue (Front-end engineer)

### Contact

- **Contact Name:** Diego Torres 
- **Contact Email:** diego@protofire.io
- **Website:** protofire.io

### Legal Structure

- **Registered Address:** 1607 Ponce de Leon Avenue, GM-06, SAN JUAN, PR, 00909
- **Registered Legal Entity:** Altoros LLC

### Team's experience

Protofire DAO team:
 - Worked as part of the Gnosis team on delivery of web and desktop versions of Gnosis Safe. 
 - Delivered Gnosis Safe Apps (such as Compound, Synthetix Mintr Safe App, designed ENS Manager).
 - Created a devkit to improve the synchronization of the code in the Gnosis DApps.
 - Is a Gnosis Chain and Gnosis Beacon Chain validator.
 - Have been deploying and maintaining Gnosis Safe instances on several networks: Astar EVM Pallet, Evmos, Velas, Moonbeam to name a few.
 - Is an active member of the Safe community (Safe Guardians); we use our power to contribute positively to the ecosystem, aligning with Safe vision to drive the adoption of smart contract wallets.

Polkadot ecosystem experience:

- Protofire DAO team is currently delivering [Polkadot Contract Wizard](https://github.com/w3f/Grants-Program/blob/master/applications/polkadot-contract-wizard.md#step1) that provides the entry point for the next generation of web3 users and developers.
- Two team members (Luca and Gabriel) have graduated from Blockchain Polkadot Academy.
- We won [Polkadot Hachathon 2022: Blockchain Tooling category](https://polkadothackathonlatam.com/proyecto-inner/LactobaciloGG/usuario-single/)
- Our DevOps team have built collators and validators tested by Parity.

### Team Code Repos

- https://github.com/protofire/polkadot-contract-wizard.git
- https://github.com/protofire/ink-compiler-be.git
- https://github.com/protofire/safe-eth-py
- https://github.com/protofire/safe-deployments
- https://github.com/protofire/safe-react-apps
- https://github.com/protofire/moonbeam-web-core
- https://github.com/protofire/moonbeam-transaction-service
- https://github.com/protofire/moonbeam-safe-react
- https://github.com/protofire/solhint
- https://github.com/protofire/blockchain-learning-path


GitHub accounts of team members.
- https://github.com/nick8319 <Nickolai Zhiltsov>
- https://github.com/GabrielCamba <Gabriel Gonzalez>
- https://github.com/0xLucca <Luca Auet>
- https://github.com/alongoni <Agustin Langoni>
- https://github.com/henrypalacios <Henry Palacios>
- https://github.com/matextrem <Matias Dastugue>


### Team LinkedIn Profiles

- https://www.linkedin.com/in/nickolai-zhiltsov/
- https://www.linkedin.com/in/gabriel-nicolas-gonzalez/
- https://www.linkedin.com/in/lucaauet/
- https://www.linkedin.com/in/agustinlongoni/
- https://www.linkedin.com/in/henrydpalacios/
- https://www.linkedin.com/in/matiasdastugue/
- https://www.linkedin.com/in/diego-torres-borda-94b70912/
- https://www.linkedin.com/in/marina-munilla-25578441


## Development Status :open_book:
We have researched the functionality of Safe, its architecture, and lessons learned from other deployments we have done. We concluded that we will be able to re-use approximately 30% to 40% of the code to accelerate the development process, mainly for front end and usability. Hence we will define an architecture with at least minimum convergence with the Safe functionality.
We have researched Polkadot Native Multisig to understand its capabilities and limitations which are listed in Project Details section. 

### Overview

- **Total Estimated Duration:** 4 months
- **Full-Time Equivalent (FTE):**  2 FTE during first month. 3.5 FTE during subsequent 3 months. 
- **Total Costs:** $ 187360

### Milestone 1 — Discovery & PoC

- **Estimated duration:** 1 month
- **FTE:** 2
- **Costs:**  USD 32,000

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License |  GPLv3 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial**. |
| **0c.** | Testing and Testing Guide | We will provide a testing documentation that validates the contract implementation will be feasible to take to the MVP stage. |
| **0d.** | Docker | There is no Docker to deliver in this phase |
| 1. | Research Document | Research existing limitations regarding Contract Pallet and ink!|
| 2. | Technical Specs Document  | It will cover architecture vision, infrastructure design and final decision on technology stack |
| 3. | Multisig Smart Contract | We will deliver an ink! smart contract with the functionality described under "POC functionality".

POC functionality: 
 - Create a new Multisig Contract with provided list of owners and threshold
 - Propose/confirm/execute transactions on-chain
 - Add/Remove/Swap Owners
 - Change Threshold

### Milestone 2 — MVP (Release 0.1)

- **Estimated Duration:** 3 month
- **FTE:**  3.5
- **Costs:** USD 155,360

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License |  GPLv3 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial**. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains what was done as part of the grant and what was our experience building an ink! multisig for the ecosystem. |
| 1. | Figma file | We will deliver a UX/UI Design of the Multisig wallet user interface.|
| 2. | Multisig Smart Contract | We will deliver the ink! smart contract built on POC phase and evaluate if an improvement is needed for UX and/or security reasons.|
| 3. | Multisig UI | We will deliver a user interface based on the UX/UI designs. It will allow to fully interact with any smart contract and also support PSP Compliant tokens.|
| 4. | Report about the backend | We will deliver a report about the pros and cons of having a backend for the multisig wallet.|

## Future Plans

 - 3rd party Smart Contract Audits.
 - Backend Development:
    - Modules logic (Spending Limit module, ie).
    - Create and approve transactions off-chain.
    - Build an SDK to allow 3rd party developers to integrate with the Multisig.
 - Marketing, business planning, events, and outreach activities to promote the project.
 - Discover business model.


## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?**  Recommendation by Toma Sadova from Astar Network

