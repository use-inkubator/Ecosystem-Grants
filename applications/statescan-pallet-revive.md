# Statescan pallet revive explorer integration

- **Team Name:** OpenSquare
- **Payment Address:** 12sNU8BXivMj1xQmcd4T39ugCyHjmhir8jkPqfAw5ZDESrx4

## Project Overview :page_facing_up:

### Overview

[Statescan](https://www.statescan.io/) is a blockchain explorer designed for substrate based chains. It provides a data
indexing solution and a user-friendly interface to query and analyze on-chain data, including basic data blocks,
extrinsics, events, accounts and transfers. It also integrated customized business for pallets including assets,
identity, multisig, proxy, etc.

We propose to implement pallet [revive](https://github.com/paritytech/polkadot-sdk/tree/master/substrate/frame/revive)
business data indexing and visualization. It will help users to track contract code info, lifecycle and call records.

### Project Details

Blockchain don't store history state in its key value database. It's hard for users to track whole lifecycle and history
state of various business and this is the reason why we need explorers. In this integration we will do following work:

1. Data indexing. We will develop a new package
   under [statescan backend](https://github.com/opensquare-network/statescan-v2/tree/main/backend/packages). Scripts
   will scan every history block, extract pallet revive related business data and save them to database.
2. Graphql API. New data schema will be defined
   under [statescan graphql-server](https://github.com/opensquare-network/statescan-v2/tree/main/backend/packages/graphql-server)
   and related resolvers will be implemented for data query.
3. Fronted pages. These pages will show code info, lifecycle, contract initializations, contract detail, call
   records and call detail.

## Team :busts_in_silhouette:

### Team members

- [Yongfeng Li](https://github.com/wliyongfeng), founder and developer of OpenSquare.
- [Chaojun Huang](https://github.com/hyifeng), developer of OpenSquare.
- [Yihan Fan](https://github.com/Popoulosss), designer of OpenSquare.
- [Leo Chen](https://github.com/leocs2417), developer of OpenSquare.
- [wolyshaw](https://github.com/wolyshaw), developer of OpenSquare.

### Contact

- **Contact Name:** Yongfeng Li
- **Contact Email:** yongfeng@opensquare.network
- **Website:** https://www.statescan.io/

### Legal Structure

- **Registered Address:** Room 4310, building No.3, West Tianmushan Road, Hangzhou City, China
- **Registered Legal Entity:** Lianzheng Technologies Ltd.

### Team's experience

OpenSquare team is a group of developers and designers, found in 2020. Our team is dedicated in the polkadot ecosystem
over 5 years. We are developing infrastructures to help users understand various polkadot on-chain business. Our
products include [subsquare](https://subsquare.io/), [dotreasury](https://www.dotreasury.com/),
[off-chain voting](https://voting.opensquare.io/) and [statescan](https://www.statescan.io/). Generally we index basic
on-chain data, extract and normalize them to business friendly data, and finally show them in fronted pages which will
help users learn polkadot and do interactions.

### Team Code Repos

https://github.com/opensquare-network/statescan-v2

Team member github links are available on the team members section.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 1 month
- **Full-Time Equivalent (FTE):**  4
- **Total Costs:** 40,000 USD

|  Number | Deliverable                         | Specification                                                                                                                                                                                                                                                  |
|--------:|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                             | Apache 2.0 / MIT                                                                                                                                                                                                                                               |
| **0b.** | Documentation                       | We will provide both inline documentation of the code and a basic tutorial for developers to setup the project.                                                                                                                                                |
| **0c.** | Testing and Testing Guide           | Core functions in the indexing scripts will be covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests.                                                                                            |
|      1. | A package to indexing pallet revive | It will scan every block of a substrate based chain, and extract contract related business data and save them to MongoDB, and code will be under [statescan-v2/backend](https://github.com/opensquare-network/statescan-v2/tree/main/backend/packages) folder. |
|      2. | Graphql API                         | It will provide data query including contract code detail/list, contract instantiate records, contract detail and contract call records.                                                                                                                       |
|      2. | Fronted pages                       | Fronted pages will cover code list, lifecycle, contract detail and call records.                                                                                                                                                                               |

## Future Plans

Since this integration is our 1st proposal about contract integration, it includes basic workflow of pallet revive. Our
future plan includes contract verification, interaction(state query and function call), solidity support and !ink
specific requirements.
