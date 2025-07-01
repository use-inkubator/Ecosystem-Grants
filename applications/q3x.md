# Q3x

- **Team Name:** Q3x
- **Payment Address:** 1j5orUDb4c9kD7h5Hfofpn5YX1dgUKjZ1753VP2KHJzsbZ8

## Project Overview :page_facing_up:

### Overview

Please provide the following:

- `Tagline`: Self-hosted multisig app built with ink!, a local-first approach for programmable asset management that removes centralized UI risk on Polkadot.
- `Brief description`: Q3x is a local-first and open-source modular multisig app. Designed as a secure alternative to frontend-dependent multisig apps like Safe, Mimir and Polkadot Multisig. Q3x empowers teams to coordinate asset management without relying on a centralized user interface. By enabling users to spin up their own lightweight UI by CLI locally, Q3x eliminates the frontend as a single point of failure, a risk that has led to over $1.5B losses for Bybit. The project will deliver an ink! v6 modular multisig smart contract, a Safe-like UI for asset management, and a CLI tool to spin up UI locally.
- `Relation to Ink!`: Q3x is built entirely using the ink! v6 smart contract language, compared to existing multisig apps such as [Polkadot Multisig](https://polkadotmultisig.com/), [PolkaSafe](https://forum.polkadot.network/t/polkasafe-making-multisig-usable-on-polkadot-kusama/3160) and [Mimir](https://docs.mimir.global/) that rely on multisig pallets, our approach uses ink! v6 smart contracts to introduce less friction for developing and deploying it. This approach is a flexible, modular multisig design inspired by systems like [Safe modules](https://docs.safe.global/advanced/smart-account-modules).
- `Chosen project category`: Business Dapp
- `Importance`: Most existing solutions rely heavily on centralized user interfaces, creating serious security and availability risks. This centralization has already led to over $1.5 billion in losses through frontend exploits in Gnosis Safe-based setups. Meanwhile, current multisig apps in the Polkadot ecosystem primarily use proxy pallets

Q3x addresses these problems by:

- A user-friendly hosted web interface for teams and DAOs
- A local-first CLI + UI setup for power users, auditors, and organizations with strict security policies
- A modular multisig account design that enables crypto-native teams and SMBs to customize their multisig experience

This modularity not only supports advanced use cases but also opens a new market for developers to build and deploy their own extensions. If a specific feature isn’t officially supported, teams can still tailor their multisig workflows by integrating community-built modules or build by their own developers.

- Why our team is interested: Our team is passionate about improving usability and security for crypto native teams and SMBs. The recent Bybit incident where attackers compromised a Gnosis Safe UI on a centralized server and tricked multisig signers into executing a malicious transaction highlighted the dangers of relying on hosted interfaces. We recognized a similar risk for Polkadot’s multisig users, if they rely on a website or web app, a hack of that frontend could lead to money losses. By creating a local-first tool, we aim to empower the community with a more secure way to use multisigs.

### Ink! Ecosystem Impact

Kindly check this document for a detailed breakdown of business model: [Q3x Business model
](https://docs.google.com/document/d/1Z8ONzIzE3Lz25q95oW5aHl1LllQksbzl/edit?usp=sharing&ouid=101167316615257009560&rtpof=true&sd=true
)

### Project Details

#### An overview of the technology

- Smart Contract: Ink! V6,
- Frontend:  Next.js (React)
- CLI Tool: Node.js, TypeScript and Commander.js or Yargs for command parser framework
- Contract integration: Papi (+ papi ink! sdk)

#### Documentation of core components

- `Programmable Multisig Smart Contracts Written In Ink!`
 The core multisig logic will be implemented in ink!, covering key functionalities such as deploying new multisig vaults, proposing transactions, collecting approvals, handling rejections, and managing signer roles and thresholds.
- `Frontend (Hosted UI)` – TypeScript, Nextjs, Papi (+ papi ink! sdk).
We will build a user interface using Next.js and “Papi”. This web interface will allow teams to manage multisig accounts, sign transactions, and monitor proposal status using injected browser extensions like Talisman and Polkadot.js.
- `CLI + Local UI` – Node.js, TypeScript
A lightweight CLI tool will enable users to spin up the full Q3x UI locally on their own machines. This provides an alternative to the hosted frontend for users who prefer self-hosting or require higher security, especially in environments where frontend compromise is a risk.

#### PoC/MVP or other relevant prior work

We have extensively researched the current state of multisig solutions in the Polkadot ecosystem and identified critical gaps that Q3x is designed to address.

Most existing Polkadot multisig apps such as Mimir, Multix, and Polkadot Multisig by Signet (as listed on the [Polkadot Wiki](https://wiki.polkadot.network/general/multisig-apps)) leverage the [prebuilt multisig pallet](https://github.com/paritytech/polkadot-sdk/tree/polkadot-stable2412/substrate/frame/multisig) and proxy pattern. While this approach offers standardization, it significantly limits customizability and extensibility. This inflexibility makes it difficult for crypto-native teams and SMBs to tailor multisig logic to their specific governance or operational needs.

In contrast, the EVM ecosystem is rapidly moving toward modular smart account architecture, with standards like EIP-7579 (used by Safe, ZeroDev, Biconomy) and EIP-6900 (pioneered by Alchemy) enabling composable account designs. Q3x aims to bring a similar level of modularity and extensibility to the Polkadot ecosystem via ink!-based smart contracts.

Additionally, our research identified a pressing need for local-first UI options in the wake of high-profile frontend exploits. For instance, Gnosis Safe’s hosted UI has been compromised multiple times, and the Bybit wallet hack reportedly exploiting this attack vector resulted in over $3 billion in losses. These incidents expose a systemic risk from over-reliance on centralized user interfaces.

Community demand for alternatives is also evident, Safe-CLI, an open-source CLI for interacting with Gnosis Safe accounts, has garnered over 240 stars on GitHub, signaling strong interest in frontend-independent workflows.

Q3x combines these insights by offering a customizable ink! multisig smart contract and a local-first UI option, empowering users to interact with their multisig setup securely without depending on any centralized frontend.

#### What your project is not or will not provide or implement

No multi parachains supported. No xcm calls for assets on other parachains yet

#### CATEGORY

Business Dapp

#### An overview of the business model

Kindly check this document for a detailed breakdown of business model: [Q3x Business model
](https://docs.google.com/document/d/1Z8ONzIzE3Lz25q95oW5aHl1LllQksbzl/edit?usp=sharing&ouid=101167316615257009560&rtpof=true&sd=true
)

#### Future production plans and growth strategy

Our long-term vision for Q3x is to evolve into a secure, programmable, and privacy-preserving asset management platform tailored for teams, DAOs, and SMBs in the Polkadot ecosystem.

Future development plans include:

- `AI-Assisted Transaction Summaries`: Integrating AI to help signers understand the intent and potential risks of each transaction, improving transparency and reducing signing errors.

- `Privacy-Preserving Multisig`: Introducing optional privacy layers to support sensitive use cases. This will enable compliant, privacy-respecting operations for teams and organizations through techniques like zero-knowledge proofs and threshold encryption.

- `Proof of Innocence`: To align with regulatory requirements while preserving user privacy, we plan to support “one-click” proof-of-innocence disclosures. Using zero-knowledge proofs, users can demonstrate regulatory compliance (e.g., AML checks) without revealing sensitive on-chain details.

- `WalletConnect-Style Integration`: Q3x will support a local “connect” feature, allowing teams to interact with other dApps in the Polkadot ecosystem directly through their multisig accounts, improving compatibility and user experience.

- `Tax & Accounting Tools`: We plan to add integrations for crypto-native bookkeeping, reporting, and tax compliance, streamlining operational workflows for organizations.
Multisig modules: We plan to deliver several multisig modules in the future, including whitelisting, daily spending limits, and time-locked transfers.
- `One-Click Migration Tool`: A one-click migration tool will be introduced to allow users to seamlessly transfer their multisig setup and assets from Safe, Mimir, Multix, and Polkadot Multisig into Q3x.

- `Payment related features for Premium Tier users`: Premium Tier payment features will include recurring payments, streaming payments, and group bill-splitting functionalities.

As outlined in the Business model section, we have a two-phase sustainability plan. Please refer it for more detail.

## Team :busts_in_silhouette:

### Team members

- Name of team leader: Gian Alarcon
- Names of team members: Ng Ju Peng, Martin Hofmann

### Contact

- **Contact Name:** Gian Alarcon
- **Contact Email:** <gian@quantum3labs.com>
- **Website:** <https://quantum3labs.com/>

### Legal Structure

- **Registered Address:** 68 Circular Road #02-01, Singapore 049422

- **Registered Legal Entity:** Quantum3 Labs Pte. Ltd.

### Team's experience

`Gian Alarcon`: (Project Lead): Software Engineer with a degree in Systems Engineering from UNMSM, Peru, and Intelligence Science Technology from USTB, China. Graduate of Polkadot Blockchain Academy (PBA 5 Singapore). Serves as main contributor to the Scaffold-Stark project with expertise in Rust backend development. Has made significant contributions to the Starknet Dojo framework and founded the onchain game The Marquis.

`Ng Ju Peng`: Blockchain developer with 3+ years of experience and a bachelor's degree in Software Engineering from Xiamen University. Winner of the Starknet Bengaluru Hacker House and founder of Q3x v1. Has contributed to fully on-chain mobile games on Starknet and served as core contributor to Scaffold-Stark. Featured as speaker at Starknet Basecamp and workshops, and built an NFT game on Caldera plus an Ethereum delegation staking platform that secured 100k+ TVL.

`Martin Hofmann`: Developer Relations Engineer with expertise in blockchain infrastructure, developer support, and technical documentation. Currently part of the team at PaperMoon.io, helping developers build on Wormhole. Graduate of Polkadot Blockchain Academy (Singapore, 2024). Previously worked at SenseiNode, focusing on blockchain infrastructure, monitoring tools, and building internal tools and dashboards to support operations.

### Team Code Repos

- <https://github.com/Scaffold-Stark>
- <https://github.com/The-Marquis-Gaming>
- <https://github.com/dojoengine/dojo>
- <https://github.com/Quantum3-Labs>
- <https://github.com/q3x-finance/>
- <https://github.com/Top-Summer-Hackers>

Please also provide the GitHub accounts of all team members.

- <https://github.com/gianalarcon>
- <https://github.com/ngjupeng>
- <https://github.com/martin0995>

## Development Status :open_book:

Q3x is currently in the **pre-development** phase for its ink! version. We have:

### Research on Existing ink! Multisig Implementation

- [ink-examples multisig implementation](https://github.com/use-ink/ink-examples/blob/c72b4cb0d6cfd7229a4c441b789d86c07e995451/multisig/lib.rs#L65)
- [ink! contract multi-sig ecosystem grant application](https://github.com/use-inkubator/Ecosystem-Grants/blob/master/applications/ink_contract_multi-sig.md)

### Q3x V1 Figma UI Prototypes for Starknet

- [Q3X UI Design](https://www.figma.com/design/I4KoJ2KXeV6JIMbC5Jqui6/Q3X-UI-Design?node-id=1-5&p=f&t=Y9voJF1uBBaQA2qd-0) (Private, happy to share if requested!)

### Research on Demand CLI-based Asset Management

Related tweets and resources:

- [safe-global/safe-cli](https://github.com/safe-global/safe-cli)
- [Tweet by @senamakel](https://x.com/senamakel/status/1893001991971905542)
- [Tweet by @newmichwill](https://x.com/newmichwill/status/1892994743434453414?s=46&t=TdPtf3LlghnKC8uRLsXlhA)

### Existing Implementation Experience

While we have not yet published a formal research diary or blog posts, our GitHub repos for the Starknet implementation reflect our experience:

- **UI Repo**: [q3x-finance/q3x](https://github.com/q3x-finance/q3x) (Private, happy to share if requested!)
- **Server Repo**: [q3x-finance/q3x-server](https://github.com/q3x-finance/q3x-server) (Private, happy to share if requested!)

### Next Steps

We will begin committing to the ink! version in public repositories immediately after grant approval. Any future research, development updates, and technical notes will also be published.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total estimated duration**: 3 months
- **Full-time equivalent (FTE)**: ~2.5 FTE
- **Total costs**: 48,000 USD

### Milestone 1

- **Estimated duration**: 1 month
- **FTE**: 2.5
- **Costs**: 14,000 USD

| Number | Deliverable | Specification |
|--------|-------------|---------------|
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic tutorial in a readme |
| 0c. | Testing and Testing Guide | The contract will be covered with unit tests |
| 0d. | Docker | A Dockerfile will be provided for testing functionalities |
| 1a. | Figma Design | We will deliver a complete Figma prototype for Polkadot version |
| 1b. | Ink! Contract Implementation | An ink! smart contract for modular multisig contract |
| 1c. | Ink! Contract Testing | A comprehensive unit and integration testing will be conducted |

### Milestone 2

- **Estimated duration**: 1 month
- **FTE**: 2.5
- **Costs**: 20,000 USD

| Number | Deliverable | Specification |
|--------|-------------|---------------|
| 0a. | License | MIT |
| 0b. | Documentation | The UI will include code-level comments and a README explaining setup, component structure, and contract interaction points. |
| 0c. | Testing and Testing Guide | Core UI flows will be tested via manual testing |
| 0d. | Docker | A Dockerfile for serving the frontend |
| 1a. | Static UI implementation | We will build the frontend using TypeScript and Next.js. It will match the Figma design |
| 1b. | ink! Contract Integration | The UI will be connected to the deployed ink! multisig contract, propose, approve and reject transaction using the PAPI |

### Milestone 3

- **Estimated duration**: 1 month
- **FTE**: 2.5
- **Costs**: 14,000 USD

| Number | Deliverable | Specification |
|--------|-------------|---------------|
| 0a. | License | MIT |
| 0b. | Documentation | The CLI will include detailed usage documentation in the README, plus inline code comments. |
| 0c. | Testing and Testing Guide | Key CLI commands will be tested using unit and integration tests. |
| 0d. | Docker | A Dockerfile will be provided to allow users to run the CLI and spin up the local UI in a self-contained environment. |
| 0e. | Article | We will publish an article on Medium or X that explains all features of the frontend application and smart contract functionality and the CLI |
| 1a. | Command Parser Framework | We will use CLI framework (e.g., Commander.js or Yargs) to handle command parsing, argument validation, and help messages. |
| 1b. | CLI Implementation | The CLI will be written in TypeScript using Node.js. It will support spinning up local UI |
| 1c. | Local UI Integration Testing | We will ensure that the local UI, when spin up via the CLI, functions seamlessly and offers the same user experience and functionality as the hosted version. |

### Future Plans

Q3x is designed with extensibility in mind. Future enhancements include multichain support across ink!-compatible parachains, multisig modules, one click migration tool, privacy-preserving multisig features, AI-assisted transaction explanations, and tooling for regulatory compliance.

## Additional Information :heavy_plus_sign:

Q3x is currently live on Starknet mainnet (deployed since March 24, 2025) with:

- **2000+ users**
- **1200+ AI assistant interactions**

## Existing Features on Starknet Q3x

- Transaction batching
- Recurring payment setup
- Multisig wallet deployment
- Wallet analysis
- Address book management
- Transaction history and wallet analysis export
- AI assistant for queries and automation

## Resources

- **Website**: <https://q3x.io/>
- **GitHub**:
  - UI: <https://github.com/q3x-finance/q3x>
  - Server: <https://github.com/q3x-finance/q3x-server>
- **Design**: [Figma Link](https://www.figma.com/design/I4KoJ2KXeV6JIMbC5Jqui6/Q3X-UI-Design?node-id=1-5&p=f&t=Y9voJF1uBBaQA2qd-0)
- **Demo Video**:
  - <https://www.tella.tv/video/cm7w8c9wa000h0ajph2geafpe/view>
  - <https://www.loom.com/share/776b33aca79a4a65a194795c40ee1e05?sid=2a01f403-e57c-497f-ad99-2812483b5d0c>

**Note**: Some links are private, we're happy to share them upon request.

Meanwhile, Q3x is collaborating with [Miden](https://x.com/0xMiden).
