# inkPilot

- **Team Name:** Mert Köklü
- **Payment Address:** 152tNeEWvJmRbdSijiqQGLVgyXiuizHkmCdUXGDutQW8wrzp


## Project Overview :page_facing_up:
### Overview

* **Tagline:** An MCP server that transforms natural-language requests into concrete ink! development actions through intelligent code generation, RAG-powered documentation assistance, and seamless toolchain integration.

* **Brief description:** inkpilot is a Model Context Protocol (MCP) server implemented in Rust that bridges the gap between MCP clients and ink! smart contract development. It exposes a comprehensive set of tools that enable conversational interfaces to scaffold projects, generate intelligent contract code, build and test contracts, deploy to networks, and provide contextual documentation assistance. Unlike existing MCP servers that focus on blockchain data access, inkpilot leverages the complete ink! development toolchain to create an integrated development experience through natural language commands.

* **Relation to ink! ecosystem:** inkpilot orchestrates the complete ink! development toolchain including `cargo-contract`, Pop CLI, and Substrate RPC calls. It provides intelligent wrappers around standard ink! workflows: project scaffolding, intelligent code generation based on ink! patterns, testing, verifiable builds, verification, and on-chain interactions (upload/instantiate/call). The tool integrates deeply with ink! documentation to provide contextual guidance and error resolution.

* **Category:** **Infrastructure** — developer tooling that enhances productivity through AI-assisted development workflows.

* **Why I'm building this:** ink! development currently requires extensive context switching between documentation, terminal commands, and code editors. Developers must memorize numerous command sequences, understand complex error messages, and frequently reference documentation. I want to eliminate these friction points by creating an AI-powered assistant that understands ink! development patterns and can execute complex workflows through simple natural language requests.

### Ink! Ecosystem Impact

**Who benefits:** ink! smart contract developers of all skill levels, from beginners learning the ecosystem to experienced developers seeking faster iteration cycles.

**How it's applied:** Developers work within their preferred IDE with an MCP-compatible AI assistant. Through natural language conversation, they can request complex development tasks that inkpilot executes by orchestrating the underlying ink! toolchain. The AI interprets intent, generates appropriate code, executes builds and tests, handles deployments, and provides contextual documentation assistance.

**Expected effect:** 
- **Faster onboarding** for new ink! developers through guided, conversational development
- **Reduced context switching** by eliminating the need to reference documentation and remember command syntax
- **Improved code quality** through AI-generated contracts that follow ink! best practices
- **Enhanced debugging** with intelligent error interpretation and suggested fixes
- **Streamlined workflows** for experienced developers tackling repetitive tasks

**Specific examples:**
- > "Create an ERC-20 token with minting capabilities and deploy it to testnet" → AI generates contract code following ink! patterns, builds with `cargo contract build`, runs tests, and deploys

- > "Fix this test failure and explain what went wrong" → AI analyzes `cargo contract test` output, correlates with ink! testing documentation, and suggests specific fixes

- > "Build this contract with verifiable build and verify against reference" → AI executes `cargo contract build --verifiable` and `cargo contract verify` with proper error handling

### Project Details

#### Technology Stack

- **MCP Server Runtime:** Rust implementation using the official Rust MCP SDK for robust, high-performance protocol compliance
- **Substrate Chain Interaction:** subxt for strongly-typed, runtime-safe interaction with any Substrate-based chain (Polkadot, Kusama, ink-node, Asset Hub, Pop Testnet, custom chains)
- **ink! Toolchain Integration:** Direct orchestration of `cargo-contract` commands
- **Pop CLI Integration:** Native support for Pop CLI workflows as an alternative to cargo-contract where preferred
- **Code Generation Engine:** Template-based code generation using ink! patterns, and best practices
- **RAG Knowledge System:** Vector-based documentation search with embedding models for contextual retrieval from ink! docs, examples, and community patterns
- **Process Management:** Robust command execution with timeout handling, error recovery

#### Differences from Existing MCP Servers

