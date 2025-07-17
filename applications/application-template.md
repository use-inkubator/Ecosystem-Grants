# PetChain

# PetChain

## Project Overview

**PetChain** is a decentralized platform for managing pet health records on-chain using ink! smart contracts. We solve the long-standing problem of fragmented, inaccessible, or lost veterinary data by building a privacy-first, globally accessible system that keeps pets safer and their care more consistent.

Pets are issued scannable smart tags linked to their medical records. These tags provide critical health data in real time—useful in emergencies or when visiting a new clinic. Pet owners can share vaccination history publicly or grant temporary full access to a vet, using zk-proofs to protect sensitive data. This creates a collaborative, tamper-proof medical system for animal care.

While our MVP is already underway on StarkNet, we aim to port core features to ink! for AssetHub deployment to expand interoperability and contribute to Polkadot’s smart contract ecosystem.

---

## Team Members

- **Name:** Llins Omoudu 
- **GitHub:** https://github.com/llinsss
- **Role:** Product Lead/co-founder 
- **Experience:** Full-stack blockchain developer with experience in smart contract integrations.

-  **Name:** Aliyu Ahmad
- **Github:** https://github.com/xaxxoo
- **Role:** Technical Lead/ co-founder
- **Experience:** Backend Developer and blockchain dev

---

## Project Details

### Problem

Pet medical data today is siloed across paper files, inaccessible PDFs, or non-interoperable vet software. 
This causes:
- Missed or duplicated treatments
- Delays in emergency response
- No continuity of care when switching providers

### Solution

PetChain enables permanent, tamper-proof, zero-trust storage and sharing of pet health records. Records are accessible via QR-tag, with customizable access permissions and zk-based privacy guarantees.

### Features

1. **Scannable Smart Tags:** QRcode tags link to live, minimal-reserve public data (e.g., emergency info), with a private vault accessed when you scan the tag.
2. **Medical Record Ledger:** Written in ink! and stored on AssetHub (Polkadot), with updates pushed via permissioned channels.
3. **Privacy Layer:** Selective disclosure of data using zk-proofs; customizable by the pet owner.
4. **Alerts & Notifications:** Auto-reminders for vaccination dates and treatments.
5. **Offline Mode:** Display basic data via cached tag scan, even without internet.
6. **Clinic Integration:** API and SDK for vet practices to upload new entries or pull past data securely.

## Roadmap and Milestones

### Milestone 1 – Core ink! Contract and AssetHub Deployment
- Build core smart contract in ink! for pet profiles and medical logs.
- Enable QR-to-data mapping (read-only access).
- Deploy contract to AssetHub.
- Document usage.

### Milestone 2 – Privacy Layer + zkProof Sharing
- Owner-signed permission for full record access.
- Build test zk circuits.
- Publish tutorial and Medium article.

### Milestone 3 – Tag System and Frontend Demo
- Connect scannable tag flow (tag > contract call > permission check).
- Build frontend mockup (React or PolkadotJS).
- Offline data fallback support.
- Public GitHub + Documentation.

---

## Innovation

PetChain is one of the first zk-integrated, medically focused smart contract systems using ink!. Unlike Solidity-based solutions, we’re building with ink! to demonstrate:
- Modular contract architecture
- Privacy-first recordkeeping on public chains

## Ecosystem Impact

We aim to:
- Onboard vet clinics and emergency responders into Polkadot's ecosystem.
- Create real-world traction for ink! by solving a physical-world problem.
- Offer privacy tooling (zk templates, access management libraries) to other ink! developers.

---

## License

All code will be licensed under **MIT** and fully open source. No external proprietary dependencies.

---

## Funding Request

**Amount:** $50,000 in DOT  
To cover:
- ink! development (3–4 months)
- zk integration (circuit dev + logic)
- Tag hardware integration (demo only)
- Community documentation and forum engagement

## Maintenance

Post-grant, PetChain will continue as a standalone startup. We’re building a business around interoperable pet health infrastructure across chains, with ink! forming the backbone of the Polkadot version.

We commit to:
- Open-source maintenance
- Forum support
- Regular contract audits as we grow

## Links

- Website (Coming Soon)
- Temp site:  https://pet-chain-frontend-tmqq-99r37ln4i.vercel.app/
- Github repo: https://github.com/orgs/DogStark/repositories
- Telegram Community: https://t.me/+fLbWYLN8jZw3ZTNk




