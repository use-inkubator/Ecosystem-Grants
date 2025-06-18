# Name of your Project

- **Team Name:** WeTEE DAO
- **Payment Address:** 138KPTyfTFEfiYo8Ju6xR4D7ZzV1fYaQuvHAm6anm4umKwah

## Project Overview :page_facing_up:
### Overview

WeTEE is a decentralized TEE computing power protocol that provides developers with secure computing power and a private computing environment in the form of a decentralized cloud.

![WeTEE](https://github.com/wetee-dao/website/blob/main/public/imgs/doc/chain.png?raw=true)

During the period of 2024-2025, the integration of off-chain computations (such as Artificial Intelligence, AI) with smart contracts has become a hot trend in the WEB3. This combination aims to address inherent issues within blockchain technology, such as scalability, privacy protection, and insufficient computational power for complex tasks.

Even JAM is not suitable for executing complex or resource-intensive tasks directly on the blockchain, like machine learning model training, data analysis, etc. As a solution to this limitation, trusted off-chain computation serves as an effective complement, providing necessary support for Polkadot Hub and JAM. It's noteworthy that current DApps on Polkadot Hub have not yet provided any protocols based on trusted computational power. WeTEE is developing a secure and easy-to-use trusted off-chain computation protocol aiming to fill this gap, offering developers more powerful tools to implement complex computational tasks.


On the other hand, the Web2 domain boasts a large number of applications and mature technical architecture systems. However, when application developers attempt to migrate their Web2 applications to Web3, they face a series of challenges:
- Compatibility issues: Addressing the interaction problems between applications and blockchain to ensure seamless collaboration between the two.
- Deployment difficulties: Finding suitable deployment methods in the new Web3 environment and ensuring the stable operation of applications becomes a complex task.
- Privacy protection: With the increasing user attention to data privacy, how to handle data privacy issues related to application business becomes particularly important.
- Security updates: Developers need to explore effective methods to update applications in order to promptly fix potential security vulnerabilities.

In short, the current Web2 application development and deployment models lack direct alternatives in the Web3 domain. By adopting a development model of "smart contracts + off-chain computation," a viable path can be provided for the transition from Web2 to full Web3. This approach enables Web2 developers to quickly and smoothly migrate their applications into the Web3 environment.

Current Challenges:

- Data Privacy Risks: Despite being in the WEB3 ecosystem, many project teams still rely on cloud services for deploying their applications. This reliance makes business data susceptible to scanning and potential selling by service providers, causing economic losses to individuals and institutions.
- Insufficient Computing Infrastructure: The Polkadot hub lacks a diversified computing infrastructure similar to that of Web2, failing to meet the computational resource demands of Web3 applications.
- Absence of Native DOT Computing Protocol: Currently, there is no computing protocol on the Polkadot hub that supports using DOT as a means of payment, limiting the flexibility of resource trading.
- Interoperability Challenges: The Polkadot hub has not yet established a universal interoperability protocol between smart contracts and trusted off-chain computing, impacting the development of complex applications and services.


WeTEE solution:

WeTEE integrates multiple technologies to provide the highest quality and most secure services at the hardware, encryption, application, data, and user layers. Its comprehensive design considerations, ranging from basic hardware compatibility to enhancements in frontend user 
experience, reflect a unique design perspective and process. This ensures that the solutions provided are not only reliable but also highly feasible in practice.

![WeTEE](https://github.com/wetee-dao/website/blob/main/public/imgs/doc/mint.png?raw=true)

- On-chain: Use DOT to pay, no additional operations are required to use the secure computing power.
- Hardware Layer: Utilizes technologies such as K3S/K8S to abstract hardware differences and ensures the security and isolation of the computing process through Trusted Execution Environment (TEE) technologies like Intel SGX/TDX and AMD SEV.
- Encryption Layer: Employs decentralized encryption algorithms to protect data transmission (Proxy Re-Encryption) and storage (Pedersen), ensuring privacy and security of sensitive information when processed off-chain.
- Application Layer: Supports seamless integration of smart contracts with off-chain computations, simplifies the development and deployment of complex applications, provides automatic compilation programs, and simplified off-chain interface calls.
- Data Layer: Implements strict data access control policies, combined with an on-chain core data and off-chain encrypted storage hierarchical design to ensure data integrity and confidentiality.
- User Layer: Focuses on user experience, offering an intuitive and easy-to-use Web UI, streamlining operational processes so that individual developers and enterprise users can easily utilize the services provided by WeTEE.

### Ink! Ecosystem Impact

Ink! ecosystem requires a native decentralized TEE computing power protocol integrated with DOT, which would enable developers to easily accomplish the following functionalities.
- Developers/DAOs/Smart contracts can use DOT to pay for the deployment of any unmodified WEB2 programs, such as AI, trading robots, and verifiable DAPP web ui.
- Smart contracts obtain off-chain data through TEE oracle.
- Through the bridge of smart contracts and TEE programs, developers can develop ink! + TEE hybrid applications, where smart contracts can accomplish most of the functions that WEB2 programs can perform.

### Project Details
WeTEE is a decentralized application deployment platform integrated with Trusted Execution Environment (TEE). It consists of a blockchain network and multiple confidential computing clusters, jointly providing an efficient decentralized solution for confidential computing. By leveraging hardware technologies such as Intel SGX, Intel TDX, and AMD SEV-SNP, computation service providers can offer secure and reliable off-chain computing resources. This architecture not only ensures privacy and security during data processing but also supports the effective execution of complex computational tasks.
- On-chain Consensus Based on Polkadot Hub Ink! v6:
WeTEE implements on-chain consensus using Ink! v6 smart contracts on the Polkadot Hub. Whether using a Polkadot wallet or wallets like MetaMask, users can directly invoke these smart contracts.
- Hardware-Level Data Protection:
After application deployment, its workload runs under hardware protection, effectively preventing data leaks. Even to confidential computing providers, these protected data are inaccessible, ensuring maximum security for user data.
- Seamless Integration with Cloud-Native Toolchains:
Designed with existing workflows of developers in mind, WeTEE seamlessly integrates with cloud-native toolchains for developers. In most cases, it can be used directly without any modifications to existing code; in rare special cases, only minimal code adjustments are needed, greatly simplifying the migration and deployment process.
- Convenient Application Monitoring and Management:
Developers can easily view critical information about their applications' resource usage, health status, etc., through the intuitive Web interface provided by WeTEE. This not only improves management efficiency but also makes monitoring application performance straightforward, helping developers quickly respond to potential issues.

WeTEE platform is mainly composed of the following three key components:
1. Smart Contracts:
WeTEE utilizes Ink! v6 smart contracts on the Polkadot Hub to achieve on-chain consensus. These smart contracts are at the core of decentralized applications, defining the behavioral rules of the application and how it interacts with users and other contracts. Through smart contracts, WeTEE ensures the transparency and immutability of operations.
2. Worker Nodes (Execution Nodes):
Worker nodes, sometimes referred to as execution nodes or mining nodes, are responsible for executing specific computational tasks within the WeTEE architecture. These nodes use Trusted Execution Environment (TEE) technologies such as Intel SGX, Intel TDX, or AMD SEV-SNP to provide secure and reliable off-chain computing capabilities. Worker nodes ensure privacy during data processing, meaning that even node operators cannot access the data being processed.
3. Dsecret Nodes:
Dsecret nodes form another crucial part of the WeTEE, specifically designed to enhance the network's security and privacy. These nodes participate in building a trusted side network, providing an additional layer of security for confidential computing. Dsecret nodes help maintain the integrity of the entire system, ensuring that data is not accessed or tampered with by unauthorized parties during transmission and processing.

![WeTEE](https://github.com/wetee-dao/website/blob/main/public/imgs/doc/arch.png?raw=true)

WeTEE greatly simplifies the development process of blockchain applications, lowers the technical threshold, and significantly accelerates the transition process from Web2 to Web3.
With WeTEE, developers can easily build an architecture that separates on-chain and off-chain elements at a very low cost while retaining the original business logic, making the integration and application of blockchain technology more intuitive and accessible.
Platform deeply integrates cloud-native technologies such as trusted compilation and DevOps, effectively addressing core challenges faced when deploying applications in a blockchain environment, such as resource scheduling, data privacy protection, and secure execution of computational tasks. This not only improves deployment efficiency but also provides a solid foundation for building high-performance, high-security decentralized applications.
More importantly, WeTEE enables developers to start developing without needing an in-depth understanding of complex underlying blockchain technologies. They can focus more on implementing the core functionalities of the application, thereby significantly enhancing development productivity and accelerating the product launch process.

Additionally, WeTEE has optimized on-chain and cross-chain interoperability to achieve faster transaction processing, thereby providing a smooth user experience and simplifying user interactions. Similarly, WeTEE empowers applications with the capability of efficient iteration, allowing better adaptation to market changes and shifts in user needs, ensuring the continuous competitive edge of the applications.
- Automatic Program Compilation: 
Code can be automatically compiled into trusted container versions according to preset compilation scripts without manual intervention. Containers can correspond one-to-one with open-source code versions, ensuring the auditability of the program.
- Simplified Off-chain API Calls: 
Developers can easily perform off-chain calls through APIs, reducing the interaction costs between applications and the chain.
- Private Data Off-chain Processing: 
When handling privacy-related data, WeTEE utilizes off-chain privacy computing hardware within the platform for data confidentiality processing.
- Scalable Computing Power: 
The platform's off-chain computing capabilities, used for processing compute-intensive tasks, can be scaled to compensate for deficiencies in on-chain computing power.
- Chain Interaction Encapsulation: 
The hybrid runtime encapsulates the interaction logic with the chain, allowing the frontend to interact with the chain transparently and reducing the risk of privacy data leaks.

![WeTEE](https://github.com/wetee-dao/website/blob/main/public/imgs/doc/detail.png?raw=true)


After an application is processed by the WeTEE compiler and successfully runs within the WeTEE platform, developers generally do not need to worry about the operational status of the application. Nevertheless, as an application deployment platform, WeTEE still provides customers with necessary and accurate tracking and monitoring capabilities for the application's chain path, along with timely fault warning and diagnostic capabilities to ensure the healthy operation of the application. The main functions of WeTEE's automated monitoring include:

- Resource Monitoring:
Regularly collect and analyze key metrics such as CPU load, memory usage rate, storage space utilization, etc.
- Application Health Monitoring:
Periodically monitor application response time, exception logs, and other indicators.
- Anomalous Behavior Monitoring:
Evaluate application behavior and report anomalous behaviors based on a generic anomalous behavior monitoring model.
- Status Alerts:
Alerts are triggered when an application's resource utilization is about to exceed the threshold or when the application exhibits anomalous behavior.
- Failure Review:
When an application experiences abnormal operation or crashes, WeTEE can provide application logs and other data to assist in troubleshooting and diagnosis.
- TEE Real-time Monitoring:
All TEE applications are real-time monitored by Dsecret nodes of the subnet for TEE attestation, ensuring the security and privacy of the applications. 

When application developers need to update the application to provide new features or security patches, they can fully utilize WeTEE's hot update mechanism to achieve rapid application updates. The hot update mechanism of WeTEE adopts a common hot update solution for current cloud-native applications, featuring:
- Code Hot Update:
After the application code is updated, it will be automatically compiled and pushed online, reducing downtime for the application.
- Seamless Experience:
Users are insensitive to application updates, thereby improving user experience.
- Development Paradigm:
Compatible with and supports cloud-native development practices. Application developers can continue using familiar tools and processes.
- Change Flexibility:
The hot update mechanism expands the update methods for decentralized applications, enhancing the adaptability and timeliness of the application.

WeTEE Protocol Offers the Following Products:
- Decentralized TEE Cloud: Provides cloud computing power based on Trusted Execution Environment (TEE), enabling both Web2 and Web3 developers to deploy Docker containers using DOT, fulfilling basic requirements for secure computing power and data privacy. All programs can be audited with real-time query of program security proof.
- Trustless TEE Bridge: Facilitates the calling path between smart contracts and trusted programs (programs deployed in Decentralized TEE Cloud). With Trustless TEE Bridge, smart contracts can easily perform oracle functions to obtain off-chain data. Additionally, smart contracts can asynchronously call any API of trusted programs through the Trustless TEE Bridge, with results returned asynchronously back on-chain.
- Trustless TEE Disk(outside of this grant): An encrypted privacy data disk that can be mounted by any trusted program (deployed in Decentralized TEE Cloud) and is suitable for data selling and Multi-Party Computation (MPC).
- Trustless TEE MPC(outside of this grant): A platform for Multi-Party Computation where smart contracts serve as a secure consensus mechanism and schedule TEE computing power, allowing multiparty computations and project collaborations without the need to trust third parties.
- Trustless TEE AI(outside of this grant): A vertical product focused on AI based on Decentralized TEE Cloud, enabling users to deploy trustworthy and data-privacy protected AI applications. Users do not have to worry about leaks of training or inquiry data, providing better defense against internal data breaches compared to local deployments.

## Team :busts_in_silhouette:

### Team members

- Bail - Full-stack Engineer
- Nina - Product Manager/UI Designer

### Contact

- **Contact Name:** Bail
- **Contact Email:** contact@asyou.me
- **Website:** https://wetee.app

### Team's experience

- In the [Polkadot Hackathon 2023 Summer](https://dorahacks.io/hackathon/polkadot-2024-singapore/detail), Our DTIM project received the first prize.
- Applied for and completed the Web3 Foundation Grant [WeTEE Network](https://grants.web3.foundation/applications/WeTEE_Network).
- In the [Polkadot Hackathon 2024 Singapore](https://dorahacks.io/hackathon/polkadot-2024-singapore/detail), Our TEE project received the second prize.

### Team Code Repos

- https://github.com/wetee-dao/contract
- https://github.com/wetee-dao/tee-worker
- https://github.com/wetee-dao/tee-dsecret
- https://github.com/wetee-dao/dapp

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/BurnWW
- https://github.com/Nina-1994


## Development Status :open_book:

We have completed the core function development of WeTEE based on Substrate,this is the code:

- https://github.com/wetee-dao/chain
- https://github.com/wetee-dao/tee-worker
- https://github.com/wetee-dao/tee-dsecret
- https://github.com/wetee-dao/dapp

this is the test network on Paseo:
- https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fpaseo.asyou.me%2Fws#/explorer

but due to the team size being insufficient to maintain the operation of the parachain, we are shifting our focus towards TEE and blockchain-oriented DAPP development. Therefore, we are moving our emphasis forward to the Polkadot hub and JAM platform, allowing us to concentrate more on our business capabilities. With ink!, we can quickly migrate existing functionalities to smart contracts and rapidly launch our DAPP. This is the best option.

## Development Roadmap :nut_and_bolt:
### Overview

- **Total Estimated Duration:** 3.5 months
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** 18,000 USD

### Milestone 1 — Basic contracts and TEE sub network

- **Estimated duration:** 1.5 month
- **FTE:**  1
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Smart contracts: DAO contract | Implement DAO personnel management, issuance, and management of assets as ERC20 tokens. DAO contract provides treasury and voting functionalities, through the DAO contract, it can hold multiple TOKENs, and use voting for decentralized decision-making.<br/>1. DAO Membership Management<br/>2. Issuance of ERC20 Governance Tokens<br/>3. Voting to Manage Treasury Assets<br/>4. Voting to Execute Proposals |
| 2. | Smart contracts: Sub TEE network contract | Provide registration and staking modules for miner nodes and dsecret nodes, as well as acceptance of proof-of-work data and detailed file hashes and addresses provided by worker and dsecret nodes. It also provides shutdown functionality (which can only be executed when all services have been stopped/migrated) and offers a channel for users to file complaints against miner nodes:<br/>1. Worker Node Registration<br/>2. Worker Node Staking<br/>3. Worker Node Upload TEE Proof Data<br/>4. Worker Node Withdrawal<br/>5. Worker Node Shutdown<br/>6. Dsecret Node Registration<br/>7. Dsecret Node Staking<br/>8. Dsecret Node Submit TEE-verifiable Transaction<br/>9. Dsecret Node Withdrawal |
| 3. | Library: TEE worker(miner) for ink! | We have already completed the full functionality based on Substrate. Now, we will implement ink! adaptation for the following functionalities in a new code branch:<br/>1. Worker Node Registration<br/>2. Worker Node Deposit Staking<br/>3. Worker Node Upload Proof-of-Work Data<br/>4. Worker Node Withdrawal<br/>5. Worker Node Shutdown |
| 4. | Library: TEE dsecret for ink! | We have completed the full functionality based on Substrate, and now we will implement the adaptation of ink! for the following functions in a new code branch:<br/>1. Dsecret node registration<br/>2. Dsecret node deposit of collateral<br/>3. Dsecret node submit TEE-verifiable Transaction<br/>4. Dsecret withdrawal |

### Milestone 2 — Decentralized cloud contracts and UI

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 5,000 USD


| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Smart contracts: Cloud contracts | We will create smart contracts responsible for the creation, update, recharge, and termination of TEE applications:<br/>1. Create TEE application<br/>2. Update TEE application<br/>3. Set TEE application configuration<br/>4. Recharge TEE application<br/>5. Terminate TEE application |
| 2. | Cloud web ui | We will provide all accompanying UI interfaces for TEE applications:<br/>1. Work cluster registration UI<br/>2. Work cluster node staking UI<br/>3. Work cluster withdrawal UI<br/>4. Work cluster termination UI<br/>5. Dsecret node registration UI<br/>6. Dsecret node staking UI<br/>7. Dsecret withdrawal UI<br/>8. Dsecret termination UI<br/>9. Create TEE application<br/>10. Update TEE application<br/>11. Set TEE application configuration<br/>12. Recharge TEE application<br/>13. Terminate TEE application<br/> |


### Milestone 3 — Bridge contracts and UI

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 5,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Smart contracts: Bridge | Provide HTTP API registration for TEE applications to facilitate invocation by smart contracts:<br/>1. TEE application registration bridge proxy<br/>2. Add API for TEE application<br/>3. Update API for TEE application<br/>4. Delete API for TEE application |
| 2. | Bridge web ui | Provide Bridge DAPP UI:<br/>1. TEE application registration bridge proxy<br/>2. Add API for TEE application<br/>3. Update API for TEE application<br/>4. Delete API for TEE application |
| 3. | Bridge examples | We will provide examples for demonstration:<br/>1. Provide a WEB2 test program for both real SGX hardware and simulated SGX hardware<br/>2. Provide the configuration files to call the trusted program<br/>3. Provide ink! smart contract examples to call the trusted program |
| 4. | Test/Main DAPP | Deploy the test dapp on the Westend Asset Hub, and after the review is passed, deploy the main dapp on the Polkadot Asset Hub |

## Future Plans

Please include here if you have a future plan after building this template in making it in to production.

In the future, We will further complete the following functions on the existing confidential cloud container:
- Trustless TEE Disk: An encrypted privacy data disk that can be mounted by any trusted program (deployed in Decentralized TEE Cloud) and is suitable for data selling and Multi-Party Computation (MPC).
- Trustless TEE MPC: A platform for Multi-Party Computation where smart contracts serve as a secure consensus mechanism and schedule TEE computing power, allowing multiparty computations and project collaborations without the need to trust third parties.
- Trustless TEE AI: A vertical product focused on AI based on Decentralized TEE Cloud, enabling users to deploy trustworthy and data-privacy protected AI applications. Users do not have to worry about leaks of training or inquiry data, providing better defense against internal data breaches compared to local deployments.

The next step will support JAM, where all functionalities can be used directly within JAM.
