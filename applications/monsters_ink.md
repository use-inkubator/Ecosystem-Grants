# Monster's Ink

> Learn ink! by creating an adorable monster on chain.

- **Team Name:** Monster's Ink

- **Payment Addresses:**

Funds to be split equally between:

13FCfaFfzzqPJ7LxVGkjgxmqbpv3RCfCW6BgXqxGJj5v6Y2J (github: owenb)

1X7mSKF4UGiMTZnGK2iKKiLZH7SksTvoakdLyJ3Q2XdQFLk (github: forever8896)

## Project Overview :page_facing_up:

### **Vision: The Future of Developer Education**

Monster's Ink represents a revolutionary approach to blockchain education, transforming dry technical tutorials into an emotionally engaging creative journey. By combining cutting-edge AI-generated art with hands-on ink! development, we're creating the first AI-powered gamified smart contract learning platform for the Polkadot ecosystem.

Imagine developers worldwide discovering ink by nurturing their own unique, AI-generated 3D monster from egg to magnificent creature. Each coding lesson they complete unlocks new customization features—changing colors, textures, lighting, and magical attributes—starting with an NFT minted after the first lesson that evolves to showcase both their technical achievement and creative vision.

### **Ecosystem-Wide Impact & Partnership Vision**

Monster's Ink is designed as a foundational educational asset for the entire **ink! ecosystem**, creating unprecedented opportunities for collaboration and growth:

**🚀 Developer Onboarding at Scale:** Transform technical barriers into creative adventures, dramatically increasing ink! adoption rates by making blockchain development approachable and rewarding.

**🎨 Viral Marketing Through Art:** Each unique monster NFT becomes a shareable work of art, organically promoting Polkadot across social media as developers proudly display their creations.

**🤝 Ecosystem Partnership Hub:** The extensible platform enables seamless integration with Ink Alliance partners. Imagine branded monster variations for different parachains, special achievements for ecosystem milestones, or collaborative educational campaigns.

**📈 Sustainable Growth Foundation:** The modular architecture supports infinite expansion possibilities: advanced ink! courses, Substrate development tracks, XCM integration tutorials, and custom educational experiences for enterprise partners.

### **Creative & Technical Innovation**

**Revolutionary 3D Pipeline:** Leveraging OpenAI's GPT-Image-1 and fal.ai's cutting-edge image-to-3D technology, every monster is uniquely generated and transformed into a rotatable, customizable 3D masterpiece displayed on the fly through Three.js.

**Progressive Gamification:** Users begin with a mysterious egg that cracks to reveal their nascent creature. As they master ink! concepts through hands-on coding, they unlock increasingly sophisticated customization options—from basic colors to advanced materials, lighting effects, and magical backgrounds.

**Community-Driven Expansion:** Built on an extensible JSON lesson framework, the platform invites the entire ink! community to contribute new educational content, ensuring continuous evolution and relevance as the ecosystem grows. (Note: Although anyone can create lessons, the Ink! Team will be responsible for curation.)

### **Technical Architecture & User Experience**

**CATEGORY:** Canary Dapp

**Technology Stack:**

- **Smart Contracts:** ink! v6
- **Frontend:** React/Next.js with Three.js for 3D visualization
- **Backend:** Node.js with Express framework
- **Database:** PostgreSQL for user data and lesson progress
- **Authentication:** GitHub OAuth integration
- **Infrastructure:** Docker containers for pop-cli compilation service
- **APIs:** OpenAI GPT-Image-1, fal.ai image-to-3D, OpenAI content moderation

**The Magic Behind the Monsters:**

Our revolutionary 3D monster generation pipeline creates truly unique creatures for each developer:

1. **AI-Powered Creature Generation:** Using OpenAI's GPT-Image-1, we generate distinctive Spore-like monsters through carefully crafted template prompts that capture each user's lesson progress and customization choices.
2. **3D Transformation:** fal.ai's cutting-edge image-to-3D technology converts each 2D monster into a fully manipulatable 3D model (.glb format) in 30-60 seconds, with engaging progress screens to maintain user engagement during generation.
3. **Interactive 3D Playground:** Advanced Three.js integration provides a sophisticated yet intuitive interface where developers can adjust lighting, materials, backgrounds, and magical effects at 1024x1024 resolution.
4. **Dynamic NFT Creation:** After completing lesson 1, users mint a dynamic NFT on Polkadot AssetHub that evolves with their learning progress. The NFT's image updates automatically through server-side generation as users customize their monster through subsequent lessons.

