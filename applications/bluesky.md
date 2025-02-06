# Bluesky


- **Team Name:** Bluesky
- **Payment Address:** 14bPDTAigrV3GCgcem7LJHJ7rb4aEzKMtWrG2V4VcGbvyKxM 
## Project Overview :page_facing_up:
### Overview

- If the name of your project is not descriptive, a tag line (one sentence summary). 
	- Bluesky is the limit riding the ink! & Wasm tailwind 
- A brief description of the template building.
	- A technical showcase dApp implementing a Polkadot native use cases that leverage on ink! and Wasm demonstrating comparative advantages over Solidity+EVM. 
	- The contrived dApp requires frequent feature changes or updates, that could benefit from flexible on-chain smart contract upgrades as compared to Ethereum.
	- The showcase leverages ink! macros for code simplicity, reusability and readability, a unique ink! faeture as comapred to Solidity.
	- Benchmark to showcase reduced gas fees, tangible cost savings over gas spike otherwise implemented in Solidity + EVM
	- The goal is to promote ink! + Wasm based smart contract development on Polkadot and Substrate blockchains with code template and tangible metrics to boost adoption confidence.  
	- Notice the showcase is mainly targeting Solidity developers who are considering alternatives yet may or may not have prior exposure to ink! / Substrate / Polkadot, or new smart contract developers who want to compare options and choose a stack based on latest objective matrix comparisons.  
- An indication of how your project relates to ink! ecosystem
	- On-chain smart contract upgradability
	- Simplified, reusable and easy-to-read ink! code via macros 
	- ink! macros for balacing common logic abstration from application logic
	- Cost effective and predictable gas fees via benchmark against Solidity
- Choosen project idea category or your alternative category with explanation of its importance
	- Technical showcase to domonstrate multiple benefits of ink! / Wasm based smart contracts, especially as compared to Solidity / EVM based ones
- An indication of why your team is interested in creating this project.
	- Unlock Polkadot / Kusama / ink! ecosystem's technical strength and potentials as an smart contract alternative to Solidity / EVM 
	- Help ink! novice, especially Solidity developers. without prior knowledge of ink! / Substrate / Polkadot

### ink! Ecosystem Impact

Please clearly describe how exactly your project will benefit the ecosystem. If it's infrastructure - how it's going to be applied and by who. If it's canary dapp we would you to clearly demonstrate how this code will be used by other people. If it's technical showcase we would like you to demonstrate how ink! will be promoted using your results. If it's a business case we would like to see b usiness model and future production plans. 

As a techbical showcase project, ink! will be promoted competitively against Solidity/EVM based smart contracts with clear quanfitied  

- Simplified, reusable and easy-to-read ink! code via macros 
- ink! macros to allow developers abstract common reusable logic from application logic and optimize over iterations to balance, yet still organically fused via ink!
- Cost effective and predictable gas fees via benchmark against Solidity/EVM resulting in quantifiable metrics 
- On-chain Wasm based smart contract upgradability, as compared to EVM based smart contract upgrades on Ethereum  
- Increase ink! adoption and future growth via competitive analysis against Solidity / EVM

### Project Details

Here's a list of more details of ink! smart contract etc to showcase simplified smart contract code, lower gas fees and better perfromance.  

- ink! Macros
	-  ink! macros are a way to define custom syntax or code that can be reused within a smart contract. Macros in ink! are defined using the Rust programming language's macro system, which provides a powerful set of tools for code generation and metaprogramming.
	- Code simplicity via macros: use ink! macros to simplify the code by abstracting away the complexity of the application logic. 
	- Design a list of ink! macros for the use case to demonstrate reusable code patterns for functions, data structures, and other elements of a smart contract, which can help to simplify code and reduce repetition, making it easier to write and maintain complex contracts

