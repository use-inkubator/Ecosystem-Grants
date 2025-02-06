# Bluesky


- **Team Name:** Bluesky
- **Payment Address:** 14bPDTAigrV3GCgcem7LJHJ7rb4aEzKMtWrG2V4VcGbvyKxM 
## Project Overview :page_facing_up:
### Overview

- If the name of your project is not descriptive, a tag line (one sentence summary). 
	- Learning ink! macros and upgradability
	
- A brief description of the template building.
	- A technical tutorial helping the community to learn ink! macros and upgradability via an example dApp
	- Learn the unique ink! macros for application level code simplicity, reusability and readability
	- Learn ink!'s on-chain smart contract upgrdes and related storage layouts 
	- Compare with Solidity to rpomote ink! as an alternative smart contract programming language
 
- An indication of how your project relates to ink! ecosystem
	- ink! macros for code simplified and reusability at application level 
	- On-chain smart contract upgradability

- Choosen project idea category or your alternative category with explanation of its importance
	- Technical showcase to domonstrate benefits of ink! / Wasm based smart contracts, to promote ink! among alternatives such as Solidity
	
- An indication of why your team is interested in creating this project.
	- Help community to learn ink! technical features as an smart contract alternative to Solidity 

### ink! Ecosystem Impact

Solidity has a more mature ecosystem than ink!, with more libraries, frameworks, and tools available. Building a robust ecosystem around ink! would make it more attractive to developers who are looking for a wider range of options when building their applications, starting from increased confidence level via specific examples showcaseing technical advantages backed up with tangible metrics.

This techbical showcase project impacts the ecosystem by introducing ink! unique macros and upgradability features to developers who are evaluating Solidity alternative smart contract languages so developers can learn the following to increase ink! adoptions:

- ink! macros to write smart contracts for applicaiton level code simplicity and reusability   
- ink! smart contract On-chain upgradability  
 
	
### Project Details

Here's a list of more details of ink! smart contract etc to showcase ink! macros and upgradability

- ink! Macros
	- ink! macros are a way to define custom syntax or code that can be reused within a smart contract. Macros in ink! are defined using the Rust programming language's macro system, which provides a powerful set of tools for code generation and metaprogramming.
	- Application code simplicity via macros: use ink! macros to simplify the code by abstracting away the complexity of reusable application logic. 
	- Design a list of ink! macros for the use case to demonstrate reusable code patterns for application logic, data structures, and other elements of a smart contract, which can help to simplify code and reduce repetition, making it easier to write and maintain complex contracts 

- Upgradability
	- Upgradability of ink! smart contract is a hidden advantage that's buried deep and lack of specific examples to better grasp.  
	- Demonstrate Upgradability via ink!'s built-in upgradeable smart contract features to upgrade the smart contract code without having to migrate the data or interrupt the user experience. 
	- Demonstrate users can continue to interact with the updated contract without losing any data or transaction history as ink!'s flexible upgrade mechanism allows for on-chain upgrades of smart contracts. 
	- When a new version of a smart contract is deployed, use set_code_hash to point to the new contract code, while persisting old contract data intact.
	- Upgradability related storage layouts, collision / corruption scenarios, and best practices 

- Documentation and publications
	- Document with screenshots in a step-by-step guide to make it tangible for potentail developers to better understand ink! smart contract potentials and related Substrate technology stack  
	- Publish Medium articles to reach out to both technical and non-technical audience to better understand ink! smart contract especially against alternatives, especially to detail not well publicized ink! features as comparative advantges.     

- What your project is _not_ or will _not_ provide or implement
  - It is not a canary dapp, not infrastructure, not business case 
  - This showcase project is not about developing tooling, libraries, templates, etc. but simply serves as an example to help community learn ink! smart contract developement focusing on ink! declarative and procedure macros at applicaiton level, and ink! upgradability.   

## Team :busts_in_silhouette:

### Team members

- Name of team leader: Daniel Deng
- Names of team members: 
	- Daniel Deng, project manager, product and technology leader in web3 / blockchain  	- Developer team for implementation  

### Contact

- **Contact Name:** Daniel Deng
- **Contact Email:** gotellme@proton.me 
- **Website:** 

### Team's experience

- web3 / blockchain / smart contract / Solidity / ink!

### Team Code Repos

- https://github.com/InkSmartContract/BlockchainFoodOrder

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/dengdaniel

