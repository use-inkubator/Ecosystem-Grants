# VIDEOWN

- **Team Name:** CONTRACT LAB
- **Project Category:** Canary DApp
- **Payment Address:** 13uNZKG1Nqmkp4usxzeBK5htuUFgcY4agGLxMWm9TPgQdAgB

## Project Overview :page_facing_up:
### Overview
Redirecting monetization opportunities to creators in their best interest in Web3 is the crux the industry has been longing to solve. Content is not truly owned by creators in most cases in Web3, most data is still being stored in centralized storage where the ownership issue prevails. VIDEOWN provides a platform where creators share and trade content with data ownership and privacy protection, bringing creators the unprecedented experience of content creation, sharing and trading in the world of Web3.

VIDEOWN is a decentralized video NFT platform, built on the CESS blockchain, to provide users a smooth video streaming experience. Users not only can upload, play or search for all tagged video content on VIDEOWN, but also mint the content as NFT in a smart contract (written in ink!). NFT is no longer just implemented in the form of smart contracts. VIDEOWN realized the concept that NFT is the data itself, and users can exchange data ownership, whether it is pictures, music or videos.

### Project Details

#### Main Frame Diagram



This grant application includes one smart contract, two backend and one frontend. We aim to provide the following key features.

#### videown-nft

Smart contract written in ink!. 

- Mint NFT
- List/Unlist NFT
- Buy NFT
- Transfer NFT

#### videown-server

Backend service written in golang and GSRPC. 

- Transaction forwarding
- Home page listing video list
- System login and logout interface
- My video NFT interface
- Listing/unlisting NFT interface
- Purchase NFT page interface
- Transfer NFT page interface

#### CMPS (CESS Media Proxy Server)

Backend service written in golang and cess-sdk-go. 

- File upload
- File download(video playback address)
- File status query
- File upload status push

#### videown-web

Frontend UI written in React.js, Polkadot.js and antd UI.

- homepage
- Wallet connection and account list
- Transaction signature
- Video upload page
- Video upload progress page
- Video playback
- System login and logout
- My Video NFT Page
- Minting NFT page
- Listing/UnListing NFT page
- Buy NFT page
- Transfer NFT page

## Team :busts_in_silhouette:

### Team members

- Hayes White
- Justin Liu
- Jack Chen

### Contact

- **Contact Name:** Hayes White
- **Contact Email:** lostinwind@protonmail.com

### Team's experience

CONTRACT LAB is a Web3 team committed to providing digital asset management and Web3 technology solutions to global enterprises. Founded in February 2018, we are headquartered in Hong Kong with offices in London, Beijing, and Guangzhou. Our services include one-stop solutions, customized Web3 projects, and incubation services for Web3 startups. We use technological innovation to optimize user experience and provide secure and reliable products, striving to make entering the world of Web3 simpler for users.

Our core team members come from early blockchain communities and projects, with years of technical development experience. Our solutions cover a wide range of business scenarios, including public chains, wallets, exchanges, NFTs, DeFi, and mining pools, and we are proficient in the latest technologies such as smart contracts, cross-chain, L2, ZKP, multi-signature, oracle, IOT, and more. We are well-equipped to provide the highest quality digital asset management and Web3 technology solutions to enterprises and comprehensive incubation services to Web3 startups to achieve their business goals and accelerate growth.

### Team Code Repos

- https://github.com/contract-lab-collections

Team Members:

- https://github.com/lost-inwind
- https://github.com/JustinQP
- https://github.com/jackchen0120

## Development Status :open_book:

The result of our research regarding the solutions and architecture has been described in above.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 28,000 USD

### Milestone — Basic functionality

- **Estimated duration:** 2 months
- **FTE:**  2
- **Costs:** 18,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how use the product, display and explain the function of each component. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1. | Smart contract: videown-nft | We will deliver a ink! smart contract that will realize the function of NFT market and comply with [psp-34](https://github.com/w3f/PSPs/blob/master/PSPs/psp-34.md). |
| 2. | Backend: videown-server | We will deliver a golang server that will provide api for frontend and interact with the CESS chain |

### Milestone 2 — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  2
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how use the product, display and explain the function of each component. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains the problems VIDEOWN solves and how it can benefit other projects. |
| 1. | Backend: CMPS | We will deliver a golang server that will provide api focus on file processing for frontend. |
| 2. | Frontend: videown-web | We will deliver a website that users can use the functions of VIDEOWN. |

## Future Plans

- Creator economy model design and realize
- Smart contract optimization design
- Network-wide video accurate rights confirmation system
- Ad slot auction system
- Large file processing system

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Twitter