- Reduced gas fees: reduce gas fees 
	- Benchmark & measurement
		- Set up a development environment that supports both ink! and substrate, as well as a test network for executing the contracts and measuring their gas costs
		- Prepare a test suite
		- Use a substrate runtime benchmarking tool, such as the frame-benchmarking module, to measure the gas costs
		- Use the ink-bench tool to measure the gas costs of the ink! smart contract
	- Compare
		- Compare the gas costs of ink! smart contract implementations, one could write equivalent smart contracts in both languages and use a test suite to measure the gas costs of each
		- Smart contract code tuning to balance the allocation of logic optimized for selected goal: lower gas fees, maximal code reuse, simplify smart contract code, performance, interoperability, etc. 
	- Compare with Solidity / EVM
		- Implment the same logic in Solidity smart contract 
		- Measure and compare the gas fees of the simplified ink! smart contract, vs Solidity / EVM based one 
	- The same gas usage benchmark suite can be reused in the future to measure different blockchains as each chain gas implmentation could differ. 
	
- Performance 
	- Smart contract performance using ink! / Wasm VM as compared to Solidity / Wasm. Future perfromance benchmark can be conducted to do side-by-side performance metrics comparisons. 
	- One of the main advantages of WebAssembly is its performance. Because it is a low-level language, it can be executed more efficiently than high-level languages like Solidity. This can result in faster transaction processing times and lower gas costs for users.
	- ink! leverages the benefits of WebAssembly to provide a more efficient and secure environment for executing smart contracts. The use of the Wasmer Runtime and the flexibility of WebAssembly allow for faster transaction processing times, lower gas costs, and a more robust development experience.
	- On reducing on-chain storage footprint, ink! provides two main types of storage: contract storage and contract env storage. Contract storage is designed to hold data that needs to be persisted on the blockchain, while contract env storage is intended for storing data that does not need to be persisted on-chain.
	- The same performance benchmark suite can be reused to masure ongoing improvements to the Polkadot network and its associated technologies with quantifiable metrics based lineage.   

- Upgradability
	- Upgradability of ink! smart contract is a hidden advantage that's buried deep and lack of specific examples to better grasp.  
	- Demonstrate Upgradability via ink!'s built-in upgradeable smart contract features to upgrade the smart contract code without having to migrate the data or interrupt the user experience. 	
	- Demonstrate users can continue to interact with the updated contract without losing any data or transaction history as ink!'s flexible upgrade mechanism allows for on-chain upgrades of smart contracts. When a new version of a smart contract is deployed, ink! creates a new contract instance on the blockchain, which can be used to replace the old contract instance. However, the old contract instance remains on the blockchain and can still be accessed if needed.
	- Shed light on ink! built-in tools and libraries for managing contract upgrades. For example, the "Upgradeable" trait that can be used to mark a smart contract as upgradeable, and the "Dispatcher" module that can be used to handle contract upgrades and routing of function calls.
	- Expose ink!'s Dispatcher module to handle contract upgrades and routing of function calls between different versions of the same contract. When a contract is upgraded, the Dispatcher module creates a new contract instance on the blockchain for the upgraded version of the contract.
	- The Dispatcher module also provides a function called migrate which can be used to migrate data from the old contract instance to the new one, demonstrating copying data from the old contract instance to the new one, using a user defined migration function as a parameter.

- Interoperability
	- While ink! is designed to be used on the Polkadot network, it would be beneficial for the language to be interoperable with other blockchain networks as well. 
	- This would allow developers to write smart contracts once and deploy them on multiple networks, increasing ink! adoption
	- This showcase project could experiment on Shiden chain or other parachains to expldore

- Adoption
	- Document this technical showcase to make it tangible for potentail developers to better understand ink! smart contract potentials and related Substrate technology stack  
	- Tooling: While there are some tools available for ink!, there is room for improvement in this area. For example, tools to manage upgrades, interoperability, gas estimator, performance benchmarks, industry tailored smart contract macros and templates, with low barrier onramping for developer for adoption and future growth.
	- Ecosystem: Solidity has a more mature ecosystem than ink!, with more libraries, frameworks, and tools available. Building a robust ecosystem around ink! would make it more attractive to developers who are looking for a wider range of options when building their applications, starting from increased confidence level via specific examples showcaseing technical advantages backed up with tangible metrics.
	- Publish blog post in Medium or other media, reaching out to both technical and non-technical audience to better understand ink! smart contract especially against incumbents such as Solidity with not well publicized benefits backed up with concrete feature comparisons and benchmark results.     


