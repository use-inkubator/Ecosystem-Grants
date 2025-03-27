# PoKa Mailer

> This document will be part of your agreement and therefore needs to contain all the required information about the project. Don't remove any of the mandatory parts presented in bold letters or as headlines (except for the title)! Lines starting with a `>` (such as this one) should be removed. Please use markdown instead of HTML (e.g. `![](image.png)` instead of `<img>`). 
>
> See the [Grant Program Process](https://github.com/smart-contract-bounty/Wasm-Bounty-01#pencil-process) on how to submit a proposal.
- **Team Name:** Legal name of your team (e.g. Duo)
- **Payment Address:** Polkadot payment address.

> :exclamation: *The combination of your GitHub account submitting the application and the payment address above will be your unique identifier during the program. Please keep them safe.*

## Project Overview :page_facing_up:
### Overview

Please provide the following:

- A npmjs package that integrates an Emailing Client with **Polkadot/Kusama blockchains** and developed and deployed via a **JSON Server** which is run on the Blockchain. It is a deep implimentation of blockchain event handling, SMTP optimization, and CLI tooling. This solution emphasizes **event-driven architecture**, **security**, and **scalability**.
The project bridges traditional communication infrastructure (email) with blockchain technology, enabling **real-world utility** for Polkadot/Kusama dApps while showcasing the ecosystem’s technical versatility.

### Ink! Ecosystem Impact

**Ecosystem Impact**:  
- **Adoption Driver**: Lowers barriers for non-crypto users to interact with blockchain apps via familiar email.  
- **Interoperability**: Works across Polkadot parachains and Kusama, demonstrating cross-chain communication.  

### Project Details

**Benefits**:  
- **Event-Driven Email System**: Triggers emails (via SMTP) based on on-chain events (e.g., transactions, staking rewards, governance votes).  
- **JSON Server on Blockchain**: Stores email templates, user preferences, and event filters as decentralized JSON configurations.  
- **CLI Tooling**: Simplifies deployment, configuration, and monitoring for developers.  

**Who Uses It**:  
- **dApp Developers**: Integrate email notifications into their apps without managing backend infrastructure.  
  - Example: A DeFi platform emails users when their liquidity pool reaches a threshold.  
- **DAO Communities**: Automate governance updates (e.g., proposal deadlines) to non-tech-savvy members via email.  
- **Enterprises**: Use blockchain-verified email trails for compliance (e.g., audit logs stored on Kusama).  

## Team :busts_in_silhouette:

### Team members

- Kunaal Gadhalay
- Salil Harit
- Vaibhav Gadhalay

### Contact

- **Contact Name:** Kunaal Gadhalay
- **Contact Email:** kunaalgadhalay93@gmail.com
- **Website:** 

### Legal Structure

- **Registered Address:** Hyderabad, India 
- **Registered Legal Entity:** Gamma Technologies Pvt Ltd

### Team's experience

Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past.

### Team Code Repos

- https://github.com//<project_1>
- https://github.com/<your_organisation>/<project_2>

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/<team_member_1>
- https://github.com/<team_member_2>

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/<gadhalaykunaal>
- https://www.linkedin.com/<haritsalil>


## Development Status :open_book:

- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to building this template,

## Development Roadmap :nut_and_bolt:

> :exclamation: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Overview

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** $45,000

### Milestone 1 — Basic functionality

- **Estimated duration:** 1 month
- **FTE:**  1,5
- **Costs:** 25,000 USD

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Package Outline | We will create a package module that will be able to set up a simple mailing system on the polkadot Blockchain.|
| 2. | Added Functionality | The functionality will be able to send emails via a email templating engine. |
| 3. | Verification | The package module will be able to verify and validate the system via ink smart contracts. |


### Milestone 2 — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  1,5
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Package Implimentation | We will create a package module that will be able to be run via npm. |
| 2. | Readme.md | A comprehensive Readme file will be developed as a part of the distribution. |
| 3. | CLI Implementation | The package will be implimented and deployed via CLI. |


## Future Plans:

The package is being developed to be deployed as in Production. 

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Medium / Personal Recommendation / etc.

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:
