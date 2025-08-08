# ink!Spector Gadget: A Gamified ink! Smart Contract Security Platform

- **Team Name:** InkCTF
- **Payment Address:** 5HnRKEhkPneEV9rRHt3vdLMevvingqMX34XXm9hnqefaN62v

## Project Overview :page_facing_up:

### Overview

- **Tag Line:** Hack your way through vulnerable ink! smart contracts and become an ink! security expert!
- **Brief Description:** ink!Spector Gadget is an Ethernaut-inspired, interactive Capture-The-Flag (CTF) style web game designed to teach developers about common vulnerabilities in ink smart contracts. Players will solve progressively challenging levels by identifying and exploiting weaknesses in real ink! contracts deployed on a testnet. The platform will feature a user-friendly interface, real-time contract interaction, persistent progress tracking, guided walkthroughs, and an achievement system to enhance the learning experience(as mentioned in [RFP](https://github.com/use-inkubator/Ecosystem-Grants/blob/master/request-for-proposals.md)).

Apart from the RFP requirements, I am thinking of interaction with the contract through a frontend, similar to how https://speedrunethereum.com/ does it, our goal is to educate users on how ink smart contracts work by enabling them to interact with the frontend of our game, and alongside that, exploit common vulnerabilities in real ink! contracts deployed on a testnet.

For example, a level might feature an ink contract with a vulnerable withdraw function that allows `reentrancy`. Through the game’s frontend, the player can interact with this contract by calling its public methods—initially depositing some balance, then triggering a crafted exploit sequence using a UI button (e.g., "Call Attack Contract") that simulates how an attacker would recursively call withdraw before the state is properly updated. The frontend would show the live contract state, event logs, and balance changes in real-time, helping the player see the vulnerability being exploited. This hands-on interaction reinforces the learning experience and bridges the gap between theoretical vulnerabilities and how they play out in actual ink! smart contracts.


- **Relation to ink! Ecosystem:** This project directly contributes to the ink! ecosystem by providing a crucial educational tool for developers. By learning to identify and mitigate vulnerabilities, developers can write more secure ink! smart contracts, strengthening the overall security and reliability of applications built on Polkadot and Substrate-based chains using ink!.
- **Chosen Project Idea Category:** Canary Dapp / Technical Showcase.
    -   **Canary Dapp:** It will be a fully functional application deployed for public use, serving as a reference for building interactive dApps with ink! and demonstrating best practices for frontend-backend-blockchain communication.
    -   **Technical Showcase:** It will showcase the capabilities of ink! for creating complex applications and highlight common security pitfalls, thereby promoting secure ink! development.
- **Team's Interest:** Our team is passionate about smart contract security and the potential of the Polkadot ecosystem. We believe that hands-on, gamified learning is the most effective way to educate developers.

### Ink! Ecosystem Impact

ink!Spector Gadget will significantly benefit the ink! ecosystem by:

1.  **Educating Developers:** Providing a practical, engaging platform for developers to learn about ink!-specific vulnerabilities and general smart contract security patterns. This will lead to a higher standard of security in ink! projects.
2.  **Improving Code Quality:** By understanding how contracts can be exploited, developers will write more robust and secure code from the outset t.
3.  **Community Building:** Fostering a community around ink! security, where users can discuss challenges, share solutions (after completion), and contribute to new levels.
4.  **Onboarding New Developers:** Serving as an attractive entry point for developers new to ink! or smart contract development, offering a fun way to learn core concepts.
5.  **Showcasing ink! Capabilities:** Demonstrating how ink! can be used to build interactive and complex applications, including those requiring on-chain logic and state.
6.  **Reference Implementation:** The platform's codebase (especially the contract interaction parts) can serve as a reference for other developers building dApps with ink!.
7.  **Attracting Security Researchers:** Potentially attracting security researchers to the ink! ecosystem by providing a playground for exploring ink! contract security.

The platform is designed for any developer working with or interested in ink!, from beginners learning the basics to experienced developers looking to deepen their security knowledge.

### Project Details

#### Data Models / API Specifications:

Architecture(https://raw.githubusercontent.com/InkCTF/InkCTF/main/public/architecture.png)

#### Technology Stack:

*   **Frontend:** Next.js, TypeScript, Tailwind CSS (Current PoC stack)
*   **Backend:**  Rust with Actix (primarily thinking of writing it in rust we can also do in nextjs/expressjs )
*   **Database:** PostgreSQL hosted on AWS (for relational data integrity)
*   **Blockchain Interaction:** Polkadot.js API for interacting with ink! contracts.
*   **Smart Contracts:** ink!
*   **Deployment & Hosting:** Docker, Vercel/Netlify (Frontend), AWS/GCP/Heroku (Backend & DB), Polkadot Testnet

#### Documentation of Core Components:

*   **Game Engine (Backend):**
    *   Manages user sessions and authentication.
    *   Handles requests for new level instances:
        *   Deploys a unique instance of the level's ink! contract to the testnet for the user.
        *   Stores the instance address associated with the user and level.
    *   Verifies level completion:
        *   Queries the state of the user's contract instance on-chain.
        *   Compares it against the level's defined solution criteria.
        *   Updates `UserProgress`.
    *   Manages achievements based on user progress and specific criteria.
*   **Contract Interaction Service (Backend/Frontend):**
    *   A service (directly on frontend via user's wallet) responsible for deploying contracts.
    *   Frontend components will use Polkadot.js and Metamask to allow users to interact with their specific contract instances (send transactions, call messages).
*   **Level Content Service (Backend):**
    *   Serves level data (description, contract source, ABI, hints, walkthroughs) via API.
*   **User Interface (Frontend):**
    *   **Level Selection Dashboard:** Displays available levels and user progress.
    *   **Level View:**
        *   Displays level information (description, objectives).
        *   Shows contract source code (Monaco Editor).
        *   Provides an interface for contract interaction (function calls, value inputs).
        *   Displays console output from interactions.
        *   Hints and Walkthrough sections.
    *   **Multi Wallet Support:** Integration with both Polkadot.js extension and MetaMask
    *   **Responsive Design:** Desktop-optimized with tablet responsiveness.
    *   **User Profile/Achievements Page.**

#### Minimum Uptime Commitment:

- Commit to maintaining the application for a minimum of 18 months post-delivery
- Including bug fixes, security updates, and basic maintenance
- Hosting costs and maintenance will be covered by the grant

#### Domain & Infrastructure:

- Host on ctf.ink domain (pending acquisition via Namecheap)
- Deploy on Paseo testnet for optimal stability and ecosystem alignment
- Desktop-first design with responsive tablet support (mobile limited by wallet connectivity)

#### PoC/MVP:

The current PoC (Proof of Concept) located at `https://github.com/Gmin2/ink-ctf-game` demonstrates:
*   Frontend structure using Next.js and Tailwind CSS.
*   UI for level selection and individual level interaction.
*   Client-side simulation of contract interaction and state changes.
*   Basic hint and walkthrough system (client-side).
*   Achievement system (client-side, localStorage).
*   All 6 level contracts (ink! source code) and their solutions are defined.

This grant aims to elevate the PoC to a fully functional, on-chain, server-backed platform.

#### What your project is *not* or will *not* provide or implement:

*   **Its own token or complex tokenomics.** The focus is purely educational.
*   **Mainnet deployment of the game platform itself.** The game will interact with testnets.
*   **A full-fledged ink! IDE.** The contract interaction interface will be tailored for gameplay, not general development.
*   **Automated generation of new CTF challenges.** Levels will be manually designed and curated with the help of ink community.
*   **Financial incentives for playing.** Rewards will be in the form of achievements and learning, I am thinking of giving faucets tokens and badges to users completing the challenges so that they can get some visibility on the community.
*   **Audits of user-submitted exploit code.**
*   **Hosting costs, ongoing maintenance, or marketing post-grant delivery within this proposal's budget.** (Long-term sustainability is a separate consideration, see Future Plans).

#### CATEGORY:

Canary Dapp / Technical Showcase (with a strong educational focus)

#### Business Model (If Applicable):

Not directly applicable for this grant's scope, as the primary goal is educational and open-source.In future we might explore:
*   Treasury funding for ongoing maintenance and new level development.
*   Sponsorships from ecosystem projects.
*   Offering it as a free educational resource to attract developers to ink! and Polkadot.

#### Future Production Plans and Growth Strategy:

*   **Community-Driven Content:** Allow community members to submit new level ideas or full challenges.
*   **Integration with Polkadot Developer Hubs:** Feature the platform on official Polkadot/ink! developer resources.
*   **Workshops & Tutorials:** Create supplementary materials (videos, articles) around the game.
*   **Partnerships:** Collaborate with educational institutions or bootcamps.
*   **Localization:** Translate the platform into multiple languages.
*   **Regular Updates:** Add new levels and features based on community feedback and evolving ink! security landscape.

To ensure a higher profile/visibility of the project in the Polkadot community, I am thinking of creating a detailed blog series on each level covering exploit examples from past, in future we could bring that into the ink system so that blog series serves as reference to each level to the ink ctf and also I am thinking of creating a video tutorial series for each level, we could make the video series published on ink youtube channel.

And also with ink v6 we will extend the contract to support bot for metamask and polkadot.js wallets, so that the projects see wider audience without setting up a polkadot.js wallets.

## Community Engagement & Promotion Strategy

### Promotion Strategy:

- Regular updates on Polkadot Forum throughout development and post-launch
- Detailed blog series covering each level's security concepts and real-world exploit examples.
- Integration of blog content as reference material within the CTF platform
- Community feedback collection and iteration on level content
Participation in ink! developer events and workshops
- We could also create a discord server for the project and invite ink! developers to join so that the developers that will be using the platform can get help from the community.

### Content Development:

- Gather feedback from ink! developers on initial level content and difficulty
- Create educational blog posts for each vulnerability type covered in the game
- I see the ink youtube channel is dead for a year now, if granted permission i could create a video walkthrough series covering each level

## Team :busts_in_silhouette:


### Team members

- Gmin2(https://github.com/Gmin2)
- ItsMoh(https://github.com/ItshMoh)

### Contact

- **Contact Name:** Mintu Gogoi
- **Contact Email:** mintugogoi567@gmail.com

- **Contact Name:** Mohan Kumar
- **Contact Email:** whitelovemohan@gmail.com

### Legal Structure

- **Registered Address:** Guwahati, Assam, India, Pin: 781006

### Team's experience

I have worked with rust lang team for implementing the autocomplete features in cargo and also I have worked with near team for implementing off chain message support in near-cli

### Team Code Repos

- `https://github.com/InkCTF/InkCTF` (Current PoC for this project)
- https://github.com/Gmin2

GitHub accounts of team members:
- `https://github.com/Gmin2`

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/mintu-gogoi/

## Development Status :open_book:

The project has an existing Proof of Concept (PoC) available at `https://inkctf.netlify.app/` and the codebase of the poc in `https://github.com/InkCTF/InkCTF`. This PoC includes:

Homepage:

[HomePage](https://raw.githubusercontent.com/InkCTF/InkCTF/main/public/home.png)

Challenges:

[Challenges](https://raw.githubusercontent.com/InkCTF/InkCTF/main/public/challenge-levels.png)

Challenge details:

[challenges-description](https://raw.githubusercontent.com/InkCTF/InkCTF/main/public/level-desc.png)

Contract interaction:

[Smart contract interaction](https://raw.githubusercontent.com/InkCTF/InkCTF/main/public/contract-interaction.png)

This grant proposal focuses on transitioning this PoC from a client-side simulation to a fully on-chain interactive platform with a robust backend.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 4 months
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 35,000 USD

### Milestone 1 — Backend Foundation & Basic On-Chain Interaction

- **Estimated duration:** 1.5 months
- **FTE:** 2
- **Costs:** 15,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | Inline documentation for all backend code. API documentation (e.g., Swagger/OpenAPI) for all new endpoints. Basic tutorial on setting up the backend and interacting with the initial API. |
| **0c.** | Testing and Testing Guide | Unit tests for critical backend logic (user auth, API handlers, basic contract deployment). Integration tests for API endpoints. Guide on running tests. |
| **0d.** | Docker | Dockerfile for backend service and database. Docker-compose setup for local development environment. |
| 1. | Backend Setup | Initialize backend project (Node.js/Express or Rust/Actix). Setup PostgreSQL database schema for Users, Levels, UserProgress. |
| 2. | User Authentication | Implement wallet-based authentication (e.g., sign a message with Polkadot.js). API endpoints for user registration/login. Session management. |
| 3. | Level Content API | API endpoints to serve level data (description, contract source, hints, etc.) from the database. Initial level data seeding. |
| 4. | Basic Contract Deployment Service | Backend service to deploy a unique instance of an ink! contract for a user for Level 1 ("Hello Squink!"). Store instance address in `UserProgress`. |
| 5. | Frontend Integration (Level 1) | Modify frontend to fetch Level 1 data from API. Integrate Polkadot.js for users to interact with their deployed Level 1 contract instance. Submit completion to backend for verification (basic verification logic for Level 1). |
| 6. | User Progress (Basic) | Backend logic to track Level 1 completion status in `UserProgress` table. API endpoint for user to fetch their progress. |
| 7. | Community Feedback Collection | Gather feedback from ink! developers on initial level content and difficulty. Create survey/feedback mechanism for iterating on level design. |

### Milestone 2 — Full Contract Lifecycle & Advanced Features Foundation

- **Estimated duration:** 1.5 months
- **FTE:** 2
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | Update API documentation. Inline documentation for new backend modules. Tutorial on how to add and manage levels |
| **0c.** | Testing and Testing Guide | Unit and integration tests for new features (all 6 level contract interactions, achievement logic). |
| **0d.** | Docker | Updated Dockerfiles and docker-compose setup. |
| 1. | Full Contract Deployment (Levels 2-6) | Extend contract deployment service to support deploying and managing instances for all 6 defined levels. |
| 2. | On-Chain Verification Logic | Implement robust backend logic to verify completion for all 6 levels by querying the state of the user's contract instances on the testnet. |
| 3. | Frontend Integration (Levels 2-6) | Integrate frontend for all 6 levels to interact with their respective on-chain instances and submit for verification. |
| 4. | Walkthrough System (Backend & Frontend) | API to serve walkthrough steps. Frontend UI to display step-by-step walkthroughs for each level. |
| 5. | Achievement System (Backend & Frontend) | Define achievement criteria in the backend. Logic to check and award achievements based on `UserProgress` and other conditions (e.g., completing a level without hints, speed). API for achievements. Frontend UI to display user's achievements and notifications for new unlocks. |
| 6. | Multi-Wallet Integration | Implement support for both Polkadot.js and MetaMask wallets using ink! v6 Solidity ABI compatibility (#[ink::contract(abi = "all")]). |
| 7. | Public Statistics Dashboard | Create publicly accessible dashboard showing user progress statistics, completion rates, and community metrics (replacing admin panel functionality). |

### Milestone 3 — Polish, Testing, Deployment & Documentation

- **Estimated duration:** 1 month
- **FTE:** 2
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | Comprehensive user guide for players. Developer documentation for anyone wanting to understand the architecture or contribute. Final API documentation. |
| **0c.** | Testing and Testing Guide | End-to-end tests for key user flows. Increased test coverage across frontend and backend. Final testing guide. |
| **0d.** | Docker | Production-ready Docker images for all services. |
| **0e.** | Article | Publish an article on a suitable platform (e.g., Medium, Polkadot Forum, dev.to) detailing the project, its architecture, how it benefits the ink! ecosystem, and how to play. |
| 1. | UI/UX Refinement | Polish all frontend components based on feedback and ensure adherence to ink! branding guidelines. Ensure responsive design across devices. |
| 2. | Performance Optimization | Optimize backend API response times and database queries. Optimize frontend load times. |
| 3. | Security Hardening | Review backend for common web vulnerabilities (OWASP Top 10). Implement rate limiting, input validation, etc. |
| 4. | Testnet Deployment | Deploy the full application (frontend, backend, database) to a chosen cloud provider, interacting with a public Polkadot testnet. |
| 5. | Comprehensive Testing | Conduct thorough internal testing of all features on the deployed testnet environment. Address any bugs found. |
| 6. | Project Handover | Provide access to all code repositories, deployment scripts, and documentation. |
| 7. | Blog Series Launch | Publish first 3 articles of the educational blog series covering security concepts from the first levels. |

## Future Plans

Upon successful completion and delivery of this grant, we envision the following future for ink!Spector Gadget:

1.  **Long-term Maintenance & Hosting:** We plan to apply for follow-up treasury funding or seek further grants to cover ongoing hosting costs, regular maintenance, updates for new ink! versions, and security patches.
2.  **Community Moderation & Level Curation:** Establish a system for community members to propose new levels, report issues, and potentially moderate content. This could involve a GitHub-based workflow for level submissions.
3.  **Expanding Level Library:** Continuously develop and add new levels covering a wider range of vulnerabilities and ink! features.
4.  **Educational Partnerships:** Collaborate with ink! bootcamps, workshops, and educational platforms to integrate ink!Spector Gadget as a learning tool.
5.  **Leaderboard & Competitive Features:** Introduce leaderboards (e.g., based on completion time, number of levels solved) and potentially time-boxed CTF events to foster friendly competition.
6.  **Advanced Analytics:** Implement more detailed analytics to understand how users progress, where they get stuck, and use this data to improve levels and create targeted educational content.
7.  **Content Evolution:** Continuously gather community feedback to refine existing levels and develop new ones based on emerging ink! security patterns
8. **Educational Content:** Complete the blog series covering all levels and expand into video tutorials

Our goal is for ink!Spector Gadget to become the go-to platform for hands-on ink! smart contract security education, continuously evolving with the ink! ecosystem.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** 

X(twitter)

I have make an poc of this product and it is availaible at https://inkctf.netlify.app/, although I need to revamp some part of the website like the editor and the contract interaction part we want to make it more engaging