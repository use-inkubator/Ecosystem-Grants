# Bluesky


- **Team Name:** Bluesky
- **Payment Address:** TBP


## Project Overview :page_facing_up:
### Overview

Please provide the following: 

- If the name of your project is not descriptive, a tag line (one sentence summary). 
	- Bluesky is the limit riding on the Ink! tailwind  
- A brief description of the template building.
	- A technical showcase implementing a use case with specific business logic that requires frequent updates due to changing requirements, that could benefit from using custom pallet implemented Ink! macros for code simplicity, reusability and readability, for flexible on-chain smart contract upgrades, for cost effective gas fees, as compared to Solidity / EVM, in order to promote Ink! / WASM based smart contracts on Polkadot and other blockchains. Notice this is from an Ink! novice perspective without prior knowledge of Ink! / Substrate / Polkadot.
- An indication of how your project relates to ink! ecosystem
	- On-chain smart contract upgradability
	- Simplified, reusable and easy-to-read Ink! code via macros 
	- Custom pallets implemented ink! macros for balacing common logic abstration from application logic
	- Cost effective and predictable gas fees via benchmark against Solidity
- Choosen project idea category or your alternative category with explanation of its importance
	- Technical showcase to domonstrate multiple benefits of Ink! / WASM based smart contracts, especially as compared to Solidity / EVM based ones
- An indication of why your team is interested in creating this project.
	- Unlock Polkadot / Kusama / Ink! ecosystem's technical strength and potentials as an smart contract alternative to Solidity / EVM 
	- Help Ink! novice, especially Solidity developers. without prior knowledge of Ink! / Substrate / Polkadot

### Ink! Ecosystem Impact

Please clearly describe how exactly your project will benefit the ecosystem. If it's infrastructure - how it's going to be applied and by who. If it's canary dapp we would you to clearly demonstrate how this code will be used by other people. If it's technical showcase we would like you to demonstrate how ink! will be promoted using your results. If it's a business case we would like to see b usiness model and future production plans. 

As a techbical showcase project, Ink! will be promoted competitively against Solidity/EVM based smart contracts with clear quanfitied  

- Simplified, reusable and easy-to-read Ink! code via macros 
- Custom substrate pallets coupled with ink! macros to allow developers abstract common reusable logic from application logic and optimize over iterations to balance, yet still organically fused via Ink!
- Cost effective and predictable gas fees via benchmark against Solidity/EVM resulting in quantifiable metrics 
- On-chain WASM based smart contract upgradability, as compared to EVM based smart contract upgrades on Ethereum  
- Increase Ink! adoption and future growth via competitive analysis against Solidity / EVM

### Project Details

Here's a list of more details of Ink! smart contract, Substrate custom pallets, etc to showcase simplified smart contract code, lower gas fees and better perfromance.  

- Ink! Macros
	-  Ink! macros are a way to define custom syntax or code that can be reused within a smart contract. Macros in Ink! are defined using the Rust programming language's macro system, which provides a powerful set of tools for code generation and metaprogramming.
	- Code simplicity via macros: use ink! macros to simplify the code by abstracting away the complexity of the application logic. 
	- Design a list of Ink! macros for the use case to demonstrate reusable code patterns for functions, data structures, and other elements of a smart contract, ehich can help to simplify code and reduce repetition, making it easier to write and maintain complex contracts

- Substrate custom pallets
	- Demonstrate the flexibility of substrate's modular architecture 
	- Pallet macros are used to define custom pallets, which are modules that contain storage items and dispatchable functions. Ink! macros can then call these dispatchable functions to interact with the pallet's storage and logic.
	- Use custom pallets to implement the macros and optimize the gas usage. Use macros that call custom pallets can potentially result in significant gas savings as it can allow for reusable code and more efficient execution.
	- The gas savings can be quantified via comparative benchmarks detailed below

- Reduced gas fees: use custom pallets to implement the macros and optimize the gas usage as compared to implementing the same logic in the smart contract code directly. 
	- Benchmark & measurement
		- Set up a development environment that supports both ink! and substrate, as well as a test network for executing the contracts and measuring their gas costs
		- Prepare a test suite
		- Use a substrate runtime benchmarking tool, such as the frame-benchmarking module, to measure the gas costs of pallet operations
		- Use the ink-bench tool to measure the gas costs of the ink! smart contract
	- Compare
		- Compare the gas costs between ink! smart contracts and substrate custom pallets, one could write equivalent smart contracts in both languages and use a test suite to measure the gas costs of each
		- Smart contract / macro / pallet tuning to balance the allocation of logic optimized for selected goal: lower gas fees, maximal code reuse, simplify smart contract code, performance, interoperability, etc. 
	- Compare with Solidity / EVM
		- Implment the same logic in Solidity smart contract 
		- Measure and compare the gas fees of the simplified ink! smart contract, vs Solidity / EVM based one 
	- The same gas usage benchmark suite can be reused in the future to measure different blockchains as each chain gas implmentation could differ. 
	
