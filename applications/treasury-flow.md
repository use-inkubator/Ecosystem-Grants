# 🪼 Treasury Flow

- **Team Name:** Treasury Flow
- **Payment Address:** 1soESeTVLfse9e2G8dRSMUyJ2SWad33qhtkjQTv9GMToRvP

## Project Overview :page_facing_up:

### Overview

TreasuryFlow - A full-stack decentralized treasury management system supporting
vested, recurring, and instant payments with multi-signature attestation and
payment categories. It enables organizations to manage and automate payouts and
accounting via a ink! smart contract and a react frontend for treasury contract
deployment and management.

#### Key Features

- Smart Contract: An ink! smart contract for managing payouts with:
  - Payment Types:
    - Vested Payments: Locked funds released over time (e.g., W3F DV payments)
    - Recurring Payments: Regular payments (e.g., salaries, monthly rewards)
    - Instant Payments: One-time fixed rewards (e.g., content rewards)
  - Governance:
    - Multi-signature approval system
    - Configurable approval thresholds based on payment amount
    - Proxy account for distribution with additional signing requirements
  - Payment Categories:
    - Configurable categories
    - Category-based reporting and tracking
  - Optimization:
    - Aggregated payments to reduce transaction fees
    - Scheduled processing for efficiency
- Frontend Application
  - Based on Papi (+ papi ink! sdk)
  - Next.js 15 application
  - Role-based access control
  - Views
    - Landing
    - Treasury Dashboard
      - Payment scheduling and management interface
      - Treasury Funds Overview
      - Upcoming Payouts
      - Past Payouts
      - Simple Statistics
    - Add New Treasury
      - Relevant fields + Metadata
    - Add New Payout
      - Relevant fields (recipient, type, amount, metadata)

#### Relation to Ink ecosystem

This project enhances the ink! ecosystem by providing a production-ready
treasury management solution that demonstrates practical use cases for ink!
smart contracts, sets standards for payment management, and enables integration
with all `pallet-contract` / `pallet-revive` enabled chains with ink. It also
showcases how a dApp without additional backend services can be built (even
though we will use a db in the canary dApp to improve UX).

#### Project Idea Category

We think the project fits best into the Canary dApp category. While there is
definitely a future business model option with the Treasury Flow app it must
evolve from a canary application before taking that step. We hope to find
several users in the ecosystem that can utilize the application freely before
developing a business model from it.

#### Team Interest

