# Band Protocol
- **Team Name:** World Data Corporation Foundation (“Band Protocol”)
- **Payment Address:** 12aj1nedSqMsVhAH5LyYJtjKPNrFWYoEh4FeGmWW2aS4DQQh

## Project Overview :page_facing_up:
### Overview

Please provide the following:

- If the name of your project is not descriptive, a tag line (one sentence summary).
    - Band Protocol is a leading cross-chain data oracle provider that aggregates and connects real-world data and APIs to smart contracts.
- A brief description of the template building.
    - BandChain is based on Cosmos SDK, designed to be compatible with all smart contract platforms and blockchain development frameworks. In a trustless and decentralized manner, BandChain does all the heavy lifting jobs of pulling data from external sources, aggregating, and packaging them into a format that is easy to use and cryptographically verified across multiple blockchains. Unlike general-purpose blockchains, BandChain is designed explicitly for oracle data requests and computation. Data request transactions are both received and resolved very quickly. Furthermore, our data source scripts and oracle scripts allow maximum customization and flexibility for the user to query and compute their desired data feed.
- An indication of how your project relates to ink! ecosystem.
    - Band Protocol has the potential to become a crucial infrastructure provider for the ink! Ecosystem. As projects develop on Astar, they will require reliable oracle services to deliver precise real-world data. By integrating with Astar, we can prepare and offer these essential services to Dapps building on the platform. Additionally, developers can be assured that they will receive high-quality data from a team of experienced professionals managing the price feed. By leveraging Band Protocol's expertise, Astar can enhance its offerings and provide a more comprehensive, reliable ecosystem for its users. Furthermore, we have a strong track record of collaborating with and offering oracle solutions for astar for more than a year now. This extensive experience positions us as a knowledgeable and skilled team in supporting the polkadot ecosystem and we are truly enthusiastic about continuing our involvement to its growth.
- Choosen project idea category or your alternative category with explanation of its importance
    - Band Protocol's decentralized oracle solutions provide critical infrastructure for blockchain networks to access external data and integrate it into their smart contracts and decentralized applications. This enables blockchain networks to become more powerful and versatile, creating new opportunities for developers and users alike.
- An indication of why your team is interested in creating this project.
    - Astar has a robust foundation and ecosystem, making it an attractive platform for many talented builders to develop on in the near future. Our team has been integrated with Astar EVM for over a year now, and we’ve already requested our technical team review the technical specifications and documentation of Astar Wasm. Our team has significant experience integrating with EVM, WASM, and Rust-based projects, which gives us the expertise needed to provide excellent services for dapps looking to build on Astar Wasm. By leveraging our technical know-how, we are confident that we can provide strong support to developers building on the Astar Wasm platform.

### Ink! Ecosystem Impact

Please clearly describe how exactly your project will benefit the ecosystem. If it's infrastructure - how it's going to be applied and by who. If it's canary dapp we would you to clearly demonstrate how this code will be used by other people. If it's technical showcase we would like you to demonstrate how ink! will be promoted using your results. 

If it's a business case we would like to see business model and future production plans. 

- Band Protocol offers a wide range of real-world data services, including cryptocurrency prices, foreign exchange rates, and commodity prices. Our services are currently available on 19 chains, including Ethereum, BNB Chain, Avalanche, and Cronos. We have also integrated with various projects on their testnets to ensure seamless data delivery. We have collaborated with lending, perpetual, yield protocols and more to provide accurate and reliable data that supports a variety of use cases. By partnering with Band Protocol, Dapps can access the data they need to build innovative and secure blockchain applications that meet the needs of their users.

### Project Details

We expect the teams to already have a solid idea about the project expected final state. Therefore, we ask the teams to submit (where relevant):

- Data models / API specifications of the core functionality
    - Not applicable
- An overview of the technology stack to be used
    - Languages: Rust, Golang
    - Infrastructure: Google Cloud
    - Database: PostgreSQL
    - Virtualization: Kubernetes, Docker
- Documentation of core components, protocols, architecture, etc. to be deployed
    - The service comprises four key components: BandChain, the requester, the relayer, and the signer. The requester initiates data requests to BandChain, converting the received data into packets that are subsequently transmitted to the relayer. Acting as a bridge, the relayer transfers the data derived from BandChain to Astar. The signer, on the other hand, operates as a separate service responsible for signing verified transaction requests issued by the requester.
- PoC/MVP or other relevant prior work or research on the topic
    - Our prior experience, partners we've integrated with: https://www.bandpartners.io/partners
    - Our team has been integrated with Astar EVM for over a year now, and we’ve already requested our technical team review the technical specifications and documentation of Astar Wasm. Our team has significant experience integrating with WASM projects, which gives us the expertise needed to provide excellent services for dapps looking to build on Astar Wasm.
- What your project is _not_ or will _not_ provide or implement
  - This is a place for you to manage expectations and to clarify any limitations that might not be obvious
    - To clarify, this integration will be for price feed only, the VRF will not be included in ink contracts at this time
    - For price feed, we have the capability to offer up to 15 symbols from our standard dataset, not all of the symbols will be available
    - We are excited about the opportunity to expand our oracle service to additional ink!-based blockchains. The grant we are seeking will be allocated to support the development for Band Protocol's oracle service on ink-enabled blockchains and to support the running costs for the oracle service on Astar WASM.
- Do you need an audit for the contacts? **YES/NO**
(don’t add it as part of Milestones! The auditor will be chosen among Auditor track participants)
    - Yes