- What your project is _not_ or will _not_ provide or implement
  - This is a place for you to manage expectations and to clarify any limitations that might not be obvious
  - This showcase project is not about developing tooling, performance benchmarks, indusrty specific macros and templates, etc. It simply serves as an example to showcase some of ink! smart contract benefits and potentials. 


Things that shouldn’t be part of the application:
- The (future) tokenomics of your project 
- For non-infrastructure projects—deployment and hosting costs, maintenance or audits
- Business-oriented activities (marketing, business planning), events or outreach

## Team :busts_in_silhouette:

### Team members

- Name of team leader: Daniel Deng
- Names of team members: 
	- Daniel Deng, project manager, product and technology leadership at bigtechs and startups, Libra / Diem / Novi / Web3 / smart contract infrastructure 
	- Bernhard Schuster, former Parity team lead, lecturer at Polkadot Academy, running local Rust meetups, mentor
	- Andrew Berger, Rust / Substrate develdoper, lecturer of Polkadot Academy, mentor

### Contact

- **Contact Name:** Daniel Deng
- **Contact Email:** gotellme@proton.me 
- **Website:** 

### Legal Structure

- **Registered Address:** Address of your registered legal entity, if available. Please keep it in a single line. (e.g. High Street 1, London LK1 234, UK)
- **Registered Legal Entity:** Name of your registered legal entity, if available. (e.g. Duo Ltd.)

### Team's experience

Lecturers of 2022 Polkadot Academy with in-depth domain knowledge and many years of Substrate / Rust software experiences actively developing in Polkadot ecosystem, running local Rust meetups

### Team Code Repos

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/coax1d
- https://github.com/drahnr

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/dengdaniel

## Development Status 

- references to conversations you might have had related to building this template: convosations in private chats 

## Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. Since these will be part of the agreement, it helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

### Overview

- **Total Estimated Duration:** Duration of the whole project (e.g. 2 months)
	- 6 months
- **Full-Time Equivalent (FTE):**  Average number of full-time employees working on the project throughout its duration (see [Wikipedia](https://en.wikipedia.org/wiki/Full-time_equivalent), e.g. 2 FTE)
	- 3+ FTE
- **Total Costs:** Requested amount in USD for the whole project (e.g. 12,000 USD). Note that the acceptance criteria and additional benefits vary depending on the level of funding requested. This and the costs for each milestone need to be provided in USD.
	- 150,000 USD

### Milestone 1 — Technical showcase example implemented in ink! Macros. Publish Article 1/3 

- **Estimated duration:** 2 month
- **FTE:**  2,3
- **Costs:** 40,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | Define use case | define a contrived use case that requires 1) business logic 2) reusable components 3) features needing smart contract upgrades 4) performance and low gas fees |
| 2. | OpenZepplin's features like Roles, Ownership | Investigate OpenZepplin's's roles / ownership to see how it might fit this showcase |
| 3. | Define list of ink! Macros | that captures reusable logic to simplify code |
| 4. | Smart contracts | Write ink! smart contract with macros to fulfil use case business functions |
| 5. | End-to-end integration | Organically integrate all pieces together to ensure working end-to-end |
| 6. | Deployment | Deploy to a Polkadot smart contract parachain, say Shiden, etc to also explore interoperability |
| 7. | Articles | We will publish article 1 of 3 walking through the technical showcase focusing on ink! macros in comparison to Solidity. Can publish the blog in Medium in English, or recommended medium to target designated audiences |

### Milestone 2 —  On-chain ink! smart contract upgrades, compared to Solidity upgrades. Publish Article 2/3   

