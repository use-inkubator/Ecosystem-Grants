# InkScope (Ink! VS Code extension)

- **Team name:** InkScope team
- **Payment address:** [Polkadot Payment Address Placeholder]

---

## Project overview :page_facing_up:

### Overview

- **Tagline**: A unified VS Code extension that simplifies debugging and development of Ink! smart contracts.
- **Brief description**: This is a developer-targeted plugin for VS Code to smoothen the entire development workflow of Ink! smart contracts, allowing for **easy deployment, interaction, and error log analysis** all in one place. Presently, there is a fragmented debugging experience due to the use of several standalone tools.
- **Relation to Ink! ecosystem**: This would bundle into one interface all the existing Ink! debugging resources, removing some of the friction for developers building on Substrate using Ink!. This would be similar to how Solidity developers have an experience using Remix but within the Ink! environment.
- **Chosen project category: Tools**
- **Importance**: Developer tools are foundational in the overall ecosystem. A unified method for debugging provides an important role to play in speeding up adoption and improving developer experience in the context of smart contracts.
- **Why our team is interested**: Our team understands the big pains for the developers of Ink! because they don't have a centralized debugging solution. We would like to contribute with a tool that will remove these obstacles, enable faster prototyping, and ultimately contribute to the growth of the Ink! ecosystem.

