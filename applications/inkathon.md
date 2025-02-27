# Ink!athon v2

- **Team Name:** Scio Labs
- **Payment Address:** Polkadot payment address.

## Project Overview :page_facing_up:
### Overview

"Ink!athon is a full-stack boilerplate for ink! dapp development"

Ink!athon is the leading full-stack boilerplate for building production-grade dapps with ink! smart contracts and helps to drastically shorten the time developers need to get started with developing a fullstack application with ink!. The boilerplate comes in a monorepo setup for an efficient development experience and includes a state-of-the-art tech stack for frontend, backend, and smart contracts. It is enriched with a typesafe react hooks library (useInkathon), multiple basic pre-styled frontend components and different custom shorthand scripts to speed up the development as much as possible.

The first version of ink!athon was released in 2023 as an answer to the lack of tooling and the high entry barrier for developers into the ink! ecosystem. It significantly supported the ink! adoption being just a few months old and a completely novel ecosystem for smart contract and protocol development. Since then, ink!athon has become the leading boilerplate for ink! dapps in the Substrate ecosystem and is used by different teams and projects with mainnet deplyoments in production such as the official name service on Aleph Zero (AZERO.ID)[https://azero.id] or the leading liqudid staking solution (ike.xyz)[https://ike.xyz].

This application aims to support the development of Ink!athon v2 which will be a complete rewrite and upgrade of the existing boilerplate in order to modernize the codebase and bring it up to date with the latest version of ink! 6.0 and the Polkadot ecosystem with its transition from Wasm and pallet-contracts to the PolkaVM with RISC-V and pallet-revive. This is crucial as the switch to ink!v6 does not entail backwards compability with Wasm and ink! v5.

Ink!athon v2 targets the infrastructure category within inkubator providing crucial tooling to enhance the developer experience in the ink! ecosystem and remain the go-to solution for bootstrapping ink! dapps.


### Ink! Ecosystem Impact

Ink!athon and it's underlying react-hooks library useInkathon have developed to one of the leading and most used developer toolings in the ink! ecosystem. Several usage & adoption metrices underline its success and importance:
- 275 Github stars
- 800+ commits
- 65+ forks
- 25k+ useInkathon downloads (total)
- 250+ depending repositories and projects (e.g. Kusamarian - thekus.xyz, lastic, azero.id, ike.xyz, abax.finance, 1delta, soroswap, Regionx CoretimeHub, etc.)

As a go-to-resource for developers building dApps on Polkadot, Inkathon offers not only a great start into any project and developer journey but also has itself proven as a reliable and robust building block for more complex production-grade dApps handling business use-cases in defi and more. Moreover, due to its ability to kickstart any ink! related product, it has become a key pillar for any ink! related hackathon and event aiming to onboard new developers and projects into the ink! ecosystem.

Ink!athon Revive will ensure that ink!athon can continue devlivering value to the ink! developer community and further enhance and strengthen its positioning as the go-to-solution for dapps running on PolkaVM with pallets-revive.

...

### Project Details

Ink!athon Revive consists of a complete update and futureproofing of the boilerplate as well as the useinkathon react hooks library. Furthermore, we make ink!athon fully compatible with ink!6.0 and the future of pallet-revive and the PolkaVM.

Updating the ink!athon boilerplate stack contains the following items and libraries:
  
- Update to ink! v6 & pallet-revive
- Update to Next v15
- Update to TailwindCSS & shadcn/ui v4
- Add Network Definitions & Extend deployments.ts
- Due Updates (i.e. polkadot.js) & Security Fixes
- Switch to Bun
- Switch to Biome.js

Updating the useInkathon react hooks library contains the following items and libraries:

- Add Connection Button Example
- Add the ability to add custom SubstrateChain objects
- Due Updates (i.e. polkadot.js) & Security Fixes
- Switch to Bun
- Switch to Biome.js

With these upgrades, ink!athon will provide all state-of-the-art frontend libraries and packages that enable production-grade dapp development without any friction. Ink! significantly relies on the quality of full-stack dapps built on top.

In addition to upgrading the boilerplate and react hooks library, the following improvements and additions are planned in order to make inkathon as a whole even more robust, useful and powerful:

- **Updating ink!athon to support Dedot:** Over the last year, Dedot has become a valuable JavaScript client for Substrate and a viable alternative to polkadot.js. It has improved the developer experience on Polkadot and is thus a great value-add for the overall ink!athon stack. This integration gives ink!athon users the option to choose between two different proven clients.
- **Creating an inkathon-app CLI:** This will allow users to create new ink!athon projects with a single command fruther improving the developer experience and speed.
- **Documentation:** Currently Ink!athon only has a basic README.md & generated Typedocs as an documentation. We will develop a new standalone documentation that is easily accessible and conprehensive for developers getting started with developing dapps with ink!.

Here is what our project Ink!athon v2 will not entail:

- abc
- abc
- abs

Furthermore, NO external audit is needed for this project.

Business Model. Ink!athon is a fully open-source community-driven project and a public good for the Polkadot developer ecosystem. As such, there is no commercial interest nor business model for the project. So far, Ink!athon has been mostly self-funded and maintained by the Scio Labs team with additional support by the Aleph Zero Foundation.

Q: betonen, dass das projekt auch langfristig aud grant funding angewiesen ist?

## Team :busts_in_silhouette:

### Team members

- Dennis Zollmann
- Maximilian Dietel
- Mike Schneider

### Contact

- **Contact Name:** Mike Schneider
- **Contact Email:** mike@scio.xyz
- **Website:** https://inkathon.xyz & https://scio.xyz

### Legal Structure

- **Registered Address:** Am Neuen Markt 9E-F, 14467 Potsdam, Germany
- **Registered Legal Entity:** Scio Labs UG (haftungsbeschränkt)

### Team's experience

Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past.

The team of Scio Labs consists of experienced web3 developers with a rich background in development of ink!-focused products and tooling. One flagship project is the official on-chain domain name service AZERO.ID on the Aleph Zero Substrate chain, which has been one of the first production-grade dapps utilizing ink! smart contracts and running on top of inkathon and use!inkathon. Moreoever, the Scio Labs team has been one of the strongest proponents of ink! since 2022 and helped pushing its adoption in the wider Polkadot & Substrateecosystem by giving workshops, talks and helping curious developers across several hackathons. The team also started the "ink! developer group" on Telegram which over time, has become the leading ink developer community. The Scio Labs team already sucessfully worked for grants from Aleph Zero Foundation, Web3 Foundation, Ethereum Foundation and Aave among others.  

### Team Code Repos

- https://github.com/scio-labs/inkathon
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

The current example frontend for ink!athon can be found [here](https://inkathon.xyz/) and the github repo [here](https://github.com/scio-labs/inkathon). The project has been started in September 2022 and has been improved and maintained ever since. In it's current state, ink!athon lacks certain updates and features to stay fully compatible with the latest and moreover, future expected updates of ink! and the Substrate ecosystem. As the go-to solution for frontend development of [ink! dapps](https://use.ink/frontend/overview#react) and its unique positioning and relevance among in-production projects, it is crucial to ensure that ink!athon always remains up to date and compatible with other building blocks in the ecosytem.

Prior to this application, we discussed the needed and required updates for ink!athon together with stakeholders such as the creators of ink! and its biggest supporters and maintainers like R0gue from Pop Network. Upgrading ink!athon to the most up-to-date stack, maintaining it and ensuring its ecosystem compatability is a priority issue for all ink! stakeholders.

## Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. Since these will be part of the agreement, it helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**.

> :exclamation: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Overview

- **Total Estimated Duration:** 5 months
- **Full-Time Equivalent (FTE):**  1.5 FTE
- **Total Costs:** 80,000 USD

### Milestone 1 Ink!athon & useInkathon stack upgrade

- **Estimated duration:** 2 month
- **FTE:**  1.5
- **Costs:** 30,000 USD

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code, a detailed **README.md** and a new detailed standalone documentation set up with a modern documentation tooling such as Gitbook. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Ink!athon Boilerplate| Upgrading & making Ink!athon compatible with Next.js v15 |
| 2. | Ink!athon Boilerplate| Upgrading & making Ink!athon compatible TailwindCSS & shadcn/ui v4 |
| 3. | Ink!athon Boilerplate| Add Network Definitions & Extend deployments.ts |
| 4. | Ink!athon Boilerplate| Due Updates (i.e. polkadot.js) & Security Fixes |
| 5. | Ink!athon Boilerplate| Switch Ink!athon stack to Bun |
| 6. | Ink!athon Boilerplate| Switch Ink!athon stack to Biome.js |
| 7. | useInkathon| Add Connection Button Example |
| 8. | useInkathon| Add the ability to add custom SubstrateChain objects |
| 9. | useInkathon| Due Updates (i.e. polkadot.js) & Security Fixes |
| 10. | useInkathon| Switch useInkathon to Bun |
| 11. | useInkathon| Switch useInkathon to Biome.js |



### Milestone 2 Ink!athon New & Advanced Features

- **Estimated Duration:** 2 month
- **FTE:**  2
- **Costs:** 40,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code, a detailed **README.md** and a new detailed standalone documentation set up with a modern documentation tooling such as Gitbook. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | ink!athon-app CLI | Create a simple ink!athon-app CLI to enable simple & fast project setup |
| 2. | ink!athon-app CLI | ...|
| 3. | Ink!athon Boilerplate | Adding support for the Dedot client as an alternative to polkadot.js |


### Milestone 3 Upgrade to ink! v6 & pallet-revive

- **Estimated Duration:** 1 month
- **FTE:**  1
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | GPLv3 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code, a detailed **README.md** and a new detailed standalone documentation set up with a modern documentation tooling such as Gitbook. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| **0e.** | Article | We will publish an **article** that explains what we achieved with Ink!athon v2 supported by the inkubator grant and how developers can get started utilzing it) |
| 1. | Ink!athon Boilerplate | Upgrade to ink! v6 & pallet-revive |
| 2. | useInkathon | Upgrade to ink! v6 & pallet-revive |


## Future Plans

We plan to continue maintaining and improving ink!athon and useInkathon as a public good and leading developer tooling for ink! ecosystem. Potential future improvemebnts and upgrades may include among others:

- abc
- abc

## Additional Information :heavy_plus_sign:

We've been in close contact with different key stakeholders in the ink! ecosystem to explore together different potential sources of funding for inkathon. 

**How did you hear about the Bounty Program?** Personal recommendation from the ink! and R0gue teams.

[...additional information...]
