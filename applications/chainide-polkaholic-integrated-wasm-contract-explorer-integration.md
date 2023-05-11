# ChainIDE + Polkaholic.io WASM Contract Explorer Integration

- **Team Name:** ChainIDE + Colorful Notion
- **Payment Addresses:** ChainIDE [15kdvsU1PnKCH9ShJ52cpiJmtmhSio4cPxwQK1pXgLrUGVSs](https://polkaholic.io/account/5GpLnYCwY13iqcSBLRycgZUd39ho2VWUKUCv9iqB8Fpx61QU?group=overview&chainfilters=all) + Colorful Notion [121Rs6fKm8nguHnvPfG1Cq3ctFuNAVZGRmghwkJwHpKxKjbx](https://polkaholic.io/account/DakP5k8XiY9DQbrCj23xdaUBEBxGrpJoenyB7bYDXWvtZbN?group=overview&chainfilters=all)

## Project Overview :page_facing_up:

### Overview
[ChainIDE](https://chainide.com/) is a development environment for EVM Contracts being extended to include WASM Contract templates.  See [this video link](https://www.dropbox.com/s/o8gds1em05dkfq4/Astar%20ChainIDE%20Demo.mp4?dl=0) ([Testnet url](https://staging-9589904a8a.chainide.com/s/dashboard/projects))
for a full demonstration of ChainIDE's usage for EVM + WASM Contract Development.

[Polkaholic.io](https://polkaholic.io), developed by Colorful Notion, is a multichain block explorer for the Substrate ecosystem covering 75+ chains, including parachains
Astar/Shiden + Amplitude/Pendulum.  Data from Polkaholic is exposed in substrate-etl's "contracts" dataset.   See [this link](https://analytics.polkaholic.io/superset/dashboard/021154ed-efe1-4538-a177-30ae5ef59911/) for a PoC of Polkaholic's WASM Contract Explorer.

In Remix and other EVM IDEs, EVM developers get a well-integrated experience where newly developed Solidity contracts can be:
1. posted ABI posted publicly so that others may also read/write to the contract
2. have code verified and posted publicly
3. have block explorers use 1+2 to show contract call decoding

These 2 teams propose to provide the above well-integrated EVM development for WASM Contract Developers for all Substrate chains using the _contracts_ pallet.
Initial milestones by ChainIDE to cover WASM Contracts have been completed while Colorful Notion has done the groundwork to decode+index WASM Contracts.

## Team :busts_in_silhouette:
### Key Team members
- Colorful Notion: Sourabh Niyogi  + Michael Chung
- ChainIDE: 
  - Xiao Wu, Founder of ChainIDE: https://www.linkedin.com/in/%E5%95%B8-%E5%90%B4-4727237a/?locale=en_US
  - Tim Zhang,  Co-founder and CTO of ChainIDE, former Amazon star employee: https://www.linkedin.com/in/timzmatrixlabs/
  - Alvin Sun, Chief Scientific Officer, CBC(Canadian Blockchain Consortium) Web3 Committee Member: https://www.linkedin.com/in/xinyao-alvin-sun/
  - Jerry Zhang, Product Manager: https://www.linkedin.com/in/jerry-zhang-5a8820220/
  - Leon Liu, Project Managerhttps://www.linkedin.com/in/leon-liu-b4a379117/



### Contact
* **Contact Name:** Sourabh Niyogi
* **Contact Email:** sourabh@colorfulnotion.com
* **Website** https://polkaholic.io/

### Legal Structure

Colorful Notion:
- **Registered Address:** 55 E Third Ave San Mateo, CA 94401
- **Registered Legal Entity:** Colorful Notion, Inc.
Colorful Notion is a multichain analytics company focused on L1/L2
Substrate+EVM Chains and bridges.  Founded in 2021, our approach has
been heavily guided by Substrate's numerous key innovations (XCM,
WASM+EVM) which we embed in our key projects Polkaholic.io, XCMGAR and
Substrate-etl.

ChainIDE:
- **Registered Address:** Vistra Corporate Services Centre, Wickhams Cay II, Road Town, Tortola, VG1110, British Virgin Islands
- **Registered Legal Entity:** Matrix Global Inc.
ChainIDE is a multi-chain tooling platform that provides one-stop development services for blockchain developers. By providing cloud-based user experiences, ChainIDE enables users to immediately begin developing decentralized applications with no configuration, without any pre-installation or requirements on their local system. It is designed to streamline the development process by providing a user-friendly interface and a suite of tools and services to help developers write, test, and deploy smart contracts and dApps.



### Team's experience
ChainIDE was founded in 2017. Our team has been working in the blockchain field for more than five years. The core members have a combined experience of more than ten years in computing science and more than five years in blockchain development experiments. Additionally, we have over 30 product developers and a research and development team comprising ten senior engineers to ensure our services and products' effective and high-quality delivery.

Colorful Notion is led by Sourabh Niyogi and Michael Chung who have been active in blockchain engineering since 2017.  Key engineers Sourabh Niyogi and Michael Chung have developed Polkaholic.io since Fall 2021. Prior to building Polkaholic.io, Sourabh and Michael worked in decentralized social networking protocol development + privacy-preserving contact tracing (Wolk), mobile advertising real-time bidding algorithm design and analytics
(CrossChannel/MdotM). Sourabh has founded social + web advertising startups (Social Media Networks) in the SF Bay and spent time doing computational cognitive science and machine vision research at MIT. Michael hails from UC Berkeley.  In the last year, Colorful Notion has worked closely with Parity Data on substrate-etl, many parachains with XCM GAR, and with many substrate parachains on polkaholic.io.  Colorful Notion is a member of Astar's dapps staking Program.

### Team Code Repos

[Colorful Notion](https://github.com/colorfulnotion)
* [polkaholic](https://github.com/colorfulnotion/polkaholic)
* [substrate-etl](https://github.com/colorfulnotion/substrate-etl)

## Development Status :open_book:

ChainIDE is actively completing the following Chain-Related functionality:
* Astar Collator Node Sandbox
* Swanky Sandbox (Swanky Suite) & EVM Sandbox
* "One-click Start" of the Swanky Node Sandbox
* Built-in Wallet (Polkadot{.js}, SubWallet, Math Wallet, Nova Wallet, and Talisman) Plugin
* Wallet Panel (Network Connect，Account Management)
* Contract Deployment Panel
* Deployed Contract Interaction Panel

Colorful Notion has developed Proof-of-Concept WASM Contract Explorer functionality:
* code hash, contract address, contact call Indexing + UI  in polkaholic.io
* regular polling of Sirato Ink Verification Service API https://ink-verifier.sirato.xyz/api/api-docs/
* substrate-etl loading into a _contracts_ dataset, which may be included in Google BigQuery's blockchain-etl 

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):** 2
- **Total Costs:** 120,000 USD Total: 60,000 USD (Colorful Notion), 60,000 USD (ChainIDE)

### Milestone 1 - Integrated ChainIDE + Polkaholic.io WASM Contract Explorer

The goal of this milestone is to have a highly integrated WASM Contract Development environment.
- **Estimated duration:** 3 months (concluding July/August 2023)
- **FTE:**  2
- **Costs:**  120,000 USD Total: 60,000 USD (Colorful Notion), 60,000 USD (ChainIDE)


|  Number | Deliverable               | Specification                                                |
| ------: | ------------------------- | ------------------------------------------------------------ |
| **0a.** | License                   | MIT                                                          |
| **0b.** | Polkaholic Documentation  | Colorful Notion will provide (1) **inline documentation** of the indexing processes; (2) documentation of the WASM Contract APIs to retrieve indexed code hashes, contract addresses, and contract calls; (3) documentation of URL parameters to access the Polkaholic.io by code hash, contract address and extrinsic hash; (4) documentation of URL parameters to access developer + chain dashboards |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
|      1. | Repository                | Additions to Polkaholic.io WASM indexing to poll ChainIDE for newly uploaded ABIs/verified WASM Contracts and decode contract calls |
|      2. | Repository                | Additions to ChainIDE to link to WASM Contract Explorers, specifically Polkaholic.io |

Key integration points:
1. [Colorful Notion] Provide ChainIDE with url endpoints to show the status of any:
(a) code hash – [example](https://polkaholic.io/wasmcode/0x608fa39ebbdfcee274fcaf23d7bc2d08b8c69d07ca842721edc03388ad9b782e)
(b) contract address [example](https://polkaholic.io/account/5EqUn3aSBdCsyyEcYfAMKQg45cirj9L9pKEDWs2kCzeJAmXu?group=overview&chainfilters=all)
(c) contract call [example](https://polkaholic.io/tx/0xb952286cb2dc342fe6db4cb9e24a7084b274cd759b0750f6de95905f19f131d7)
2. [ChainIDE] After uploading and Deploying Code (which will generate a new code hash) and/or a new Contract (which will generate a new Contract Address), the developer will be asked whether they wish to (a) share the ABI/metadata (b) have their code verified and submitted for open source.  After obtaining, they may link to the Polkaholic.io code hash or contract address endpoint

<img src="https://cdn.polkaholic.io/screenshots/chainide-wasmcontract0.png"/>

3. [Colorful Notion] Colorful Notion will provide an endpoint covering the 2 POST and 4 GET calls of https://ink-verifier.sirato.xyz/api/api-docs/.  Colorful Notion will develop the API endpoint and provide test cases to ChainIDE. 

4. [ChainIDE] ChainIDE will use test cases to post user’s contract-related data, specifically:
* ABI + metadata via /upload/{network}/{codeHash} 
* verified source code via /verify/{network}/{codeHash}

5. [ChainIDE] When users submit a contract call extrinsic, a link to the contract call will take them to the Polkaholic.io using the extrinsicHash generated, which will show a fully decoded contract call.

<img src="https://cdn.polkaholic.io/screenshots/chainide-wasmcontract1.png"/>

6. [Colorful Notion] Provide ChainIDE with a WASM Developer dashboard, which when provided an address, shows all code hashes, contract addresses, and contract calls made by that address.

7. [ChainIDE] ChainIDE will include an iframe including the WASM Developer dashboard, or directly link to the dashboard using the developers wallet address; this can be used to link any developer dashboard.

## Future Milestones

### Support for Development Chains + Solo chains: API, substrate-etl

The goal of this milestone is to support WASM Contract developers using ChainIDE in context.  It is expected that this will range from developers just learning the basics of WASM Contract with simple contracts (flipper) to highly experienced developers pushing the boundaries of what is possible with WASM (e.g. lending protocols).

WASM developers generally deploy on a no-cost testnet such as Shibuya and Rococo Contracts before deploying to a production chain such as Astar and Aleph Zero.  While Colorful Notion has indexed production chains Astar + Shiden (as well), it has not indexed testnet chains or solo chains.  Indexing of production chains is to be covered through a substrate-etl bounty covering Polkadot + Kusama parachains.  In addition, it is expected that many new WASM Contract developers will need technical support in understanding WASM Contracts generally and WASM Contract Development within ChainIDE and how operations appear within Polkaholic.io specifically.  For this support, ChainIDE and Colorful Notion would like to support adequately with education and debugging assistance within Telegram channels, Matrix channels, and Discord channels as deemed appropriate by the curators.  

Colorful Notion & ChainIDE expect to request 30,000 USD per chain to cover 6 months ($5K USD/mo), shared equally between the two teams to support 3 different development-oriented chains:
* Shibuya [testnet]
* Rococo Contracts [testnet]
* Aleph Zero [solo chain + testnet]
It is expected that production chains will not need anywhere near the level of support that developers on testnets need; indexing for Polkadot+Kusama chains will be covered by a Polkadot Treasury grant.

To support developers after Milestone 1, Colorful Notion will operate a dedicated Polkaholic Matrix room, ChainIDE will operate a Discord channel.

### EVM + WASM Contract Integration and XCM Extensions

WASM Contracts are considered the future of smart contracts.  However, because EVM smart contracts currently dominate the entire, it is clear that for WASM Contract Development to gain adoption, interfaces with EVM Contracts are being developed, which are actively being worked on by the Astar team with swanky+XVM.  In addition, to support chain interoperability, it is extremely likely that EVM+WASM Contracts will need to link to XCM Messages by message hash, Extrinsics + Calls involving XCM by extrinsic hash or transaction hash.  Both the ChainIDE and Colorful Notion team are well suited to support future integrations between EVM + WASM + XCM-enabled Contracts.

### Additional Substrate Chains + Testnets

With a successful WASM contract development ecosystem, it is hoped that additional Substrate chains will follow Astar, Aleph Zero and others in deploying the _contracts_ pallet in their parachains.  Each new parachain would bring on a new set of WASM Contract developers to support and educate, and our teams hope to be able to support them in the same way.  If new testnets emerge in the Substrate ecosystem with entirely new WASM Contract Developers, both teams would expect to be able to support them in the same way.

### Support for additional WASM Contract Explorers and IDEs

The interfaces between ChainIDE and Polkaholic.io are modular in nature.

ChainIDE may link to other WASM Contract Explorers with URLs and iframes in very similar ways.

Polkaholic.io’s interface will be able to support other WASM IDEs in very similar ways, including additional verifiers (e.g. Sirato).


## Additional Information :heavy_plus_sign:

The Inkubator Bounty Program was recommended by Maarten Henskens, Sota Watanabe + Toma of Astar team.