**Progressive Learning Journey:**

- **Progressive Monster Evolution:** Users experience distinct stages within their learning journey:

  1. **Initial Stages:** Start with a mysterious egg that progresses through early lesson stages
  2. **Stage 3 of Lesson 1:** Egg cracks to reveal creature emerging (spiny tentacles visible, triggers GitHub OAuth requirement)
  3. **Post-Authentication:** Two AI-generated monster evolution stages - young monster and grown-up monster - with unlimited personalization options

- **Strategic Authentication:** GitHub OAuth integration occurs at stage 3 of lesson 1, before any custom AI generation begins. This optimizes user experience while protecting expensive server resources from abuse.
- **Hands-On Validation:** Real code compilation through Dockerized pop-cli ensures genuine learning, with immediate feedback and helpful error guidance.

**Extensible Learning Framework:**

Built on a comprehensive JSON schema that enables the entire ink! community to contribute new lessons, challenges, and creature customizations.

**Core Curriculum - "From Flipper to Creator":**

The platform launches with 5 core lessons that take users from zero to building complete ink!-powered experiences. Each lesson is split into progressive stages, ensuring a smooth journey from fundamentals to advanced integration. The architecture is fully extensible, enabling the community to add unlimited specialized lessons on ecosystem products and advanced techniques.

Initial Lesson Path:

1. ink! Fundamentals – Syntax, variables, data types, and core patterns

2. Advanced Development – Storage, constructors, state changes, testing, and key smart contract  
   Standards

3. Deployment & Integration – Build, deploy via pop-cli, and connect to frontends

Every stage blends technical learning with a creative monster-evolution theme, so users feel like they’re creating, not just coding—while gaining all the skills needed to develop full ink! applications.

## **Sustainability & Revenue Model**

### **Long-term Sustainability Strategy**

Upon successful demonstration of platform viability through the initial $2,000 AI credit allocation, Monster's Ink has multiple pathways to financial sustainability:

**Ecosystem Expansion:**

- **Multi-Product Course Offerings:** Expand beyond basic ink! to offer specialized courses for other Polkadot ecosystem products (Substrate, XCM, parachain development), each with unique monster variations and themes.
- **Commercial Partnerships:** Partner with Polkadot ecosystem projects to create branded monster variations featuring sponsor logos and project-specific educational content in exchange for course funding.
- **Premium Monster Collections:** Offer exclusive, limited-edition monster designs for advanced courses or special events (e.g. SubZero).

The modular lesson framework ensures minimal development overhead for content expansion, making each new course easy to add once the core platform is established.

## **AI Cost Analysis & Budget Allocation**

### **Cost Breakdown Per User Journey**

These are best guesses based on current API pricing research and usage patterns:

**Per Image Generation (including 20% tax):**

- **GPT-Image-1 (1024x1024, high quality):** $0.216 per image
- **fal.ai 3D Conversion:** $0.54 per 2D-to-3D conversion
- **OpenAI Content Moderation:** $0.00 (free service)
- **Cost per successful image + 3D conversion:** $0.756

**Per User Experience:**

- **Initial stages:** Egg progression (no AI generation costs)
- **Post-GitHub auth:** 2 AI-generated monster evolution stages (young + grown-up) × $0.756 = $1.512 per user
- **30% failure rate requiring retries:** $1.512 × 1.3 = $1.97 per user
- **Total cost per complete user journey:** $1.97

### **Development Phase Budget Allocation**

**AI Credit Allocation:** $2,000 **Docker/Hosting and Image Serving Infrastructure:** $1,000

This allocation enables:

- **~ 1,015 complete user journeys** ($2,000 ÷ $1.97)
- **~ 2,030 total successful monster generations** (1,015 users × 2 monsters each)
- **Expected user base:** ~1,000 users over first 3 months, providing budget for development/testing overhead and unexpected usage spikes
- **Secure Docker hosting** for the pop-cli compilation service, restricted to users who have authenticated via GitHub authentication to prevent abuse

### **Budget Flexibility & Real-Time Adaptation**

These allocations ($2,000 AI credits, $1,000 hosting) represent soft budgeting to demonstrate cost awareness and planning. The actual budget distribution will adapt in real-time based on observed usage patterns, user engagement, and operational requirements during development and launch phases.

