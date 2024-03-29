# Bright Disputes

- **Team Name:** Bright Inventions
- **Payment Address:** 15LpomjmegxcrVwT7zDPvScWtx6FVYoTLxEkSzqwr3po9TCc

## Project Overview :page_facing_up:
### Overview

Bright Disputes is a dApp for solving disputes. Our goal is to create a smart contract (written in ink!) which could be used to raise and solve disputes on the Substrate-based blockchains. We would like to leverage a Zk-Snarks to accomplish privacy of voting.

The brief descritpion of this project, we will start by presenting the roles:
* Owner - a person who raises the dispute.
* Contractor - a person who is on the side of the dispute.
* Judge - is responsible for counting the votes.
* Jury - can votes in a dispute agains one of the sides.

Dispute can be raise by the person who is the Owner. He points a Contractor, who is a side here, to join the dispute. Both of them need to provide a description of the dispute and their position on the matter as well as paying the fees. When all formalities are fulfilled, the dispute can start. The first step is to appoint a Judge, who will be responsible for counting the votes. Than we choose Juries, who will vote against one of the sides. Jurieas as well as Judge are radonomly picked by the smart contract from the pool of Juries.

Voting phase will start when all Juries and Judge confirm their assignment for the dispute, by providing an escrow. If someone will not confirm their assignment, Owner / Contractor can trigger smart contract to repick persons from the Juries pool. 

In the voting phase, the Jury votes for one of the parties. The vote is encrypted with the public key of the Judge and a proof of a valid vote is delivered to smart contract. From now only the Judge can read the votes.

At the end of the voting phase, the Judge is responsible for counting all the votes and issuing a verdict. If there is no majority of the votes (at least 60% against one party), verdict can not be unequivocal. In that case the dispute round need to be repeated, but the number of juries is increated by two. What is worth to mention is that votes are not revealed, so Juries doesn't know how others vote. Thats why Judge need to provides a proof (zk-snark) of his correct counting of the votes. When there is a majority of votes, the Judge issues a verdict and make votes public. Now Judge and the Juries which were in the majority of the votes are rewarded by their work. Juries whose votes are in the minority are penalized, by slashing their escrows. If Judge or Jury will not fulfill his duties (take action in time), their will lose their escrows.

Beneath is the diagram showing the basic logic of the Bright Disputes, which were here described.

