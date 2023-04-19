# Roloi Multi-Sig Vault

- **Team Name:** NeoPower Digital
- **Project Category:** Canary DApp
- **Payment Address:** `1dz667uQX199rHyj6tizmL6EJe4AZxjH1RhnyrT1QuQ4pfS`

## Project Overview :page_facing_up:
### Overview

Multi-Sig Vault Canary Dapp. 

### Project Details

**Roloi Multi-Sig Vault** is a generic multi-key wallet that empowers the security of funds. The DApp allows **sharing a vault between multiple users** to enable collective asset management.

- A transaction requires **approval of multiple users.**
- The **required** number of **confirmations** can be **configured by the owners**. 
  - An owner should submit a transaction with the update request.

The Roloi Multi-Sig Vault will enable **two time-restriction settings** to add an extra layer of security for withdrawals:

- **Lockup period:** time until a deposited amount of tokens can be withdrawn. 
- **Confirmation window:** time available to reach the required number of owner confirmations before the transaction is automatically revoked.

![ink!ubator Ecosystem Grant Application](https://user-images.githubusercontent.com/107150702/233152410-bb95f6af-2a5b-4011-9252-8cf9e3fbc2a6.jpg)

This grant application includes two smart contracts and one front-end:
- Roloi Multi-Sig tracker
- Roloi Multi-Sig vault
- Vault UI

#### Roloi Multi-Sig tracker

This contract will contain the relation between users and multi-sig vaults.

- Instantiated multi-sig vault smart contracts will be persisted in the storage.
- When the owners of a multi-sig vault are changed, the storage of this smart contract will be updated. 

#### Roloi Multi-Sig vault

This contract will be the vault that enables secure transactions through multiple approvals and adds time restrictions to withdrawals:

- Owners and requirements are saved in the storage of the smart contract.
- Messages to change the ownership and requirements that follow the required number of confirmations.
- Messages to submit, confirm, revoke, cancel, and invoke transactions. 
- Security validations for all the transactions to avoid mismanagement of assets.

#### Vault UI

And finally, the second milestone will provide a **Next.js UI for the users to interact with the vaults**. See Milestone 2 for requirements.

![multi-sig-vault wireframe](https://user-images.githubusercontent.com/107150702/233193720-28a157dd-515a-4a39-b23a-2b42952cf1d3.png)

## Team :busts_in_silhouette:

### Team members

We are NeoPower, a Web3 software company. Our core team members:

- **Brian Sasbon** (Co-Founder & CEO)
- **Pablo Corrado** (Co-Founder & CTO)
- **Hernán Hermida** (CGO)

### Contact

- **Contact Name:** Brian Sasbon
- **Contact Email:** bsasbon@neopower.digital
- **Website:** https://www.neopower.digital/ 

### Legal Structure

- **Registered Address:** Pacheco 2131, CABA, Buenos Aires, Argentina (CP1431)
- **Registered Legal Entity:** NeoPower Digital, LLC

### Team's experience

#### Founders

We are Brian and Pablo, **Software Engineers** with a Degree from the National Technological University (UTN) from Buenos Aires, Argentina, and have more than **10 years of experience** as developers for many different projects. We have strong experience working as **Full-stack Developers and Team Managers** for US traditional finance clients like Morgan Stanley, Visa, and JP Morgan.

6 years ago **we founded NeoPower**, our own software company to work for different clients building freelance teams of designers, developers and testers.

We are building Roloi, a payment automation platform to enable on-chain payment flow automation in Astar. Our project was supported through a grant from the Web3 Foundation.

We are also very active in the Polkadot spanish community:
- [ink! workshop (Polkadot Hackathon Latam)](https://www.youtube.com/watch?v=IevnhbLQg-k&ab_channel=PolkadotHackathonLatam)
- [ink! workshop (Polkadot Blockchain Academy - Buenos Aires)](https://www.youtube.com/watch?v=o11eUZ2X2XY)
- [ink! intro (Polkadot Hackathon Latam - Closing event)](https://www.youtube.com/watch?v=78BmvjtBP_M)
- [ink! official docs - Translation to spanish](https://github.com/paritytech/ink-docs/pulls?q=is%3Apr+is%3Aclosed+author%3Apcorrado-np)
- (coming soon) ink! 8-week course in Spanish (Polkadot Hub)

#### CGO

**Hernán S. Hermida** (aka Milstein) is a **DeFi Researcher** with more than 2 years of experience contributing to educational communities in Latam. Currently, he **hosts #DeFiSpace** a weekly Twitter Spaces cycle, with more than 50 episodes, interviewing builders from different multi-chain projects, and creates content for **[“La Multisig”](https://www.youtube.com/@LaMultisig)**, a web3 educational YouTube Channel with its own community. 

He’s the growth lead of [DeFi Argentina](https://twitter.com/DeFiArgentina) a non-profit project that helps children’s food banks in Argentina by collecting donations in cryptocurrencies. 

He’s also been an OAK ambassador since Nov 2022.

Hernán is part of the Roloi team as CGO to help with the growth, research and networking strategy, leveraging his knowledge about DeFi and communities.


### Team Code Repos

- [NeoPower Github Repository](https://github.com/NeoPower-Digital)

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):** 3
- **Total Costs:** 30,000 USD

### Milestone 1 — Smart Contracts

- **Estimated duration:** 1 month
- **FTE:** 4
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | **License** | MIT |
| **0b.** | **Documentation** | The milestone will include technical documentation of the smart contracts. |
| **0c.** | **Testing Guide** | Core functions will be covered by unit tests to ensure functionality and robustness. We will describe how to run these tests in the docs. |
| **1.** | **Multi-Sig Vault - ink! Smart Contract** | This smart contract will be a multi-signature vault that facilitates secure transactions by requiring multiple approvals and implementing time-based restrictions for withdrawals.  |
| 1a. | Ownership | The contract will store the owners of the multi-sig vault and expose messages to add and remove them.  |
| 1b. | Submit Transaction | The contract will include a message to submit a new transaction to be executed after the required confirmations.  |
| 1c. | Confirm/Revoke Transaction | The contract will include two messages to confirm and revoke a transaction.  |
| 1d. | Cancel Transaction | The contract will include a message to cancel a transaction. This action can only be executed if the corresponding transaction has not received more than one confirmation and is done by the same account that initiated the transaction. |
| 1e. | Invoke Transaction | The contract will include a message to invoke a transaction that has received the required confirmations. |
| 1f. | Requirements Management | The contract will include messages to modify the required number of confirmations and the time restriction settings. |
| 1g. | Security Validations | The contract will inspect the ownership, the requirements and the integrity of the storage to ensure the multi-sig vault.  |
| **2.** | **Multi-Sig Tracker - ink! Smart Contract** | This smart contract will contain the relation between users and multi-sig vaults. |
| 1a. | Accounts - Multi-Sig Vaults Relation | The contract will store a mapping between the user’s accounts and their multi-sig vaults. |
| 1b. | Ownership update | The contract will keep updated the relation between the user’s accounts and their multi-sig when an ownership change was done. |

### Milestone 2 — UI

- **Estimated duration:** 1 month
- **FTE:** 2
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | **License** | MIT |
| **0b.** | **Documentation** | The milestone will include technical documentation of the smart contracts. |
| **0c.** | **Testing Guide** | Core functions will be covered by unit tests to ensure functionality and robustness. We will describe how to run these tests in the docs. |
| **1.** | **UI Source Code** | We will deliver a Next.js UI project enabling interaction and managing users' multi-signature vaults. The features will be described below. *Tools and libraries: Next.js, Typescript, Material UI, XState, polkadot.js.* |
| 1a. | Wallet connection | The UI will connect with Polkadot Wallets using polkadot.js functionalities.  |
| 1b. | Chain connections | The UI will allow the user to connect with some parachains that support ink! smart contracts, using polkadot.js functionalities. |
| 1c. | Multi-sig vaults list | Multi-sig vaults list related to the connected wallet. |
| 1d. | Multi-sig vault interaction | Actions over the vault: submit, confirm, revoke, cancel, and execute transactions. |
| 1e. | Multi-sig vault configuration | Ability to update: required number of signers and time-based settings (lockup period, confirmation window) |

## Future Plans

- Reuse the multi-sig vault smart contracts in [Roloi](https://twitter.com/RoloiMoney)
- Push notifications to sign transactions
- Automatic transactions trigger when reaching the required confirmations.
- Add guards to make checks before and after a transaction.


## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Twitter.

Links:

https://roloi.money

https://neopower.digital
