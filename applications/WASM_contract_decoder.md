
# WASM Contract Decoder
- **Team Name:** Tokenguard.io (Block Solutions Sp z o.o.)
- **Payment Address:** Polkadot payment address.

## Project Overview :page_facing_up:
### Overview

On-chain analytics platform for Substrate chains

Tokenguard is an on-chain growth analytics tool dedicated for Substrate based blockchains & dApps. With its no-code and no-SQL approach, Tokenguard provides access to core and advanced metrics with user-friendly & easy-to-use dashboards. It is a fully customizable tool that allows to add and change desired metrics and tracking data. Additionally, with its real-time chain monitoring feature, Tokenguard helps strengthen chain security by setting alert notifications for events such as rugpulls, hacks, or other abnormal behaviours.

Main features:

 - Ecosystem Analytics - dashboards with off and on-chain metrics that allow to get insights about ecosystem growth and marketing strategies efficiency.
 - Advanced Analytics:
	 - dApps Analytics – dashboard with off & on-chain metrics for individual dApps. This feature allows to track inflow of new users into the ecosystem from specific dApps.
	 - Security Monitoring – real-time on-chain monitoring tool allowing to set-up security rules for abnormal activity and receive notifications to the Pendulum team.

### Substrate Ecosystem Impact

Tokenguard simplifies the management of blockchain data, providing quick and easy access to information for informed business decisions. As an analytical tool, it provides insights necessary for the functioning and growth of both the community and the Core team:
-   Transparency & Credibility
    -   access to data and on-chain insights is the basis for a community driven blockchain
    -   the ability to track and verify activity and growth in the Polkadot networks reinforces trust
-   Investment
    -   a tool that gives access to the performance of individual dApps and DeFi allows for a better assessment of the market situation in terms of investment
    -   insight into data on developer activity and TVL allows to attract additional additional community members who want to invest in Vara and its ecosystem
-   Engagement
    -   a well-informed community is more likely to be involved in the building programs on a given chain and in ongoing activities
    -   access to insights allows the community to actively promote chain in social media, at events and in ordinary media
      
### Ink! Ecosystem Impact

In order to enable smart contracts analytics for Ink! builders, there needs to be a solution allowing infrastructure apps such as Tokenguard, Polkaholic and others decode on-chain contract activity. Currently there's no solution that would allow indexing on-chain data from Ink! smart contracts into normalized data available for parsing and presenting insights to dApp builders & creators in Ink!.

As an effect, most of Ink! teams that we spoke with, are wasting hundreds of hours and thousands of $ to build their own indexing solutions and maintain them which effectively defocuses them from building and developing user-centric features. Most of these solutions are hard to maintain and manage, increasing the technological debt of each project.

Tokenguard proposes to create a universal smart contract decoding solution based on SubSquid technology which currently offers the most flawless indexing experience that could be used by any Ink! builder out there. The code can also be used by analytics tools created in the space. 

### Project Details

- An overview of the technology stack to be used
	- SubSquid, TypeScript
- PoC/MVP or other relevant prior work or research on the topic
	- [app.tokenguard.io](http://app.tokenguard.io)
- Do you need an audit for the contacts? **NO**
- CATEGORY: Infrastructure 



## Team :busts_in_silhouette:

### Team members

- Kamil Gorski - CEO (https://www.linkedin.com/in/gorskikamil/)
- Jakub Rojek - CTO / Backend developer (https://www.linkedin.com/in/jakub-rojek-dev/)
- Damian Rolek - CDO / Data Analyst (https://www.linkedin.com/in/damianrolek/)
- Matt Saczewski - Business Development Manager (https://www.linkedin.com/in/msaczewski/)
- Jacob Piorecki - UI/UX Designer (https://www.linkedin.com/in/jacobpiorecki/)
- Piotr Józefowicz - Backend Developer (https://www.linkedin.com/in/piotr-jozefowicz-529669220/)
- Adam Król - Backend Developer (https://www.linkedin.com/in/adam-kr%C3%B3l-7b3a831b6/)
- Krystian Trepczyński - Frontend Developer (https://www.linkedin.com/in/krystiantrepczynski/)
- Jan Kwiatkowski - Blockchain Developer (https://www.linkedin.com/in/jan-kwiatkowski-web3/)

### Contact

- **Contact Name:** Matt Saczewski
- **Contact Email:** matt@tokenguard.io
- **Telegram:** @mattsac

### Legal Structure

- **Registered Address:** Foksal 3/5 St., 00-366 Warsaw, Poland
- **Registered Legal Entity:** Block Solutions Sp z o.o.

### Team's experience

Tokenguard's clients include Swiss Sygnum Bank, [Bitcoin.com](http://Bitcoin.com), Astar and many others recognizable brands. Each of cofounders has tremendous web3 experience - Damian was co-creating DeFi analytics platform Kasuria. Jacob was working at OpenLoyalty, helping web3 projects engage their users and Kamil created web3 security analytics solutions, conducting more than 30+ audits.

### Team Code Repos

- [https://github.com/tokenguardio](https://github.com/tokenguardio)


## Development Status :open_book:

Tokenguard is currently developing the following features:

- Publicly accessible core analytics for Substrate communities, available at https://app.tokenguard.io
- Ecosystem Analytics for [Astar](https://astar.network/)
- Ecosystem Analytics for [Aleph Zero](https://alephzero.org/)
- dApp analytics for [AZero ID](https://azero.id/), [ArthSwap](https://app.arthswap.org), [Panjea](https://panjea.io/), [Interlock](https://www.interlock.network/) and others
- Partnership with [SubSquid](https://www.subsquid.io/)

## Development Roadmap :nut_and_bolt:


### Overview

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):**  3 FTE
- **Total Costs:** 30,000 USD

### Milestone 1 

- **Estimated duration:** 2 months
- **FTE:**  3
- **Costs:** 30,000 USD

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Substrate module: X | We will create a Substrate module that will... (Please list the functionality that will be implemented for the first milestone. You can refer to details provided in previous sections.) |
| 2. | Substrate module: Y | The Y Substrate module will... |
| 3. | Substrate module: Z | The Z Substrate module will... |
| 4. | Substrate chain | Modules X, Y & Z of our custom chain will interact in such a way... (Please describe the deliverable here as detailed as possible) |
| 5. | Library: ABC | We will deliver a JS library that will implement the functionality described under "ABC Library" |
| 6. | Smart contracts: ... | We will deliver a set of ink! smart contracts that will...


...


## Future Plans

Please include here if you have a future plan after building this template in making it in to production.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
