# Praze

* **Team Name:** Praze
* **Payment Address:** 14g8BwU9erExNomJUDjRq4SZxRDoNYZ3kG7FEfdJipyURKiB

---

## Project Overview

### Overview

* **Tagline:** Empowering creators with on-chain tipping.

* **Description:** Praze is a platform where creators can earn DOT, KSM, and testnet tokens directly from their supporters. They can set up a custom profile, offer exclusive content, sell digital downloads, and run memberships—all powered by ink! smart contracts on Polkadot. With a clean interface and creator-first tools, Praze makes on-chain monetization easy, elegant, and built for the Polkadot ecosystem.

* **Relation to ink!:** All monetization logic (tipping, membership access, paywalls, downloadable content validation) will be built with ink! smart contracts deployed on a supported testnet and AssetHub.

* **Category:** Canary Dapp

* **Team's Motivation:** We’re passionate about enabling creators in the Polkadot ecosystem to succeed. We believe creators are underrepresented in on-chain tooling, and Praze helps them be rewarded in a way that feels native, elegant, and sustainable. The current landscape is dominated by generic tipping tools; Praze sets a new standard.

---

## Ink! Ecosystem Impact

* **Practical Use Case:** Praze will be one of the first full-featured creator monetization platforms built with ink!. It will demonstrate ink!'s power to go beyond infrastructure and deliver end-user value in elegant applications.

* **Showcase Potential:** We will document the smart contract design in a Medium post, open-source the contracts, and deploy them to Polkadot AssetHub and a testnet.

* **Ecosystem Benefit:** This project will:

  * Onboard more creators to Polkadot.
  * Showcase how ink! smart contracts can handle nuanced business logic like gated access and recurring memberships.
  * Serve as a boilerplate dapp reference for others building consumer-grade apps using ink!.

* **Business Case:** While not monetized via tokens, Praze introduces a sustainable model for creators to earn DOT/KSM directly and build their micro-economies, increasing token velocity in the ecosystem.

---

## Project Details

* **Data Models / APIs:**

  * User Profile

    * `id`, `name`, `bio`, `image`, `links`, `theme`
  * Creator Assets

    * `type`, `title`, `price`, `content_url`, `access_rules`
  * Tips/Memberships

    * `creator_id`, `supporter_id`, `amount`, `timestamp`, `access_granted`

* **Tech Stack:**

  * Frontend: Svelte + Tailwind
  * Contracts: ink! (v6) + Polkadot.js for wallet interaction
  * Backend: Supabase for metadata and analytics