## Development Status 

- Previous milestone1 and milestone2 already developed and submitted. This is application resubmission per private chats.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 
	- 5-6 months
- **Full-Time Equivalent (FTE):**
	- 2 FTE
- **Total Costs:** Requested amount in USD for the whole project (e.g. 12,000 USD). Note that the acceptance criteria and additional benefits vary depending on the level of funding requested. This and the costs for each milestone need to be provided in USD.
	- 90,000 USD

### Milestone 1 — Technical showcase example implemented with ink! macros. Publish Medium article 

- **Estimated duration:** 3-4 months
- **FTE:**  2
- **Costs:** 50,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Open source Apache 2.0 |
| **0b.** | Documentation | We will provide both inline documentation of the code and a basic tutorial that explains how a user can deploy and send test transactions with step-by-step guide |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests and how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| **0e.**  | Articles | We will publish a Medium article focusing on learning ink! macros |
| 1. | Why learning ink! | Background, context, stages and target audiences|
| 2. | Define the use case | Order Food on the Blockchain use case that defines: 1) business functionalities such as registration, order, food preparation, delivery, payment, etc.; 2) Personas: consumer, restaurants, couriers, dApp manager, users, etc. 3) workflow of a food marketplace with service providers and consumers interacting with each other on the blockchain |
| 3. | ink! implementations | Highlight the data, services, security, and access control implemented in this ink! smart contract |
| 4. | Security & Access Control | Openbrush's Ownable and Access Control with roles, permissions and policies |
| 5. | ink! macro introduction | List of benefits such as reusability, code simplicity, abstract dApp business logic |
| 6. | Define and implement declarative macro | Payment macro with code snippets|
| 7. | Define and implement procedure macros | Crud_item macros with code snippets |
| 8. | Smart contract | Implement the business logic of the use case in ink! smart contract |
| 9.| Testing | Testing scripts and end-to-end test results |
| 10.| Deployment | Deploy to a Polkadot smart contract testchain for user interactions with step-by-step guide |
| 11.| ink! learning resources | List of related ink! learning materials|
| 12.| Recommendations | Learnings and recommendations | 


### Milestone 2 —  On-chain ink! smart contract upgrades, compared to Solidity. Publish Medium article   

- **Estimated Duration:** 2-3 months
- **FTE:**  2
- **Costs:** 40,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Open source Apache 2.0 |
| **0b.** | Documentation | We will provide both inline documentation of the code and a basic tutorial that explains how a user can deploy and send test transactions with step-by-step guide |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests and how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| **0e.**  | Articles | We will publish a Medium article focusing on learning ink! upgradability and related storage layouts |
| 1. | Upgrade ink! smart contracts due to business logic changes | Smart contract upgradability challenges, demonstrate ink!'s built-in upgrade features with persistent contract data and seamless user experiences |
| 2. | Seamless interaction during upgrades | Demonstrate users can continue to interact with the before and ufter contract upgrades without data loss / corruptions as ink!'s flexible upgrade mechanism allows for on-chain upgrades |
| 3. | Understand ink! smart contract storage layout | Packed vs non-Packed, Eager loading vs lazy loading, layout-ful vs layout-less, Manual vs automatic storage key generation |
| 4. | ink! smart contract upgrade best practices | ink! storage collisions and corruptions scenarios and best practices |
| 5. | smart contract upgrade patterns | Patterns, comparisons and recommendations |
| 6. | Compare with Solidity smart contract upgrades | Solidity smart contract upgrades comparisons |
| 7. | Business logic changes trigger upgrades | Example of why frequent smart contract upgrades needed to accommodate business changes | 
| 8. | Demo ink! built-in contract upgrade features | Code snippet with the "Upgradeable" trait to mark a smart contract as upgradeable,  set_code_hash to the new contract |
| 9. | Unit and regression test script | Step by step test script output before and after upgrade to demo business continuity with old data and appending new data |  
| 10.| Step by step guide of the smart contract flow | Step-by-step Guide on ink! smart contract upgrde with screenshots |
| 11.| Suggestions on ink! upgradability improvements | Learnings and suggestions to improve ink! upgradability |


## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** ink!cubator program 

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- This is a resubmission per conversations with the program, adapted from previous applicaiton milestone1 and milestone2, dropped the original milestone3 to reduce scope.

- If there are any other teams who have already contributed (financially) to the project. None
