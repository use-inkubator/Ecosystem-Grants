# OverTheInk: Interactive ink! Security Challenge Platform

- **Team Name:** OverTheInk
- **Payment Address:** <To be provided after team legal setup>

> :exclamation: *The combination of your GitHub account submitting the application and the payment address above will be your unique identifier during the program. Please keep them safe.*

## Project Overview :page_facing_up:
### Overview

- **Tag Line:** "Ethernaut for ink! - Learn ink! smart contract security through hands-on challenges"
- **Project Description:** OverTheInk is an interactive educational platform featuring security challenges for ink! smart contracts on Aleph Zero and Polkadot. Inspired by the popular Ethernaut CTF on Ethereum, it provides developers with hands-on experience in identifying and exploiting common smart contract vulnerabilities in the ink! ecosystem, while learning best practices for secure contract development.
- **Ink! Ecosystem Relation:** OverTheInk directly contributes to the security maturity of the ink! ecosystem by training developers on Wasm smart contract vulnerabilities specific to Aleph Zero and Polkadot. It promotes ink! adoption by providing an engaging learning platform that showcases contract capabilities and security best practices.
- **Project Category:** Technical Showcase - We chose this category because OverTheInk demonstrates advanced ink! contract interactions, cross-contract calls, and decentralized application patterns while educating developers on security vulnerabilities. This serves as both a learning tool and a showcase of ink! contract capabilities.
- **Team Motivation:** As a developer passionate about blockchain security and WebAssembly smart contracts, I'm creating OverTheInk to fill a critical educational gap in the ink! ecosystem. With the growing adoption of Aleph Zero, there's an urgent need for security-focused educational resources tailored to ink! contracts rather than EVM contracts.

### Ink! Ecosystem Impact

As a Technical Showcase project, OverTheInk promotes ink! adoption through several key mechanisms:

**Security Education & Developer Training:**
- Trains 100+ developers in ink! contract security best practices through interactive challenges
- Covers critical vulnerabilities unique to Wasm/ink! contracts (cross-contract calls, storage exhaustion, XCM DoS)
- Creates reusable vulnerable contract patterns that developers can learn from and auditors can reference
- Reduces security incidents by establishing standardized learning resources for the ecosystem

**Technical Demonstration:**
- Showcases advanced ink! patterns like multi-contract interactions, cross-contract calls, and complex state management
- Demonstrates ink! capabilities for educational platforms and gamification using blockchain
- Promotes ink! ecosystem by providing engaging content that attracts new developers
- Serves as a reference implementation for CTF-style platforms on Polkadot/Aleph Zero

**Ecosystem Security Maturity:**
- Addresses the lack of security educational resources for ink! contracts
- Builds community knowledge through shared solutions and discussion of vulnerability patterns
- Establishes ink! as a mature platform capable of supporting educational and gamified applications
- Indirectly benefits all ink! projects by creating a pool of security-aware developers

**Business Model for Sustainability:**
- Target market: Blockchain developers, smart contract auditors, and students interested in Polkadot/Aleph Zero
- Revenue channels: Challenge completion certificates, premium advanced challenges, corporate training licensing
- Expected adoption: 500+ users in first year through organic growth and targeted outreach to Polkadot community
- Long-term value: Become the go-to educational platform for ink! security, fostering ecosystem growth

**Measuring Impact:**
- Track number of developers completing challenges
- Monitor forum discussions and shared solutions
- Measure reduction in reported ink! vulnerabilities through improved developer practices
- Community feedback and expansion into custom challenge creation for enterprises

Since this is an educational tool with real-world utility, our success will be measured by how effectively it reduces security vulnerabilities and increases the number of competent ink! developers.

### Project Details

- **Data Models:** Challenge structure (contract address, vulnerability type, difficulty level, required exploit steps), User progress (completed challenges, points earned, submission history), Transaction records (exploit attempts, contract interactions)

- **API Specifications:** REST API for challenge retrieval and user management, WebSocket endpoints for real-time contract state monitoring, GraphQL interface for complex progress analytics and leaderboard queries

- **Technology Stack:** Frontend: React.js with useInkathon library, TypeScript, Material-UI. Contracts: ink! smart contracts with PSP34/37 standards where applicable. Infrastructure: Node.js backend, PostgreSQL database, IPFS for challenge metadata, Docker containers for deployment

- **Core Components:** Challenge Factory Contract (deploys vulnerable contracts per user), Frontend React dApp (challenge interface, wallet connection, progress tracking), Validation Engine (verifies successful exploits), Multi-tenant testing environment (isolated contract deployments)