![](https://i.imgur.com/jWWw54D.png)


More specifically, BrightDisputes would be used in connection with a job advertising platform. In the following diagram our own project SubFunds is used as an example of such platform. The diagram illustrates the whole use case scenario that involves a funding part that advertised the job (Bob), a contractor obliged to perform it (Alice) and a judge selected for the case (Charlie):

![](https://i.imgur.com/aLGOXbJ.png)

### Project Details

"Bright Disputes" is a smart contract fully written in ink! From the development perspective, the most chalenging and interesting part will be the zk-snarks. Privacy is very important in our dispute system while the Juries publishes the encrypted votes, and the Judge counts them to reach a verdict. Role of the Judge requires honesty, he is the only one who can decrypt the votes. That's why we want to use zk-snarks to prove Judge honesty and correctness of the vote counting. Especially when the verdict is not clear and we need to repeat the voting round. The jury cannot see how others vote, otherwise the verdict will not be fair.

Based on our knowlage of zk-snarks ([zk-snarks-in-substrate](https://brightinventions.pl/blog/zk-snarks-in-substrate-part-1/)), using this technology have some consequences. Creating of zk-snarks will generate some artifacts (verification / proving key). We will provide a CLI, which will simplify this process. As it shown on the diagram below Juries / Judge are going to use CLI to communicate with the smart contrant, while Owner / Contractor can use polkadot.js dApp.

![](https://i.imgur.com/WjZczZx.png)

Our target plaform for the deployment will be AlephZero, which provides zk-snarks verification.

As a part of this project we will also provide UI that will allow users to test the functionality and already create an environment for solving disputes, without any connection with external job advertising platform.

It will be available as a web application, connecting with our BrightDisputes CLI. 

Example screens from the app:

#### A. Creating a dispute
![](https://i.imgur.com/HqXeBmQ.png)

#### B. Judging a dispute
![](https://i.imgur.com/AXw8JCp.png)

## Team :busts_in_silhouette:

### Team members

- Michał Graliński - Rust Developer
- Maciej Sawicki - Frontend Developer
- Joanna Cieszyńska - Product Designer
- Katarzyna Łukasiewicz - Project Manager

### Contact

* **Contact Name:** Katarzyna Łukasiewicz
* **Contact Email:** katarzyna.lukasiewicz@brightinventions.pl
* **Website** https://brightinventions.pl/

### Legal Structure

- **Registered Address:** ul. Jana Matejki 12, 80-232 Gdańsk, Poland
- **Registered Legal Entity:** Bright Inventions Sp. z o. o.

info@brightinventions.pl

www.brightinventions.pl


Bright Inventions is a team of oveer 70 full-time onsite developers, project managers & UX/UI designers - experts in mobile and web applications, systems integration, IOT devices and Blockchain platforms. 

We believe that building a software product is about people working together in a collective way. By offering complex support – mobile and web development as well as IT consultancy we try to eliminate roadblocks towards engaging clients as partners at every step of the process. 

We support startups, digital agencies as well as medium to big businesses. We cooperate with startups, accelerators and incubators. Whatever the client profile is, we always  aim to establish a satisfying partnership for both sides. Since 2012 we have built software for more than 40 businesses worldwide.

### Team's experience
As a company we have a 4 year experience with blockchain technologies, including cooperation with Parity. Since almost 2 years we’re developing our own Substrate based product [BrightTreasury](https://treasury.bright.dev/), that's been funded first by Web3 Foundation Grants program and has been supported by Polkadot and Kusama treasuries since. More recently, we’ve engaged in Rust development for Substrate as well, with two Web3 Foundation grants: [ZK-Snarks tutorial](https://github.com/w3f/Grants-Program/pull/1290) and [High-availability validator setup with Raft](https://github.com/w3f/Grant-Milestone-Delivery/pull/813).

Who would work on Bright Disputes?
- Michał - Rust Developer, for over 12 years he has been working as a C++ developer. In his career he participated in various projects, starting from the embedded devices, automotive, mobile games and ending on the financial systems. Right now he is focused on the blockchain technology.
- Maciej - Frontend Developer with over 15 years of experience, for the last couple of years working mainly with React. He has been taking part in projects for various industries - always keen to get to know new business domains.
- Joanna - Product Designer, who’s passionate not only about the aesthetic part of the products, but also the accessibility aspect of it. Likes to make sure that the products she designs are inclusive and users get to experience them equally.
- Kasia - she has been working with agile methods for over 10 years, both as a researcher and a practitioner. She believes in teamwork and a power of user centered mindset. With experience in leading international projects, she knows how to support and encourage timely and high quality deliveries.

### Team Code Repos

-  https://github.com/bright

Team Members:
-  Michał: https://github.com/mgralinski-bright
-  Maciej: https://github.com/unagigd
-  Joanna: https://www.behance.net/joannacieszynska
-  Kasia: https://github.com/bufta

### Team LinkedIn Profiles

- https://www.linkedin.com/in/michal-gralinski-b464152/
- https://www.linkedin.com/in/maciej-sawicki-69306648/
- https://www.linkedin.com/in/joannacieszynska/
- https://www.linkedin.com/in/katarzyna-łukasiewicz-b473901aa/

## Development Status :open_book:

The result of our research regarding the solutions and architecture has been described in this proposal.

## Development Roadmap :nut_and_bolt:


### Overview

- **Total Estimated Duration:** 5,5 months
- **Full-Time Equivalent (FTE):** 1,2
- **Total Costs:** 53 000 USD

### Milestone 1 — Basic functionality

- **Estimated duration:** 1 month
- **FTE:**  1,1
- **Costs:**  10 000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | We will provide **inline documentation** of the code. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Repository | We will create a GitHub repository for Dispute project.
| 2. | Smart contract | Create a smart contract according to documentation, where voting is public.
| 3. | Script | Create a `deploy` script, it will allows to setup the local environment (run aleph-node, deploy smart contract)

### Milestone 2 — Additional features

- **Estimated Duration:** 1,5 month
- **FTE:**  1,1
- **Costs:** 12 000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | We will provide **inline documentation** of the code. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) / Docker Compose that can be used to test all the functionality delivered with this milestone. |
| 1. | CLI | Create a CLI (in Rust) for calling smart contract messages.
| 2. | Library | Create `R1CS` relations library for vote counting. We are going to use primitives from the `liminal`.

### Milestone 3 — Additional features

- **Estimated Duration:** 2 month
- **FTE:**  1,1
- **Costs:** 20 000 USD


| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | We will provide **inline documentation** of the code. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains the dispute resolution solution. (Content, language and medium should reflect your target audience described above.) |
| 1. | Smart contract | Modify a smart contract to accomplish a private voting goal, by encrypting votes using Judge's public key and signing them with their private keys.
| 2. | Smart contract | Modify smart contract with the private vote counting and zk-snarks.
| 3. | CLI | Extend CLI to use created relations from the Milestone 2.
| 4. | Script | Extend `deploy` script to accomplish for the smart contract (ex: generate veryfications / proving keys)

### Milestone 4 - User Interface

- **Estimated Duration:** 1 month
- **FTE:** 1,3 
- **Costs:**  11 000 USD


| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT |
| **0b.** | Documentation | We will provide **inline documentation** of the code. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains how to use the BrightDispute user interface. (Content, language and medium should reflect your target audience described above.) |
| 0f. | YouTube video | We will publish a **tutorial video** that explains how to use the BrightDispute user interface and how the solution behind it. (Content, language and medium should reflect your target audience described above.) |
| 1. | Add new dispute | Allow users to log in using the polkadot.js plugin and add a new dispute, specifying who's a part of the dispute and adding a link to an external service (description of the case)
| 2. | Add defending info | Once a dispute is created, a defendant of the dispute can present their own side of the case (adding a link to the external service).
| 3. | Follow the status of the dispute |Both sides of the dispute can follow the status of the dispute status and outcome.
| 4. | Application to the jury pool | A user, after loging in with their wallet address, can request to become a part of the jury pool
| 5. | Confirm jury role in a case | For each case, a jury is randomly selected from the jury pool. A user selected for a specific case should confirm their participation in order to take part in the case.
| 6. | Vote on a case | A jury member that confirmed their participation in a case is expected to vote in a voting round.

## Future Plans

Our plan for the future is to create a protocol that would allow the use of Bright Disputes from various smart contracts. Our goal would be to create a real use case scenario where our dispute system could resolve issues, such as bounties disputes. 

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?**  personal recommendation from W3F Grants team

In addition to the Dispute module, we've been researching the potential use case for it. We've already started to develop a POC for private funding bounties mechanism, using WASM and IPFS. We see this as a potential showcase and next step for Bright Disputes.  
