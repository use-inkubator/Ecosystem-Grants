# Solink


- **Team Name:** Polkadot Kisumu
- **Payment Address:** Polkadot payment address.



## Project Overview :page_facing_up:
### Overview

Solink is a dApp Template using a Solidity frontend library with an ink! contract that has the Solidity ABI enabled.

Solink provides a production-ready template that bridges the Polkadot and Ethereum ecosystems by showcasing ink! contracts with Solidity ABI compatibility. Developers can leverage familiar Ethereum tools (MetaMask, Wagmi, ethers.js) while deploying on Substrate-based chains, combining the best of both worlds - Ethereum's mature tooling ecosystem with Polkadot's superior performance and lower costs.

Solink directly showcases ink! v6's Solidity ABI compatibility feature, one of the ecosystem's most significant interoperability advancements. By providing a complete dApp template that integrates ink! contracts with Ethereum tooling (MetaMask, Wagmi, ethers.js), it serves as both a reference implementation and developer onboarding tool for the ink! community. The template leverages core ink! infrastructure including cargo-contract and the latest ABI generation capabilities, while demonstrating how ink! contracts can seamlessly bridge Substrate and Ethereum ecosystems. This directly supports ink!'s strategic vision of unifying blockchain development experiences and helps validate the practical applications of ink!'s cross-chain compatibility features.

#### Category Choice & Its Importance 
Infrastructure.
The dapp provides essential developer tooling that improves the ink! ecosystem's integration capabilities. By creating a comprehensive template that bridges ink! contracts with Ethereum's mature frontend ecosystem (MetaMask, Wagmi, ethers.js), it serves as foundational infrastructure that enables developers to leverage familiar tools while building on Substrate chains. This infrastructure is critically important because it reduces adoption barriers, accelerates development time, and demonstrates the practical value of ink!'s Solidity ABI compatibility feature - ultimately expanding the developer base by making ink! accessible to the large Ethereum developer community through familiar tooling patterns.

#### Team's Motivation 

As members of the Kisumu Polkadot Community with recent intensive training in Rust and ink! through Polkadot Africa, our team combines diverse expertise in software engineering, design, and product management. Having experienced the learning curve firsthand, we're uniquely positioned to understand the challenges developers face when transitioning to ink! from other ecosystems. This project directly aligns with our mission to significantly improve developer experience by creating infrastructure that reduces learning barriers and development friction. Our goal is to leverage familiar Ethereum tooling patterns to make ink! more accessible, ultimately accelerating ecosystem adoption and empowering developers to build robust applications more efficiently.

### Ink! Ecosystem Impact

#### Infrastructure Application & Adoption:
This template will serve as foundational infrastructure that directly addresses the developer onboarding bottleneck in the ink! ecosystem. The template will be applied by three key user groups: Ethereum developers transitioning to Substrate who can immediately leverage familiar tools (MetaMask, Wagmi, ethers.js) without learning new frontend patterns; ink! developers seeking to tap into Ethereum's mature tooling ecosystem for better UX and faster development cycles; and development teams building production dApps who need proven integration patterns rather than experimental implementations.
#### Concrete Usage Scenarios:
The open-source template provides immediate value through reusable components, integration patterns, and configuration setups that eliminate weeks of trial-and-error development. Teams can fork the repository, customize the CRUD contract for their specific use case (NFT marketplace, DeFi protocol, governance system), and deploy with confidence knowing the Ethereum tooling integration is production-tested. Educational institutions and bootcamps can use it as a teaching resource, while hackathon participants can rapidly prototype cross-ecosystem dApps.
#### Measurable Ecosystem Benefits:
This infrastructure multiplies development efficiency across the ecosystem, instead of each team independently solving Ethereum integration challenges, they can build upon proven foundations. It validates ink!'s Solidity ABI compatibility through real-world usage, encourages broader adoption by reducing technical barriers, and establishes best practices that benefit all future ink! + Ethereum integrations. The template essentially transforms ink!'s interoperability features from documentation into actionable developer infrastructure.

### Project Details

