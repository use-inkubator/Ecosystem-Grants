# Polkadart

- **Team Name:** Polkadart Dev Team
- **Payment Address:** 167QS6UiF1ZJBkHtngCBoHTSbLm4Rokc2ehfFBEniEGQXB4k

## Project Overview :page_facing_up:
### Overview

[Polkadart](https://polkadart.dev) - A multi-platform library for creating hybrid applications (windows, linux, macOS, android, iOS, web) for any Polkadot-SDK based blockchain.

We have initiated the development of Polkadart through [W3F Grants Program](https://github.com/w3f/Grants-Program/blob/master/applications/Polkadart.md) focusing in making a full replacement implementation of Polkadot-JS in Dart.

Multiple packages were delivered and are being maintaining ever since, those include: `polkadart, polkadart_cli, polkadart_keyring, polkadart_scale_codec, secp256k1_ecdsa, sr25519, ss58, substrate_bip39, substrate_metadata, ink_abi, ink_cli`

Our full documentation is available at https://polkadart.dev


### Ink! Ecosystem Impact

Polkadart is allowing any Dart & Flutter developer to make hybrid applications for the Polkadot ecosystem.

It is important to note that Flutter is known by being able to support any platform with a single codebase

Those include Windows, Linux, macOS, Android, iOS, and the web.

Being able to support every polkadot feature on flutter is a big step forward in the ecosystem adoption.

We believe that ink v6 is a very new exciting feature and really important to not be supported.

This will allow the onboarding of new developers into the ecosystem easier, it will improve what they can achieve and reduce the time that they might take it

It also reduces the learning curve of Polkadot knowledge necessary to make a dApp.

### Project Details

We want to improve polkadart and its package by bring full support for the pallet-revive and ink! v6.

As of April 22, polkadart has over 1.47k downloads on [pub.dev](https://pub.dev), 44 stars on github, 179 issues solved, and 12 contributors.

A few projects we know that are using it include: Encointer Wallet, Threefold Connect, WeTEE, Reown/WalletConnect

Our team believes that ink! v6 is capable of bringing even more people to our ecosystem and we need to be ready in the Dart & Flutter side to make that possible.

For that we plan to work in the following features in this project:
- Contract deployment module
- Metadata handling
- Contract invocation module
- Event decoding and handling
- Error handling and logging
- Storage access module
- Support for complex data types
- Documentation
- Tutorials
- Playground

#### Category: Infrastructure


## Team :busts_in_silhouette:

### Team members

- Leonardo Custodio (Team Leader)
- Kawal Singh

### Contact

- **Contact Name:** Leonardo Custodio
- **Contact Email:** leonardo@custodio.me
- **Website:** https://polkadart.dev

### Legal Structure

- **Registered Address:** R. Cap Souza Franco, 350 - Cj 22 - Curitiba, PR - Brazil
- **Registered Legal Entity:** Snowpine Labs Inovacao em Tecnologia Ltda

### Team's experience

**Leonardo Custodio**

A Blockchain Engineer with a robust software development background. He has over four years of dedicated experience in Polkadot-related technologies and six years of experience as a Flutter developer and over 10 years of experience in software development. Currently, he is working on PolkaIdentity and creating innovative SDKs tailored for game developers that enables seamless interactions with polkadot based systems.

**Kawaljeet Singh**

An experienced Flutter developer and that has good understanding of Polkadot's stack and protocols. With numerous apps published on iOS and android in Flutter ranging from data-management to live appointment systems and drag-and-drop desktop designing tool, he brings good knowledge and vast skill-sets to the team. In his free time he is focused on developing Flutter tools and libraries like excel useful to ease developers work. On week-ends, he publishes complex UIs made in Flutter to showcase Flutter's use-cases.

### Team Code Repos

- https://github.com/leonardocustodio/polkadart

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/leonardocustodio
- https://github.com/justkawal

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/leogcustodio
- https://www.linkedin.com/in/singhkawal


## Development Status :open_book:

Polkadart development has been supported by W3F Grants Program, we have successfully delivered all milestones.
This proposal aims in bringing new features and capabilities to polkadart.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 6 months
- **Full-Time Equivalent (FTE):**  1 FTE
- **Total Costs:** 50,000 USD


### Milestone 1 - Core features & metadata

- **Estimated duration:**  2 months
- **FTE:**  1
- **Costs:** 15,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains what we have achieved and how can people use what we created in this grant |
| 1. | Pallet Revive | Develop all utilities and core features we need to support the new pallet-revive |
| 1. | Contract deployment module | We will add support for ink! v6 deployment, maintaining backward compability with the previous already immplented versions |
| 2. | Metadata handling | Make a new parser for v6 that will be able to utilize the metadata for dynamic interactions |


### Milestone 2 - Contract interactions

- **Estimated duration:**  1.5 months
- **FTE:**  1
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains what we have achieved and how can people use what we created in this grant |
| 1. | Contract invocation module | Implemment functions to call contract methods, including read-only (queries) and state-changing (transactions) functions |
| 2. | Event decoding and handling | Develop mechanism to decode and handle events emitted by contracts |
| 3. | Error handling and logging | Integrate error handling and logging to aid in debugging | 


### Milestone 3 - Storage access

- **Estimated duration:**  1.5 months
- **FTE:**  1
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains what we have achieved and how can people use what we created in this grant |
| 1. | Storage access module | Implement functions to read from and write to contract storage
| 2. | Support for complex data types | Extend storage access capabilities to handle complex and nested data types within contract storage
| 3. | Performance optimization | Optimize storage access functions for better performance


### Milestone 4 - Docs & tutorials
- **Estimated duration:**  1 month
- **FTE:**  1
- **Costs:** 15,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains what we have achieved and how can people use what we created in this grant |
| 1. | Documentation | We will add to polkadart.dev the full documentation for every new API created |
| 2. | Tutorials | We will create tutorials and guides for different use-cases so the developer can check examples |


## Future Plans

We believe that one of the biggest issue of adoption to the Polkadot Ecosystem is the learning curve. Polkadart Team is trying to reduce this curve and make the ecosystem more attractive to any developer regardless of their level.

In the next few months we are planning to bring a playground that will help people to try-out everything directly in the browser without installing any dependencies or softwares.

With that in mind we want to bring the ink! v6 support to that as well.


## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Polkadot Blockchain Academy

Everything done in Polkadart so far was funding by Web3 Foundation. We have also applied to the Polkadot Open Source Grants with a different scope of what we have here. There is no overlap or double spending between the two applications.