- **Estimated Duration:** 2 month
- **FTE:**  2,3
- **Costs:** 50,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | Upgrade ink! smart contracts due to feature changes | Demonstrate Upgradability via ink!'s built-in upgradeable smart contract features to upgrade the smart contract code without having to migrate the data or interrupt the user experience |
| 2. | Seamless interaction during upgrades | Demonstrate users can continue to interact with the updated contract without losing any data or transaction history as ink!'s flexible upgrade mechanism allows for on-chain upgrades of smart contracts |
| 3. | Demo ink! built-in tools and libraries for managing contract upgrades | For example, the "Upgradeable" trait that can be used to mark a smart contract as upgradeable, and the "Dispatcher" module that can be used to handle contract upgrades and routing of function calls|
| 4. | Expose ink!'s Dispatcher module | To handle contract upgrades and routing of function calls between different versions of the same contract. When a contract is upgraded, the Dispatcher module creates a new contract instance on the blockchain for the upgraded version of the contract |
| 5. | Improve storage example of upgradable contracts | This [issue](https://github.com/paritytech/ink/issues/1679) says "The documentation around storage and upgradeability isn't thorough enough", use this showcase to address the pain points ([issue](https://github.com/paritytech/ink/issues/1678)) of "The current examples of upgradeability and call forwarding are confusing, incomplete, and some cases misleading" to provide better examples and documentation for contract developers|
| 6. | Demo ink! upgradability and parachain flexibility without hard fork | Compare to Solidity smart contract upgrades |
| 7. | Articles | We will publish article 2 of 3 using the same technical showcase focusing on ink! smart contract upgrade flow, ease of upgradability and flexibility. Can publish the blog in Medium in English, or recommended medium to target designated audiences |


### Milestone 3 —  Gas usage / performance benchmarks compared, ink!+Wasm vs Solidity+EVM, Publish Article 3/3

- **Estimated Duration:** 2 month
- **FTE:**  3+
- **Costs:** 60,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Open source Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| **0e.**  | Articles | We will publish article 3 of 3 that explains ink!+Wasm's competitive advantage against Solidity/EVM, with tangible technical examples and benchmark metrics, to lower the adoption barrier and increase developer confidence. Can publish the blog in Medium in English, or recommended medium to target designated audiences |
| 1. | Set up a development environment | that supports both ink! and substrate, as well as a test network for executing the contracts and measuring their gas costs |
| 2. | Prepare a test suite | for gas usage and performance benchmark |
| 3. | Frame-benchmarking module | Use a substrate runtime benchmarking tool to measure the gas costs of variations |
| 4. | Ink-bench tool | Use the ink-bench tool to measure the gas costs of the ink! smart contract |
| 5. | Optional tuning between smart contract code implementing the same logic | Compare the gas costs between ink! smart contract implementations, use a test suite to measure the gas costs, then tune smart contract code to optimize for overall gas costs |
| 6. | Compare with Solidity / EVM | Implment the same logic in Solidity smart contract and benchmark against Solidity / EVM |
| 7. | ink!'s string feature | ink's string feature tends to add code bloat. Explore solutions to reduce the footprint |
| 8. | Compare Solidity binary size vs Wasm by business logic | Compare Solidity compiled binaries compare to Wasm via ink! using the latest versions of each | 
| 9. | Compare OpenZepplin and OpenBrush | Explore difference between OpenZepplin and OpenBrush in this context and share learning in documents |  
| 10. | Website and publications | Website hosted via Github Pagers with all collaterals including code, documentations, benchmark results, comparative analysis, etc. We'll publish a series of Medium posts to summarize the outcome targeting smart contract developers. | 

## Future Plans

Please include here if you have a future plan after building this template in making it in to production.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Substrate Builders Program

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Previous work on migrating MOVE EVM to Polkadot helped to learn Polkadot tech stack including Substrate, smart contract, etc as compared to competitions 
- We believe this technical showcase will be able to:
	- reach out to many ink! / Wasm doubtfuls, especially ink! novice / hard core Solidity devs, with tangible examples and metrics to increase adoption confidence level
	- publish articles have a long lasting impact to future developers to convert, adopt and contribute in the ink! / Polkadot / Substrate ecosystem     
	- some assets be reused to develop useful tools to benefit ink! ecosystem in the future  
	- share unique comparative advantages of ink! + Wasm, especially as increasing bitcoin / ethereum congestions causing fee spikes and waitings, to position ink! as an attractive smart contract alternative against competition
- If there are any other teams who have already contributed (financially) to the project. None