- Substrate MCP Server - https://github.com/ThomasMarches/substrate-mcp-rs
A specialized MCP server that exposes dynamic Substrate blockchain operations via the MCP protocol. It focuses on querying balances, blocks, pallets, storage, events, and submitting transactions to Substrate nodes. While effective for blockchain data access, it's limited to live chain interaction without development workflow integration. Corresponds only to 'Chain Interaction' feature of inkpilot.

- Cairo Coder MCP - https://www.cairo-coder.com (StarkNet ecosystem)
A specialized MCP server that provides Cairo and StarkNet development assistance, focusing primarily on code generation for Cairo language smart contracts. This project is very similar to inkpilot in its approach to intelligent code generation and has demonstrated strong community adoption with 770+ downloads since its July 2024 release. However, it's limited to smart contract code generation without broader ecosystem integration or development workflow capabilities. inkpilot extends this concept by adding comprehensive development workflow interactions (building, testing, deployment, verification) alongside similar intelligent code generation features. 

- Kapa AI - https://www.kapa.ai
A documentation AI platform that enables companies to create custom AI assistants trained on their technical documentation. Many blockchain projects use Kapa to provide conversational access to their docs, helping developers find answers without manual searching. The whole product is one of the features of inkPilot ('RAG-Powered Knowledge System' feature).