- **Architecture:** Modular monorepo structure (separate frontend, contracts, backend), Cross-contract interaction testing, Progressive Web App for accessibility, Multi-testnet support (Aleph Zero testnet, Polkadot Canary), Automated contract deployment and cleanup

- **Prior Work:** MVP includes 6 implemented challenges (Hello ink!, Integer overflow, Signed-integer, Address validation, Replay attacks, Insecure randomness), Basic frontend with polkadot.js integration, Wireframe completed, GitHub repos established (frontend: inkwell-challenges, contracts: OverTheInk-contracts)

- **Project Limitations:** No native token or reward system, no direct user-to-user interactions beyond leaderboards, initial focus on Aleph Zero testnet only (expandable to other Polkadot parachains), no mobile native app in initial release, no integration with external oracle services

- **CATEGORY:** Technical Showcase

- **Business Model:** Hybrid educational platform model combining free community resources with premium features. Revenue streams: Premium challenge subscriptions ($10/month), Corporate training license fees ($500/year per company), Completion certificates ($25 each), Sponsored challenge bounties. Target market: 500+ active users in first year (blockchain developers, auditors, students)

- **Growth Strategy:** Phased expansion from MVP to full platform (6 months initial, then continuous improvement). Measure success through user engagement metrics, vulnerability reduction reports from secured ink! contracts, community feedback surveys. Achieve sustainability through premium features and enterprise partnerships


Things that shouldn’t be part of the application:
- The (future) tokenomics of your project 
- For non-infrastructure projects—deployment and hosting costs, maintenance or audits
- Business-oriented activities (marketing, business planning), events or outreach


## Team :busts_in_silhouette:

### Team members

- Name of team leader: Hritwik Tripathi

### Contact

- **Contact Name:** Hritwik Tripathi
- **Contact Email:** info@innoviksha.xyz
- **Website:** https://innoviksha.xyz/

### Legal Structure

- **Registered Address:** <Individual contributor - legal setup TBD>
- **Registered Legal Entity:** Individual Developer (Legal entity setup planned)

### Team's experience

The project founder is a solo developer with extensive experience in smart contract security and WebAssembly ecosystems:

- **ink! Smart Contract Development:** 2+ years experience building and auditing ink! contracts for Aleph Zero testnet
- **Security Research:** Comprehensive knowledge of smart contract vulnerabilities, demonstrated by implementing 6 unique security challenges covering critical issues like integer overflows, replay attacks, and insecure randomness
- **Web3 Frontend Development:** Proficient in React.js, TypeScript, and integration with polkadot.js libraries
- **Aleph Zero Ecosystem:** Active contributor to Aleph Zero community through development and security research
- **Prior Projects:** OverTheInk frontend (https://github.com/3scava1i3r/inkwell-challenges) and contracts (https://github.com/3scava1i3r/OverTheInk-contracts) repositories showing practical experience with the full stack

Past contributions include building ink! tutorial contracts, participating in Aleph Zero hackathons, and research into Wasm-specific security patterns.

### Team Code Repos

- https://github.com/3scava1i3r/inkwell-challenges (Frontend - React dApp without useInkathon integration)
- https://github.com/3scava1i3r/OverTheInk-contracts (ink! smart contracts implementing security challenges)

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/3scava1i3r

### Team LinkedIn Profiles (if available)

- <To be added>


## Development Status :open_book:

- **Technical Development**
  - MVP prototype built with 6 security challenges implemented
  - Frontend dApp created with React and polkadot.js integration
  - Wireframe and basic UI completed
  - Repository structure established for monorepo architecture

- **Links to Current Work:**
  - GitHub Frontend: https://github.com/3scava1i3r/inkwell-challenges
  - GitHub Contracts: https://github.com/3scava1i3r/OverTheInk-contracts
  - <To be added: Blog posts on ink! security research>

- **Community Engagement:**
  - Active discussions with Aleph Zero developer community
  - Security vulnerability research conducted and documented
  - Initial user feedback collected for platform design

## Development Roadmap :nut_and_bolt:

> :exclamation: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Overview

- **Total Estimated Duration:** 6 months
- **Full-Time Equivalent (FTE):** 1.5 FTE (solo developer)
- **Total Costs:** 15,000 USD

### Milestone 1: Monorepo Setup and Frontend Integration

- **Estimated duration:** 2 months
- **FTE:** 1.5
- **Costs:** 5,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | Complete documentation for setting up development environment, running the platform, and contributing to challenges |
| **0c.** | Testing and Testing Guide | Unit tests for all ink! contracts and frontend components, end-to-end testing for challenge workflows |
| **0d.** | Docker | Docker configuration for full-stack deployment and local development |
| 1. | Monorepo Architecture | Unified repository structure combining frontend, contracts, and backend into single monorepo |
| 2. | useInkathon Integration | Complete integration of useInkathon library for enhanced ink! contract interactions |
| 3. | Challenge Factory Contract | Deployable ink! contract factory for generating challenge instances per user |
| 4. | Frontend Platform | Fully functional dApp with wallet connection, challenge selection, progress tracking |

### Milestone 2: Complete Remaining Challenges

- **Estimated duration:** 2 months
- **FTE:** 1.5
- **Costs:** 5,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | Comprehensive challenge documentation including solution explanations and vulnerability details |
| **0c.** | Testing and Testing Guide | Full test coverage for all challenges, including exploit attempts and validation logic |
| **0d.** | Docker | Updated Docker configuration for all challenge types |
| 1. | Advanced Challenges | Implementation of remaining vulnerabilities: Role-based access control, Storage exhaustion, XCM DoS, Verbosity Issues, Dependency confusion, XCM arbitrary execution, Unsafe conversion, Reentrancy, Insufficient benchmarking, Access control bypass |
| 2. | Problem Description System | Rich markdown descriptions with hints, difficulty indicators, and learning objectives for each challenge |
| 3. | Solution Validation Engine | Automated system to verify successful exploits and track user progress |
| 4. | Leaderboard Integration | Global and per-challenge benchmarking with user engagement metrics |

### Milestone 3: Multi-testnet and Localization

- **Estimated duration:** 1 month
- **FTE:** 1.5
- **Costs:** 2,500 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | Multi-chain deployment guide and chain-specific configuration documentation |
| **0c.** | Testing and Testing Guide | Cross-chain integration tests and localization testing |
| **0d.** | Docker | Multi-environment Docker configuration for different testnets |
| 1. | Multi-testnet Support | Deployment support for Aleph Zero testnet, Polkadot Canary network, and other ink!-compatible chains |
| 2. | Localization Framework | Multi-language support for English, additional languages based on community demand |
| 3. | Network Configuration System | Automatic detection and switching between supported testnets |
| 4. | User Experience Optimization | Responsive design improvements and progressive web app features |

### Milestone 4: Production Deployment

- **Estimated duration:** 1 month
- **FTE:** 1.5
- **Costs:** 2,500 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | Production deployment guide, user manual, and platform maintenance documentation |
| **0c.** | Testing and Testing Guide | Production-ready test suites and performance benchmarking |
| **0d.** | Docker | Production-grade Docker configuration with monitoring and logging |
| 0e. | Article | Technical article and tutorial on "Building Education Platforms with ink! Smart Contracts" |
| 1. | Custom Domain Deployment | Platform deployment to custom domain with SSL certificates |
| 2. | Analytics Integration | User behavior analytics and challenge completion metrics |
| 3. | Community Features | Basic forum for solution discussions and feature suggestions |
| 4. | Operational Monitoring | Error tracking, performance monitoring, and automated alerts |


## Future Plans

After completing the initial OverTheInk platform, we plan to expand the project in several key directions:

**Short-term (Post-Grant - 6 months):**
- Community-driven challenge creation platform allowing security researchers to contribute custom challenges
- Expanded multi-chain support beyond Aleph Zero and Polkadot Canterbury to include other ink!-compatible parachains
- Mobile application development for improved accessibility across devices
- Social features including solution discussions, mentorship matching, and developer communities

**Medium-term (1 year):**
- Enterprise-grade training modules and certification programs for corporate clients
- Integration with automated security analysis tools and audit frameworks
- Expansion to other Wasm-based blockchain platforms beyond the Polkadot ecosystem
- Academic partnerships for structured curriculum development and university courses

**Long-term (2+ years):**
- Global education hub becoming the primary learning resource for WebAssembly smart contract security
- Industry-recognized certification programs for different skill levels (beginner to expert)
- Integration with DeFi protocols and decentralized security platforms
- Support for additional languages and cultural localization for worldwide adoption

These expansion plans are designed to create multiple sustainable revenue streams while continuing to drive major positive impact on the ink! ecosystem through comprehensive developer education, security awareness, and community building.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** <To be provided before submission - Community announcement/Referral>

- **Original Work:** OverTheInk represents original development work inspired by successful educational platforms like Ethernaut, but custom-built specifically for the ink! ecosystem
- **No External Funding:** No other teams have contributed financially to the project to date
- **Open Source Commitment:** All development work will be open-source with Apache 2.0 license, following ink! community best practices
- **Community Focus:** Platform designed as a collaborative educational resource for the entire Polkadot/Aleph Zero developer ecosystem
