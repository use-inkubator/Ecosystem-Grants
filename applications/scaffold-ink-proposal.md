# Scaffold-ink!

- **Team Name:** HIE Agency
- **Payment Address:** NA

## Project Overview :page_facing_up:

### Overview

Scaffold-ink! is a fully forkable, end-to-end developer toolkit built to simplify and accelerate ink! smart contract creation and frontend integration within the Polkadot ecosystem. Modeled after Ethereum’s Scaffold-ETH, it provides:

A Next.js + React + TypeScript starter template preconfigured with Polkadot-JS and useInkathon hooks for seamless contract interaction.

An intelligent hot-reload engine that automatically rebuilds and redeploys ink! contracts on every change, instantly updating the frontend.

Custom React hooks (useInkathon and typink) offering type-safe contract calls, real-time event subscriptions, and on-chain state queries.

A library of pre-styled UI components (e.g., wallet connectors, transaction monitors, event lists) leveraging Tailwind CSS for rapid interface development.

A turnkey local development environment: a launcher script for substrate-contracts-node (a local ink!-compatible chain), bundled with a burner wallet and faucet for quick testing.

Out-of-the-box support for major Polkadot wallets, including the Polkadot.js browser extension, SubWallet, and Talisman.

First-party SubQuery and Subsquid templates to index ink! contract events and auto-generate GraphQL/REST APIs with matching TypeScript types.

By delivering a cohesive, production-ready infrastructure, Scaffold-ink! fills the critical gap in Polkadot’s ink! ecosystem, lowering boilerplate by up to 80% and removing onboarding friction for new and experienced builders alike.

**Category:** Infrastructure  
**Importance:** Accelerates Polkadot project development through ergonomic tooling comparable to leading Ethereum solutions  
**Objective:** Empower developers with a one-stop ink! toolkit, closing the usability gap and driving ecosystem growth

### Ink! Ecosystem Impact

The Polkadot ecosystem currently lacks a unified, developer-friendly toolkit for ink! smart contracts analogous to Ethereum’s Scaffold-ETH. Scaffold-ink! addresses this critical gap by providing a cohesive infrastructure that reduces repetitive boilerplate by approximately 80%, dramatically shortening the time from project inception to functional prototype. By bundling starter templates, type-safe React hooks (useInkathon and typink), a curated component library, and an automated local development environment, Scaffold-ink! empowers builders to focus on innovation rather than configuration. Native integration with popular Polkadot wallets and first-party SubQuery and Subsquid indexing templates further streamlines end-to-end development workflows, ensuring that dApp teams can launch, test, and iterate rapidly within the Polkadot ecosystem.

### Project Details

**Technology Stack:** Next.js + React + TypeScript, Polkadot-JS API, useInkathon hooks, typink type generator, Tailwind CSS, substrate-contracts-node.

**Component Library:** Ready-to-use UI components such as AccountBalance, ContractCaller, EventList, TransactionManager, and more—fully styled with Tailwind CSS and optimized for ink! interactions.

**Local Development Environment:** A launcher script automates setup of a local ink!-compatible chain, burner wallet, and faucet for seamless testing. Docker support ensures reproducible environments.

**Wallet Integration:** Out-of-the-box support for Polkadot.js browser extension, SubWallet, and Talisman, with automatic network detection and multi-account management.

**Data Indexing:** First-party SubQuery and Subsquid project templates enable one-click setup for indexing ink! contract events, generating GraphQL and REST APIs alongside TypeScript types for safe, efficient data queries.

**Out of Scope:** Scaffold-ink! focuses strictly on developer tooling and does not cover tokenomics design, marketing activities, or production deployment costs for end applications.

**Category:** Infrastructure

**Business Model:** Fully open-source and grant-funded, with potential for community-developed extensions and optional paid support services in the future.

**Future Production Plans:** Refer to the “Future Plans” section for modular plugin architecture, enterprise features, and ecosystem expansion strategies.

## Team :busts_in_silhouette:

### Team members

- Name of team leader: Hritwik Tripathi
- Names of team members: Hritwik Tripathi

### Contact

- **Contact Name:** Hritwik Tripathi
- **Contact Email:** info@hie.agency
- **Website:** hie.agency

### Legal Structure

