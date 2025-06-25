# Name of your Project

- **Team Name:** Benchmark Elite
- **Payment Address:** <b>[TODO]</b> Polkadot payment address.

## Project Overview :page_facing_up:
### Overview

The purpose of this proposal is to build a public benchmark and analytics dashboard that monitors solidity and ink! smart contracts deployed on the PassetHub network. The dashboard will help users, developers, and researchers observe, compare, and validate the performance and cost-efficiency of PVM smart contracts (in contrast to EVM contracts on various chains), with a particular focus on showcasing the advantages of the Risc5 PassetHub's PVM implementation.

**[Orig]** An indication of how your project relates to ink! ecosystem.
The project is related to ink! because it strive to present PassetHub and ink! in the best form that exists out there.

This project is focused on DevEx by DebugEx by showcasing benchmark analysis in a transperant way.
We believe that such a project will increase the speed of PassetHub development while ensuring at the same time high quality and preformace of the underline building blocks of PVM.

### Ink! Ecosystem Impact

While PassetHub now is being developed there are challenges that revolve around PVM-EVM compatibility, huge smart contract size inflation and a big amount of uncertainty when it comes to whether PVM is the right approach to improve block chain evaluation.
The goal of this project is to display the current state of the ecosystem, and pin point the bottlenecks and silos of PVM technology as a belief that transparency will lead to easier DevEx and DebugEx, which as a result will yield a better developed PVM tech stack.

This proposal is a response to the following problems:
1. PassetHub’s PVM is not compatible with EVM byte code, especially when it comes to heavy smart contracts such as Zk-verifiers
2. It is not clear whether Risc5 is a better compiled format then EVM byte code.
3. It is not clear what are the current bottlenecks in PVM compilation process
  I. Is it the memory?
  II. Is it the running time?
  III. Is it the memory/time? Maybe it is applied to specific evaluation and to some other not…?
4. PVM’s smart contracts compilation at the moment is inefficient in memory size
5. There is no gas comparison between PVM and EVM yet
6. Generally speaking there is no tool that showcases the comparison between PVM and EVM


### Project Details

**[Orig]** We expect the teams to already have a solid idea about the project expected final state. Therefore, we ask the teams to submit (where relevant):

#### Application Structure
This section lists and describes the structure of the end-to-end application. The application is composed from:

* **Frontend** Display the data on the user browser in a human readable fashion and pleasant to the eye format.
* **Backend** The connecting back bone of the system, responsible for database update and funneling stored stated to the frontend.
* **Database** Responsible for application’s persistency and state management 

##### Front End
This section presents the layout and the functional requirements of the application.

**Home Page**
The home page is the landing page of the website - the entry point for the user. It should display a hero component that is 100% height and 100% width and should fit exactly the view.
There should be 2 buttons at the landing page:
1. View Contacts - Should redirect to "Contracts Index Page"
2. Deploy a contract - Should redirect to "Contract Page"

**Contracts Index Page**
Should display a table with all the deployed contracts, where each row describes a deployed contract - Contract Name, Deployed Address, Deployed Time, Deploy status (success/failure). The table should support sort and filtration functionalities that are aggregated with one another for a fully felxible user experience.

**Contract Page**
This page is changing according to the contract provided as input to the page component and it displays the full details of a contract:
1. Deployment status,
If the contract was deployed successfully:
2. Contract address
3. Deployment gas consumption
4. PVM and EVM byte code and their metadata
5. Benchmark of run time and gas consumption average out of x runs (1, 10, 100, 1000)

**Deploy Contract Page**
This page is responsible for adding a new smart contract to the benchmark dashboard. A user will be able to add his previously deployed smart contract to the dashboard by pointing to the address of the already deployed smart contract on PassetHub and other Networks.

##### Back End

This section presents the functional non-functional requirements of the application.

The backend would be written in Rust, with a consideration of security and efficiency first. Leveraging Rust’s real time characteristics and strong type system.

##### Database Hosting and State Managment
A Web2 Centralized Cloud solution would be leveraged to store the database state (Bucket or NoSQL hosted solutions can be utilized for that), also a Cloud instance would be used to host Rust based backend server.

Features
Tack deployment status - failed/succeeded
Display statistics of the following metrics - gas consumption, run time speed, PVM VS EVM size



