# Polkadot Meetup Hub

- **Team Name:** Polkadot Meetup Hub Team  
- **Payment Address:** `<Your Polkadot Payment Address>` *(DOT)*

---

## Project Overview 📜

### Overview

- **Tagline:** *A decentralized event platform fostering Polkadot community growth through governance discussions and collaboration.*  
- **Description:** Polkadot Meetup Hub is a decentralized event platform powered by ink! smart contracts on a Polkadot parachain. It empowers users to create, discover, and join online and in-person meetups, driving community engagement with a deposit-based registration system for accountability.  
- **Relation to ink! Ecosystem:** Built with ink! v6.X smart contracts on a Polkadot parachain, leveraging multiple wallet integrations (e.g., Polkadot.js, Talisman) for secure, on-chain interactions.  
- **Project Category:** Canary Dapp—a live-use decentralized meetup application showcasing ink!’s real-world potential.  
- **Motivation:**  
Our team is driven to bolster Polkadot’s community engagement by facilitating on-chain governance discussions and knowledge-sharing. We’ve previously led efforts like "Proof of Chaos" to increase voter turnout in the Kusama and Polkadot ecosystems, achieving temporary boosts in participation. However, these gains faded over time, highlighting a challenge: one-off initiatives alone don’t sustain governance activity. This led us to prioritize meetups—both online and in-person—as a way to build lasting connections among developers, governance participants, and community members.<br><br>
Polkadot’s 2024 ecosystem data supports this focus. OpenGov peaked at 171 referenda in July 2024, coinciding with Polkadot Decoded in Brussels, and recorded the second-highest monthly DOT voting volume (source: [Tekedia, Q3 2024](https://www.tekedia.com/the-polkadot-ecosystems-remarkable-growth-in-q3-2024/)). This surge suggests major events can drive engagement, yet the subsequent drop-off (e.g., fewer referenda in later months per Tekedia) shows the need for ongoing interaction. Polkadot Meetup Hub addresses this gap with a trustless, on-chain platform for organizing meetups, aiming to sustain governance participation and fuel ecosystem growth.

### ink! Ecosystem Impact

Polkadot Meetup Hub strengthens the ink! ecosystem by:  
- Showcasing ink!’s real-world utility in event management with efficient, WASM-based contracts.  
- Boosting on-chain app adoption within Polkadot’s community.  
- Offering a reference Canary Dapp for decentralized event platforms.  
- Ensuring trustless coordination via deposit and refund mechanisms.  
- Supporting onboarding with educational meetups (e.g., ink! workshops, parachain tutorials).  
- Fostering collaboration among developers and governance participants, enhancing network cohesion.

### Project Details

- **Core Functionality:**  
  - *Event Creation & Management*: Create meetups (`create_meetup`) with customizable fields (title, description, location, time), cancel events (`cancel_meetup`) with automated refunds, and update states (`update_state`) for attendance tracking.  
  - *Deposit-Based Registration*: Attendees stake a deposit to RSVP, refunded on attendance or forfeited for no-shows.  
  - *Timezone-Aware Scheduling*: Global timezone support with automatic conversions for seamless coordination.  
  - *On-Chain Tracking*: Immutable event records on the parachain for transparency.  

- **Technology Stack:**  
  - *ink! Smart Contracts*: Rust-based, ink! v6.X contracts deployed on a Polkadot parachain (e.g., Astar or Moonbeam) for WASM execution of all logic.  
  - *Multi-Wallet Integration*: Frontend supports Polkadot-compatible wallets (e.g., Polkadot.js, Talisman, Nightly, SubWallet) for authentication and interactions.  
  - *IPFS (Optional)*: Decentralized storage for event metadata (e.g., images, descriptions) to optimize costs.  

- **Audit Required:** Yes  
- **Category:** Canary Dapp  
- **Business Model:**  
  - Revenue from event creation fees and sponsorship tiers.  
  - Scaling to enterprise conferences with premium features.  
- **Future Plans:**  
  - NFTs for proof of attendance/hosting, enhancing reputation and rewards.  
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
- **Smart Contract Development:** Core ink! v6.X contracts are being built in our public repository (`<https://github.com/<your_organisation>/<project_repo>>`). Features like `create_meetup`, deposit registration, and state management are in progress, tracked via GitHub issues. Initial prototypes for event creation and deposits are deployed on Astar Shibuya testnet, with iterations based on testing feedback.  
- **Current Progress:** As of April 2025, we’ve achieved a proof-of-concept with working smart contracts and preliminary multi-wallet integration (Polkadot.js, Talisman, etc.). The frontend is in early stages with mockups and basic connectivity. Next steps align with Milestone 1 of our roadmap.  

---

## Development Roadmap 🔩

### Overview
- **Total Estimated Duration:** 3 months  
- **Full-Time Equivalent (FTE):** 2 FTE  
- **Total Costs:** 20,000 USD (payable in DOT)  
- **Description:** Two milestones: core system deployment (Milestone 1) and UI/feature enhancements (Milestone 2), with rigorous testing and documentation.

### Milestone 1: Core Event Management
- **Estimated Duration:** 1.5 months  
- **FTE:** 1.5 (1 developer full-time, 1 part-time QA/docs)  
- **Costs:** 10,000 USD  
- **Goal:** Functional on-chain event system with basic frontend.

| Number | Deliverable           | Specification                                                                                   |
|--------|-----------------------|-------------------------------------------------------------------------------------------------|
| 0a.    | License              | Apache 2.0, applied to all repositories.                                                        |
| 0b.    | Documentation        | Inline Rust/ink! comments and a Markdown deployment tutorial.                                   |
| 0c.    | Testing & Guide      | Unit/integration tests for `create_meetup`, `cancel_meetup`, deposits; includes testing guide.  |
| 0d.    | Docker               | Dockerized setup with ink! contract deployment for local testing.                               |
| 0e.    | Article              | ~800-word blog post on decentralized event management, published on team or ecosystem channel.  |
| 1.     | Meetup Creation      | ink! contract for event creation (title, description, datetime, location, capacity).           |
| 2.     | Registration & Deposits | Deposit logic with automated refunds/forfeiture, including balance checks.                    |
| 3.     | Timezone Scheduling  | Basic frontend component for timezone-aware event display, validated on-chain.                 |

- **Acceptance Criteria:**  
  - Contracts deploy on a testnet (e.g., Astar Shibuya).  
  - Deposits/refunds work in test scenarios.  
  - Frontend shows timezone-adjusted events.

### Milestone 2: Enhancements & UI
- **Estimated Duration:** 1.5 months  
- **FTE:** 1.5 (1 developer full-time, 1 part-time UI/UX)  
- **Costs:** 10,000 USD  
- **Goal:** Polished UI and advanced features for a production-ready dApp.

| Number | Deliverable           | Specification                                                                                   |
|--------|-----------------------|-------------------------------------------------------------------------------------------------|
| 0a.    | Updated Documentation | Revised docs for Milestone 2 features, hosted on GitHub wiki/ReadMe.                           |
| 0b.    | Testing Expansion    | Integration and end-to-end tests for state updates and verification (e.g., RSVP to refund).    |
| 1.     | UI/Frontend          | Responsive Next.js frontend with wallet integration, event listings, and RSVP dashboard.       |
| 2.     | Event State Management | Enhanced `update_state` and `cancel_meetup` with host-only permissions via signatures.         |
| 3.     | Advanced Verification | On-chain check-in (e.g., QR codes, message signing) tied to refunds; revenue split (10% platform, 90% host).    |

- **Acceptance Criteria:**  
  - UI integrates with wallets and shows real-time data.  
  - State changes execute correctly on-chain.  
  - Check-in and revenue distribution work on testnet.

### Additional Notes
- **Dependencies:** Milestone 2 builds on Milestone 1 contracts.  
- **Cost Breakdown:** 60% development, 20% docs/outreach, 20% UI/UX.  
- **Next Steps:** Post-Milestone 2, focus on feedback, audits, and mainnet prep with NFTs.

---

## Additional Information ➕

- **How did you hear about the Bounty Program?** Twitter  
- **Note:** All code will be open-source under Apache 2.0, using ink! v6.X