- **Registered Address:** NA
- **Registered Legal Entity:** NA

### Team's experience

- contribution in web3uikit
- 8+ web3 hackathon winner web3 majorly
- Top 16 Auditor (16/231)
- Ranked in the top 16 out of 231 participants for outstanding performance in identifying vulnerabilities and analyzing smart contract security during the Cork Protocol audit competition.
- Selected as top 0.5% candidates and awarded fellowship in Track 2.

### Team Code Repos

- NA

- https://github.com/<team_member_1>: https://github.com/3scava1i3r

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/hritwikt/

## Development Status :open_book:

- Ideation

## Development Roadmap :nut_and_bolt:

This section breaks the development roadmap into two milestones, with indexing handled exclusively via SubQuery.

### Overview

- **Total Estimated Duration:** 4 months
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** 42,000 USD

### Milestone 1 — Core Toolkit Foundation (0–2 months)

- **Estimated duration:** 2 months
- **FTE:** 1 FTE
- **Costs:** 21,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | Comprehensive setup guide, component API docs, and quick-start tutorial with code examples. |
| 0c. | Testing Guide | Unit tests for CLI, hooks, and components; integration test suite with substrate-contracts-node. |
| 0d. | Docker | Dockerfile for local dev environment with substrate-contracts-node, pre-funded accounts, and automated setup. |
| 1. | CLI & Project Generator | create-scaffold-ink CLI with customizable templates for basic dApp, DeFi, and NFT projects. |
| 2. | Hot Reload Engine | File watcher with cargo-contract compilation, automatic deployment, and real-time frontend synchronization. |
| 3. | Core UI Component Library | 8 essential React components: WalletConnector, ContractInteraction, AccountBalance, TransactionStatus, EventListener, NetworkSelector, ContractDeployer, ErrorBoundary. |
| 4. | SubQuery Indexing Templates | One-click SubQuery project template for ink! event indexing, automatic GraphQL API generation, and TypeScript types. |
| 5. | Local Development Environment | Automated substrate-contracts-node launcher with Docker support, pre-configured accounts, local faucet. |

### Milestone 2 — Enhancement & Polish (3–4 months)

- **Estimated Duration:** 2 months
- **FTE:** 1.0 FTE
- **Costs:** 21,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | Advanced tutorials, video walkthroughs, and comprehensive API reference with interactive examples. |
| 0c. | Testing Guide | End-to-end tests with DRink! framework, performance benchmarks, and CI/CD templates for GitHub Actions. |
| 0d. | Docker | Enhanced Docker setup with multi-network support and optimized builds. |
| 1. | Advanced Components | Additional UI elements for multi-signature operations, batch transactions, and governance interfaces. |
| 2. | Multi-Network Support | Configuration templates and switching capabilities for Rococo, Westend, and parachain testnets. |
| 3. | SubQuery Integration Enhancement | Advanced SubQuery templates with complex event filtering, aggregations, and real-time subscriptions for ink! contracts. |
| 4. | Example Applications | Three complete dApp examples: token contract, NFT marketplace, and simple DAO with full frontend integration and SubQuery indexing. |
| 5. | Community Integration | GitHub templates, contribution guidelines, plugin development docs, and early adopter feedback integration. |

## Future Plans

Phase 2 Development (Months 7-12): Extension marketplace for community-developed plugins, advanced debugging tools with contract execution tracing, and enterprise features including team collaboration and deployment pipelines. Enhanced SubQuery templates for complex multi-contract indexing scenarios.

Long-term Vision: Establish Scaffold-ink! as the de-facto development standard for ink! projects, foster a thriving ecosystem of community extensions, and maintain compatibility with evolving Polkadot infrastructure while serving as a catalyst for developer adoption and ecosystem growth. SubQuery will remain the primary indexing solution with deep integration and optimization.

## Additional Information :heavy_plus_sign:

How did you hear about the Grant Program? Through active participation in the Polkadot developer community, engagement in hackathons, and following Web3 Foundation announcements regarding ecosystem development initiatives.

Work you have already done: Prototype development of core CLI functionality, research and validation of useInkathon integration patterns, extensive analysis of developer pain points through community engagement and hackathon participation, and preliminary SubQuery template development for ink! contract event indexing.