In short, if people really love it, we'll find the money somehow!

### **Cost Efficiency Strategy**

The combined $3,000 operational allocation serves as a proof-of-concept budget. Once platform viability is demonstrated through user engagement and educational effectiveness, the sustainability pathways outlined above provide multiple revenue streams to cover ongoing operational costs while maintaining the platform's educational mission.

Note:

- This project is not a generic NFT marketplace. The focus is on the creation and minting process as a reward for learning.
- The initial version will not involve complex tokenomics beyond the NFT minting.
- This app will be designed for desktop/laptop/ipad browsers only - not mobile screens. We do not believe we can give people a great experience on mobile, at least not for now.

## **Platform Security & Integrity**

### **Developer-Focused Anti-Farming System**

To ensure NFTs reach legitimate developers while maintaining zero payment friction, we've implemented a GitHub-based verification system:

- **Staged GitHub OAuth Authentication:** Users progress through initial lesson stages with basic egg progression, then must authenticate via GitHub with verified email addresses at stage 3 of lesson 1, before any AI-generated monster customization or NFT minting occurs.
- **Repository Requirement:** At least one public repository required, ensuring participants have established coding presence. We can add additional ‘account age’ requirements in the future if necessary.
- **One Account = One NFT:** Database tracking and on-chain verification prevent multiple NFT mints per GitHub identity, with immutable linking between GitHub user IDs and minted NFTs.
- **Educational Integrity:** While some users may attempt to bypass educational content, the GitHub integration ensures NFTs primarily reach legitimate developers with established coding presence.

### **Content Safety & Technical Security**

- **Content Moderation:** All server-generated images pass through OpenAI's content moderation API before display or NFT creation, ensuring no inappropriate content can be minted.
- **DDoS Protection:** Dockerized pop-cli compilation service protected behind GitHub OAuth authentication prevents abuse and ensures stable performance.
- **Input Security:** User customization inputs are strictly limited to predefined options (dropdown menus, sliders) that map to safe template variables, eliminating prompt injection risks.
- **Service Resilience:** Robust retry mechanisms for API failures, comprehensive error handling, and graceful degradation maintain functionality during service interruptions.

### **Risk Assessment & Mitigation**

**Primary Technical Risks:**

- **DDoS Attacks:** Dockerized pop-cli service protected by GitHub OAuth authentication, rate limiting, and resource monitoring to prevent abuse of compilation resources.
- **AI Service Dependencies:** External API failures mitigated through retry logic, error handling, and cost monitoring to prevent budget overruns from failed generation attempts.
- **Security Vulnerabilities:** Input validation, content moderation, and secure authentication flows protect against malicious inputs and ensure platform integrity.
- **Scalability Challenges:** Modular architecture with database optimization, caching strategies, and monitoring systems enable graceful scaling as user adoption grows.

## Team :busts_in_silhouette:

### **Team members**

- Owen Barnes
- Kilián Valdman

### **Contact**

- **Contact Name:** Owen Barnes
- **Contact Email:** owen@owenbarnes.com
- **Website:** owenbarnes.com

### **Legal Structure**

N/A

### **Team's experience**

Our two-person team has a proven track record of creating compelling, user-centric applications within the Polkadot ecosystem. We were invited directly by the ink! team to submit this proposal based on our past work at the WebZero Hackathon in Berlin (July 2024).

Our team won three separate awards for our MonstersInk! project: the Polkadot Main Track prize, the UX Award, and the main Ink prize. This provides tangible evidence of our ability to deliver on the "beautiful design" and "emotional resonance" that is core to the Monster's Ink proposal.

The labor will be divided according to our specializations, with significant crossover:

- **Owen Barnes:** Full-stack web developer with extensive experience at Advertising.com/AOL, McKinsey and as tech lead at multiple London startups. Early web3 adopter (Bitcoin since 2013, attended Devcon 1) with deep expertise in frontend development, UI/UX design, and decentralized technologies. Creator of Poly.site and frequent speaker at technical conferences including Urbit Assembly, EthBrno, and Urbit Volcano Summit. Will lead Frontend, UI/UX, Graphics, and the Art Generation pipeline.

