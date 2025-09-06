# Indexing Co

- **Team Name:** The Indexing Company
- **Payment Address:** 145jCYEs2uY5jzUR1BBtNyMd936gjT7Eg17JanN5JP3TLLW5

## Project Overview :page_facing_up:
### Overview

Indexing Co proposes to further improve the Ink! ecosystem by deploying The Neighborhood, a high-performance, chain-agnostic indexing and ETL (Extract, Transform, Load) solution, alongside onchain payment systems and production-grade protocol templates. Our project will enable developers and chains within the Polkadot ecosystem to access scalable, low-latency blockchain data processing, seamless payment mechanisms using Ink! smart contracts, and customizable templates for DeFi and NFT protocols. Built with Ink! v6.X, our solution will showcase the language’s flexibility and RISC-V compatibility, driving adoption and innovation in the Polkadot network.

#### Key Objectives
1. Chain Onboarding with The Neighborhood: Deliver a distributed, horizontally scalable indexing solution optimized for real-time blockchain data streaming and transformation, tailored for Ink.
2. Onchain Payments: Implement a payment system using Ink! smart contracts, allowing data consumers to pay for indexing services for stablecoins.
3. Protocol Templates: Develop open-source, production-grade indexing templates for Ink!-based DeFi and NFT protocols, including DEXs, money markets, and token analytics.

### Ink! Ecosystem Impact

#### Why Ink!?

Ink! is ideal for this project due to its:

- RISC-V Compatibility: Enables efficient execution of complex data processing logic
- Polkadot Integration: Leverages Polkadot’s shared security and interoperability for Dapp development
- Developer-Friendly Syntax: Simplifies smart contract development for payment systems and event decoding, outperforming Solidity in modularity and gas efficiency
- Open-Source Ecosystem: Aligns with our commitment to open-source templates and tools

#### Impact on Ink! Ecosystem

- Developer Adoption: Our indexing solution and templates will lower the barrier for developers building Ink!-based Dapps, showcasing Ink!’s advantages over EVM-based languages
- Scalability: The Neighborhood’s horizontal scalability will support high-throughput Ink! chains, driving ecosystem growth
- Economic Activity: Onchain payments will create a sustainable model for data services, incentivizing further Ink! development
- Community Resources: Open-source templates will serve as a foundation for future Ink! projects, fostering innovation in DeFi, NFTs, and analytics
- Co-Marketing:  We will collaborate with Ink! to drive adoption this data product and thus interest in Ink!, through:
- Amplification of the product launches through official channels from both Indexing Co and Ink! directed at the developer community. We will also create case studies with developers in the form of tweet threads or articles, to showcase our success.
- Opportunity to showcase the data product in developer-focused streams or workshops and inclusion in developer docs.
Introductions to active builder teams within the Ink! ecosystem, especially the teams who work on applications that are data-intensive or new applications.

### Project Details

#### Problem Statement

Modern blockchain ecosystems, including Polkadot and Ink, demand robust indexing solutions to handle high-throughput, low-latency data processing. Existing solutions like GraphQL subgraphs or hosted APIs are rigid, break under chain reorganizations, require costly infrastructure maintenance, and struggle with scalability. Additionally, developers lack accessible payment systems for data services and reusable templates for protocol-specific analytics, hindering adoption of Ink! for scalable dApps.

#### Proposed Solution

Indexing Co’s solution leverages The Neighborhood, a streaming ETL pipeline, to address these challenges:

- High-Performance Indexing: The Neighborhood is a distributed data processing network that streams and transforms blockchain data in real time. It is chain-agnostic, programmable in JavaScript, and supports streaming to databases like Postgres, BigQuery, or data cues like Kafka. For Ink!, we will adapt The Neighborhood to process data from Ink! smart contracts, leveraging Ink! v6.X’s RISC-V compatibility for optimized performance
- Onchain Payments: We will deploy Ink! smart contracts to enable data consumers (e.g., developers, analytics platforms) to pay for indexing services using stablecoins native to Ink. The payment system will be secure, transparent, and integrated with The Neighborhood’s API
- Protocol Templates: We will create open-source indexing templates for Ink!-based protocols, including:
- DEXs: Templates for Uniswap-like or chain-native DEXs, with transformations for swap events and liquidity pools
- Money Markets: Templates for Aave-like or chain-native lending protocols, covering borrowing and lending analytics
- NFT Activity: Templates for tracking NFT mints, transfers, and marketplace activity
- Token and Stablecoin Analytics: Templates for token-specific metrics and stablecoin transaction tracking. Each template includes ready-to-deploy transformations, preset filters, SQL schema files, and integration examples, all built with Ink! smart contracts for event decoding and data formatting

#### Technical Approach

- The Neighborhood on Ink!: We will integrate The Neighborhood’s streaming ETL pipeline with Ink! v6.X smart contracts to decode and process blockchain events. The pipeline will use JavaScript for programmable transformations and support parallelized data processing for scalability
- Onchain Payments: Ink! smart contracts will manage payment logic, with functions for subscription-based access to indexing services. The contracts will handle token transfers (stablecoins) and emit events for payment tracking
- Protocol Templates: Templates will be implemented as JavaScript transformation scripts, open-sourced under Apache 2.0. Each template will include documentation, SQL schemas, and example integrations (e.g., streaming to Postgres or webhooks)
- Testing and Deployment: We will deploy a testnet version on a Polkadot parachain supporting Ink! (e.g., Astar or Moonbeam’s Ink! environment) to validate performance under real-world conditions.