---`

### Ink! ecosystem impact

This **VS Code extension** will benefit the Ink! ecosystem by offering:

- **Infrastructure**: A centralised environment of interaction, deployment, and debugging of Ink! contracts that will reduce the barrier to entry.
- **Accelerating adoption**: An easier-to-use, more intuitive development workflow will attract new developers to Polkadot/Substrate-based smart contracts.
- **Technical showcase**: Demonstrate how Ink! can facilitate a modern dev experience on par or better than existing Ethereum-based tooling.
- **Scalability of development**: Smooth debugging reduces the time-to-market for new dApps and may result in more robust production-ready projects on Ink!.

---

### Project details

1. **Core functionality & data flow**
    1. **Data models / API specs**:
        - We shall be using the **local node logs**, **dry-run API**, amongst other existing debug/log endpoints in Ink! to fetch transaction results and error messages.
        - These logs will, in turn be parsed and presented in user-friendly format by the **VS Code extension.**
    2. **Architecture overview**:
        - **VS Code extension layer**: Responsible to handle UI/UX, allows developers to deploy and interact with contracts.
        - *Integration layer*: Responsible for gathering data from local nodes and dry-run endpoints, interpreting logs, and surfacing them back to the extension.
        - *Ink! contracts*: Example contracts to test end-to-end functionality.
2. **Technology stack**:
    - **VS Code extension**: TypeScript, Node.js
    - **APIs for integration**: Ink! dry-run, local node logs
    - **Smart contracts**: Ink! (Rust-based), used primarily for demonstration and testing
3. **Documentation & prior research**:
    - Early prototypes include a simple command-line approach to read logs, but we’ve identified the need for an integrated UI.
    - This extension focuses strictly on providing debugging, deployment, and logging features—not on tokenomics or chain-specific business logic.
4. **Non-goals / limitations**:
    - No token or chain deployments beyond what's necessary to demonstrate debugging.
    - We aren't offering a hosting platform of our own or any special deployment services.
    - The scope doesn't include specialized audits.
5. **Audit needed?** No
6. **Category**: Infrastructure (Tools)
7. **Business model**: Our project exists as a developer tool to improve the debugging and development experience within the Ink! ecosystem. There is no revenue or monetization stream at this time. The main goal is to provide a stable, open-source extension that meets the current needs of Ink! developers by simplifying their workflow.
8. **Growth strategy and future plans**: Ahead, we envision building the platform into something more than a bare-bones VS Code extension. Coming releases could see advanced features - a complete contracts debugger, AI analyser and suggestions, and additional tooling. This phased approach allows us to take input from the community and iterate on the tooling in smaller chunks before considering monetization strategies.

> Exclusions:
> 
> - We are not providing tokenomics or fee models—this is purely a developer tool.

---

## Team :busts_in_silhouette:

### Team members - TODO

- Illia Abrosimov – Team leader / project lead
- Yaroslav Kulpin – Ink! integration & testing engineer
- **[Name 2]** – Front-end & extension engineer

### Contact

- **Contact name:** Illia Abrosimov
- **Contact email:** aillia.dev@gmail.com

### Team's experience

Our team has combined expertise in:

- **Ink! / Substrate** development, having contributed to small PoC contracts and experimenting with cross-contract calls.
- **VS Code extensions / Front-end tools**: Experience using TypeScript and Node.js to build and publish custom extensions on the marketplace.

### Team code repos - TODO

- [https://github.com/your_organisation/ink-vscode-prototype](https://www.notion.so/Ink-VS-Code-Extension-1766adfdc5b48063a6edfeafa10d097d?pvs=21) *(Example — Placeholder)*
- [https://github.com/your_organisation/ink-experiments](https://www.notion.so/Ink-VS-Code-Extension-1766adfdc5b48063a6edfeafa10d097d?pvs=21) *(Example — Placeholder)*

**GitHub accounts - TODO**:

- [https://github.com/team_member_1](https://www.notion.so/Ink-VS-Code-Extension-1766adfdc5b48063a6edfeafa10d097d?pvs=21)
- [https://github.com/team_member_2](https://www.notion.so/Ink-VS-Code-Extension-1766adfdc5b48063a6edfeafa10d097d?pvs=21)
- [https://github.com/team_member_3](https://www.notion.so/Ink-VS-Code-Extension-1766adfdc5b48063a6edfeafa10d097d?pvs=21)

### Team LinkedIn profiles - TODO (if available)

- [https://www.linkedin.com/in/person_1](https://www.notion.so/Ink-VS-Code-Extension-1766adfdc5b48063a6edfeafa10d097d?pvs=21)
- [https://www.linkedin.com/in/person_2](https://www.notion.so/Ink-VS-Code-Extension-1766adfdc5b48063a6edfeafa10d097d?pvs=21)

---

## Development status :open_book:

- **Research**: We have spoken to various developers in the Ink Developer Group chat (tg: @inkathon) who constantly switch between multiple debugging solutions, for example, local node logs or contract-UI.
- **Open GitHub issues**: There have been discussions on some topics related to the friction in debugging and lack of integrated logs in various community repos.
- **Prototyping**: We have a prototype command-line script to parse the local node logs but will be substituting it with a robust UI for VS Code.

---

## Development roadmap :nut_and_bolt:

### Overview

- **Total estimated duration:** 3 months
- **Full-time equivalent (FTE):** ~3 FTE
- **Total costs**: 60,000 USD

### Month 1 — Foundational development & core features

- **FTE**: 2
- **Costs**: 20,000 USD
- Set up the core framework with basic debugging functionality, establishing the foundational work for the features of deploying contracts.

### Deliverables

| **Number** | **Deliverable** | **Specification** |
| --- | --- | --- |
| **1.** | License | Publish all applicable code under the **MIT** license. |
| **2.** | Documentation | Include inline code documentation and a brief tutorial for installation and getting started. |
| **3.** | Extension core setup | Lay down the skeleton of a VS Code extension: commands, configuration, UI placeholders, and packaging ready for distribution. |
| **4.** | Local node log integration | Allow reading logs from a local node to display real-time contract events and errors. |
| **5.** | Testing framework | Unit tests for core functionality, including deploying contracts and retrieving logs. |
| **6.** | Docker | Dockerfile for a minimal Ink! node environment to show the workflow of the extension. |
| **7.** | Build & deploy workflow (Phase 1) | Add the functionality of building Ink! smart contracts directly from the extension and output a deployable `.wasm` file. |

---

## Month 2 — Advanced features & contract management

- **FTE:** 3
- **Costs:** 30,000 USD
- Enhance debugging features and add contract deployment and instantiation features.

### Deliverables

| **Number** | **Deliverable** | **Specification** |
| --- | --- | --- |
| **8.** | Testing guide | Increase test coverage for dry-run simulation, error parsing, and contract workflows - update the test guide. |
| **9.** | Dry-run simulation hook | Add a simple interface for calling the dry-run API, parsing data, and showing results in real time. |
| **10.** | Basic error parsing | User-friendly error summaries, such as out-of-gas errors and invalid calls. |
| **11.** | Interactive troubleshooting | Use Aha! moment suggestions, smart suggestions or tips for known error patterns. For example - Insufficient Balance and permissions). |
| **12.** | Deploy & instantiate contracts - phase 2 | Give the possibility to deploy an Ink! Smart Contract and instantiate straight from the extension with given constructor inputs. |
| **13.** | Docker update | Update Docker environment accommodate new advanced debugging and contract deployment workflows. |
| **14.** | Community Feedback | Engage with the developer community through Telegram chat (@inkathon) to gather insights and feedback for improving the extension |

---

**Month 3 — Debugging polish, community outreach, & final release**

- **FTE:** 1.5
- **Costs:** 10,000 USD
- Finalize the deployment contract, debug and polish the extension for a stable release, and create community engagement.

### Deliverables

| **Number** | **Deliverable** | **Specification** |
| --- | --- | --- |
| **15.** | Cross-contract debugging | Capture logs from multiple contract calls and unify output with references to where errors originated. |
| **16.** | Build, deploy & instantiate (Phase 3) | Establish a seamless developer experience to building, deploying and instantiating a contract that implements mechanisms to deliver feedback for deployment successes or failures. |
| **17.** | Production-ready extension | Stabilise the extension, ready for stable release in VS Code Marketplace based on tagging and preparation of release notes |
| **18.** | Community engagement | Host 1 x Twitter Space on using advanced debugging features in real-world Ink! scenarios. |
| **19.** | Outreach article | Publish an article highlighting the extension's main features, targeting both basic and advanced Ink! developers. |

---

## Future Plans

Once the core functionality of the extension is complete, we would like to explore:

1. **Advanced error suggestions**: Build a full-featured error resolution assistant that provides detailed explanations, proposed fixes, and links to the relevant documentation for debugging complex issues.
2. **Smart contract interaction**: Extend the extension to offer functionality that allows developers to invoke smart contract methods, change parameters, and observe responses within their IDE itself.
3. **Performance analytics**: Visualizing resource usage metrics - gas, storage, and execution time - of every interaction a contract has in real time to drive optimizations that a developer may need to perform in their contracts.
4. **Workflow automation**: The automation of deployment, testing, and instantiation via customizable pipelines and integration to CI/CD tools.
5. **Community-driven features**: Building a feedback loop with the developer community for the prioritization and implementation of features based on real-world pain points while developing and debugging smart contracts.
6. **Treasury funding application**: While this application focuses on delivering the MVP of the extension, our future plans include applying to the treasury program to secure additional funding. This will enable us to scale the extension significantly, adding advanced features and broadening its capabilities for the developer community.

---

## Additional information :heavy_plus_sign:

**How did you hear about the Bounty Program?**

Recommendation from a colleague.