- CATEGORY: Infrastructure OR Canary Dapp OR Technical Showcase
    - Infrastructure
## Team :busts_in_silhouette:

### Team members

- Name of team leader: Sireethorn Satchatippavarn
- Names of team members: Nile Buranasiri, Warittorn Cheevachaipimol 

### Contact

- **Contact Name:** Buranapong Buranasiri
- **Contact Email:** buranapong@bandprotocol.com
- **Website:** https://www.bandprotocol.com/

### Legal Structure

- **Registered Address:** Portcullis Chambers, 4th Floor, Ellen Skelton Building, 3076 Sir Francis Drake Highway, Road Town, Tortola, British Virgin Islands
- **Registered Legal Entity:** World Data Corporation Foundation

### Team's experience

Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past.

- Band Protocol has been a trusted player in the blockchain space since 2017. We have experienced the ups and downs of the industry and have consistently performed well. On the technical side, our engineers have extensive experience integrating with EVM, WASM, and Rust-based projects, making us well-equipped to deliver a high-quality final product. Notably, we have successfully integrated with several prominent projects in the Cosmos ecosystem, including Injective, Cronos, OKC, and Secret Network. Our expertise and track record of successful integrations make us a reliable partner for projects looking to incorporate decentralized data oracles into their architecture.

### Team Code Repos

- https://github.com/bandprotocol/

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/warittornc
- https://github.com/taobun

### Team LinkedIn Profiles (if available)

- Sireethorn: linkedin.com/in/sireethorn-fon-satchatippavarn-11792aaa
- Buranapong: linkedin.com/in/buranapongburanasiri
- Sirada: linkedin.com/in/sirada-lorhpipat
- Warittorn: linkedin.com/in/warittorn-cheevachaipimol-467878230


## Development Status :open_book:

- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to building this template,
    - Band Partners: https://www.bandpartners.io/
    - Blog: https://blog.bandprotocol.com/
    - Github: https://github.com/bandprotocol/

## Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. Since these will be part of the agreement, it helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**.

### Overview

- **Total Estimated Duration:** 3-4 months
- **Full-Time Equivalent (FTE):**  2
- **Total Costs:** 80,000 USD

### Milestone 1
- **Estimated duration:** 2-3 months
- **FTE:**  2
- **Costs:** 45,000 USD

|  Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT 
| **0b.** | Documentation | We will provide inline documentation of the code, a basic tutorial on how to use the smart contract and an example consumer contract that shows a practical example on how to use the smart contract|
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests.|
| **0d.** | Docker | N/A for smart contracts|
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Data Source | Data sources on BandChain which will be the core of getting data that will be delivered to Astar |
| 2. | Oracle Script | An oracle script on BandChain which will verify and aggregate data from the data sources on BandChain|
| 3. | PDS | A service on BandChain that will allow paid services to deliver data to BandChain safely and securely |
| 4. | Smart contract | An ink! smart contract that will allow consumers to query various price feed from BandChain |
| 5. | Testing and Audit | Unit tests for each component and live testing and audits for the ink! smart contract on testnet |
### Milestone 2
- **Estimated duration:** 1-2 months
- **FTE:**  2
- **Costs:** 35,000 USD

|  Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License |  MIT 
| **0b.** | Documentation | We will provide inline documentation of the code, a basic tutorial on how to use the smart contract and an example consumer contract that shows a practical example on how to use the smart contract|
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests.|
| **0d.** | Docker | N/A for smart contracts|
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | BandChain Requester | A service that will prepare and request data from BandChain to be sent to Astar | 
| 2. | Astar ink! Relayer | A service that will prepare and execute data to be bridged over to Astar|
| 3. | ink! Signer | A seperate service which upon request, creates and signs a transction which is sent to the relayer service. The signer service is run on an isolated VPC to prevent unauthorized requests and uses a key management service to keep the signing key secure |
| 4. | Maintenance | Reviewer can continuously read the state of the contract to get an asset's price|
| 5. | Infrastructure | Hosting cost - Storage, GCP|
| 6. | Monitoring | 24/7 monitoring service ensures the continuous operation of the relayer. This includes the comprehensive monitoring of both the Astar EVM and Astar WASM chains for a duration of one year|

## Future Plans

Please include here if you have a future plan after building this template in making it in to production.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.
- As we have already integrated with Astar EVM, we maintain regular communication with their team. Recently, Toma, the head of Wasm Initiatives, informed us about this program, and we are extremely keen to participate.

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:
- Here's our Band Standard Dataset: https://data.bandprotocol.com/
    - For our Band Protocol’s flagship Oracle product, we have undergone a quality assurance process in which the listing criteria has been improved to provide more security to Band’s customers and end users. Symbols listed on the Band Standard Dataset are those that have been verified and passed several criteria
- Here's our Band Partners website: https://www.bandpartners.io/
    - In addition to providing our statistics, including total value secured (TVS), total requests, and data requests, our website showcases the various DeFi projects we have collaborated with in the past and the blockchain networks on which we are already integrated.
- Here's our Cosmoscan: https://www.cosmoscan.io/
    - Cosmosscan provides an accessible platform for everyone to effortlessly monitor and analyze the latest real-time blocks, requests, and transactions on BandChain. Additionally, users can access valuable information about our validators, datasources, and oracle scripts, ensuring a comprehensive understanding of the BandChain ecosystem.