- **Kilián Valdman:** Self-taught blockchain developer with a proven track record building Web3 platforms—most notably allstake.io (NFT launches, raffles, auctions), plus apps like Cellular Domination Station (Game of Life–inspired game that placed Top 20 overall and 8th in Idea out of 105 entries in a game jam) and CrypTick (real-time crypto price alert app in Rust/Tauri/Svelte). Active developer for the Ronkeverse community on the Ronin blockchain, delivering NFT gaming applications and interactive Web3 experiences. Winner of multiple international hackathons, including ETHGlobal Cannes – Best Consumer App on Ronin, and a triple win at Polkadot Berlin (Main Track, Ink Alliance Bounty, UX Bounty). Specialized in smart contract architecture, scalable backend systems, and developer tooling. Will lead Backend, Lesson Content, pop-cli infrastructure, Dockerization, and code validation.

### **Team Code Repos**

- **MonstersInk! (WebZero Hackathon Winner):** [https://github.com/forever8896/inkverse](https://github.com/forever8896/inkverse)
- **WebZero Hackathon:** [https://www.joinwebzero.com/events/web3-summit-berlin](https://www.joinwebzero.com/events/web3-summit-berlin)

**GitHub accounts of all team members:**

- **Owen Barnes:** [https://github.com/owenb](https://github.com/owenb)
- **Kilián:** [https://github.com/forever8896](https://github.com/forever8896)

### **Team LinkedIn Profiles (if available)**

- **Owen Barnes:** [https://www.linkedin.com/in/owenbarnes/](https://www.linkedin.com/in/owenbarnes/)
- **Kilián:** Not available

## Development Status :open_book:

The project concept is well-defined, and a clear 9-week development roadmap has been planned across three focused milestones. The core technical architecture has been established, including the AI-powered 3D monster generation pipeline and phased code validation strategy. The curriculum design process and validation plan with the ink! team are in place, with budget allocations optimized for proof-of-concept success.

## Development Roadmap :nut_and_bolt:

### **Overview**

- **Total Estimated Duration:** 9 Weeks (3 milestones × 3 weeks each)
- **Full-Time Equivalent (FTE):** 2
- **Total Costs:** $50,000 USD

### **Milestone 1 — Pipeline Research & Proof-of-Concept (3 Weeks)**

- **Estimated duration:** 3 Weeks from project approval
- **FTE:** 2
- **Costs:** $18,000 USD

| Number  | Deliverable                    | Specification                                                                                                                                                                 |
| :------ | :----------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **0a.** | License                        | Apache 2.0                                                                                                                                                                    |
| **0b.** | Documentation                  | Technical feasibility report documenting pipeline testing results, quality metrics, API integration analysis, and cost validation with actual usage data.                     |
| **0c.** | Testing and Testing Guide      | Testing methodology and results for the complete pipeline: GPT-Image-1 → fal.ai → Three.js workflow with documented success/failure rates and quality assessments.            |
| **0d.** | Docker                         | Basic Docker environment setup for local development and testing of the AI generation pipeline components.                                                                    |
| 1\.     | Working Proof-of-Concept       | Functional (non-production) pipeline demonstrating: prompt input → GPT-Image-1 generation → fal.ai 3D conversion → Three.js browser display for at least 10 test monsters.    |
| 2\.     | Cost Optimization Research     | Detailed analysis of actual vs. projected costs, failure rate patterns, retry strategies, and recommendations for cost reduction without quality compromise.                  |
| 3\.     | Risk Assessment & Mitigation   | Comprehensive document identifying technical risks (API limitations, service dependencies, quality issues) with specific mitigation strategies for production implementation. |
| 4\.     | Foundation Architecture Design | Technical specifications and architectural plans for Milestones 2 & 3, including database schema, API design, and scalability considerations based on Milestone 1 findings.   |

### **Milestone 2 — Educational Platform & Lesson System (3 Weeks)**

- **Estimated duration:** 3 Weeks
- **FTE:** 2
- **Costs:** $18,000 USD

| Number  | Deliverable                    | Specification                                                                                                                                                                                      |
| :------ | :----------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **0a.** | License                        | Apache 2.0                                                                                                                                                                                         |
| **0b.** | Documentation                  | Comprehensive lesson schema documentation, curriculum extension guide, and educational methodology documentation for community contributors.                                                       |
| **0c.** | Testing and Testing Guide      | Full test coverage for lesson validation, code compilation testing, and educational progression tracking. Guide for testing lesson content and user code validation.                               |
| **0d.** | Docker                         | Production-ready Dockerfile for the `pop-cli` code validation service with security hardening.                                                                                                     |
| 1\.     | JSON Lesson Schema & Framework | Extensible JSON schema for lessons with validation, progression tracking, and community contribution workflows. Documentation for creating new lessons.                                            |
| 2\.     | Browser-based IDE              | Interactive coding environment with syntax highlighting, auto-completion, and real-time feedback for ink! development.                                                                             |
| 3\.     | Code Validation Service        | Secure, scalable `pop-cli` service for compiling and testing user-submitted ink! code with detailed error reporting and educational feedback.                                                      |
| 4\.     | Initial Lesson Content         | Complete draft curriculum "From Flipper to Creator" - 5 comprehensive lessons, each containing multiple steps, covering fundamental to advanced ink! concepts. Reviewed and approved by ink! team. |
| 5\.     | User Progression System        | Monster evolution system tied to lesson stage completion, with GitHub authentication integration and dynamic NFT updating.                                                                         |

### **Milestone 3 — Production Polish & Deployment (3 Weeks)**

- **Estimated duration:** 3 Weeks
- **FTE:** 2
- **Costs:** $14,000 USD (includes $3,000 for operational costs: AI credits and hosting infrastructure)

| Number  | Deliverable               | Specification                                                                                                                            |
| :------ | :------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------- |
| **0a.** | License                   | Apache 2.0                                                                                                                               |
| **0b.** | Documentation             | Complete system documentation, deployment guides, maintenance procedures, and handover documentation for ink! team.                      |
| **0c.** | Testing and Testing Guide | End-to-end testing suite, load testing, browser testing, and comprehensive testing documentation for all system components.              |
| **0d.** | Docker                    | Production deployment configuration with Docker Compose for full application stack.                                                      |
| **0e.** | Article & Communication   | Medium article about the project, Polkadot Forum posts with regular updates, and tutorial documentation for AssetHub deployment.         |
| 1\.     | Production Error Handling | Comprehensive error handling, logging, monitoring, and graceful degradation for all system components including AI service failures.     |
| 2\.     | Performance Optimization  | Optimized asset loading, 3D model compression, caching strategies, and performance monitoring for production-scale usage.                |
| 3\.     | Analytics Dashboard       | Basic administrative dashboard showing user engagement metrics, lesson completion rates, drop-off points, and platform usage statistics. |
| 4\.     | Production Deployment     | Fully deployed application on public URL with monitoring, analytics, and handover documentation for long-term ink! team maintenance.     |

## **Future Plans & Maintenance**

### **Ecosystem-Wide Impact**

Monster's Ink is designed as a foundational resource for the entire **ink!** ecosystem. Upon completion, this platform will serve as a shared educational asset benefiting all alliance members, from core developers to parachain teams, fostering broader ecosystem growth and developer onboarding across the Polkadot landscape.

### **Project Handover & Sustainability**

Upon successful completion and launch, the Monster's Ink project, including all code and assets, will be handed over to the core ink! team for long-term maintenance, hosting, and community support. This arrangement was initiated by the ink! team and has been agreed upon prior to this application. Our team's role is to deliver a complete, well-documented, and production-ready system within the 9-week grant period.

The extensible lesson format is designed to allow the ink! team and the wider community to contribute new content easily, ensuring the platform remains a relevant and evolving resource.

### **Future Collaboration Potential**

This initial project represents an opportunity to establish effective collaboration patterns between our team and the ink! ecosystem. Success here could naturally lead to future educational initiatives, though our immediate focus remains on delivering exceptional value through this foundational platform.

## **Communication & Community Engagement**

In accordance with ink!ubator program requirements, our team commits to:

- **Polkadot Forum Engagement:** Create a dedicated project thread on the Polkadot Forum immediately following grant approval, providing regular milestone updates and community engagement throughout the development process.
- **Medium Publication Strategy:** Publish a comprehensive Medium article documenting the deployed smart contract usage on Polkadot AssetHub Testnet, demonstrating practical ink! implementation patterns.
- **Final Documentation & Tutorial:** Upon project completion, publish a detailed Medium tutorial covering the complete Monster's Ink platform usage, educational methodology, and technical architecture to serve as a reference for future ink! projects.
- **AssetHub Deployment:** Deploy example ink! smart contracts to Polkadot AssetHub Testnet with comprehensive usage documentation and tutorials.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** We were invited to apply by the ink! team.