- Performance 
	- Smart contract performance using Ink! / WASM VM as compared to Solidity / WASM. Future perfromance benchmark can be conducted to do side-by-side performance metrics comparisons. 
	- One of the main advantages of WebAssembly is its performance. Because it is a low-level language, it can be executed more efficiently than high-level languages like Solidity. This can result in faster transaction processing times and lower gas costs for users.
	- Ink! leverages the benefits of WebAssembly to provide a more efficient and secure environment for executing smart contracts. The use of the Wasmer Runtime and the flexibility of WebAssembly allow for faster transaction processing times, lower gas costs, and a more robust development experience.
	- On reducing on-chain storage footprint, Ink! provides two main types of storage: contract storage and contract env storage. Contract storage is designed to hold data that needs to be persisted on the blockchain, while contract env storage is intended for storing data that does not need to be persisted on-chain.
	- The same performance benchmark suite can be reused to masure ongoing improvements to the Polkadot network and its associated technologies with quantifiable metrics based lineage.   

- Upgradability
	- Upgradability of Ink! smart contract is a hidden advantage that's buried deep and lack of specific examples to better grasp.  
	- Demonstrate Upgradability via ink!'s built-in upgradeable smart contract features to upgrade the smart contract code without having to migrate the data or interrupt the user experience. 	
	- Demonstrate users can continue to interact with the updated contract without losing any data or transaction history as Ink!'s flexible upgrade mechanism allows for on-chain upgrades of smart contracts. When a new version of a smart contract is deployed, Ink! creates a new contract instance on the blockchain, which can be used to replace the old contract instance. However, the old contract instance remains on the blockchain and can still be accessed if needed.
	- Shed light on Ink! built-in tools and libraries for managing contract upgrades. For example, the "Upgradeable" trait that can be used to mark a smart contract as upgradeable, and the "Dispatcher" module that can be used to handle contract upgrades and routing of function calls.
	- Expose Ink!'s Dispatcher module to handle contract upgrades and routing of function calls between different versions of the same contract. When a contract is upgraded, the Dispatcher module creates a new contract instance on the blockchain for the upgraded version of the contract.
	- The Dispatcher module also provides a function called migrate which can be used to migrate data from the old contract instance to the new one, demonstrating copying data from the old contract instance to the new one, using a user defined migration function as a parameter.

- Interoperability
	- While Ink! is designed to be used on the Polkadot network, it would be beneficial for the language to be interoperable with other blockchain networks as well. 
	- This would allow developers to write smart contracts once and deploy them on multiple networks, increasing Ink! adoption
	- This showcase project could experiment on Shiden chain and expldore

- Adoption
	- Document this technical showcase to make it tangible for potentail developers to better understand Ink! smart contract potentials and related Substrate technology stack  
	- Tooling: While there are some tools available for Ink!, there is room for improvement in this area. For example, tools to manage upgrades, interoperability, gas estimator, performance benchmarks, industry tailored smart contract macros and templates, with low barrier onramping for developer for adoption and future growth.
	- Ecosystem: Solidity has a more mature ecosystem than Ink!, with more libraries, frameworks, and tools available. Building a robust ecosystem around Ink! would make it more attractive to developers who are looking for a wider range of options when building their applications, starting from increased confidence level via specific examples showcaseing technical advantages backed up with tangible metrics.
	- Publish blog post in Medium or other media, reaching out to both technical and non-technical audience to better understand Ink! smart contract especially against incumbents such as Solidity with not well publicized benefits backed up with concrete feature comparisons and benchmark results.     


- What your project is _not_ or will _not_ provide or implement
  - This is a place for you to manage expectations and to clarify any limitations that might not be obvious
  - This showcase project is not about developing tooling, performance benchmarks, indusrty specific macros and templates, etc. It simply serves as an example to showcase some of Ink! smart contract benefits and potentials. 


Things that shouldn’t be part of the application:
- The (future) tokenomics of your project 
- For non-infrastructure projects—deployment and hosting costs, maintenance or audits
- Business-oriented activities (marketing, business planning), events or outreach

## Team :busts_in_silhouette:

### Team members

- Name of team leader
- Names of team members

### Contact

- **Contact Name:** Full name of the contact person in your team
- **Contact Email:** Contact email (e.g. john@duo.com)
- **Website:** Your website

### Legal Structure

- **Registered Address:** Address of your registered legal entity, if available. Please keep it in a single line. (e.g. High Street 1, London LK1 234, UK)
- **Registered Legal Entity:** Name of your registered legal entity, if available. (e.g. Duo Ltd.)

### Team's experience

Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past.

### Team Code Repos

- https://github.com/<your_organisation>/<project_1>
- https://github.com/<your_organisation>/<project_2>

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/<team_member_1>
- https://github.com/<team_member_2>

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/<person_1>
- https://www.linkedin.com/<person_2>


## Development Status :open_book:

- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to building this template,

## Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. Since these will be part of the agreement, it helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**.

> :exclamation: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Overview

- **Total Estimated Duration:** Duration of the whole project (e.g. 2 months)
	- 6 months
- **Full-Time Equivalent (FTE):**  Average number of full-time employees working on the project throughout its duration (see [Wikipedia](https://en.wikipedia.org/wiki/Full-time_equivalent), e.g. 2 FTE)
	- 2,3 FTE
- **Total Costs:** Requested amount in USD for the whole project (e.g. 12,000 USD). Note that the acceptance criteria and additional benefits vary depending on the level of funding requested. This and the costs for each milestone need to be provided in USD.
	- 150,000 USD

### Milestone 1 — Technical showcase example implemented in Ink! Macros and Substrate custom pallets for Ink! / Substrate / Polkadot novice. Publish Article 1/3 

- **Estimated duration:** 2 month
- **FTE:**  2,3
- **Costs:** 40,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | Define use case | define a contrived use case that requires 1) business logic 2) reusable components 3) features needing smart contract upgrades 4) performance and low gas fees |
| 2. | define list of Ink! Macros | that captures reusable logic to simplify code |
| 3. | Substrate modules | implement substrate custom pallets corresponding to above macros |
| 4. | Smart contracts | Write Ink! smart contract with macros integrated with custom pallets to fulfil use case business functions |
| 5. | End-to-end integration | Organically integrate all pieces together to ensure working end-to-end |
| 6. | Deployment | Deploy to a Polkadot smart contract parachain, say Shiden, etc to also explore interoperability |
| 7. | Article | We will publish article 1 of 3 walking through the technical showcase focusing on Ink! macros and substrate pallets. Can publish the blog in Medium in English, or recommended medium to target designated audiences |

### Milestone 2 —  On-chain Ink! smart contract upgrades, compared to Solidity upgrades. Publish Article 2/3   

- **Estimated Duration:** 2 month
- **FTE:**  2,3
- **Costs:** 50,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | Upgrade Ink! smart contracts due to feature changes | Demonstrate Upgradability via ink!'s built-in upgradeable smart contract features to upgrade the smart contract code without having to migrate the data or interrupt the user experience |
| 2. | Seamless interaction during upgrades | Demonstrate users can continue to interact with the updated contract without losing any data or transaction history as Ink!'s flexible upgrade mechanism allows for on-chain upgrades of smart contracts |
| 3. | Demo Ink! built-in tools and libraries for managing contract upgrades | For example, the "Upgradeable" trait that can be used to mark a smart contract as upgradeable, and the "Dispatcher" module that can be used to handle contract upgrades and routing of function calls|
| 4. | Expose Ink!'s Dispatcher module | To handle contract upgrades and routing of function calls between different versions of the same contract. When a contract is upgraded, the Dispatcher module creates a new contract instance on the blockchain for the upgraded version of the contract |
| 5. | Copying data from the old contract | Migrate data from the old contract instance to the new one, demonstrating copying data from the old contract instance to the new one, using migrate function|
| 6. | Demo Ink! upgradability and parachain flexibility without hard fork | Compare to Solidity smart contract upgrades |
| 7. | Article | We will publish article 1 of 3 using the same technical showcase focusing on Ink! smart contract upgrade flow, ease of upgradability and flexibility. Can publish the blog in Medium in English, or recommended medium to target designated audiences |


### Milestone 3 —  Gas usage / performance benchmarks compared, Ink!+WASM vs Solidity+EVM, Publish Article 3/3

- **Estimated Duration:** 2 month
- **FTE:**  3
- **Costs:** 60,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Set up a development environment | that supports both ink! and substrate, as well as a test network for executing the contracts and measuring their gas costs |
| 2. | Prepare a test suite | for gas usage and performance benchmark |
| 3. | Frame-benchmarking module | Use a substrate runtime benchmarking tool to measure the gas costs of pallet operations|
| 4. | Ink-bench tool | Use the ink-bench tool to measure the gas costs of the ink! smart contract |
| 5. | Smart contract / macro / pallet tuning | Compare the gas costs between ink! smart contracts and substrate custom pallets, one could write equivalent smart contracts in both languages and use a test suite to measure the gas costs of each |
| 6. | Compare with Solidity / EVM | Implment the same logic in Solidity smart contract and benchmark against Solidity / EVM |
| 7. | Optional performnace benchmark | Smart contract performance using Ink! / WASM VM as compared to Solidity / WASM. Future perfromance benchmark can be conducted to do side-by-side performance metrics comparisons|
| 8. | Article | We will publish an article that explains Ink!+WASM's competitive advantage against Solidity/EVM, with tangible technical examples and benchmark metrics, to lower the adoption barrier and increase developer confidence. Can publish the blog in Medium in English, or recommended medium to target designated audiences |
 
	- 
## Future Plans

Please include here if you have a future plan after building this template in making it in to production.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