The Team has worked on several ecosystem projects where treasury management was
needed and handled in complex ways
(https://github.com/orgs/Wag-Media/repositories) which includes storing private
keys in server environments: A discord bot tracks payment emojis added users
posts. Every week the aggregated payouts are sent to the users' wallets by the
bot. Treasury flow can shift important parts to the blockchain and authorized
smart contract requests.

- We recognize the growing need for robust treasury management in the Polkadot
  ecosystem
- We want to contribute a working, audited solution with powers to become
  production-ready
- The project combines technical challenges (smart contract development) with
  practical business needs
- The project can showcase how to use contemporary frontend tooling to create a
  nice UI + UX for smart contract interaction (papi based)
- We see an opportunity to set standards for treasury management in the Polkadot
  ecosystem with ink!
- We're excited to contribute to the broader Polkadot ecosystem through a
  practical, reusable open-source solution with many development options in the
  future

### Ink! Ecosystem Impact

TreasuryFlow will directly benefit the ink! ecosystem by providing a real,
treasury management dApp that is immediately usable by DAOs, teams, and
organizations operating on Polkadot and any chain supporting `pallet-revive`
with ink!. Here's how:

1. **Immediate Utility for Ecosystem Users**: DAOs, community treasuries, grant
   programs, and working groups needing to automate and govern payouts. Users
   can deploy the ink! contract via the provided frontend, configure their
   treasury, and manage all types of payments (vested, recurring, instant) with
   multi-signature approvals and category-based reporting - without writing
   code. The dApp will be open-source and free to use, lowering the barrier for
   new teams to adopt ink! smart contracts for real-world treasury operations.

2. **The frontend** (built with Papi and Next.js) will demonstrate how to build
   modern, user-friendly dApps that interact with **and deploy** ink! contracts,
   serving as a template for future projects. With treasury flow we demonstrate
   how modern dApps can use the blockchain (Polkadot) as a backend and replace
   API calls by contract calls - powered by ink! - while maintaining the API
   nature. E.g. the smart contract can be called from any ts app, e.g. react
   frontend, discord bot, ...

3. **Open-Source Reusability:** Other teams can fork, extend, or integrate
   TreasuryFlow's (audited) contracts and frontend for their own use cases
   (e.g., grant programs, payroll, bounty management). The code can be used for
   educational purposes too.

4. **Community Growth and Feedback:** By launching as a canary dApp,
   TreasuryFlow will gather real user feedback, drive adoption, and surface new
   feature requests, helping to shape the future of ink! dApp development.

### Project Details

> - CATEGORY:

Canary Dapp

> - What your project is _not_ or will _not_ provide or implement

- fungibles apis for smart contracts (we rely on
  [pop-api](https://github.com/r0gue-io/pop-node/blob/main/pop-api/src/v0/fungibles/mod.rs))
- xcm calls for assets on other chains (not yet)
- indexers or other apis for reading historical smart contract storage (e.g.
  balances)

> - An overview of the business model, including revenue streams, target market,
>   and scalability, if applicable.

There are several possible revenue streams. The smart contract itsself will be
open source so it can be deployed and altered by tech enthusiasts. The dApp will
hover offer a good UX that can be marketed and sold - either with monthly
payments to use the service (dashboard) or by adding a small percentage to
signed transactions as fees to the app.

Target market is: DAOs, (small) ecosystem grants, bounty managers, projects and
enterprises

#### Tech Stack

- ink v6 smart contract deployable on pallet-revive enabled chains
- next.js frontend, powered by papi

#### Core Functionality

- Add Payout
  - Different Payout Types (immediate, recurring, vested)
  - Payout Dates
  - Payout Thresholds (higher treasurer acceptens for higher amounts,
    configurable), e.g. p < 1000 USD: 1 treasurer, p > 5000 USD 2 treasurers,
    p > 10000 USD 3 treasurers.
- Process Payouts
  - Can be triggered by anyone, signed
- Authorization
  - Treasurers can be added and removed
  - relevant smart contract functions can only be executed by treasurers
  - relevant smart contract functions need a threshold of existing treasurers to
    be executed
- The contract stores processed payouts

Functions and function signatures can be seen in the provided smart contracts.

> - Future production plans and growth strategy, highlighting how the project
>   intends to achieve sustainability and long-term success, if applicable.

See below

## Team :busts_in_silhouette:

### Team members

- Niklas Jurij Plessing
- Mohammad Izabul Khaled

### Contact

- **Contact Name:** Niklas Jurij Plessing
- **Contact Email:** niklas@eedee.net
- **Website:** https://eedee.net

### Legal Structure

- **Registered Address:** Luxemburger Straße 31, 13353 Berlin, Germany
- **Registered Legal Entity:** Name of your registered legal entity, if
  available. (e.g. Duo Ltd.)

### Team's experience

niftesty has over 15 years of experience in software development and 4 years of
dApp development experience in the Polkadot ecosystem and has worked for
[different projects](https://eedee.net) using relevant libraries (polkadot.js,
polkadot-api) for chain connection. He has gathered relevant experience in rust
and ink! from the Polkadot Blockchain academy 2023 and worked on managing a
[treasury dApp with WagMedia](https://thewagmedia.com/audit/treasury).

Izabul has over 13 years of experience in software and product development.
Since 2021, he has been leading WagMedia with other team members, one of the
most prominent content creation platforms within the Polkadot ecosystem. He
brings expertise in project management and testing, taking full ownership of the
software development lifecycle. Izabul is also deeply involved in the Polkadot
DAO and actively participates in OpenGov discussions as a member of KusDAO.

### Team Code Repos

- https://github.com/Wag-Media/wagmedia-com-web
- https://github.com/niklasp/polkadot-nextjs-starter
- https://github.com/Wag-Media/wagmi-bot

Please also provide the GitHub accounts of all team members. If they contain no
activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/niklasp/
- https://github.com/ikhaled28

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/niklas-jurij-plessing-6b0295125/
- https://www.linkedin.com/in/mohammad-izabul-khaled-b9a53b35/

## Development Status :open_book:

- Created a
  [demo next.js application](https://v0-treasury-page-design.vercel.app/) with a
  demo landing page and a demo dashboard of the app (not connected to smart
  contracts yet)
- Created a
  [demo ink! v5 smart contract](https://github.com/niklasp/treasuryflow/blob/main/contract_treasury_v5/lib.rs)
  (with non-native asset functionality to test that functionality)
- Created a
  [demo ink! v6 smart contract](https://github.com/niklasp/treasuryflow/blob/main/contract_treasury_v6/lib.rs)
  (only native asset functionality)
- QA

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 4 Months
- **Full-Time Equivalent (FTE):** total 2.5 FTE (in a 3:1 ratio between Dev/QA)
- **Total Costs:** 40,000 USD

### Milestone 1 — Basic smart contracrt functionality + Frontend

- **Estimated duration:** 2.5 month
- **FTE:** 1.5
- **Costs:** 24,000 USD

| Number  | Deliverable               | Specification                                                                                                                                                                                                                                 |
| ------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **0a.** | MIT                       |                                                                                                                                                                                                                                               |
| **0b.** | Documentation             | We will provide both **inline documentation** of the code and a basic **tutorial** in a readme that explains how the smart contract can be deployed manually and how the frontend can be setup (also to deploy the smart contracts)           |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the readme, we will describe how to run these tests.                                                                              |
| **0d.** | Docker                    | We will provide a Dockerfile that sets up a complete frontend + contract environment for compiling, testing and interacting with the treasury flow contract.                                                                                  |
| 1a.     | Payout Creation           | We will create smart contract functions to add immediate / recurring / vested payouts that require signatures of a changing amount of treasurers based on configurable thresholds. There will also be functions to update and delete payouts. |
| 1b.     | User Management           | We will create smart contract functions to add and remove treasurers to the treasury contract. There will be options for priviledged or disabled owner access                                                                                 |
| 1c.     | State Retrieval           | We will create smart contract functions to read smart contract state of all relevant values                                                                                                                                                   |
| 1d.     | State Mutation            | We will create smart contract functions to mutate relevant smart contract state (threshold, payout frequency, ...)                                                                                                                            |
| 2a.     | Landing Page              | The landing page will list features of the app and a working CTA to create a treasury as well as see a demo app                                                                                                                               |
| 2b.     | Dashboard Page            | The dApp will show a dashboard page for each deployed treasury contract, some features (e.g. add payout) will be disabled / invisible for viewers and only be accessible to treasurers / owner of the contract                                |
| 2c.     | Add Treasury Form         | The dApp will show a form with relevant fields that will trigger the deployment of a new treasury contract                                                                                                                                    |
| 2d.     | Contract Configuration    | The dApp will allow authorized users to change contract settings = sign txs to interact with smart contract functions                                                                                                                         |

### Milestone 2 — Additional features

- **Estimated duration:** 1.5 month
- **FTE:** 1
- **Costs:** 16,000 USD

|  Number | Deliverable               | Specification                                                                                                                                                                                                                                                              |
| ------: | ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **0a.** | MIT                       |
| **0b.** | Documentation             | We will provide both **inline documentation** of the code and a basic **tutorial** in the frontend (/docs) that explains how the smart contract can be deployed manually and how the frontend can be setup (also to deploy the smart contracts)                            |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the readme, we will describe how to run these tests.                                                                                                           |
| **0d.** | Docker                    | We will provide a Dockerfile that sets up a complete frontend + contract environment for compiling, testing and interacting with the treasury flow contract and includes all changes made in Milestone 2                                                                   |
|     0e. | Article                   | We will publish an **article** on Medium or X that explains all features of the frontend application and smart contract functionality as well as how it could be used in existing tresuries.                                                                               |
|      1. | User Feedback             | We will prepare a form to collect user feedback and incentivize participation in order to find missing functionality and UX issues                                                                                                                                         |
|     2a. | Contract Optimizations    | After an external and funded audit from e.g. [vCISO Program w/Spearbit](https://polkadot.subsquare.io/referenda/797) or [Polkadot Assurance Legion](https://dotpal.io/), we will implement all proposed changes and focus on optimizing storage and contract upgradability |
|     2b. | Contract Events           | The smart contract will emit relevant events after state mutations for better indexability and apply [topics](https://use.ink/docs/v5/basics/events#topics) where possible                                                                                                 |
|     2c. | Non Native Assets         | The smart contract will allow logic for payouts and other relevant functions for multiple (+non native) assets                                                                                                                                                             |
|      3. | Frontend Optimizations    | The frontend will work on all device sizes and apply best practises in web development e.g. Server Side Rendering + caching where possible                                                                                                                                 |

## Future Plans

- General

  - Leveraging Polkadot Powers to make cross chain asset management and payouts
    possible via xcm
  - Explore how JAM can be of use for the project

- Smart Contract

  - Configurable payout categories for better organization of funds (e.g.
    Development, Design, QA, ...)

- Frontend

  - Approval Flow Visualization (similar to multisig like mimir)
  - Accounting / Advanced statistics
  - Indexer that indexes contract events for better spending tracking
  - Category management

- Integrations
  - Github Payments: create a service that allows priviledged accounts to add
    payments to github issues via reactions
  - Discord Payments: create a service that allows priviledged accounts to add
    payments via discord emojis

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Created the updated
https://use.ink page wich also includes the https://use.ink/inkubator/ page

Part of the success of the project relies on non-native asset functionality.
Currently the pop-api used in ink5 is not ported to inkv6 yet but the
[ink alliance confirmed it will be developed](https://t.me/inkathon/569/2713).

At the moment of submitting this application the v5 contract in the provided
repository is more feature rich than the v6 contract (vesting, cleanup, data
types). We are aware that v6 contracts are needed for the submission. The
difference is that some tooling did not work yet fully, that is why we continued
developing the v5 contract first.

A project with some similarities has been funded by the w3f 2 years ago:
https://github.com/ankas-lab/openPayroll. We are aiming for a contract with
extended functionality, inkv6 and a more feature rich frontend.