We expect the teams to already have a solid idea about the project expected finl state.
####  Data models / API specifications of the core functionality
##### Core CRUD Contract Interface:
```rust
// Primary data model
#[ink::storage_item]
pub struct Record {
    id: u32,
    title: String,
    description: String,
    owner: AccountId,
    created_at: u64,
    updated_at: u64,
}

// Contract storage
#[ink(storage)]
pub struct CrudContract {
    records: Mapping<u32, Record>,
    next_id: u32,
    owners: Mapping<AccountId, Vec<u32>>,
}

// Public API (Solidity ABI compatible)
impl CrudContract {
    #[ink(message)]
    pub fn create_record(&mut self, title: String, description: String) -> u32;
    
    #[ink(message)]
    pub fn get_record(&self, id: u32) -> Option<Record>;
    
    #[ink(message)]
    pub fn update_record(&mut self, id: u32, title: String, description: String) -> bool;
    
    #[ink(message)]
    pub fn delete_record(&mut self, id: u32) -> bool;
    
    #[ink(message)]
    pub fn get_user_records(&self, owner: AccountId) -> Vec<u32>;
}
```
####  An overview of the technology stack to be used
##### Smart Contract Layer:
- Language: Rust with ink! v6 framework
ABI Compatibility: Solidity ABI generation via abi = "sol" configuration
- Build Tool: cargo-contract (latest from GitHub)
- Network: Polkadot Hub Testnet initially, with mainnet compatibility

##### Frontend Stack:
- Framework: React 18+ with TypeScript
- Ethereum Integration: Wagmi v2 + Viem for type-safe contract interactions
- Wallet: MetaMask connection with custom network configuration
- UI Components: Tailwind CSS 
- Build Tool: Vite for fast development and optimized production builds

##### Development Infrastructure:

- Testing: Hardhat integration for contract testing
- Deployment: Automated deployment scripts using ethers.js
- Documentation: Comprehensive README with setup instructions and examples
####  Documentation of core components, protocols, architecture, etc. to be deployed