* **PoC / MVP:**

  * Working MVP at [https://dotme-two.vercel.app/](https://dotme-two.vercel.app/) (formerly dotme)
  * MVP supports wallet connect, profile creation, and DOT tipping (static for now)

* **Need Audit:** YES

* **Category:** Canary Dapp

* **Business Model:**

  * Platform will not take a cut from creators at launch
  * Future: optional premium analytics/dashboard for creators

* **Growth Strategy:**

  * Start on testnet with curated creators
  * Launch a leaderboard campaign to drive usage
  * Expand to mobile-friendly views and embeddable widgets

---

## 👥 Team

* **Team Name**: Solo developer (Abinash)
* **Contact Name**: Abinash Sahoo
* **Contact Email**: [implabinash@gmail.com](mailto:implabinash@gmail.com)
* **Website**: [https://dotme-two.vercel.app/](https://dotme-two.vercel.app/)

### Team Members

* Abinash Sahoo (solo developer)
* **Contact Email**: [implabinash@gmail.com](mailto:implabinash@gmail.com)

### LinkedIn Profiles

* N/A

### Legal Structure

* N/A

### Team Code Repos

* Dotme: [https://github.com/implabinash/dotme](https://github.com/implabinash/dotme)
* Praze: [https://github.com/implabinash/praze](https://github.com/implabinash/praze)

### Team GitHub Accounts

* [https://github.com/implabinash](https://github.com/implabinash)

### Team's experience

Abinash Sahoo:

* In blockchain since 2022, in the Polkadot ecosystem since 2024
* Built 4–5 Rust CLIs with over 4,500 downloads
* Built various web apps using SvelteKit
* Strong background in product design, smart contract platforms

## Development Status

* MVP at [https://dotme-two.vercel.app/](https://dotme-two.vercel.app/)
* Forum conversation: [https://forum.polkadot.network/t/introducing-dotme-support-your-favorite-creators-with-dot/12870](https://forum.polkadot.network/t/introducing-dotme-support-your-favorite-creators-with-dot/12870)
* Video demo: [https://x.com/implabinash/status/1922288543142986118](https://x.com/implabinash/status/1922288543142986118)
* **Praze redesign:**
  * [https://x.com/implabinash/status/1924854114917482994](https://x.com/implabinash/status/1924854114917482994)
  * [https://x.com/implabinash/status/1925574537954955760](https://x.com/implabinash/status/1925574537954955760)

## Development Roadmap

### Overview

* **Total Estimated Duration:** 5 months
* **FTE:** 1.5 FTE
* **Total Cost:** \$48,000 USD

### Milestone 1 Profile Management & Customization

* **Estimated Duration:** 0.75 month
* **FTE:** 1
* **Cost:** \$7,000 USD

| Number | Deliverable          | Specification                                                         |
| ------ | -------------------- | --------------------------------------------------------------------- |
| 0a     | License              | Apache 2.0                                                            |
| 0b     | Documentation        | Inline and online documentation of smart contracts and platform logic |
| 0c     | Testing & Guide      | Comprehensive unit tests and usage documentation                      |
| 0d     | Article & Updates    | Blog post + forum/social updates announcing feature launch            |
| 1      | Creator Dashboard | Edit avatar, banner, name, username, bio, predefined tip amounts, wallet address |
| 2      | Theming Tools     | Theme/color selector with public preview                                         |
| 3      | Social Links      | Dynamic links to social media                                                    |

### Milestone 2 — Creator Discovery & Leaderboards

* **Estimated Duration:** 1 month
* **FTE:** 1.5
* **Cost:** \$8,000 USD

| Number | Deliverable          | Specification                                                         |
| ------ | -------------------- | --------------------------------------------------------------------- |
| 0a     | License              | Apache 2.0                                                            |
| 0b     | Documentation        | Inline and online documentation of smart contracts and platform logic |
| 0c     | Testing & Guide      | Comprehensive unit tests and usage documentation                      |
| 0d     | Article & Updates    | Blog post + forum/social updates announcing feature launch            |
| 1      | Creator Directory | Search by name/tags, verified creators          |
| 2      | Leaderboards      | Weekly/monthly most tipped creators             |

### Milestone 3 — Analytics & Dashboard

* **Estimated Duration:** 1 month
* **FTE:** 1.5
* **Cost:** \$10,000 USD

| Number | Deliverable          | Specification                                                         |
| ------ | -------------------- | --------------------------------------------------------------------- |
| 0a     | License              | Apache 2.0                                                            |
| 0b     | Documentation        | Inline and online documentation of smart contracts and platform logic |
| 0c     | Testing & Guide      | Comprehensive unit tests and usage documentation                      |
| 0d     | Article & Updates    | Blog post + forum/social updates announcing feature launch            |
| 1      | Creator Analytics | Total tips, unique supporters, tip time heatmaps |
| 2      | Top Supporters    | Display top supporters and tip insights          |

### Milestone 4 — DOT, KSM, and Testnet Token Support

* **Estimated Duration:** 0.75 month
* **FTE:** 1
* **Cost:** \$5,000 USD

| Number | Deliverable          | Specification                                                         |
| ------ | -------------------- | --------------------------------------------------------------------- |
| 0a     | License              | Apache 2.0                                                            |
| 0b     | Documentation        | Inline and online documentation of smart contracts and platform logic |
| 0c     | Testing & Guide      | Comprehensive unit tests and usage documentation                      |
| 0d     | Article & Updates    | Blog post + forum/social updates announcing feature launch            |
| 1      | Token Handling | Accept DOT, KSM, and 1 testnet token with contract logic |

### Milestone 5 — Paywalled Downloadables and Memberships

* **Estimated Duration:** 1.5 months
* **FTE:** 1.5
* **Cost:** \$18,000 USD

| Number | Deliverable          | Specification                                                         |
| ------ | -------------------- | --------------------------------------------------------------------- |
| 0a     | License              | Apache 2.0                                                            |
| 0b     | Documentation        | Inline and online documentation of smart contracts and platform logic |
| 0c     | Testing & Guide      | Comprehensive unit tests and usage documentation                      |
| 0d     | Article & Updates    | Blog post + forum/social updates announcing feature launch            |
| 1      | ink! Smart Contracts | Membership validation, downloadable gating logic                      |
| 2      | Gated Downloads      | Access control for files and resources                                |

## Future Plans

* **Post-Grant Development**: Add ecosystem integrations (e.g., Discord bot, embeddable widgets)
* **Messaging**: In future, we will let supporters talk to their creators and support anonymous messaging from supporters.  
* **Vision**: Establish Praze as Polkadot’s go-to creator monetization tool, driving adoption and transactions across the ecosystem and beyond.

## Additional Information

**How did you hear about the Bounty Program?** Twitter and forum announcements

* **Forum Post**: [https://forum.polkadot.network/t/introducing-dotme-support-your-favorite-creators-with-dot/12870](https://forum.polkadot.network/t/introducing-dotme-support-your-favorite-creators-with-dot/12870)
* **Demo Tweet**: [https://x.com/implabinash/status/1922288543142986118](https://x.com/implabinash/status/1922288543142986118)
* **Website URL**: [https://dotme-two.vercel.app/](https://dotme-two.vercel.app/)
* **My Dotme Page**: [https://dotme-two.vercel.app/u/implabinash](https://dotme-two.vercel.app/u/implabinash)
* **Work Done**: MVP built and live, with positive community feedback on X [@implabinash](https://x.com/implabinash).
* **No Other Teams**: Solo project.
* **Other Funding**: No other funding applications submitted; this is Praze's first grant request.

Additional Notes:

* Praze was formerly called DotMe
* Rebranded to Praze to reflect broader token support and deeper purpose: creators don’t just get tips, they get praised.
