# PVM Benchmark Dashboard

- **Team Name:** Benchmark Elite

## Project Overview :page_facing_up:
### Overview

The purpose of this proposal is to build a public benchmark and analytics dashboard that monitors solidity and ink! smart contracts deployed on PVM compatible networks. The dashboard will help users, developers, and researchers observe, compare, and validate the performance and cost-efficiency of PVM smart contracts (compare and contrast  between a Solidity and ink! contracts), with a particular focus on showcasing the advantages of the ink! PVM implementation.

Checkout live [demo](https://pvm-dashboard.vercel.app/)!

The project is related to ink! because it strive to present ink! in the best form. Focused on DevEx and DebugEx by showcasing benchmark analysis in a transperant way.
We believe that such a project will increase the speed of ink! development while ensuring at the same time high quality and preformace of the underline building blocks of PVM.

### Ink! Ecosystem Impact

While ink! now is being developed there are challenges that revolve around PVM-EVM compatibility, huge smart contract size inflation and a big amount of uncertainty when it comes to whether PVM is the right approach to improve block chain evaluation.
The goal of this project is to display the current state of the ecosystem, and pin point the bottlenecks and silos of PVM technology as a belief that transparency will lead to easier DevEx and DebugEx, which as a result will yield a better developed PVM tech stack.

This proposal is a response to the following problems:
1. PVM and ink! are not compatible with EVM byte code, especially when it comes to heavy smart contracts such as Zk-verifiers
2. It is not clear whether Risc5 is a better compiled format then EVM byte code.
3. It is not clear what are the current bottlenecks in PVM compilation process:
  I. Is it the memory?
  II. Is it the running time?
  III. Is it the memory/time? Maybe it is applied to specific evaluation and to some other not…?
4. PVM’s smart contracts compilation at the moment is inefficient in memory size
5. There is no gas comparison between PVM and EVM yet
6. Generally speaking there is no tool that showcases the comparison between PVM and EVM


### Project Details

#### Application Structure
This section lists and describes the structure of the end-to-end application. The application is composed from:

* **Frontend** Display the data on the user browser in a human readable fashion and pleasant to the eye format.
* **Backend** The connecting back bone of the system, responsible for database update and funneling stored stated to the frontend.
* **Database** Responsible for application’s persistency and state management 
* **CI/CD** Responsible for seemless deployment and system upgradability both for frontend and backend.

##### Front End
This section presents the layout and the functional requirements of the application.

**Home Page**
The home page is the landing page of the website - the entry point for the user. It should display a hero component that fit exactly the view.
There should be 2 buttons at the landing page:
1. View Contacts - Should redirect to "Contracts Index Page"
2. Deploy a contract - Should redirect to "Contract Page"

**Contracts Index Page**
Should display a table with all the deployed contracts, where each row describes a deployed contract - Contract Name, ink! Deployed Address, ink! Deployed Time, Solidity Deployed Address, Solidity Deployed Time. The table should support sort and filtration functionalities that are aggregated with one another for a fully felxible user experience.

**Contract Page**
This page is changing according to the contract provided as input to the page component and it displays the full details of a contract:
Each contract that exists in the system, might have a either solidity contract deployed, or a ink! or both. The page should display the following:
1. Deployment status - either solidity or ink! or both,
2. Contract address (for solidity and ink! according to the deployment status)
3. Deployment gas consumption (for solidity and ink! according to the deployment status)
4. Solidity and ink! byte code and their metadata (for solidity and ink! according to the deployment status)
5. Benchmark of run time and gas consumption for each function (for solidity and ink! according to the deployment status)

* Present data in tabs:
1. The default tab should display metadata
2. abi tabs should display abi of both ink! and solidity in a diff format (expandable and collapsable)
3. PVM Bytecode tabs should display bytecode sizes and  bytecode of both ink! and solidity in a diff format (expandable and collapsable)
4. Benchmark tab should provide a convenient way benchmark the "same" functions of the contracts (with inputs)
5. Analytics tab should compare and contrast gas consumption, bytecode, bytecode size, last test runtime of each function.
 

**Deploy Contract Page**
This page is responsible for adding a new smart contract to the benchmark dashboard. A user will be able to add his previously deployed smart contract to the dashboard by pointing to the address of the already deployed smart contract on PVM based network.

The form for contract creation will consist of the following fields:

1. Contract Name
2. ink! address
3. ink! abi
4. Solidity address
5. Solidity abi
6. Description (Optional)

* In case the abi are not the same should warn about it, but not prevent from creation.
* At contract creation should redirect to newly created contract page.


##### Back End

This section presents the non-functional requirements of the application.

The backend would be written in Rust, with a consideration of security and efficiency first. Leveraging Rust’s real time characteristics and strong type system for extra security.

##### Database Hosting and State Managment
A Web2 Centralized Cloud solution would be leveraged to store the database state (Bucket or NoSQL hosted solutions can be utilized for that), also a Cloud instance would be used to host Rust based backend server.

##### DevOps
Automated pipelines for system maintanance and upgradabilty, will be accomplished by installing CI/CD pipelines with Github Runner, Github Actions, Terraform, Terraform Cloud, HCL and Vercel.

#### Technological Stack
This scetion presents the required tech stack to develop as system according to the specs above.

##### Frontend
The frontend will be develop leveraging "de-facto" Web3 industry standards such as:
1. NextJs
2. Css
  I. TailwindCss
  II. ShadCn
3. Eth Scaffold-2
4. React
5. Typescript

##### Backend
Backend will use Rust.
Tools such as message broker may or may not be part of the system. Should be decided in the next steps of the grant.

##### Database
A storage solution would be selected according to the needs of the scale of the system, there are a few viable solution - Bucket or NoSQL DB's on top of cloud provider such as - AWS, GCP, Azure.

##### DevOps
For CI/CD pipelines Github Runner, Github Actions, Terraform, Terraform Cloud, HCL and Vercel will be leveraged, also docker, docker-compose and github-packages will be leveraged for containerization solution.

#### What the Project Will Not Provide
The dashboard will not provide a deployment functionality - by specifing the address of already a deployed contract and an abi, the platform will be able to be flexible enough to support all contracts that are deployed on various networks.


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

Down below are listed some projects that showcase work that is similar and required to develop the devised system.

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

The idea for this project was created during EthBelgrade Hackton, at the very beginning while brainstorming with WebZero team.

Here is a link to an alpha version of the project's layout: [https://pvm-dashboard.vercel.app/](https://pvm-dashboard.vercel.app/). Link to [Repo](https://github.com/gil7788/pvm-dashboard).

## Development Roadmap :nut_and_bolt:

This section presents the roadmap for PVM's Benchmark Dashboard:

### Overview

- **Total Estimated Duration:** Duration of the whole project 12 weeks
- **Full-Time Equivalent (FTE):**  Average number of full-time employees working on the project throughout its duration 480 hrs => 40hrs for 12 weeks.

- **Total Costs:** 
1. Developers Payment: 
  I. Iteration 1: 13,500 USD
  II. Iteration 2: 4,500 USD
  Total: 18,000 USD
2. Domain URL: Can leverage vercel's free url or by annual url
3. Monthly expenses for Cloud services:
  I. Compute Instance
  II. Storage solution
4. Terraform Cloud - Free for small team up to 5 collaborators and open source projects


* There might be a need for scaling and maintenance with time as the tool will be used more and more and with higher rate. Tools such as Message Broker (probably not needed at small scale) might also be included with time and increase maintenance costs.

### Iteration 1 - MVP and Seemless CI/CD
In this iteration we present the bare minimum features that are required for the benchmarck dashboard to provide some value for ink! developers. Each iteration is a self contain unit that is layer on top of the prevoius iteration in such a way that they provide new features and flexible use cases that improve DevEx.

#### Milestone 1 Frontend — Stateless Layout

- **Estimated duration:** 2 weeks
- **FTE:**  1
- **Costs:** 3,000 USD

This milestone focuses on the implementation of appliaction's frontend layout and data management in the browser.

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide standard documentation that is analogous to Eth-Scaffold-2 |
| **0c.** | Tests | There is nothing to test in this step; it is just a stateless layout being developed. A by-hand test video demonstrating the flow will be provided. |
| **0d.** | Docker | Application will not be dockerized as it is not needed in order to deploy to Vercel. |
| **1.** | Front End Layout | A full working layout written in React and Next.js that leverages Tailwind CSS and ShadCN frameworks. It includes implementation of the following pages:<br>I. Home Page<br>II. Contract Creation Page<br>III. Contracts Index Page<br>IV. Contract Info Page<br><br>The pages will display only static information. Further details of layout of each page can be found in the [Application Structure](#application-structure) section. |
| **2.** | Infrastructure | Leverage a hosted Vercel server for frontend |
| **3.** | CI/CD Pipeline | Configure and setup a Vercel CI/CD pipeline for easy and continuous work. |

#### Milestone 2 Backend Development — Rust Server Development 

- **Estimated Duration:**  3 Weeks
- **FTE:**  1 FTE
- **Costs:** 4,500 USD


This milestone focuses on the implementation of appliaction's backend functionality in Rust with a stored state on the Rust server - moving the state managment to the server and facilitating the integration of the cloud provider for the next step.

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide standard documentation leveraging Rust standard docs |
| **0c.** | Tests | Thourough unit tests for CRUD operations will be provided to validate backend correcteness.
| **0d.** | Docker | Application will be dockarized with docker and docker-compose file for deployment and future utilization in the CI/CD pipeline. |
| **1.** | Back End Server | A fully working Rust server that stores state in memory (not in file system or some other hosted solution) the server will support <br> 1. CRUD operations for contracts - Create, Remove, Update and Delete over restful https api.
| **2.** | Front End | Front end will be refactor to fetch state from newly implemented server |
| **3.** | Infrastructure | A compute server will be provisioned to deploy newly implemeted server. Frontend will stay hosted on firebase |

At the end of this milestone the system will be functional yet stateless - this is when the development team will get to test the first version and provide first cycle of feedback while working in parallel (next milestones) on solid foundation and rubust infrastructor.

#### Milestone 3 Cloud Integration — Integration of Cloud Compute and Storage

- **Estimated Duration:**  2 Weeks
- **FTE:**  1 FTE
- **Costs:** 3,000 USD


This milestone focuses on manual provisioning of cloud service such as compute and storage, and integration with of Rust server, compute instace and hosted storage. That includes - manual provisioning of resources, server deployment to the compute resource, code refactoring to integrate and authenticate with cloud compute and hosted storage, test might be rewritten to fit the right format returned from the hosted storage.


| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide standard documentation that is analogous to Eth-Scaffold-2 |
| **0c.** | Tests | Thourough unit tests for CRUD operations will be provided to validate backend correcteness.
| **0d.** | Docker | Application will be dockarized with docker and docker-compose file for deployment and future utilization in the CI/CD pipeline. |
| **1.** | Cloud Resources | In order to run a persistent system, we will leverage a standard and minimalistic design that seperate compute resources and storage resources by provisioning by hand a compute instance (VM) and a storage (either a bucket or NoSQL solution) on GCP/AWS|
| **2.** | Back End Server | Refactor server implementation:<br>  1. Refactor CRUD to integrate with storage solution <br> 2. Implement cloud authentication functionality | **3.** | Infrastructure | A compute server will be provisioned to deploy newly implemeted server. Frontend will stay hosted on firebase |



At the end of this milestone the system will be deployed, stateful and accessiable online. Core features should be delivered leaving only infastructure programability (IAC) as the missing part of the puzzle. 

#### Milestone 4 DevOps — CI/CD Pipeline Installation

- **Estimated Duration:**  1 Week
- **FTE:**  1 FTE
- **Costs:** 1,500 USD


This milestone focuses on CI/CD pipeline installation, Terraform Cloud configuration, HCL Terrafom IAC files implementation, and server docker deployment to the Github package service as a docker registry.

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | Docmentation for automatic system spin up will be provided. Also instruction for contribution will be provided, facilitating the ability to future contributers to so with extream ease  |
| **0c.** | Tests | There is nothing to test in this step it is installation of a CI/CD pipeline being developed, a by-hand test video demostrading the flow will be provided.
| **0d.** | Docker | Docker will be provided and stored in Github package service |
| **1.** | Terraform | Programable HCL files will be provided for compute and storage provisioned in the last step |
| **2.** | Terraform Cloud and CI/CD | Terraform Cloud  will be configured and set, including CI/CD workflows to update the source code. |

At this step all the features should be delivered as they are described in all the milestones above (including this one). Each and every contributor should be able to contribute and a seemless and continous way (with out knowing the underling setup of the system, leveraing installed CI/CD pipelines).

#### Milestone 5 Test, Validation, Corrections and System Documenation

- **Estimated Duration:**  1 Week
- **FTE:**  1 FTE
- **Costs:** 1,500 USD


This milestone focuses on polishing and making sure that project is clear enough so (if need it be) it can be handed off to some random developer. Ideally by this time core user team had the chances to provide feedback. This week is a great opportunity to iterate on the dashboard again and address any unexpected issues/features that were suggested in the feedback process.

### Iteration 2 - Public Hosted Benchmarking PolkaVM
This iteration will focus on implementing a hosted PolkaVM solution that will run on the backend server and leverage homogeneous testing environment for all the tested functionalities.


#### Milestone 6 DevOps — CI/CD Pipeline Installation

- **Estimated Duration:**  2 Weeks
- **FTE:**  1 FTE
- **Costs:** 3,000 USD


This milestone, the backend will implement dry-running capabilities for smart contract calls.

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | Docmentation for automatic system spin up will be provided. Also instruction for contribution will be provided, facilitating the ability to future contributers to so with extream ease  |
| **0c.** | Tests | Tests for PVM will be provided
| **0d.** | Docker | Docker will be provided and stored in Github package service |
| **1.** | Back End Server | At this milestone, the backend will implement dry-running capabilities for smart contract calls. This will be handled using one of the following options, the most sutiable one will be selected after tech research:<br><br>XCM Runtime API (DryRunApi): Enables runtime-level dry-run execution of XCM messages, suitable for simulating contract behavior without committing state changes.<br> EthRPC Dry Run (from pallet_revive): Exposes a dry run method for Ethereum-like execution environments. Although less commonly used, it may provide compatibility with EVM contracts. <br>System Extrinsic Dry Run (frame_system): Offers general-purpose dry-run support for extrinsics, making it suitable for testing contract deployment and interaction logic before submission. |
| **2.** | Front End | Front End will support and expose a new option to select a PVM public network |
| **3.** | Deployment | CI/CD Pipeline will be leveraged from previous milestones for continuous development |

At this step all the features should be delivered as they are described in all the milestones above (including this one). Each and every contributor should be able to contribute and a seemless and continous way (with out knowing the underling setup of the system, leveraing installed CI/CD pipelines).

#### Milestone 7 Test, Validation, Corrections and System Documenation

- **Estimated Duration:**  1 Week
- **FTE:**  1 FTE
- **Costs:** 1,500 USD


This milestone focuses on polishing and making sure that project is clear enough so (if need it be) it can be handed off to some random developer. Ideally by this time core user team had the chances to provide feedback. This week is a great opportunity to iterate on the dashboard again and address any unexpected issues/features that were suggested in the feedback process.



## Future Plans
A short list of ideas that might be interesting to implement in the future, it's just likely that as the system will be developed, more and more use cases will be considered so that it will make to plan for iteration 3.


### Features and Future Iterations
1. Support native Smart Contract deployed from the dashboard
2. Community vote on Smart Contract - which of the contracts implement the same functionalities.
3. Expand benchmark for PVM vs EVM for end-to-end benchmark.

### Maintenance
1. Develop, deploy and maintain - including system monitoring, feature development and support to the team which responsible for PVM compilation process.
2. Devise and develop non-functional requirements that are required at scale such as - server/browser caching, horizontal/vertical scaling, message brokers and redesign for the underling architecture if needed.
3. Support Green/Blue Deployments (zero down time deployment) if system is widely used and there an going developement. 

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Personal recommendation.