- Data models / API specifications of the core functionality
- An overview of the technology stack to be used
- Documentation of core components, protocols, architecture, etc. to be deployed
- PoC/MVP or other relevant prior work or research on the topic
- What your project is _not_ or will _not_ provide or implement
  - This is a place for you to manage expectations and to clarify any limitations that might not be obvious
- CATEGORY: Infrastructure OR Canary Dapp OR Technical Showcase
- An overview of the business model, including revenue streams, target market, and scalability, if applicable.
- Future production plans and growth strategy, highlighting how the project intends to achieve sustainability and long-term success, if applicable.


Things that shouldn’t be part of the application:
- The (future) tokenomics of your project 
- For non-infrastructure projects—deployment and hosting costs, maintenance or audits
- Business-oriented activities (marketing, business planning), events or outreach


## Team :busts_in_silhouette:

### Team members

- Gil Henkin

### Contact

- **Contact Name:** Gil Henkin
- **Contact Email:** gil7788@gmail.com
- **Website:** https://gil-henkin.web.app/

### Legal Structure

- **Registered Address:** Address of your registered legal entity, if available. Please keep it in a single line. (e.g. High Street 1, London LK1 234, UK)
- **Registered Legal Entity:** Name of your registered legal entity, if available. (e.g. Duo Ltd.)

### Team's experience

Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past.

### Team Code Repos
Github account: https://github.com/gil7788
- End-to-end DApp: https://github.com/gil7788/meowmeow
This project showcases Solidity and DeFi hands on experience of the team members as well as the ability to deliver products from scratch, that includes React front end with smart contracts integration, smart contract development and CI/CD integration for frontend webpage hosting.

- https://github.com/gil7788/portfolio
This project showcases React and design practices with hands on experience of the team members.

- https://github.com/gil7788/zero-knowledge-polkadot-machine
This project showcases the knowledge of Rust, PassetHub hands on experience and is the reason for the create of this project as of a trial to migrate Groth16 Risc0 verifier failed due to PVM contract size.

- https://github.com/gil7788/terraform-cloud
This repository show cases IAC with Terraform/Terraform Cloud hands on experience (unfortunatly I cannot share real world utilization of Terrform project as it is private and I cannot disclose it, that why I share a boilerplate)


### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/gilhenkin/


## Development Status :open_book:

The idea for this project was created during EthBelgrade Hackton, at the very begging I was brainstorming with WebZero team.

Here is a link to an alpha version of the project's layout: **[TODO]**

## Development Roadmap :nut_and_bolt:

This section presents the roadmap for PassetHub's Benchmark Dashboard:

### Milestone 1

### Milestone 2
### Milestone 3
### Milestone 4

This section should break the development roadmap down into milestones and deliverables. Since these will be part of the agreement, it helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**.


### Overview

- **Total Estimated Duration:** Duration of the whole project 2 months
- **Full-Time Equivalent (FTE):**  Average number of full-time employees working on the project throughout its duration 320 hrs => 1 FTE for 2 month.

- **Total Costs:** 
1. Developers Payment: 12,000
2. Domain URL: ???
3. Monthly expenses for Cloud services:
  I. Compute Instance
  II. Storage solution

* There might be a need for scaling and maintenance with time as the tool will be used more and more.

### Milestone 1 Example — Front End Layout

- **Estimated duration:** 2 weeks
- **FTE:**  1
- **Costs:** 2,000 USD

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Substrate module: X | We will create a Substrate module that will... (Please list the functionality that will be implemented for the first milestone. You can refer to details provided in previous sections.) |
| 2. | Substrate module: Y | The Y Substrate module will... |
| 3. | Substrate module: Z | The Z Substrate module will... |
| 4. | Substrate chain | Modules X, Y & Z of our custom chain will interact in such a way... (Please describe the deliverable here as detailed as possible) |
| 5. | Library: ABC | We will deliver a JS library that will implement the functionality described under "ABC Library" |
| 6. | Smart contracts: ... | We will deliver a set of ink! smart contracts that will...


### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  1,5
- **Costs:** 8,000 USD

...


## Future Plans

Develop, deploy and maintain - including system monitoring, feature development and support to the team which responsible for PVM compilation process. 

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Personal recommendation.