## Team :busts_in_silhouette:

### Contact

- **Contact Name:** Dennis Verstappen
- **Contact Email:** dennis@indexing.co
- **Website:** https://www.indexing.co

### Team members

- **Brock Haugen, CEO:** Brock is a long-time engineer with a degree in Mathematics, now co-founder. He’s spent the last 7 years leading engineering and indexing efforts for products and infrastructure in the web3 space for companies such as Coinbase and Dappcentral. [LinkedIn](https://www.linkedin.com/in/brockhaugen/)
- **Jake Horn, CPO:** Jake is a product designer and startup founder with over a decade of experience building and scaling digital products. Before co-founding Indexing Co., he was the Design Director at R/GA and co-founder of Tripgrid, where he now serves as a board member. At Indexing Co., Jake leads product and branding, bringing a human-centered approach to developer infrastructure. His belief is that the best products come from teams that feel supported, trusted, and connected, a philosophy he brings to both design and leadership. [LinkedIn](https://www.linkedin.com/in/hornjake/)
- **Dennis Verstappen, Head of Research:** Dennis is a data analyst with a passion for making data actionable. Been in crypto since 2017 where he gained experience with trading, DeFi, venture capital. Dennis worked with various projects on product development, analytics, tokenomics and marketing. [LinkedIn](https://www.linkedin.com/in/dennis-verstappen-57aa10101/)
- **Lazaro Vilches, Head of Business Development:** Laz, bringing 4yrs of experience in scaling ecosystems in Web3. He has been able to identify data related challenges faced by teams. [LinkedIn](https://www.linkedin.com/in/lazaro-vilches-38536a214/)

### Legal Structure

- **Registered Address:** 921 Topaz Ln, Oak Point, TX 75068, USA
- **Registered Legal Entity:** The Indexing Company

### Team's experience

A group of experienced blockchain developers and data engineers from [Indexing Co](https://www.indexing.co/), with expertise in building The Neighborhood and indexing solutions for EVM, Solana, and Move-based chains.

Indexing Co has processing petabytes of blockchain data with sub-second latency for customers across web3 including: Mesh Connect, Delegate, Coridal Systems, Once Upon, RPS Labs, ... and many more.

### Team Code Repos

https://github.com/indexing-co
https://github.com/runninyeti

### Team LinkedIn Profiles (if available)

- [LinkedIn](https://www.linkedin.com/in/brockhaugen/)
- [LinkedIn](https://www.linkedin.com/in/hornjake/)
- [LinkedIn](https://www.linkedin.com/in/dennis-verstappen-57aa10101/)
- [LinkedIn](https://www.linkedin.com/in/lazaro-vilches-38536a214/)

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 4 months
- **Full-Time Equivalent (FTE):** 2
- **Total Costs:** $50,000 USD

### Budget and Funding

Total Funding Requested: $50,000

Breakdown:
- Development (60%): $30,000 for smart contract development, The Neighborhood integration, and template creation (4 months).
- Testing and Deployment (20%): $10,000 for testnet deployment, performance optimization, and handling chain reorganizations.
- Documentation and Community Support (15%): $7,500 for comprehensive documentation, tutorials, and Polkadot Forum updates.
- Contingency (5%): $2,500 for unforeseen expenses (e.g., additional testnet resources).

Funding Schedule:
- Milestone 1 (30%): $20,000 upon approval, for initial smart contract development and The Neighborhood integration (Month 1).
- Milestone 2 (40%): $20,000 upon testnet deployment and first template release (Month 3).
- Milestone 3 (30%): $10,000 upon final delivery of all templates, payment system, and documentation (Month 4).

### Milestones and Timeline

Duration: 4 months

**Milestone 1 (Month 1):** Develop Ink! smart contracts for payment system and event decoding; integrate The Neighborhood’s ETL pipeline.

**Milestone 2 (Months 2-3):** Deploy testnet version on an Ink!-compatible parachain; release DEX and money market templates; validate performance under reorgs.

**Milestone 3 (Month 4):** Finalize templates; complete onchain payment system; publish documentation and Polkadot Forum updates.

### Post-Grant Maintenance

- Ongoing Support: Indexing Co will maintain The Neighborhood’s Ink! integration and templates for at least 12 months post-grant, providing bug fixes and updates for Ink! v6.X compatibility.
- Community Engagement: We will post monthly updates on the Polkadot Forum, host a developer workshop on Ink! indexing, and open-source all code under Apache 2.0.
- Sustainability: The onchain payment system will generate revenue to fund ongoing maintenance, ensuring long-term viability.

### Additional Information

- Open-Source Commitment: All code, including smart contracts, templates, and transformation scripts, will be open-sourced under Apache 2.0, hosted on Indexing Co’s GitHub (https://github.com/Indexing Co).
- Polkadot Forum Updates: We will post regular progress updates at https://forum.polkadot.network/, tagged with [Ink! Ecosystem Grant].
- Contact for Queries: Reach us at hello@indexing.co or via X (@Indexing Co).

### Compliance with Guidelines

- Ink! Version: All smart contracts will use Ink! v6.X, ensuring RISC-V compatibility.
- License: Apache 2.0 for the smart contract code and templates.
- Exclusions: The project avoids gambling, illicit activities, or token sales, focusing on infrastructure and developer tools.
- Uniqueness: Unlike EVM-based indexing solutions (e.g., The Graph), our solution is optimized for Ink! and Polkadot’s unique architecture, offering streaming ETL and programmable templates.
