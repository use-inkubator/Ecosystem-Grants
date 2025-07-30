# Solink


- **Team Name:** Polkadot Kisumu
- **Payment Address:** Polkadot payment address.



## Project Overview :page_facing_up:
### Overview

Please provide the following:

Solink is a dApp Template using a Solidity frontend library with an ink! contract that has the Solidity ABI enabled.

Solink provides a production-ready template that bridges the Polkadot and Ethereum ecosystems by showcasing ink! contracts with Solidity ABI compatibility. Developers can leverage familiar Ethereum tools (MetaMask, Wagmi, ethers.js) while deploying on Substrate-based chains, combining the best of both worlds - Ethereum's mature tooling ecosystem with Polkadot's superior performance and lower costs.

Solink directly showcases ink! v6's Solidity ABI compatibility feature, one of the ecosystem's most significant interoperability advancements. By providing a complete dApp template that integrates ink! contracts with Ethereum tooling (MetaMask, Wagmi, ethers.js), it serves as both a reference implementation and developer onboarding tool for the ink! community. The template leverages core ink! infrastructure including cargo-contract and the latest ABI generation capabilities, while demonstrating how ink! contracts can seamlessly bridge Substrate and Ethereum ecosystems. This directly supports ink!'s strategic vision of unifying blockchain development experiences and helps validate the practical applications of ink!'s cross-chain compatibility features.

####Category Choice & Its Importance 
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
- UI Components: Tailwind CSS with shadcn/ui components
- Build Tool: Vite for fast development and optimized production builds

##### Development Infrastructure:

- Testing: Hardhat integration for contract testing
- Deployment: Automated deployment scripts using ethers.js
- Documentation: Comprehensive README with setup instructions and examples
####  Documentation of core components, protocols, architecture, etc. to be deployed

####  PoC/MVP or other relevant prior work or research on the topic
- We've reviewed provided documentation at use.ink on Ethereum compatibility
- We've deployed the flipper smart contract and integrated with a front-end.(github.com/fredmunene/ink)[github.com/fredmunene/ink]
- During rust & ink cohort, wrote extensive articles ()[] ,()[], ()[]
#### Scope Exclusions:
- Production Deployment: Template provides local development setup only when project is cloned; users deploy to their chosen networks
- Advanced Features: No complex DeFi functionality, governance mechanisms, or multi-sig implementations
- Custom UI Themes: Single, clean UI theme; customization left to developers
- Backend Services: No off-chain indexing, APIs, or database integration
- Multi-Chain Support: Focus solely on Polkadot/Substrate chains with Ethereum tooling
- Security Audits: Template includes best practices but requires independent security review for production use
- Maintenance/Support: Open-source template with community-driven updates only
- 
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

Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past.

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
- **Full-Time Equivalent (FTE):** 9.6 FTE
- **Total Costs:** 50,000 USD

### Milestone 1 Example — Basic functionality

- **Estimated duration:** 1 month
- **FTE:**  1,5
- **Costs:** 8,000 USD

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Smart contracts: ... | We will deliver a set of ink! smart contracts that will...


### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  1.5
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Substrate module: X | We will create a Substrate module that will... (Please list the functionality that will be implemented for the first milestone. You can refer to details provided in previous sections.) 
| 5. | Library: ABC | We will deliver a JS library that will implement the functionality described under "ABC Library" |
| 6. | Smart contracts: ... | We will deliver a set of ink! smart contracts that will...




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

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
