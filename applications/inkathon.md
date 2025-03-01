# ink!athon v2

- **Team Name:** Scio Labs
- **Payment Address:** 14KM5QPHLFBBj6DJ15FZv3oY8HvYEQji3EPqfzFZ2cbrb3UX

## Project Overview :page_facing_up:
### Overview

> Full-stack boilerplate for ink! dapp development.

`ink!athon` is the leading full-stack boilerplate for building production-grade dapps with ink! smart contracts and helps to drastically shorten the time developers need to get started with developing any application on ink!. The boilerplate comes in a monorepo setup for an efficient development experience and includes a state-of-the-art tech stack for frontend, backend, and smart contracts. It is enriched with a React hooks & utility library (`useInkathon`), multiple basic pre-styled frontend components and different custom shorthand scripts to speed up the development as much as possible.

The first version of ink!athon was released in 2023 as an answer to the lack of tooling and the high entry barrier for developers into the ink! ecosystem. It significantly supported the ink! adoption being just a few months old and a completely novel ecosystem for smart contract and protocol development. Since then, ink!athon has become the leading boilerplate for ink! dapps in the Substrate ecosystem and is used by different teams and projects with mainnet deployments in production such as the official name service on Aleph Zero [AZERO.ID](https://azero.id) or the leading liqudid staking solution [ike.xyz](https://ike.xyz).

This application aims to support the development of **ink!athon v2** which will be a massive upgrade of the existing boilerplate including a lot of new features, improvements, updates, and documentation. It will be fully compatible with the latest version of ink! v6 to support the Polkadot ecosystem transition from Wasm-based `pallet-contracts` to the PolkaVM with `pallet-revive` leveraging RISC-V. This is crucial as the switch to ink!v6 does not entail backwards compability with Wasm and ink! v5.

ink!athon v2 targets the *infrastructure* category within inkubator providing crucial tooling to enhance the developer experience in the ink! ecosystem and remain the go-to solution for bootstrapping ink! dapps.


### ink! Ecosystem Impact

ink!athon and it's underlying library useInkathon have developed to one of the leading and most used developer toolings in the ink! ecosystem. Several usage & adoption metrics underline its success and importance:

- 275 Github stars
- 800+ commits
- 65+ forks
- 25k+ useInkathon downloads (total)
- 250+ depending repositories and projects (e.g. Kusamarian - thekus.xyz, lastic, azero.id, ike.xyz, abax.finance, 1delta, soroswap, Regionx CoretimeHub, etc.)

As a kickstarter for developers building dApps on Polkadot, ink!athon offers not only a great start into any project and developer journey but also has itself proven as a reliable and robust building block for more complex production-grade dApps handling business use-cases in defi and more. Moreover, due to its ability to kickstart any ink! related product, it has become a key pillar for any ink! related hackathon and event aiming to onboard new developers and projects into the ink! ecosystem.

ink!athon v2 a.k.a. "ink!athon Revive" will ensure that ink!athon can continue delivering value to the ink! developer community and further enhance and strengthen its positioning as the go-to-solution for dapps running on PolkaVM with pallets-revive.


### Project Details

ink!athon v2 consists of major upgrades, rewrites, and futureproofing of the boilerplate. Furthermore, we make ink!athon fully compatible with ink! v6 and the future of pallet-revive and the PolkaVM.

We have broken down the project into three major milestones which are further specified below under *Development Roadmap*:

- **Milestone 1:** Upgrades & Improvements
  - [ink!athon & useInkathon] Restore compatiblity with latest polkadot.js (currently 3 versions behind due to breaking changes)
  - [ink!athon & useInkathon] Improve AI-driven DX with custom Cursor Project Files 
  - [ink!athon & useInkathon] Switch tooling to Bun for increased DX
  - [ink!athon & useInkathon] Switch formatting & linting to use Biome.js for increased performance
  - [ink!athon & useInkathon] Update/add network definitions & extend deployments.ts
  - [ink!athon] Integrate Pop CLI as the core tool to create/build/test contracts
  - [ink!athon] Major upgrade to TailwindCSS & shadcn/ui v4
  - [ink!athon] Major upgrade to Next.js v15
  - [ink!athon] Fix Dockerfiles for improved self-hosted deployment
  - [useInkathon] Add vanilla (w/o ink!athon) connection button example 
  - [useInkathon] Add the ability to add custom SubstrateChain objects

- **Milestone 2:** New CLI & Alternative Client
  - **Creating an ink!athon-app CLI:** We will create a `create-ink!athon` CLI to empower developers with simple and fast project scaffolding using a single command, significantly enhancing the developer experience and accelerating project setup.
  - **Providing an Alternative ink!athon Boilerplate with Dedot:** We will deliver a completely alternative version of the ink!athon boilerplate utilizing `dedot` as a robust and type-safe alternative to polkadot.js. This integration will offer developers improved type safety and an enhanced overall development experience, allowing them to choose between two proven JavaScript clients for Substrate.

- **Milestone 3:** ink! v6 Compatibility & New Standalone Documentation
  - *Note:* This important upgrade is the last milestone on purpose, as depends on the ink! v6 development and certain ecosystem changes & tooling updates to be ready. We're happy to ship this milestone earlier when everything is ready.
  - **New Standalone Documentation:** Currently, ink!athon only has a basic README.md & generated Typedocs as an documentation. We will completely rewrite this and will supply a new standalone documentation that is easily accessible and comprehensive for developers getting started with developing dapps with ink!.

  
With these upgrades, ink!athon will be able to continuously fuel production-grade dapp development on PolkaVM. ink! significantly relies on the quality of full-stack dapps built on top.


## Team :busts_in_silhouette:

### Team members

- Dennis Zollmann
- Maximilian Dietel
- Mike Schneider

### Contact

- **Contact Name:** Mike Schneider
- **Contact Email:** mike@scio.xyz
- **Website:** https://ink!athon.xyz & https://scio.xyz

### Legal Structure

- **Registered Address:** Am Neuen Markt 9E-F, 14467 Potsdam, Germany
- **Registered Legal Entity:** Scio Labs UG (haftungsbeschränkt)

### Team's experience

The team of Scio Labs consists of experienced web3 developers with a rich background in development of ink!-focused products and tooling serving thousands of users. Our flagship project is the official domain name service AZERO.ID on the Aleph Zero Substrate chain fueling over 4,000 registered onchain domains. It has been one of the first production-grade & audited dapps utilizing ink! smart contracts is running on top of ink!athon and use!ink!athon.

Moreoever, the Scio Labs team has been one of the strongest proponents of ink! since 2022 and helped pushing its adoption in the wider Polkadot & Substrate ecosystem by giving dozens of workshops, talks and helping curious developers across several hackathons. The team also started the "ink! developer group" on Telegram which over time, has become the leading ink developer community. The Scio Labs team already successfully worked for grants from Aleph Zero Foundation, Web3 Foundation, Ethereum Foundation, Aave, and others.  

### Team Code Repos

- https://github.com/scio-labs/ink!athon
- https://github.com/azero-id

GitHub accounts of all team members:

- https://github.com/wottpal
- https://github.com/MaximilianDietel03
- https://github.com/mike1third

### Team LinkedIn Profiles

- https://www.linkedin.com/in/dennis-zoma/
- https://www.linkedin.com/in/maxdietel/
- https://www.linkedin.com/in/mike1third/

## Development Status :open_book:

The current example frontend for ink!athon can be found [here](https://ink!athon.xyz/) and the github repo [here](https://github.com/scio-labs/ink!athon). The project has been started in September 2022 and has been improved and maintained ever since. Though, ink!athon & useInkathon currently lack certain updates and features to maintain its importance in the ecosystem. Moreover, ink!athon is not fully compatible with the latest and future expected updates of ink! and the Substrate ecosystem. As the go-to solution for frontend development of [ink! dapps](https://use.ink/frontend/overview#react) and its unique positioning and relevance among in-production projects, it is crucial to ensure that ink!athon always remains up to date and compatible with other building blocks in the ecosytem.

Prior to this application, we discussed the needed and required updates for ink!athon together with stakeholders such as the creators of ink! and its biggest supporters and maintainers like R0gue from Pop Network. Upgrading ink!athon to the most up-to-date stack, maintaining it and ensuring its ecosystem compatibility is a priority issue for all ink! stakeholders.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 5 months
- **Full-Time Equivalent (FTE):**  1.5 FTE
- **Total Costs:** 80,000 USD

### Milestone 1: Upgrades & Improvements

- **Estimated duration:** 2 month
- **FTE:**  1.5
- **Costs:** 30,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | We will provide both inline documentation of the code and a detailed README. As part of this grant, we will also provide a new standalone documentation. |
| **0c.** | Testing and Testing Guide | Contract-level functions will be fully covered by unit tests and the boilerplate simplifies contract testing as part of the development workflow.  |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | ink!athon & useInkathon | Restore compatibility with latest polkadot.js (currently 3 versions behind due to breaking changes) |
| 2. | ink!athon & useInkathon | Improve AI-driven DX with custom Cursor Project Files |
| 3. | ink!athon & useInkathon | Switch tooling to Bun for increased DX |
| 4. | ink!athon & useInkathon | Switch formatting & linting to use Biome.js for increased performance |
| 5. | ink!athon & useInkathon | Update/add network definitions & extend deployments.ts |
| 6. | ink!athon | Integrate Pop CLI as the core tool to create/build/test contracts |
| 7. | ink!athon | Major upgrade to TailwindCSS & shadcn/ui v4 |
| 8. | ink!athon | Major upgrade to Next.js v15 |
| 9. | ink!athon | Fix Dockerfiles for improved self-hosted deployment |
| 10. | useInkathon | Add vanilla (w/o ink!athon) connection button example |
| 11. | useInkathon | Add the ability to add custom SubstrateChain objects |

### Milestone 2: New CLI & Alternative Client

- **Estimated Duration:** 2 month
- **FTE:**  1.5
- **Costs:** 30,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | We will provide both inline documentation of the code and a detailed README. As part of this grant, we will also provide a new standalone documentation. |
| **0c.** | Testing and Testing Guide | Contract-level functions will be fully covered by unit tests and the boilerplate simplifies contract testing as part of the development workflow.  |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | ink!athon-app CLI | Create a `create-ink!athon` CLI to empower simple & fast project scaffolding in one command. |
| 2. | ink!athon Boilerplate | Provide an completely alternate version of ink!athon using `dedot` as an alternative to polkadot.js for better type safety. |

 
### Milestone 3: ink! v6 Compatibility & New Standalone Documentation

- **Estimated Duration:** 2 month
- **FTE:**  1
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | We will provide both inline documentation of the code and a detailed README. As part of this grant, we will also provide a new standalone documentation. |
| **0c.** | Testing and Testing Guide | Contract-level functions will be fully covered by unit tests and the boilerplate simplifies contract testing as part of the development workflow.  |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| **0e.** | Article | We will publish an article that explains what we achieved with ink!athon v2 supported by the inkubator grant and how developers can get started utilzing it! |
| 1. | ink!athon & useInkathon | Compatibility with ink! v6 & pallet-revive |
| 2. | ink!athon | Update examples to use ink! v6 & pallet-revive |
| 3. | New Standalone Documentation | Create comprehensive, easily accessible standalone documentation for developers getting started with developing dapps with ink! |


## Future Plans

We plan to continue maintaining and improving ink!athon and useInkathon as a public good and leading developer tooling for the ink! ecosystem.

## Additional Information :heavy_plus_sign:

We've been in close contact with different key stakeholders in the ink! ecosystem to explore together different potential sources of funding for ink!athon. 

**How did you hear about the Bounty Program?** Personal recommendation from the ink! and R0gue teams.

**Audit:** No external audit is needed for this project.

**Business Model:** ink!athon is a fully open-source community-driven project and a public good for the Polkadot developer ecosystem. As such, there is no commercial interest nor business model for the project. So far, ink!athon has been mostly self-funded and maintained by the Scio Labs team with additional support by the Aleph Zero Foundation. Open source grants such as the inkubator play a crucial role in ensuring the long-term sustainability and maintenance of ink!athon.
