# Name of your Project

- **Team Name:** Tolga Yaycı
- **Payment Address:** 5EF96qzqDfHPT4kz8ebdiPUsp6S3GpXZz4GQL9FGHtBTK6Go


## Project Overview :page_facing_up:
### Overview

**Tagline:** A browser IDE for ink! smart contracts that lets developers write, compile, deploy, and call contracts without local setup.

**Project Description:** ink! Playground is a browser-based integrated development environment specifically designed for writing, compiling, and deploying ink! smart contracts on Substrate-based networks. The platform eliminates the need for local Rust toolchain setup, cargo-contract installation, or node environment configuration by providing a complete development environment accessible through any web browser.

**Relation to ink! Ecosystem:** The Playground operationalizes the ink! v6 toolchain in a browser, using cargo-contract to produce Wasm and metadata and submitting calls to a contracts pallet chain (initially a testnet). It complements the official docs and CLI by giving a zero‑install pathway to compile and deploy sample contracts, which the community has repeatedly requested since the previous browser IDE was archived and taken offline.

**Project Category:** Infrastructure. A maintained, open‑source, web IDE is developer infrastructure that shortens the time from “curious about ink!” to “on‑chain test deployment”, supports education and hackathons, and reduces support load across the ecosystem.

**Personal Interest:** Having previously built similar tool called `Wizard` (a web IDE for Arbitrum Stylus smart contracts: https://thewizard.app), I've witnessed firsthand how browser-based development environments dramatically improve accessibility for blockchain developers. I'm particularly interested in applying this experience to the ink! ecosystem, where setup complexity remains a significant barrier. My goal is to create a tool that meaningfully accelerates adoption of ink! by reducing friction in the development process.

### Ink! Ecosystem Impact

* **Lowering friction:** Today, new developers must install Rust + targets, `cargo-contract`, find a contracts‑enabled chain, secure test funds, and wire up a wallet just to see code run. A hosted, OSS Playground gives them an immediate path to “type → compile → deploy → call” in the browser. The community has asked for a live, up‑to‑date ink! Playground since the prior one went offline, and W3F has explicitly sought maintainers for a browser IDE through an RFP. ([Polkadot Forum](https://forum.polkadot.network/t/ink-playground/3052), [Web3 Foundation Grants](https://grants.web3.foundation/docs/RFPs/IDE_for_ink_Smart_Contracts#:~:text=with%20Substrate))

* **Who uses it and how:**
  * **Developers new to Polkadot/ink!:** try ink! in minutes, learn the deployment flow end‑to‑end.
  * **Educators/hackathons:** avoid hours of environment setup; share permalinked examples.
  * **Parachain teams with contracts pallet:** quick test/demonstration against a public testnet.

* **Why this matters now:** The previous `use-ink/ink-playground` project is archived and no longer maintained, and forum discussions still reference the gap this leaves for onboarding and code‑sharing. A maintained replacement aligned with ink! v6 removes a tangible blocker to exploration and education.

* **Hackathon Participants & Educators:** At Polkadot hackathons or in academic settings, an online IDE is invaluable for quick setups. Participants can start building on Pop (testnet) instantly, and instructors can use the Playground to demonstrate ink! concepts live, without spending time on environment configuration.

* **Testnet Connectivity:** Direct deployment to test networks like Pop (Paseo testnet) enables immediate contract testing on live networks, bridging code experimentation and real deployment.

* **Community Contributors and QA:** Community Contributors and QA – The Playground will also be useful for community members who want to review examples or answer questions. For instance, someone on the forum can share a permalink to an ink! snippet demonstrating an issue or solution, making knowledge exchange more effective.

* **Ecosystem Evaluation:** Web3 developers from other ecosystems can quickly evaluate ink! without local setup, potentially attracting talent from Ethereum, Solana, and other platforms.

### Project Details

#### Technology stack

* **Frontend:** Vite + React (TypeScript), Monaco editor (Rust/ink! syntax highlighting), polkadot‑js/api for RPC, minimal state via React Query/Zustand.
* **Backend:** **Rust** (Axum), `tokio` for job orchestration, `cargo-contract` invocations within Docker.
* **Infrastructure:** Supabase, Dockerized services, PostgreSQL, GitHub OAuth, public deployment on AWS EC2 behind Nginx with HTTPS.
* **Target network:** one contracts‑enabled testnet endpoint (Pop on Paseo, or another stable contracts pallet testnet), selectable in settings in next versions but defaulted for now.

#### Mockups

| | | |
| -----: | ----------- | ------------- |
| <img width="1482" height="744" alt="Screenshot 2025-09-05 at 17 50 00" src="https://github.com/user-attachments/assets/ba1db927-0de7-4d67-815c-7c4adfc958e1" /> | <img width="3000" height="1575" alt="Screenshot 2025-09-05 at 17 52 51" src="https://github.com/user-attachments/assets/4ea23eb6-aa0e-423a-bf32-b452529cf14e" /> | <img width="1295" height="1201" alt="Screenshot 2025-09-05 at 17 53 07" src="https://github.com/user-attachments/assets/398b09ab-2de6-41fc-82e3-0349b1f50cf4" /> |
| <img width="711" height="465" alt="Screenshot 2025-09-05 at 17 56 08" src="https://github.com/user-attachments/assets/778fe91b-ce74-49c0-b3ac-033236800d3e" /> | <img width="1282" height="818" alt="Screenshot 2025-09-05 at 17 56 49" src="https://github.com/user-attachments/assets/98a409a5-1293-4112-ab82-2364e9a97fbd" /> | <img width="608" height="470" alt="Screenshot 2025-09-05 at 17 57 07" src="https://github.com/user-attachments/assets/722ec55f-4467-4ab8-83e7-8eb9622e851e" /> |
| <img width="1285" height="815" alt="Screenshot 2025-09-05 at 17 57 19" src="https://github.com/user-attachments/assets/add17dcf-be33-463b-b394-1204c7646a1d" /> | <img width="892" height="611" alt="Screenshot 2025-09-05 at 17 57 43" src="https://github.com/user-attachments/assets/6dfb741a-32d5-463c-be21-f4f0c72b8c7f" /> | <img width="1451" height="1177" alt="Screenshot 2025-09-05 at 18 03 19" src="https://github.com/user-attachments/assets/3aacf80a-8a6e-4b0d-9cac-57bfff826d14" /> |
| <img width="1371" height="502" alt="Screenshot 2025-09-05 at 18 04 03" src="https://github.com/user-attachments/assets/17cd971e-a8ba-4a45-b629-bf75f96b76a6" /> | <img width="1401" height="1187" alt="Screenshot 2025-09-05 at 17 59 35" src="https://github.com/user-attachments/assets/af52b3e5-241e-44fb-ae0b-dc02c723c086" /> |


#### Deliverables

* Browser-based Monaco code editor with Rust/ink! syntax highlighting
* Secure, containerized compilation service using cargo-contract with support for ink! v6 and real-time compiler output 
* GitHub OAuth integration for user authentication with project saving, loading, and sharing via generated permalinks
* Advanced multi-project management allowing developers to organize multiple projects simultaneously
* In-browser wallet for testnet account management with direct deployment to Pop testnet and transaction status monitoring
* Automatically generated UI for contract deployment and interaction, supporting both read-only queries and state-changing transactions with parameter forms from contract metadata and result display
* Comprehensive library of ink! contract examples and templates (ERC/PSP standards, access control patterns) with one-click import functionality
* Fully hosted solution on AWS EC2 with HTTPS, documented Docker setup, and open-source codebase under Apache 2.0 license


#### Data models / API specifications

The spesification is kept minimal to give an idea.

* **Entities**

  * **User**: `{ id, github_id, email?, created_at }`
  * **Project**: `{ id, user_id, title, source_code, created_at, updated_at }`
  * **Build**: `{ id, project_id, ink_version, toolchain, status, stderr, stdout, wasm_cid?, metadata_cid?, created_at }`
  * **Deployments**: `{ id, project_id, network, tx_hash, code_hash?, contract_address?, success, created_at }`

* **REST Endpoints** (Rust/Axum; representative paths)

  * `POST /api/compile` → input: `{ user_id, project_id, source_code, ink_version }` → output: `{ status, stderr, stdout, wasm, metadata }`
  * `POST /api/projects` / `GET /api/projects/:id` / `PUT /api/projects/:id` (auth required)
  * `POST /api/deploy` → input: `{ user_id, project_id, source_code, ink_version }` → output: `{ status, stderr, stdout, wasm, metadata }`

* **Authentication**

  * **Supabase Auth** for user management and persistence.
  * **GitHub OAuth** for login; session managed server‑side with secure cookies. 


#### What this project is **not** (v1 scope fences)

* No **polkadot.js browser extension** integration in v1; **built‑in wallet only**.
* No **code completion** or language server integration; **syntax highlighting only**.
* No **multi‑file** projects; one source file per project in v1.
* No mainnet deployments; **testnet only** in v1.
* No audits, no token, no business/marketing features.


#### Similar Projects and Distinction

Within Polkadot’s ecosystem itself, there is currently no comparable alternative — developers either use local environments or limited tools like the polkadot.js Apps UI (which allows deploying and calling contracts but doesn’t provide a coding environment). Our project is unique in providing a full coding-to-deployment journey in one web interface for ink! developers.

- **Previous ink! Playground (Parity)** – The prior iteration of an ink! web IDE (open-sourced by Parity Technologies) is the direct predecessor to this project. It used a similar tech stack (TypeScript, React, Monaco, Docker) and proved the concept’s value. The project effectively revives and modernizes this idea: targeting ink! v6 (whereas the old one targeted ink! 3/4), and addressing known issues (container deployment, multi-version support, etc.). Unlike the previous version, which fell out of maintenance, I will establish a sustainable maintenance plan (with potential follow-up grants for upkeep) to ensure the Playground remains live and up-to-date long term.

- **Remix (Ethereum)** – A highly popular web IDE for Solidity on Ethereum. Remix demonstrates how a web IDE can become an indispensable part of a developer ecosystem. Our ink! Playground is analogous in purpose – providing similar one-stop convenience – but for Substrate-based Wasm contracts. 

- **Other Web IDEs** – Solana, Move, and others have web IDEs. For example, Solana Playground allows in-browser Rust program deployment, and ICP has a web REPL for Motoko. These projects validate the approach. 

- **The Wizard (Arbitrum Stylus)** – I have already successfully built and deployed a fully functional web-based IDE for Arbitrum Stylus called Wizard. 

  You can try it out at <https://thewizard.app>

  Here is the Wizard demo presented by official Arbitrum OffchainLabs: <https://x.com/arbitrum/status/1889010128562933845>

  - 303 active users have interacted with the playground so far this year.
  - There have been a total of 489 sessions recorded during this period.
  - The users have performed approximately 2,800 activities in total.
  - Total 243 contracts compiled
  - Total 198 contract calls recorded
  - Over 60,000 views for Wizard related posts on X (Many accounts shared including official Arbitrum account)
  
  | | | |
  | -----: | ----------- | ------------- |
  | <img width="782" height="403" alt="traction1" src="https://github.com/user-attachments/assets/8bc1c15b-224d-45fc-ad3d-caf58a0ba5b5" /> | <img width="621" height="403" alt="traction2" src="https://github.com/user-attachments/assets/00927e38-84ea-497d-ae2f-8e8216ffceea" /> |  ![traction3](https://github.com/user-attachments/assets/c4b7384c-b45d-4d1d-bfbf-766c21a219fb) |


## Team :busts_in_silhouette:

### Team members

- Tolga Yaycı

### Contact

- **Contact Name:** Tolga Yaycı
- **Contact Email:** [tolgayayci@protonmail.com](mailto:tolgayayci@protonmail.com)
- **Website:** https://github.com/tolgayayci

### Legal Structure

- **Registered Address:** Individual - N/A
- **Registered Legal Entity:** Individual

### Team's experience

Tolga is an experienced software engineer with a strong background in developer tooling and frontend systems. He holds a Bachelor's degree in Computer Engineering and has successfully delivered numerous developer tools across prominent blockchain ecosystems including IOTA, Arbitrum, Stellar, Internet Computer and so on. 

His recent notable grantee projects include:

- Arbitrum Stylus Playground: An online IDE for Arbitrum Stylus smart contracts - https://thewizard.app/
- Arbitrum Stylus VS Code Extension: Developer tooling integration for Arbitrum Stylus - https://marketplace.visualstudio.com/items?itemName=tolgayayci.stylussuite
- ICP DFX Dashboard: User-friendly graphical interface for ICP dfx-cli - https://github.com/tolgayayci/dfinity-dfx-gui/
- Sora: Desktop app to interact with Stellar network - https://github.com/tolgayayci/sora

### Team Code Repos

- https://github.com/tolgayayci/wizard
- https://github.com/tolgayayci/dfinity-dfx-gui
- https://github.com/tolgayayci/sora
- https://github.com/tolgayayci/stylus-vscode-extension
- https://github.com/tolgayayci/radix-agent-kit
- https://github.com/tolgayayci

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/tolgayayci

## Development Status :open_book:

The ink! Playground project is currently in the research and planning phase. I have completed initial architectural planning and component design based on my experience building similar tools. Specifically, I've experience in Monaco editor integration with Rust syntax highlighting, and researched cargo-contract. My previous project (Wizard for Arbitrum) provides validated technical patterns that will be adapted for the ink! ecosystem. No active development has begun yet, as I am awaiting grant approval before starting implementation.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 15 weeks
- **Full-Time Equivalent (FTE):**  1 FTE
- **Total Costs:** 50,000 USD

### Milestone 1: Core IDE & Compilation Pipeline

- **Estimated Duration:** 6 weeks
- **FTE:** 1
- **Costs:** $20,000

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | I will provide a README with build/run instructions for the repository. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, I will describe how to run these tests. |
| **0d.** | Docker | I will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Frontend: Monaco Editor Setup | Implementation of the code editor component using Monaco with Rust/ink! syntax highlighting and a clean UI layout |
| 2. | Backend: Compilation Service | A Rust backend service that compiles ink! source code using cargo-contract and returns WebAssembly output or error messages. This includes Docker containerization.|
| 3. | API Integration | Connect the frontend to backend APIs, including error handling, request state management, and displaying compilation output |
| 4. | Error Reporting | Parse Rust/ink! compiler errors and display them in the stdout/stderr UI sections |
| 5. | User Authentication | Implement Supabase Auth and GitHub OAuth to handle user session management |
| 6. | Project Persistence | Supabase integration: Basic database schema and API endpoints for creating, saving, and loading user projects |


### Milestone 2: Deployment & Contract Interaction

- **Estimated Duration:** 5 weeks
- **FTE:** 1
- **Costs:** $20,000

#### Deliverables:

| Number | Deliverable | Specification |
| ------ | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | Updated documentation including deployment usage guide and contract interaction |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, I will describe how to run these tests. |
| **0d.** | Docker | I will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | In-Browser Wallet | Implementation of a built-in wallet for testnet usage |
| 2. | Network Connection | Integration with polkadot.js/api to connect to a test network (Pop on Paseo), with network status indicator |
| 3. | Contract Deployment UI | Interface for deploying compiled contracts, including constructor parameter forms based on contract metadata |
| 4. | Transaction Monitoring | Real-time tracking of deployment transactions with status updates (pending, success, error) |
| 5. | Contract Interaction | UI for calling contract methods (both read-only and state-changing) after deployment, with parameter forms generated from metadata |
| 6. | Deployment History | Track and display user's deployment history with contract addresses and timestamps |


### Milestone 3: Templates, Additional Features, and Deployment

- **Estimated Duration:** 4 weeks
- **FTE:** 1
- **Costs:** $10,000

#### Deliverables:

| Number | Deliverable | Specification |
| ------ | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | Comprehensive user documentation, API documentation, and maintenance guide |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | I will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| **0e.** | Article | Tutorial showcasing the complete workflow from writing to deploying an ink! contract |
| 1. | ink! Contract Templates | Implementation of the template gallery featuring standard, commonly used smart contracts and patterns with one-click import functionality |
| 2. | Multi-Project Management | Dashboard for managing multiple projects |
| 3. | Project Sharing | Generate shareable links for projects (permalink functionality) |
| 4. | Production Deployment | Full deployment to AWS EC2 with HTTPS, proper DNS, and analytics implementation |


## Future Plans

To ensure ink! Playground remains actively maintained unlike its predecessor, I commit to supporting the platform for at least 12 months post-launch with regular updates for new ink! releases. My track record demonstrates this commitment - my previous grant-funded project, Wizard Web IDE (for Arbitrum), has shown consistent maintenance with regular commits since its February 2025 launch (visible at https://github.com/tolgayayci/wizard/tree/dev). 

The technical roadmap will focus on keeping the tool relevant as the ecosystem evolves. After completing v1 and gaining initial traction, I plan to propose a v2 of the project through follow-up grants that will implement advanced features not supported in the initial version. These would include language server integration for intelligent code completion, testing framework support, expanded network support for additional parachains, and enhanced collaboration tools. 

Regular collection of usage metrics will guide the prioritization of these v2 features based on actual developer needs. This phased approach ensures sustainable development while maintaining a continuously valuable tool for the ecosystem.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Web3 Foundation Grants page
