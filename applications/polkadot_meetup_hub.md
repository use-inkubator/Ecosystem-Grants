# Polkadot Meetup Hub

- **Team Name:** Polkadot Meetup Hub Team  
- **Payment Address:** `<Your Polkadot Payment Address>` *(DOT)*

---

## Project Overview 📜

### Overview

- **Tagline:** *A decentralized event platform fostering Polkadot community growth through governance discussions and collaboration.*  
- **Description:** Polkadot Meetup Hub is a decentralized event platform powered by ink! v6 smart contracts, deployed on either the Pop Network or Kusama Asset Hub parachain. It enables users to create, discover, and join online and in-person meetups, driving community engagement with a deposit-based registration system for accountability. Leveraging PAPI and light clients, the platform ensures efficient, lightweight interactions with the Polkadot ecosystem.  
- **Relation to ink! Ecosystem:** Built with ink! v6 smart contracts, utilizing PAPI for seamless blockchain queries and light clients for low-resource access, all hosted on a Polkadot parachain (Pop Network or Kusama Asset Hub). It supports multiple wallet integrations (e.g., Polkadot.js, Talisman) for secure, on-chain interactions.  
- **Project Category:** Canary Dapp—a live-use decentralized meetup application showcasing ink!’s real-world potential.  
- **Motivation:**  
Our team is driven to bolster Polkadot’s community engagement by facilitating on-chain governance discussions and knowledge-sharing. We’ve previously led efforts like "Proof of Chaos" to increase voter turnout in the Kusama and Polkadot ecosystems, achieving temporary boosts in participation. However, these gains faded over time, highlighting a challenge: one-off initiatives alone don’t sustain governance activity. This led us to prioritize meetups—both online and in-person—as a way to build lasting connections among developers, governance participants, and community members.<br><br>
Polkadot’s 2024 ecosystem data supports this focus. OpenGov peaked at 171 referenda in July 2024, coinciding with Polkadot Decoded in Brussels, and recorded the second-highest monthly DOT voting volume (source: [Tekedia, Q3 2024](https://www.tekedia.com/the-polkadot-ecosystems-remarkable-growth-in-q3-2024/)). This surge suggests major events can drive engagement, yet the subsequent drop-off (e.g., fewer referenda in later months per Tekedia) shows the need for ongoing interaction. Polkadot Meetup Hub addresses this gap with a trustless, on-chain platform for organizing meetups, aiming to sustain governance participation and fuel ecosystem growth.

### ink! Ecosystem Impact

Polkadot Meetup Hub strengthens the ink! ecosystem by:  
- Demonstrating ink! v6’s capabilities in event management with efficient, WASM-based contracts on Pop Network or Kusama Asset Hub.  
- Utilizing PAPI for optimized blockchain queries and light clients.  
- Boosting on-chain app adoption within Polkadot’s community.  
- Providing a reference Canary Dapp for decentralized event platforms.  
- Ensuring trustless coordination with deposit and refund mechanisms.  
- Supporting onboarding via educational meetups (e.g., ink! workshops, parachain tutorials).  
- Enhancing network cohesion by connecting developers and governance participants.

### Project Details

- **Core Functionality:**  
  - *Event Creation & Management*: Create meetups (`create_meetup`) with customizable fields (title, description, location, time), cancel events (`cancel_meetup`) with automated refunds, and update states (`update_state`) for attendance tracking—all powered by ink! v6.  
  - *Deposit-Based Registration*: Attendees stake a deposit to RSVP, refunded on attendance or forfeited for no-shows, managed on-chain.  
  - *Timezone-Aware Scheduling*: Global timezone support with automatic conversions for seamless coordination.  
  - *On-Chain Tracking*: Immutable event records stored on Pop Network or Kusama Asset Hub for transparency.  

- **Technology Stack:**  
  - *ink! Smart Contracts*: Rust-based ink! v6 contracts deployed on Pop Network or Kusama Asset Hub for WASM execution of all logic.  
  - *PAPI Integration*: Polkadot API (PAPI) for efficient querying of blockchain state (e.g. balances) and real-time updates.  
  - *Light Clients*: Embedded light client support (e.g., via smoldot or similar) for lightweight, trustless frontend interactions without full nodes.  
  - *Multi-Wallet Integration*: Frontend supports Polkadot-compatible wallets (e.g., Polkadot.js, Talisman, Nightly, SubWallet) for authentication and transactions.  
  - *IPFS (Optional)*: Decentralized storage for event metadata (e.g., images, descriptions) to reduce on-chain costs.  

- **Audit Required:** Yes  
- **Category:** Canary Dapp  
- **Business Model:**  
  - Revenue from event creation fees and sponsorship tiers.  
  - Scaling to enterprise-grade conferences with premium features.  
- **Future Plans:**  
  - NFTs for proof of attendance/hosting, minted on Kusama Asset Hub.  
  - Decentralized identity integration (e.g., KILT Protocol or Polkadot Citizenship).  
  - Partnerships with Polkadot projects for co-hosted events.  

---

## Team 👥

### Team Members
- **Team Lead:** `Gabriel Jaeger`  
- **Developers:** `Gabriel Jaeger`, `<Team Member 2>`  
- **Designer:** `<Team Member 3>` 

### Contact
- **Contact Name:** `Gabriel Jaeger`  
- **Contact Email:** `<Your Email>`  
- **Website:** `<Your Website>`  

### Legal Structure
- **Registered Address:** `<Your Address>`  
- **Registered Legal Entity:** `<Your Legal Entity Name>`  

### Team Experience
- Proven expertise in ink! smart contract and Polkadot development.  
- Contributions to open-source blockchain projects.  
- Background in decentralized governance and dApp design.  

### Team Code Repositories
- `https://github.com/orgs/Proof-Of-Chaos/repositories`  

### Team LinkedIn Profiles
- `<https://www.linkedin.com/in/<person_1>>`  
- `<https://www.linkedin.com/in/<person_2>>`  

---

## Development Status 📖

Polkadot Meetup Hub is in active development, with foundational progress underway:  
- **Smart Contract Development:** Core ink! v6 contracts are being built in our public repository (`<https://github.com/<your_organisation>/<project_repo>>`). Features like `create_meetup`, deposit registration, and state management are in progress, tracked via GitHub issues. Initial prototypes are deployed on a testnet (e.g., Pop Network testnet or Kusama Asset Hub test environment), with iterations based on testing feedback.  
- **Current Progress:** As of April 2025, we’ve achieved a proof-of-concept with working ink! v6 contracts, PAPI integration for state queries, and light client support in early testing. The frontend is in early stages with mockups and basic connectivity to Pop Network or Kusama Asset Hub. Next steps align with Milestone 1 of our roadmap.  

---

## Development Roadmap 🔩

### Overview
- **Total Estimated Duration:** 3 months  
- **Full-Time Equivalent (FTE):** 2 FTE  
- **Total Costs:** 25,000 USD  
- **Description:** Two milestones: core system deployment with PAPI and light clients (Milestone 1) and UI/feature enhancements (Milestone 2), with rigorous testing and documentation.

### Milestone 1: Core Event Management
- **Estimated Duration:** 1.5 months  
- **FTE:** 1.5 (1 developer full-time, 1 part-time QA/docs)  
- **Costs:** 12,500 USD  
- **Goal:** Functional on-chain event system with PAPI, light clients, and basic frontend on Pop Network or Kusama Asset Hub.

| Number | Deliverable           | Specification                                                                                   |
|--------|-----------------------|-------------------------------------------------------------------------------------------------|
| 0a.    | License              | Apache 2.0, applied to all repositories.                                                        |
| 0b.    | Documentation        | Inline Rust/ink! comments and a Markdown deployment tutorial for Pop Network/Kusama Asset Hub.  |
| 0c.    | Testing & Guide      | Unit/integration tests for `create_meetup`, `cancel_meetup`, deposits; includes testing guide.  |
| 0d.    | Docker               | Dockerized setup with ink! v6 contract deployment for local testing.   |
| 0e.    | Article              | Blog post on decentralized event management with ink! v6, published on ecosystem channels.  |
| 1.     | Meetup Creation      | ink! v6 contract for event creation (title, description, datetime, location, capacity).         |
| 2.     | Registration & Deposits | Deposit logic with automated refunds/forfeiture, balance checks.          |
| 3.     | Timezone Scheduling  | Basic frontend with light client integration for timezone-aware event display, validated on-chain. |

- **Acceptance Criteria:**  
  - Contracts deploy on Pop Network testnet or Kusama Asset Hub.  
  - Deposits/refunds work in test scenarios.  
  - Light client frontend shows timezone-adjusted events.

### Milestone 2: Enhancements & UI
- **Estimated Duration:** 1.5 months  
- **FTE:** 1.5 (1 developer full-time, 1 part-time UI/UX)  
- **Costs:** 12,500 USD  
- **Goal:** Polished UI and advanced features for a production-ready dApp.

| Number | Deliverable           | Specification                                                                                   |
|--------|-----------------------|-------------------------------------------------------------------------------------------------|
| 0a.    | Updated Documentation | Revised docs for Milestone 2 features, hosted on GitHub wiki/ReadMe.                           |
| 0b.    | Testing Expansion    | Integration and end-to-end tests for state updates and verification.    |
| 1.     | UI/Frontend          | Responsive frontend with wallet integration, event listings, and RSVP dashboard using light clients. |
| 2.     | Event State Management | Enhanced `update_state` and `cancel_meetup` with host-only permissions via signatures.         |
| 3.     | Advanced Verification | On-chain check-in (e.g., QR codes, message signing) tied to refunds; revenue split (10% platform, 90% host). |

- **Acceptance Criteria:**  
  - UI integrates with wallets and shows real-time data via PAPI/light clients.  
  - State changes execute correctly on-chain.  
  - Check-in and revenue distribution work on testnet.

### Additional Notes
- **Dependencies:** Milestone 2 builds on Milestone 1 contracts and PAPI/light client setup.  
- **Cost Breakdown:** 60% development, 20% docs/outreach, 20% UI/UX.  
- **Next Steps:** Post-Milestone 2, focus on feedback, audits, and mainnet deployment with NFTs.

---

## Additional Information ➕

- **How did you hear about the Bounty Program?** Twitter  
- **Note:** All code will be open-source under Apache 2.0, using ink! v6, PAPI, and light clients on Pop Network or Kusama Asset Hub.