- Substrate MCP Server - https://github.com/ThomasMarches/substrate-mcp-rs
A specialized MCP server that exposes dynamic Substrate blockchain operations via the MCP protocol. It focuses on querying balances, blocks, pallets, storage, events, and submitting transactions to Substrate nodes. While effective for blockchain data access, it's limited to live chain interaction without development workflow integration. Corresponds only to 'Chain Interaction' feature of inkpilot.

  **1. Developer-Focused vs. Data-Focused Approach**

  [*Existing Substrate MCP server by ThomasMarches*](https://github.com/ThomasMarches/substrate-mcp-rs) focuses on exposing blockchain data and state to MCP clients:
  - Query account balances and storage
  - List pallets and their entries  
  - Fetch events and extrinsics
  - Submit transactions
  - Access system and block information

  *inkpilot* focuses on the complete development workflow:
  - Project scaffolding and code generation
  - Build automation and testing frameworks
  - Deployment pipelines and verification
  - Error interpretation and debugging assistance
  - Documentation-guided development

  **2. Target Audience Distinction**

  *Substrate MCP Server* target: MCP users who want to interact with live blockchain data through conversational interfaces

  *inkpilot* targets: ink! developers who want to accelerate their development workflow through intelligent assistance

  **3. Use Case Comparison**

  | Substrate MCP Server | inkpilot |
  |---------------------|----------|
  | "What's Alice's balance?" | "Create an ERC-20 token with minting capabilities" |
  | "Show me recent transfers" | "Fix this compilation error and explain the issue" |
  | "List all pallets" | "Deploy this contract with verifiable build to testnet" |
  | "Submit this transaction" | "Generate tests for this contract function" |


#### Deliverables

**1. Core Integrations**

Complete orchestration of the ink! development toolchain through MCP tools that handle the entire development lifecycle from project creation to deployment across the Substrate ecosystem.

*Key Integration Points:*
- **Project Scaffolding:** `cargo contract new` and `pop new` with intelligent template selection and Pop CLI's enhanced project setup workflows
- **Build Automation:** `cargo contract build` with support for verifiable builds, alongside `pop build` for streamlined compilation with Pop-specific optimizations
- **Testing Framework:** `cargo contract test` and `pop test` with detailed result parsing, failure analysis, and Pop's integrated testing environment
- **Deployment Pipeline:** Upload and instantiate workflows using subxt's strongly-typed API for type-safe contract deployment to any Substrate chain
- **Chain Interaction:** subxt integration for runtime-safe queries, contract calls, and state inspection with full metadata support
- **Verification System:** `cargo contract verify` for deterministic build verification with Pop CLI compatibility checks

*Example Workflow:*
```
Developer: "Create a governance token contract and deploy it to Pop testnet"

> MCP calls project.new("governance_token", template="erc20_governance")
> Scaffolds project using pop new with governance template and enhanced project structure
> MCP calls build.contract(verifiable=true, use_pop=true)
> Executes pop build --verifiable leveraging Pop's optimized build pipeline
> MCP calls test.run(framework="pop")
> Runs comprehensive test suite using pop test with integrated environment
> MCP calls deploy.upload(endpoint="wss://rpc1.paseo.popnetwork.xyz", use_subxt=true)
> Uses subxt to upload contract code with strongly-typed metadata validation
> MCP calls deploy.instantiate(constructor="new", args={"name": "GovToken", "symbol": "GOV"})
> Creates contract instance via subxt with type-safe parameter encoding
> Returns: "Governance token deployed at 5D4k8... with code hash 0x7a9b..."
```

**2. Intelligent Code Generation**

Pattern-based code generation that understands ink! patterns and creates smart contracts from natural language specifications. The system identifies contract types from developer descriptions, generates complete contracts with proper ink! macros and error handling, and integrates security patterns and gas optimizations. 

*Example Scenario:*

```
Developer: "Create an NFT marketplace with royalties and auction functionality"

> System analyzes requirements: NFT standards + marketplace logic + auction mechanisms
> Generates base ERC-721 contract with marketplace extensions
> Includes royalty distribution logic following ink! patterns
> Adds auction state management with proper timing controls
> Implements security checks for ownership and payment validation
> Creates comprehensive test suite covering edge cases
> Returns: Complete contract with documentation and deployment instructions
```

**3. Knowledge Base & Documentation Assistant**

RAG-powered documentation system that provides contextual assistance, error interpretation, and development guidance throughout the ink! development process. The system maintains a comprehensive vectorized knowledge base of ink! documentation, examples, best practices, and community solutions, enabling contextual search that retrieves relevant information based on current development context and error states. It maps compilation errors, test failures, and runtime issues to specific documentation sections while providing step-by-step assistance for complex workflows and maintaining a library of proven ink! patterns with usage examples and implementation guidance.

*Example Interaction:*

```
Developer: "My test is failing with 'AccountId not found' error"

> MCP calls error.interpret(error_output)
> Analyzes test failure and identifies missing test account setup
> MCP calls docs.search("ink test AccountId setup")
> Retrieves relevant testing documentation sections
> Correlates error with common testing patterns
> Returns: "This error occurs when test accounts aren't properly initialized. 
  Here's how to set up test accounts in ink!: [code example]
  See: https://use.ink/docs/v6/testing/unit-testing#test-environment"
```


**What inkpilot is NOT:**
- Not an IDE or code editor
- Not a wallet or key management system
- Not a hosted service (runs locally as MCP server)
- Not limited to specific AI models (works with any MCP-compatible client)

**CATEGORY:** Infrastructure

**Business model:** Open source project (Apache 2.0 license) with no commercial monetization. Sustainability through community contributions and potential follow-on grants for advanced features.


## Team :busts_in_silhouette:

### Team members

- Mert Köklü

### Contact

- **Contact Name:** Mert Köklü
- **Contact Email:** kklumert@gmail.com
- **Website:** https://github.com/justmert

### Legal Structure

- **Registered Address:** Individual - N/A
- **Registered Legal Entity:** Individual

### Team's experience

Mert is an experienced software engineer with a strong background in blockchain development, smart contract tooling, and backend infrastructure. He holds a degree in Computer Science and has led both AI and blockchain-focused engineering teams.

He previously worked with ApeWorX where he developed StarkNet plugins and compiler tools for the Cairo language. He also served as the AI Video Analytics Team Lead at an NVIDIA partner company, managing intelligent vision-based projects at scale.

Mert has received over 20 ecosystem grants from leading blockchain networks. Below are some of the grantee projects,


### Team Code Repos

- ICP Agent Kit: https://github.com/justmert/icp-agent-kit
- Arbitrum Python SDK: https://github.com/justmert/arbitrum-python-sdk
- Kurtosis-Orbit: Deployment tool that spins up complete Arbitrum Orbit rollup environment - https://github.com/justmert/kurtosis-orbit
- Compound-React: React kit for interacting with Compound III protocol - https://github.com/justmert/compound-react
- SAI: Framework for interacting with the Sia blockchain through natural language - https://github.com/justmert/sai
- SiaQL: A GraphQL interface for the Sia decentralized storage network - https://github.com/justmert/SiaQL
- Koios Rust SDK: A Rust SDK for Cardano’s Koios API - https://github.com/justmert/koios.rs


### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/mertkoklu


## Development Status :open_book:

This project is in the initial planning and design phase. I have completed preliminary research on MCP protocol specifications, ink! toolchain integration patterns, and Rust MCP SDK capabilities. No implementation has begun pending grant approval.

## Development Roadmap :nut_and_bolt:

### Overview

* **Total Estimated Duration:** 12 weeks
* **Full-Time Equivalent (FTE):** 1.0
* **Total Costs:** 30,000 USD

### Milestone 1 — Core MCP Infrastructure & Intelligent Development Tools

* **Estimated duration:** 7 weeks
* **FTE:** 1.0
* **Costs:** 18,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 license clearly included in all repositories |
| **0b.** | Documentation | Comprehensive README with installation instructions, MCP client setup guide, and detailed examples for each tool. Include troubleshooting section and architectural overview. |
| **0c.** | Testing and Testing Guide | Unit tests covering tool parameter validation, command execution, and error handling. Integration tests with real ink! projects. Guide explaining how to run tests locally and in CI. |
| **0d.** | Docker | Dockerfile that installs Rust toolchain, complete cargo ecosystem, `cargo-contract`, Pop CLI, and configures inkpilot server. Include docker-compose setup for local development with various Substrate chains. |
| 1. | **MCP Server Foundation** | Complete Rust-based MCP server implementation using official MCP Rust SDK with handshake protocol, tool registration system, and request/response lifecycle. |
| 2. | **cargo-contract Integration** | Full integration of all `cargo-contract` commands and subcommands including project creation, building, testing, deployment, and verification workflows with structured output parsing. |
| 3. | **Pop CLI Integration** | Complete Pop CLI integration covering all `pop` commands and subcommands as alternative workflows to cargo-contract with enhanced developer experience features. |
| 4. | **subxt Chain Interaction** | Comprehensive subxt integration for strongly-typed Substrate chain interaction, contract deployment, state queries, and transaction submission across all compatible chains. |
| 6. | **Example Project & Documentation** | Complete example repository demonstrating all integrated tools and workflows. Include sample chat transcripts showing natural language interactions and expected responses from MCP clients. |


### Milestone 2 — Advanced Features & Production System

* **Estimated Duration:** 5 weeks
* **FTE:** 1.0
* **Costs:** 12,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 license clearly included in all repositories |
| **0b.** | Documentation | Production-ready documentation with comprehensive API reference, deployment guides, and integration examples for various MCP clients |
| **0c.** | Testing and Testing Guide | Comprehensive test coverage including unit tests, integration tests, and end-to-end workflow tests |
| **0d.** | Docker | Hardened Docker images with multi-platform support, optimized performance configurations, and production deployment documentation |
| **0e.** | Article | Technical article explaining inkpilot architecture, Rust MCP implementation patterns, and practical usage scenarios. Include step-by-step tutorial for setting up and using inkpilot with different MCP clients. |
| 1. | **RAG Documentation System** | Vector-based documentation search system providing contextual retrieval from ink! knowledge base. Covers contract templates, testing patterns, deployment guides, and troubleshooting with source links and confidence scoring. |
| 2. | **Intelligent Code Generation** | Code generation system that creates ink! contracts from natural language specifications, supporting common patterns like tokens, NFTs, governance, and DeFi protocols. |
| 3. | **Error Intelligence & Pattern Recognition** | Advanced error interpretation system that analyzes compilation errors, test failures, and deployment issues. Correlates errors with documentation and provides actionable fix suggestions with pattern recognition for code improvements. |
| 6. | **Release & Distribution** | Cargo crate publication with semantic versioning, prebuilt binaries for multiple platforms, and community contribution guidelines. |


## Future Plans

After the initial release, inkpilot development will be driven by community feedback and requests. The modular Rust architecture ensures new features can be added incrementally while maintaining stability and performance for existing users.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Web3 Foundation Website
