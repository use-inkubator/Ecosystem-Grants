# VaultOne

**Team Name:** VaultOne Labs  
**Payment Address:** `15cyCGodVcZpgCkfxSLxLr5XGS4bC5yqXcLrUNdugsp7yJHq`

---

## Project Overview

**Tagline:**  
Secure, milestone-based escrow on ink! — fast, flexible, and trust-minimized.

**Description:**  
VaultOne is a lightweight, on-chain escrow system for peer-to-peer and freelance transactions. It enables secure payments with milestone tracking, embedded dispute resolution, and optional mediator integration — all powered by ink! smart contracts. The system reduces trust overhead between unknown parties and is ideal for Web3 contributors, clients, and small DAOs seeking non-custodial agreements.

**Relation to ink! ecosystem:**  
VaultOne will be entirely developed using ink! smart contracts. It aims to serve as a public escrow module for teams and contributors working within the Polkadot and Substrate ecosystems, particularly those transacting without intermediaries.

**Category:** Canary Dapp

**Why we're building it:**  
We’ve faced broken agreements and loss of funds in remote collaborations. VaultOne was born out of this pain. We want to provide a decentralized, user-owned solution to help others avoid the same pitfalls and improve the reliability of on-chain commitments.

---

## Ink! Ecosystem Impact

VaultOne contributes directly to the ink! ecosystem by offering a real-world dApp use case: secure on-chain escrow. It showcases ink!'s capability to manage:

- State transitions (milestone tracking)
- Access control (roles)
- Conflict resolution (disputes + mediators)

Once open-sourced, VaultOne can be forked or extended by other teams building vertical-specific marketplaces (e.g., freelance platforms, bounty boards, task DAOs).

**Goal:**  
Serve as a production-ready escrow template for Polkadot projects, validators hiring devs, DAOs commissioning creative work, and developers managing staged deliverables.

---

## Project Details

### Data Models / API Specs

- **EscrowContract** with roles: payer, payee, optional mediator  
- **Milestone struct:** amount, status, description  
- **Functions:** `initiate_escrow`, `approve_milestone`, `raise_dispute`, `resolve_dispute`, `release_payment`

### Technology Stack

- ink! smart contracts for core logic  
- Polkadot.js and Ethers.js for frontend contract interactions  
- Minimal TypeScript-based frontend for demo

### Documentation / Architecture

- Modules: Role Logic, Milestone Engine, Dispute Engine  
- Contracts will follow open standards for account abstraction and modular upgradability

### PoC or Prior Work

- Fresh implementation, with prototyped UX in Figma  
- Team has previously built similar mechanisms in Solidity

### Limitations

- No fiat ramps or KYC features  
- No DAO governance layer initially (planned for future)

---

## Business Model

VaultOne is intended as open escrow infrastructure. A hosted version could generate revenue through:

- Optional mediation fees  
- API access for platforms  

The MVP will remain free and open-source to enable adoption and forking.

### Future Production Plans

- Integrate with freelancing dApps and bounties  
- Add plug-and-play governance for teams/DAOs  
- Launch a mediation DAO for decentralized conflict resolution  
- Potential integration with zk-identity tools for private arbitration

---

## Team

**Team Members:**

- Keith Otieno — Frontend Developer  
- Kevin Mulinge — Backend Developer  
- Cyril Obuya — Backend Developer

**Contact:**

- **Name:** Keith Otieno  
- **Email:** keithomark@gmail.com

**Legal Structure:**

- **Registered Address:** Nairobi, Kenya  
- **Legal Entity:** In progress

**Team Experience:**  
Our team brings experience from multiple Web3 hackathons, where we’ve delivered working prototypes across multiple ecosystems. We've previously built tools that focus on seamless user experience, contributor coordination, and secure handling of digital assets.

We care deeply about making blockchain applications usable for everyday people and have worked on products that aim to simplify interactions without compromising functionality.

---

## Code Repositories

- [VaultOne Repo](https://github.com/OtienoKeith/vaultone)  
- GitHub Profiles:
  - [OtienoKeith](https://github.com/OtienoKeith)
  - [ceeroblaq](https://github.com/ceeroblaq/)
  - [kevinmulinge](http://github.com/kevinmulinge)

**LinkedIn:**  
- [Keith Otieno](https://www.linkedin.com/in/keith-otieno/)

---

## Development Status

- Project currently in ideation stage  
- Exploring escrow pain points for DAOs, freelancers, and small teams in Web3  
- Gathering insights from early informal discussions with potential users  
- Planning contract architecture and key user roles to align with ink! capabilities

---

## Development Roadmap

### Overview

- **Total Duration:** 4 months  
- **FTE:** 1.5  
- **Total Costs:** $50,000 USD

---

### Milestone 1 — Core Architecture

- **Duration:** 1 month  
- **FTE:** 1.5  
- **Cost:** $12,500

| Deliverable       | Specification |
|-------------------|---------------|
| 0a. License        | MIT |
| 0b. Documentation  | Inline contract docs and user flow diagrams |
| 0c. Testing Guide  | Unit tests for contract state transitions and role logic |
| 0d. Docker         | Dockerfile for local testnet deployment |
| 1. Contract Schema | Data structures and function definitions |
| 2. Role Logic      | Role-based execution for payer, payee, mediator |
| 3. Payment Config  | Milestone setup, sequencing, and locking logic |

---

### Milestone 2 — Implementation

- **Duration:** 1 month  
- **FTE:** 1.5  
- **Cost:** $12,500

| Deliverable       | Specification |
|-------------------|---------------|
| 0a–0d             | As above |
| 1. Smart Contracts | Full implementation of escrow & milestone logic |
| 2. Role Enforcement| Function access control |
| 3. Milestone Tracking | State machine for milestone management |

---

### Milestone 3 — Dispute Module

- **Duration:** 1 month  
- **FTE:** 1.5  
- **Cost:** $12,500

| Deliverable         | Specification |
|---------------------|---------------|
| 0a–0d               | As above |
| 1. Dispute Logic    | Per-milestone dispute handling |
| 2. Mediator Integration | Support third-party mediation |
| 3. Arbitration Outcomes | Enforce mediator decisions in contract |

---

### Milestone 4 — Frontend

- **Duration:** 1 month  
- **FTE:** 1.5  
- **Cost:** $12,500

| Deliverable   | Specification |
|---------------|---------------|
| 0a–0e         | Includes article |
| 1. Demo UI    | Frontend for contract interaction |
| 2. UX Flows   | Onboarding, milestone, and dispute flows |
| 3. Documentation | User + dev guides |
| 4. Tests & Walkthrough | E2E test instructions and UI/contract suite |

---

## Future Plans

- Deploy on public testnet with verified contract hashes  
- Partner with bounty boards and freelance platforms  
- Add governance layer for mediator whitelisting  
- Integrate zk-based identity/privacy for disputes  
- Offer white-label VaultOne modules for DAOs & multisigs

---

## Additional Information

**How did you hear about the Bounty Program?**  
Dorahacks

**Additional Notes:**  
We believe VaultOne can become a key component for trust-minimized collaboration in the Web3 economy.