####  PoC/MVP or other relevant prior work or research on the topic
- We've reviewed provided documentation at [use.ink](use.ink) on Ethereum compatibility
- We've deployed the flipper smart contract(provided as an example in docs) and integrated with a front-end.[github.com/fredmunene/ink](github.com/fredmunene/ink)
- During rust & ink cohort, wrote extensive articles 

    + [understanding-ownership-in-rust-a-devs-guide-to-safe-memory-management](https://dev.to/nyagooh/understanding-ownership-in-rust-a-devs-guide-to-safe-memory-management-51o5)
    + [lifetimes-traits-enums-and-pattern-matching-in-rust](https://dev.to/nyagooh/understanding-lifetimes-traits-enums-and-pattern-matching-in-rust-2dc7)
    + [beginners-guide-to-rust-for-polkadot-devs](https://dev.to/githaiga22/getting-your-feet-rust-y-a-beginners-guide-to-rust-for-polkadot-devs-3bh)
    + [steps on deploying ink! smart contracts](https://dev.to/fredgitonga/getting-started-with-smart-contracts-on-polkadot-a-guide-to-ink-4lgg)
    + []()


#### Scope Exclusions:
- Production Deployment: Template provides local development setup only when project is cloned; users deploy to their chosen networks
- Advanced Features: No complex DeFi functionality, governance mechanisms, or multi-sig implementations
- Custom UI Themes: Single, clean UI theme; customization left to developers
- Backend Services: No off-chain indexing, APIs, or database integration
- Multi-Chain Support: Focus solely on Polkadot/Substrate chains with Ethereum tooling
- Security Audits: Template includes best practices but requires independent security review for production use
- Maintenance/Support: Open-source template with community-driven updates only


#### Technical Boundaries:
- Limited to ink! types that have established Solidity ABI mappings
- No support for Rust-specific features (Option, Result) that lack Solidity equivalents
- Template demonstrates core patterns; complex business logic implementation is user responsibility
#### Category: Infrastructure
This template serves as foundational infrastructure enabling developers to bridge ink! contracts with Ethereum tooling ecosystems efficiently.


## Team :busts_in_silhouette:

### Team members

- Cheryl Owalla (Team Leader)
- Anne Maina
- Valery Odinga
- Allan Robinson
- Fred Gitonga



### Contact

- **Contact Name:** Cheryl Owalla
- **Contact Email:** cherylowalla@gmail.com
- **Website:** https://github.com/polkadotkisumubootcamp

### Legal Structure

N/A

### Team's experience


### Team Code Repos

- https://github.com/polkadotkisumubootcamp/polkadot-kisumu-Rust-workshop
- https://github.com/polkadotkisumubootcamp/Ink-Bootcamp-Kisumu

#### Team GitHub Profiles

- https://github.com/Cherrypick14
- https://github.com/odingaval
- https://github.com/nyagooh
- https://github.com/FredMunene
- https://github.com/Githaiga22


### Team LinkedIn Profiles

- https://www.linkedin.com/in/cheryl-owala-423731191
- https://www.linkedin.com/in/odinga-valery/
- https://www.linkedin.com/in/maina-anne-37797820b/
- https://www.linkedin.com/in/allan-robinson-3b54511a4
- https://www.linkedin.com/in/Fredmunene


## Development Status :open_book:

- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to building this template,

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):** 3 FTE
- **Total Costs:** 25,000 USD

### Milestone 1 Example — Basic functionality

- **Estimated duration:** 1 month
- **FTE:**  1.5
- **Costs:** 15,000 USD

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT  |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **README** that explains how to set up the development environment and run the frontend application. |
| **0c.** | Testing and Testing Guide | Frontend components will be covered by unit tests. We will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile that can be used to run the frontend development environment. |
| 0e. | Article | We will publish an **article** that explains the design decisions and user experience approach for bridging Ethereum tooling with ink! contracts. |
| 1. | UI/UX Design & Wireframes | We will deliver wireframes and design mockups for the dApp interface, including wallet connection, contract interaction flows, and CRUD operations interface. |
| 2. | Frontend Application Setup | We will deliver a React 18+ TypeScript/Javascript application with Vite build setup, Tailwind CSS styling, and basic routing structure. |
| 3. | Wallet Integration | We will implement MetaMask connection with custom network configuration for Polkadot/Substrate chains using Wagmi . |
| 4. | UI Components Library | We will create reusable React components for contract interactions, including forms for CRUD operations and data display components. |
| 5. | Mock Contract Interface | We will implement mock contract interactions to demonstrate the frontend functionality without requiring deployed contracts. |


### Milestone 2 — Smart Contract Development & Integration

- **Estimated Duration:** 1 month
- **FTE:**  1.5
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License |  MIT |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a **tutorial** that explains how to deploy contracts and interact with them via the frontend. |
| **0c.** | Testing and Testing Guide | Smart contracts will be covered by unit tests and integration tests. Frontend-contract integration will be tested. We will describe how to run all tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone, including contract deployment and frontend integration. |
| 0e. | Article | We will publish an **article** that explains the complete Solink template, demonstrating how developers can leverage Ethereum tooling with ink! contracts and showcasing the bridge between ecosystems. |
| 1. | CRUD Smart Contract | We will deliver an ink! v6 smart contract with Solidity ABI compatibility that implements create, read, update, and delete operations for records with proper access control and event emission. |
| 2. | Contract Deployment Scripts | We will provide automated deployment scripts using ethers.js that can deploy contracts to Polkadot Hub Testnet. |
| 3. | Frontend-Contract Integration | We will integrate the deployed smart contract with the frontend application, replacing mock interfaces with real contract interactions using Wagmi v2 . |
| 4. | Testing Infrastructure | We will implement Hardhat integration for contract testing and provide test suites for both smart contracts and frontend-contract interactions. |
| 5. | Complete Template Package | We will deliver the complete production-ready template with setup scripts, configuration files, and comprehensive documentation for developers to fork and customize. |



## Future Plans

#### Community Engagement:
- Conduct workshops and tutorials at Polkadot and Ethereum developer conferences
- Partner with Polkadot Africa and other regional hubs for developer training programs
- Establish feedback loops with early adopters to identify improvement areas

#### Extended Template Features:
- Add multiple contract examples (token contracts, simple DeFi protocols, basic NFT functionality)

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Polkadot Africa forum

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- **Work you have already done:** Our team has successfully completed the Polkadot Africa ink! and Rust bootcamp, gaining hands-on experience with ink! smart contract development and Rust programming. We have also deployed and tested the flipper smart contract with frontend integration as part of our learning process.
- **Training Background:** As recent graduates of the intensive Rust and ink! training through Polkadot Africa, we have documented our learning journey through comprehensive articles covering Rust fundamentals, ownership, lifetimes, traits, and ink! development patterns.
- **Community Involvement:** We are active members of the Kisumu Polkadot Community and have contributed to local developer education through workshops and bootcamp participation.
- **No external financial contributors:** This project is being developed independently by our team without external financial backing.
