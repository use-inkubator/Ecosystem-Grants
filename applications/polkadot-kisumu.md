# 🖼️ dApp Template for an ink! contract using the Solidity ABI

- **Team Name:** Polkadot Kisumu
- **Payment Address:** Polkadot payment address.

## Project Overview :page_facing_up:
### Overview

A dApp Template using a Solidity frontend library with an ink! contract that has the Solidity ABI enabled.

This project aims to deliver:
- A smart contract demonstrating CRUD (Create, Read, Update, Delete) functionality, written in ink! and compiled with Solidity ABI support enabled.
- A website frontend for this contract, built using an established Solidity TypeScript (or JavaScript) library/framework (e.g., ethers.js, web3.js, wagmi, etc.).
- MetaMask integration for seamless contract interactions from the frontend.

**Relation to ink! ecosystem:**  
This project bridges the gap between ink! smart contracts and the large ecosystem of Solidity tooling and dApp frameworks, making ink! contracts more accessible to developers familiar with Ethereum tools.

**Category:** Technical Showcase / Canary Dapp  
**Motivation:**  
Our team is passionate about expanding the usability and reach of ink! smart contracts by enabling developers to use familiar Solidity-based frontend tools and workflows.

### Ink! Ecosystem Impact

This template will significantly lower the barrier for Ethereum developers to experiment with and adopt ink! smart contracts. By providing a working example of a CRUD contract with Solidity ABI enabled and a frontend using standard Solidity libraries and MetaMask, the project will:

- Demonstrate interoperability between ink! contracts and Ethereum dApp tooling.
- Serve as a reference implementation for teams wanting to port or build dApps on Polkadot using ink! with minimal friction.
- Encourage more frontend developers to build on Polkadot/Substrate by leveraging their existing skills and tools.
- Promote ink! as a viable smart contract language for projects seeking EVM compatibility and beyond.

### Project Details

- **Data models / API specifications:**  
  The contract will expose CRUD operations for a simple data structure (e.g., a list of records with fields like id, name, value). The ABI will be compatible with Solidity tooling.

- **Technology stack:**  
  - Smart contract: ink! (Rust), compiled with Solidity ABI enabled.
  - Frontend: React (TypeScript), using ethers.js or web3.js for contract interaction.
  - Wallet: MetaMask for user authentication and transaction signing.
  - Tooling: Hardhat/Foundry for frontend contract interaction testing.

- **Documentation:**  
  - Inline code documentation.
  - Step-by-step tutorial for deploying the contract and connecting the frontend.
  - Guide for extending the template for custom use cases.

- **PoC/MVP:**  
  - A working demo contract and frontend will be provided.
  - Example deployment scripts and test cases.

- **Limitations:**  
  - The template will not cover advanced contract patterns (e.g., upgradability, complex access control).
  - No tokenomics or business logic beyond CRUD.
  - No backend server; all interactions are on-chain or via the frontend.

- **CATEGORY:** Technical Showcase / Canary Dapp

- **Business model:**  
  - Open-source template for the community; no direct monetization.
  - Potential for future consulting, support, or premium features.

- **Future production plans:**  
  - Encourage adoption by other teams.
  - Gather feedback and iterate on the template.
  - Explore additional integrations (e.g., wallet providers, more complex contract examples).

## Team :busts_in_silhouette:

### Team members

- Cheryl Owala (Team Leader)
- Allan Robinson
- Fred Gitonga
- Ann Maina
- Quinter Ochieng
- Hillary Ombima

### Contact

- **Contact Name:** Cheryl Owala
- **Contact Email:** owalacheryl@gmail.com
- **Website:** 

### Legal Structure

- **Registered Address:** 
- **Registered Legal Entity:** 

### Team's experience

Our team has extensive experience in smart contract development (ink!, Solidity), frontend dApp development (React, TypeScript), and blockchain integrations. Members have contributed to open-source projects and have backgrounds in both Ethereum and Substrate ecosystems.

### Team Code Repos

- https://github.com/Cherrypick14
- https://github.com/Githaiga22
- https://github.com/fredmunene
- https://github.com/annemaina
- https://github.com/quinter
- https://github.com/hiombima

### Team LinkedIn Profiles

- https://www.linkedin.com/in/allan-robinson-3b54511a4/
- https://www.linkedin.com/in/cheryl-owala-423731191/
- https://www.linkedin.com/in/fredgitonga/
- https://www.linkedin.com/in/hillary-ombima-724430207/
- https://www.linkedin.com/in/maina-anne-37797820b/
- https://www.linkedin.com/in/quinter-ochieng/

## Development Status :open_book:

- Initial research and planning completed.
- Team discussions on architecture and technology stack.
- Some members have prior experience with ink! and Solidity ABI integration.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):** 2
- **Total Costs:** 12,000 USD

### Milestone 1 — Contract & Backend Integration

- **Estimated duration:** 1 month
- **FTE:** 1
- **Costs:** 6,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | Inline code docs and a tutorial for deploying and interacting with the contract. |
| **0c.** | Testing and Testing Guide | Unit tests for all contract functions; guide for running tests. |
| **0d.** | Docker | Dockerfile for local development and testing. |
| 1. | ink! CRUD Contract | Contract with Solidity ABI enabled, supporting create, read, update, delete operations. |
| 2. | ABI Generation | Scripts and documentation for generating and using the Solidity ABI. |

### Milestone 2 — Frontend & MetaMask Integration

- **Estimated Duration:** 1 month
- **FTE:** 1
- **Costs:** 6,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | Frontend usage guide and integration steps. |
| **0c.** | Testing and Testing Guide | Frontend tests for contract interaction. |
| **0d.** | Docker | Dockerfile for frontend deployment. |
| 1. | React Frontend | Website using ethers.js/web3.js to interact with the contract. |
| 2. | MetaMask Integration | Support for MetaMask wallet connection and transaction signing. |
| 3. | Example Deployment | Scripts and instructions for deploying both contract and frontend. |

## Future Plans

- Promote the template to the Polkadot and Ethereum developer communities.
- Gather feedback and iterate on features.
- Explore more advanced contract templates and frontend integrations.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?**  
Personal recommendation and community channels.

- The team has prior experience with ink! and Solidity ABI integration.
- No other teams have contributed financially to this
