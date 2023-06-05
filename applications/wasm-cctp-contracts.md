# WASM CCTP Contracts

- **Team Name:** Colorful Notion
- **Payment Address:** Colorful Notion [121Rs6fKm8nguHnvPfG1Cq3ctFuNAVZGRmghwkJwHpKxKjbx](https://polkaholic.io/account/DakP5k8XiY9DQbrCj23xdaUBEBxGrpJoenyB7bYDXWvtZbN?group=overview&chainfilters=all)
- **[Level](https://github.com/w3f/Grants-Program/tree/master#level_slider-levels):** 3

## Project Overview :page_facing_up:

[Cross-Chain Transfer Protocol (CCTP)](https://developers.circle.com/stablecoin/docs) is a permissionless on-chain utility developed by [Circle](https://circle.com) (issuer of Stablecoin USDC).  In CCTP's "lock-and-mint" pattern, the user burns one token (eg. native USDC) on a source chain, causing an issuer (after observing an attestation) to mint the same token (eg. native USDC) of the same amount on a destination chain.  This is in contrast to the "lock-and-mint" pattern that results in "wrapped assets" (WETH, WBTC, ...) because CCTP depends on centralized issuer trusting one or more attesters.  To date, CCTP has only been used on 2 EVM Chains with USDC ([Ethereum - $27B](https://etherscan.io/token/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48) and [Avalanche $0.4B](https://snowtrace.io/token/0xB97EF9Ef8734C71904D8002F8b6Bc66Dd9c48a6E)) to transfer USDC between using EVM Contracts ([demo video](https://www.youtube.com/watch?v=UHP4ZxC83CA)).  However, the CCTP protocol can be extended to other smart contract systems (ink! WASM, Stellar, Cosmos WASM) and other tokens types: PSP-22, TRC-20 which can represent the underlying in different ways.

This proposal is about Colorful Notion extending the [CCTP EVM Contracts](https://github.com/circlefin/evm-cctp-contracts)
to WASM Contracts + PSP-22 tokens natural to the Substrate ecosystem.

The core generalization envisioned is:

1. Token A (ERC-20 or PSP-22) is burned on the source chain: Using an
app, a user initiates a transfer of A from one chain to another, and
specifies the recipient wallet address on the destination chain.  The
app facilitates a burn of the specified amount of Token A on the
source chain.

2. A _signed attestation_ is fetched from Colorful Notion (the
"Attester"), who attests to the burn event on the source chain.  The
app requests the attestation from Colorful Notion's multichain
indexing, which provides authorization to mint the specified amount of
Token A on the destination chain.

3. Token A (ERC-20 or PSP-22) is minted on the destination chain: The
app uses the attestation to trigger the minting of Token A.  The
specified amount of Token A is minted on the destination chain and
sent to the recipient wallet address.

In no case are assets "locked" -- instead a centralized issuer of the token is responsible for minting in response to  one or more attesters reporting on a "BurnMessage" being finalized.  In Circle's CCTP case of USCD, Circle are both the attester and the centralized issuer of USDC.  However, we believe we can separate the attester and issuer roles, where the issuers are other ERC-20s (USDT, DAI), PSP-22s, or other native asset types standing in the same relationship.

In particular, we envision this CCTP pattern to be high impact for 2 core use cases:

* Stablecoin issuers -- specifically USDC and USDT -- will be able to use the "burn-and-mint" pattern between EVM Chains and Substrate chains with the "contracts" pallet using the WASM CCTP Contracts.   We believe stablecoin issuers will prefer the simplicity of mint-and-burn of CCTP (invented by Circle) implemented in WASM Contracts over the alienness/complexity of XCM remote execution with keyless accounts, which to date are not widely used, not even within the Substrate ecosystem, and require exceptional cognitive load for both users and developers alike to reason about.  

* ERC-20 Issuers on Ethereum L1/L2 Chains.  Ethereum has high transaction costs, but many ERC-20 tokens are issued there and need to be moved across to L2 chains.  We believe many ERC-20 issuers can benefit from much of the quality block space in the Substrate ecosystem, along with its many innovations.

The industry is poised for L2 Chains to take on the transaction volume that has been become too expensive / congested to run on Ethereum alone or just designed out at the L1 chain (Polkadot) altogether.   Many new defi projects are running their projects on multiple chains systematically, many users will use these projects in multiple chains systematically, many token issuers will wish to ensure their tokens can transfer.   With CCTP EVM contracts and WASM contracts living on Ethereum and other EVM chains (Avalanche, Solana, ...) and their L2s (Polygon, Arbitrum), the above centralized issuers can eliminate all the complexity of managing "wrapped" token and support multi-chain transfers in a new way

We propose to translate CCTP EVM Contracts to ink! WASM Contracts using [PSP-22](https://github.com/w3f/PSPs/blob/master/PSPs/psp-22.md), enabling 3 cases:
* 1. User (a) burns PSP-22 tokens on a Substrate chain (e.g. Shiden) and (b) mints PSP-22 tokens in a Substrate chain (e.g. Pendulum)
* 2. User (a) burns PSP-22 tokens on a Substrate chain (e.g. Pendulum) and (b) mints ERC-20 tokens in an EVM Chain (eg Ethereum)
* 3. User (a) burns ERC-20 tokens on a EVM chain (e.g. Ethereum) and (b) mints PSP-22 tokens in a Substrate chain (eg Astar).

In the above cases, a single centralized issuer is common to the underlying PSP-22 and ERC-20 token.  In _none_ of the above cases is there a shared relay chain, nor is there an open channel, nor is XCM used. The security rest on a trusted centralized issuer relying on one or more attesters, who share proofs with the issuer that an event occurred.  This can be decentralized in the future with BLS signatures but is not the scope of this work here.

The same cross-chain use cases Circle envisions with USDC applies to any ERC-20 token:
* Cross-chain swaps:  Any ERC-20/PSP-22 on any EVM/Substrate Chain can cross-chain swaps with digital assets that live on distinct chains (e.g. swapping X ERC-20 on an EVM Chain for Y PSP-22 on a Substrate Chain).   In a completely automated way, X can be swapped for Y on an EVM Chain (Ethereum, Arbitrum or Avalanche), routed by CCTP to a Substrate chain (Astar or Pendulum or Aleph), and swapped for Z.  Routing and execution are hidden from the user to deliver a seamless user experience.
* Cross-chain deposits:  Users can utilize X on Ethereum to open a position on a decentralized exchange on a Substrate exchange.  Because CCTP can route X across chains behind the scenes, the user never needs to switch wallets or even think about which chain they’re holding X on.  A registry like XCM Asset Registry can hold the mapping between ERC-20 and PSP-22 tokens.
* Cross-chain NFT purchases.  A user with X on a Substrate/EVM Chain can buy an NFT on *-swap and list it for sale on an NFT Marketplace. When the user initiates a transaction from their Substrate wallet, CCTP routes their X from one Substrate/EVM to another Substrate/EVM to purchase the NFT from Uniswap, then opens the listing on OpenSea.

### Project Details:  Core Deliverables

The core work pursued is to translate Circle's CCTP EVM Contract into
ink! WASM Contracts with PSP-22 being taking the place of ERC-20.  To
the fullest extent possible, we will make it compatible with ERC-20
tokens and the message format.  

Core deliverables:
1. [Milestone 1] CCTP WASM Contracts and Testing: written in Rust and ink! based on [OpenBrush](https://learn.brushfam.io/docs/openbrush)
2. [Milestone 1] Node.js will be used to index EVM and Substrate cains, listening to CCTP messages, recording attestations that may be queried by message hash
3. [Milestone 2] Node.js will be used to develop a CCTP UI + support a CCTP Asset registry component generalization 
4. [Milestone 2] Documentation on how to use and participate in the system for the core roles of CCTP: the issuers, the attester, CCTP 

All deliverables will be open-source (Apache 2.0 License).

#### CCTP WASM Contracts

The basic research and protocol development has been done by Circle with [CCTP EVM Contracts](https://github.com/circlefin/evm-cctp-contracts), including an [Chainsecurity audit](https://chainsecurity.com/security-audit/circle-cross-chain-transfer-protocol-cctp/).

Our ability to do a WASM Contract "port" is enabled by [OpenBrush](https://learn.brushfam.io/docs/openbrush) and may be simplified with [sol2ink](https://github.com/Supercolony-net/sol2ink).  Colorful Notion will make best efforts to develop WASM Contracts that are production-grade, but there is not a wide body of knowledge of WASM Contracts yet to make them production-grade secure.  Between Milestone 1 and 2 we request an audit process, supported by the [inkubator program](https://github.com/use-inkubator/Ecosystem-Grants).

In addition, the EVM Contract implementation contemplates multiple
attesters coming together with BLS.  To our knowledge, this is not possible within the
ink! environment and will not be attempted.

Specific choices to generalize the messages to fit within the Polkadot
ecosystem (represent destination and ERC-20 and PSP-22 assets) will be
made and documented in Milestone 2.  We will make best efforts to be
compatible with Circle's CCTP message format.

#### CCTP EVM/WASM Contract Indexing and Attestation  API

CCTP Contracts emit Burn messages, which generate attestations.

We will deliver standalone indexing code, that given an RPC Endpoint for WASM CCTP Contracts and EVM CCTP Contracts records them in MySQL by `messageHash`.

Given this index a simple API endpoint of:
```
https://api.polkaholic.io/attestations/:messageHash
```
can be exposed, matching [Circle's Attestation API](https://developers.circle.com/stablecoin/reference/getattestation).

#### CCTP UI + CCTP Asset Registry

A standalone basic UI matching that of [Circle's demo video](https://www.youtube.com/watch?v=UHP4ZxC83CA) will be developed using Node.js and Express.

This may be used as a foundation for other teams to utilize in their dapps/defi projects.

We will add the ability add mappings between ERC-20 and PSP-22 assets to [XCM Global Asset Registry](https://github.com/colorfulnotion/xcm-global-registry) (XCM GAR) in Milestone 2.  

#### Documentation

To support use of CCTP by multiple blockchain ecosystems (WASM Contracts, parachain defi, ERC-20 issuers generally), we will provide documentation for all core deliverables in standalone
* Standalone WASM CCTP Contracts (for auditors, other WASM Contract developers)
* Deployment/Test script for WASM Contract, Test Script for ERC-20 + PSP-22 (for auditors, other WASM Contract developers)
* Standalone CCTP UI (as a user and developer)
* How to add assets to XCM GAR (for ERC-20/PSP-22 issuers and Substrate parachain teams with EVM+WASM Contracts)
* article/blog post introducing WASM CCTP Contracts and the CCTP UI (for blockchain engineers genearlly)

### Ecosystem Fit

#### Overview

CCTP is well suited for the Substrate ecosystem for several reasons:
- The WASM Contracts ecosystem would benefit from an influx of PSP-22 "twins" of ERC-20 tokens coming in from other ecosystems.  Many other Substrate chains, especially those with defi capabilities, may wish to add the "contracts" pallet to their chain to attract issuers.
- Specifically, the Substrate ecosystem needs liquidity from stablecoins (USDC, USDT) for defi parachains to achieve maximal potential.  In particular, Circle will may see CCTP WASM Contracts as a tighter fit to their stack within the Substrate ecosystem than XCM, and Tether/Bitfinex may wish to match Circle's CCTP in a comprehensive Substrate+EVM solution.  Other stablecoins and multichain blockchain projects may follow suit. 
- Many people have grown distrustful of the lock-and-mint pattern given the bridge hacks, and may reason that CCTP that is more suitable to them than other efforts.  This is not an either-or pattern -- WETH and WBTC _must_ continue to use the lock-and-mint pattern.  

#### Target CCTP Users

Target users of CCTP Contracts would be:
- Issuers: ERC-20 tokens, Stablecoins can increase their multichain footprint by enabling more uses of their tokens and Stablecoin
- Defi Users: people and institutions who wish to move assets between chains without the complexity of wrapped assets, XCM remote execution
- Defi Projects: projects who wish to support defi users across EVM L2  chains and Substrate parachains will find it extremely easy to reason about CCTP, especially given the importance of USDC (using CCTP).
- Substrate chains/parachains: Standalone chains (e.g. Aleph) win a new bridge option.   Polkadot/Kusama parachains who do not otherwise think of their chain as being a developer platform may be amenable to having PSP-22 assets appear to generate fees for their chain.

#### Similar projects

CCTP EVM Contracts are already on Ethereum and Avalanche, and can be
expected on other EVM chains (BSC, Tron).  We are not aware of CCTP
implementations of Substrate WASM Contracts, but it may be possible
Cosmos, Stellar or smart contract platform development teams are
working on similar efforts for other token types.

[Forta](https://explorer.forta.network/) monitors EVM contract events,
which may be used as source of attestations for CCTP Contracts.

#### Risks

- Centralized bridge solutions like CCTP reduce the risk of due to
software errors since there is no locking of assets.  Instead, there
is a risk that the central issuer can be regulated into censoring
burn-and-mint operations.  The degree to which popular ERC-20
stablecoins are decentralized is thrown into question.

- RPC manipulation risk - attesters require RPC services to retrieve
data from blockchains.  If someone manages to manipulate RPC data,
attestations can be blocked. A potential mitigation could be to
introduce connections to multiple RPCs simultaneously.

- Overdependence on single attestor.  This risk can be reduced.   The CCTP EVM Contracts contemplate
having a BLS scheme to support [EVM now](https://hackmd.io/@liangcc/bls-solidity) and this can added into [Substrate
soon](https://wiki.polkadot.network/docs/learn-cryptography#are-bls-signatures-used-in-polkadot)).
Then, both EVM+WASM contracts could  have a process wherein the issuer can approve a set of independent
valid attestors to write a BLS aggregated signature.

## Team :busts_in_silhouette:

### Team

Colorful Notion is a multichain analytics company focused on L1/L2
Substrate+EVM Chains and bridges.  Founded in 2021, our approach has
been heavily guided by Substrate's numerous key innovations (XCM,
WASM+EVM) which we embed in our key projects Polkaholic.io, XCMGAR and
Substrate-etl, which aim to be funded by Polkadot Data Alliance Bounty.

### Contact

- **Contact Name:** Sourabh Niyogi
- **Contact Email:** sourabh@colorfulnotion.com
- **Website:** https://colorfulnotion.com/

### Legal Structure

- **Registered Address:** 55 E Third Ave San Mateo CA 94401
- **Registered Legal Entity:** Colorful Notion, Inc.

### Team's experience

Colorful Notion is led by Sourabh Niyogi and Michael Chung who have
been active in blockchain engineering since 2017.  Key engineers
Sourabh Niyogi and Michael Chung have developed Polkaholic.io since
Fall 2021.  Prior to building Polkaholic.io, Sourabh and Michael worked
in decentralized social networking protocol development +
privacy-preserving contact tracing (Wolk), mobile advertising
real-time bidding algorithm design and analytics
(CrossChannel/MdotM). Sourabh has founded social + web advertising
startups (Social Media Networks) in the SF Bay and spent time doing
computational cognitive science and machine vision research at
MIT. Michael hails from UC Berkeley.  In the last year, Colorful
Notion has worked closely with Parity Data on substrate-etl, many
parachains with XCM GAR, and with many substrate parachains on
polkaholic.io.  Colorful Notion is a member of Astar's dapps staking
Program.


### Team Code Repos

[Colorful Notion](https://github.com/colorfulnotion)
* [polkaholic](https://github.com/colorfulnotion/polkaholic) - a multichain block explorer supporting the Substrate ecosystem
* [substrate-etl](https://github.com/colorfulnotion/substrate-etl) - an index of Polkaholic, onboarded to Google BigQuery public datasets
* [XCM GAR](https://github.com/colorfulnotion/xcm-global-registry) - an index of all XCM assets in the ecosystem

## Development Status :open_book:

Colorful Notion has developed Proof-of-Concept WASM Contract Explorer
functionality: * code hash, contract address, contact call Indexing +
UI in polkaholic.io * regular polling of Sirato Ink Verification
Service API https://ink-verifier.sirato.xyz/api/api-docs/ *
substrate-etl loading into a _contracts_ dataset, which may be
included in Google BigQuery's blockchain-etl and is improving this
with [ChainIDE](https://chainide.com/), a leading Cloud-Based
Multi-Chain IDE in the context [ChainIDE + Polkaholic.io WASM Contract
Explorer Integration](https://github.com/use-inkubator/Ecosystem-Grants/blob/master/applications/chainide-polkaholic-integrated-wasm-contract-explorer-integration.md).  We propose to develop WASM Contracts ("eat the dog food") in the context of this integration.

Our interest in CCTP has been developed through the above, highly
informed by our XCM Indexing work on
[polkaholic.io](https://github.com/colorfulnotion/polkaholic), [XCM
GAR](https://github.com/colorfulnotion/xcm-global-registry).

We have studied CCTP EVM Contracts and learned about OpenBrush and
deployed a small number of test contracts and have deep knowledge of
smart contracts from Substrate indexing.  We have not engaged
in a production grade WASM Contract system and welcome collaborators
to ensure our success.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 5.0 months
- **Full-Time Equivalent (FTE):** 800 hours
- **Total Costs:** 90,000 USD

### Milestone 1 - Core WASM Contract Functionality

- **Estimated duration:** 2.5-3 months
- **FTE:**  500 hours
- **Costs:** 50,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide  **inline documentation** of the WASM Contracts code. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure CCTP functionality for WASM Contracts will be developed. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that introduces the CCTP WASM Contracts. |
| 1. | WASM Contracts Core | We will develop audit-ready WASM CCTP Contracts. |
| 2. | CCTP Indexer + Attestation API | Standalone  |

We will build a complete translation (but with one, not multiple attestors) of the CCTP EVM Contracts, and test them with use 3 parachains that do NOT share a relay chain:
* Rococo Contracts - with CCTP WASM Contracts + a PSP-22 contract
* Shibuya - with CCTP WASM Contracts + a PSP-22 contract
* Moonbase - with CCTP EVM Contracts + a ERC-20 contract

Setup:
* post a ERC-20 to Moonbase and PSP-22 to Rococo and Shibuya.  The token is thus represented on 3 chains in 2 different ways.
* post EVM CCTP Contracts on Moonbase and WASM CCTP Contracts to Rococo and Shibuya, and register the tokens local to the chain within these contracts.
* launch attestation API, which indexes Burn events on the above parachains.

There are 3 channels but 6 possible transfers.

Core test case will test all 6 transfers:
* **Source chain**: `ERC-20` or `PSP-22` contract `approve()` - user approves the `TokenMessenger` contract to transfer a specified amount of the users token
* **Source chain**: `TokenMessenger` contract  `depositForBurn()` - users calls "depositForBurn" to will deposit the users PSP-22 or ERC-20 tokens to the `TokenMessenger` contract, which in turn burns the token, then calls `MessageTransmitter` to pass the message and emit a `MessageSent` event.
* **Attestation**: The signed attestation can be fetched using the message hash from the `MessageSent` event by calling the Colorful Notion Attestation API.
* **Destination chain**: `MessageTransmitter` contract `receiveMessage()` -- Anyone (could be the user) can call this function to mint the PSP-22 or ERC-20 tokens, which are transferred to the address specified in the original  `depositForBurn` function call.

The above will be done solely with a Node.js script for all 6 possible transfers.  The test script will be modelled after [this OpenBrush Typechain transfer example] of Alice and Bob transferring PSP-22 on one chain.  

Dockerfile will contain:
* Open-source (Apache 2.0 License) WASM CCTP + EVM CCTP Contracts 
* Setup / Deployment script to 3 parachains
* Core Test Case
* Testing guide

At the conclusion of this process, we will request feedback from a security audit team who would ideally review
[CCTP EVM Contracts](https://chainsecurity.com/wp-content/uploads/2023/04/Circle-Smart-Contract-Audit-_-Cross-Chain-Transfer-Protocol-CCTP-_-EVM-Bridge-_-ChainSecurity.pdf) and be extremely familiar with OpenBrush and PSP-22.

### Milestone 2 - Basic CCTP UI + XCM GAR Generalization

- **Estimated duration:** 2.5-3 months
- **FTE:**  400 hours
- **Costs:** 40,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **documentation** of the core deliverables from the issuer, CCTP user and attester point of view. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that introduces to the solution with all the guidelines included. |
| 1. | CCTP UI | We will develop a UI to support transfer between any supported chains |
| 2. | XCM GAR Generalization | We will develop a registry for representing ERC-20 and PSP-22 assets across multichain ecosystem, building upon our work in XCMGAR. |
| 3. | Incorporate CCTP Contracts Audit Feedback | We will act on security audit feedback provided. |


A basic CCTP UI will be designed and developed with the same functionality as the [Circle USDC transfer demonstration](https://www.youtube.com/watch?v=UHP4ZxC83CA).

XCM GAR will be used to represent CCTP Assets.

Security audit feedback will be incorporated into the CCTP WASM Contracts and made public.  

Time permitting within the allocated budget after we complete this
audit, we will take the opportunity to deploy CCTP EVM and WASM
Contracts on Ethereum and up to 10 Substrate chains.  We anticipating
1 day per chain.

## Future Plans

Follow on milestones deploying the EVM + WASM Contracts across the
Substrate ecosystem are envisioned.  It is hoped that a high
footprint of CCTP WASM Contracts in Substrate parachains can support a
broader ecosystem with PSP-22 tokens enjoying a serious fraction of
the success of ERC-20 tokens in the EVM ecosystems.

It is believed cross-chain transfer protocols can benefit
decentralized finance projects within Substrate and EVM greatly, and
that Colorful Notion may act as a facilitator, attester with defi projects,
ERC-20 / Stablecoin issuers.  Financial support as an indexer, attester,
or contract fee earner in WASM Contracts and EVM Contracts.

Colorful Notion may connect the Standalone CCTP UI into Polkaholic.io
and to combine it with Dotswap UI and XCM Remote Execution patterns,
which are complementary in nature.

## Additional Information :heavy_plus_sign:

* Colorful Notion is working on [ChainIDE+Polkaholic WASM Contract Development](https://github.com/use-inkubator/Ecosystem-Grants/blob/master/applications/chainide-polkaholic-integrated-wasm-contract-explorer-integration.md) in Summer 2023, which supports WASM Contract development.
* Collaborations with experienced OpenBrush team members are welcome.
* We welcome collaborating on CCTP with other ecosystems on other token types in other smart contracts in a broader view of what a Web3 multichain future.  Interested parties can email info@colorfulnotion.com or find us on Telegram

