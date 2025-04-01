# Dedot + Typink

- **Team Name:** Dedot Dev Team
- **Payment Address:** `TODO`

## Project Overview :page_facing_up:
### Overview

Dedot and Typink are complementary projects that together provide a comprehensive solution for developers building applications in the Polkadot ecosystem, with a particular focus on ink! smart contracts. 

[Dedot](https://dedot.dev) is the next-generation JavaScript client for Polkadot and Substrate-based blockchains. Designed to elevate the dapp development experience, Dedot is built & optimized to be lightweight and tree-shakable, offering precise Types & APIs suggestions for individual Substrate-based blockchains and ink! Smart Contracts.

[Typink](https://typink.dev) is a fully type-safe React hooks library built on top of Dedot, designed to accelerate ink! dApp development by providing a robust API for seamless interaction with ink! smart contracts. It simplifies contract integration, ensuring reliable and efficient handling of contract messages and events. Typink also comes with a built-in CLI that helps developers set up new projects in seconds, streamlining the initial development process.

With this proposal, we aim to enhance both projects by adopting ink! v6 integration with pallet-revive support for Dedot & Typink, at the same time improving the current Typink toolkit, ultimately delivering a significantly better developer experience for building ink! smart contract applications.

### Ink! Ecosystem Impact

Our project will directly benefit the ink! ecosystem in several key ways:

1. **Enhanced Developer Experience**: By providing fully type-safe APIs for interacting with ink! smart contracts, we reduce the learning curve and minimize errors, making it easier for developers to build robust applications.

2. **Streamlined Onboarding**: Improvements to the [create-typink](https://docs.dedot.dev/typink/create-typink-cli) CLI will make it faster and easier for new developers to start building ink! dApps with best practices built-in.

3. **Future-Proofing**: Supporting ink! v6 while maintaining compatibility with v4/v5 ensures developers can leverage the latest features without breaking existing applications.

4. **Comprehensive Documentation**: Updated documentation and new tutorials will help educate developers about ink! smart contracts and how to effectively build applications with them.

These improvements will collectively lower the barrier to entry for developers interested in building on ink!, expand the potential user base for ink! dApps, and ensure the tooling evolves alongside the protocol itself.

### Project Details

#### 1. Dedot

##### 1.1. **pallet-revive Support**
   - Support for 20-byte (H160) address format
   - Signing transactions with EVM-compatible Wallets (e.g: MetaMask, SubWallet ...)
   - Contract interactions: 
      - Sending contract queries (read)
      - Signing & submitting contract transactions (write)
      - Deploying contracts
   - Listen to and decode contract events

##### 1.2. **ink! v6 Integration**
   - Ensure compatibility with ink! v4 and v5, allowing developers to use the latest ink! v6 version without breaking existing applications.
   - Generate TypeScript Types and APIs based on contract metadata.
   - Enable Auto-suggestions/IntelliSense for contract APIs based on the generated Types and APIs.
   - Ensure seamless interactions (queries, transaction, events) with ink! v6 contracts via pallet-revive.

#### 2. Typink

##### 2.1. **Integration with Dedot's ink! v6 support**
   - **Compatibility with ink! v4/v5**: Maintain backward compatibility to support existing contracts.
   - **Type and API suggestions**: Leverage Dedot's type generation to provide suggestions for existing hooks.
   - **Comprehensive contract interactions**: Support all contract operations including:
      - Signing & submitting contract transactions
      - Sending contract queries
      - Deploy contracts
      - Listen to & decode contract events.

##### 2.2. **Improved [txToaster](https://docs.dedot.dev/typink/utilities/txtoaster) system**
   - **What is txToaster**: A utility that provides real-time transaction status notifications, keeping users informed about their blockchain transactions from submission to confirmation or failure.
   - **Current limitation**: It's tightly coupled with [react-toastify](https://www.npmjs.com/package/react-toastify), limiting developers who prefer other notification libraries.
   - **Planned improvements**: Create an abstraction layer that separates transaction tracking from UI implementation, enabling support for multiple notification libraries through a simple adapter pattern while maintaining backward compatibility.

##### 2.3. **`create-typink` CLI & template project improvements**
   - **What is create-typink**: The create-typink CLI tool is designed to help developers quickly scaffold a new ink! dApp project using Typink & Dedot. It allows for various customizations, including template selection, example contracts, wallet connectors, and target networks.
   - **Planned improvements**:
     - **Flexible package manager support**: Allowing developers to choose between pnpm, npm, yarn, or bun during project initialization
     - **ink! version support**: ink! v6 or ink! v5/v4
     - **Network configuration**: Adjust supported network lists to accommodate differences between ink! v6 and v5/v4 environments
     - **Expanded stack options**: Provide templates for:
       - Framework options: Next.js or Pure React
       - Upgrade Chakra UI to latest version (v3)
     - **Enhanced template projects**: Update templates to handle differences between ink! v6 and v5/v4 implementations, including wallet integration and contract interactions

##### 2.4. **EVM wallets support**
   - Integrate with MetaMask, SubWallet EVM, and potentially other EVM wallets to enable signing transactions that will be sent through pallet-revive

##### 2.5. **Documentation and tutorials**
   - **Updated documentation**: Comprehensively update [Typink](http://typink.dev/) documentation to cover all new features & changes.
   - **New tutorial**: Develop a step-by-step tutorial for building a dApp with the new ink! v6 integration.

#### Category: Infrastructure

This project falls under the Infrastructure category as it provides essential developer tooling that will be used by many teams building ink! dApps.

## Team :busts_in_silhouette:

### Team members

- Thang X. Vu (Team Leader)
- Tung Vu

### Contact

- **Contact Name:** Thang X. Vu
- **Contact Email:** thang@dedot.dev
- **Website:** https://github.com/dedotdev

### Legal Structure

- N/A

### Team's experience

Dedot is a small but highly specialized team with extensive experience in JavaScript/TypeScript development and Polkadot ecosystem tooling. Founded with a mission to bring Web3 closer to the world, our team combines technical expertise with a practical understanding of developer needs in the blockchain space, consistently delivering high-quality, well-documented & tested code.

We have successfully delivered multiple grant-funded projects through the W3F Grants Program:

- [Typink](https://grants.web3.foundation/applications/typink): a fully type-safe React hooks library designed to accelerate ink! dApp development.
- [Dedot](https://grants.web3.foundation/applications/delightfuldot): a next generation Javascript Client for Polkadot & Substrate.
- [Coong Wallet](https://grants.web3.foundation/applications/coong_wallet): a website-based wallet solution to address the inconsistent wallet experience on mobile & desktop and bring a new approach to onboard new users to Polkadot & Kusama ecosystem.

### Team Code Repos

Project repositories are hosted at https://github.com/dedotdev/dedot

### Team GitHub Profiles

- https://github.com/sinzii
- https://github.com/1cedrus

## Development Status :open_book:

Both Dedot and Typink have been developed through the W3F Grants Program, where we've successfully completed multiple milestones that established the foundation for these tools:

- **Dedot** serves as a foundation for ink! contract interactions in JavaScript/TypeScript, with its lightweight design and type-safe approach reducing development errors and improving code quality for ink! developers.

- **Typink** provides fully type-safe React hooks for ink! contract interactions and a built-in CLI that helps developers onboard and set up projects easier and faster than before.

This proposal builds upon these foundations to address the next set of challenges in the ink! ecosystem: supporting the latest protocol changes (ink! v6) with `pallet-revive` integration, and further improve the toolings to streamline the developer experience and onboarding process.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 5 months
- **Full-Time Equivalent (FTE):** 1.5 FTE
- **Total Costs:** 50,000 USD

### Milestone 1: Dedot - pallet-revive Support & ink! v6 Integration

- **Estimated duration:** 2.5 months
- **FTE:** 1.5
- **Costs:** 25,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and **online documentation** for the new features on https://dedot.dev |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 1. | pallet-revive support | - Add support for 20-byte (H160) address format used in Ethereum-compatible environments<br />- Implement support for signing transactions with EVM wallets like MetaMask and SubWallet<br />- Implement comprehensive support for sending contract queries, submitting contract transactions, and deploying contracts.<br />- Develop functionality to listen to and decode contract events from pallet-revive<br /> |
| 2. | ink! v6 integration | - Add support for ink! v6 while maintaining compatibility with v4/v5<br />- Implement processing of ink! v6 metadata for type generation<br />- Enhance the type and API generation based on ink! v6 metadata<br />- Enable auto-suggestions and IntelliSense for generated types and APIs<br />- Ensure seamless interaction between ink! v6 contracts and pallet-revive |

### Milestone 2: Typink - ink! v6 Integration, Wallet Support & CLI Improvements

- **Estimated duration:** 2.5 months
- **FTE:** 1.5
- **Costs:** 25,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and **online documentation** for the new features on http://typink.dev |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Article | We will publish an article introducing the new features and improvements for Dedot & Typink |
| 1. | Integration with Dedot's ink! v6 support | - Maintain backward compatibility with ink! v4/v5 to support existing contracts<br />- Leverage Dedot's type generation to provide suggestions for existing hooks<br />- Support all contract operations including signing & submitting contract transactions, sending contract queries, deploying contracts, and listening to & decoding contract events |
| 2. | Improved txToaster system | - Create an abstraction layer that separates transaction tracking from UI implementation<br />- Enable support for multiple notification libraries through a simple adapter pattern<br />- Maintain backward compatibility with existing implementations |
| 3. | `create-typink` CLI & template project improvements | - Allow developers to choose between pnpm, npm, yarn, or bun during project initialization<br />- Support ink! v6 while maintaining compatibility with v5/v4<br />- Adjust supported network lists to accommodate differences between ink! v6 and v5/v4 environments<br />- Provide expanded stack options including Next.js/React and updated UI libraries<br />- Update templates to handle differences between ink! versions |
| 4. | EVM wallet support | - Integrate with MetaMask, SubWallet EVM, and potentially other EVM wallets to enable signing transactions that will be sent through pallet-revive |
| 5. | Documentation and tutorials | - Comprehensively update Typink documentation with all new features<br />- Develop a step-by-step tutorial for building a dApp with the new ink! v6 integration |

## Future Plans

Our long-term vision for Dedot and Typink includes:

1. **Continued Protocol Alignment**: We will continue to adapt our tools to support the latest changes in the Polkadot ecosystem & the ink! language, ensuring developers always have access to cutting-edge features.

2. **Expanded Framework Support**: Beyond React, we plan to extend Typink to support other frameworks like Vue and React Native, broadening the potential user base.

3. **Community Building**: We will actively engage with the developer community through workshops, hackathons, and other events to promote the adoption of ink! smart contracts and our tools.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?**: Polkadot Forum
