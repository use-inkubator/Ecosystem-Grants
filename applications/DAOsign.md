#  Wasm Smart Contract Bounty (Ink!)

- **Team Name:** DAosign
- **Payment Address:** cidt.eth 


## Project Overview :page_facing_up:
### Overview

Please provide the following:

- Project description: Trade pairs liquidity system
- A brief description of the template building: see deliverables. 
- An indication of how your project relates to ink! ecosystem: implementation of Uniswap-like functionality on !ink
- Choosen project idea category or your alternative category with explanation of its importance
- An indication of why your team is interested in creating this project: 

### Project Details

We expect the teams to already have a solid idea about the project expected final state. Therefore, we ask the teams to submit (where relevant):

- Data models / API specifications of the core functionality:
see RUST interfaces below:

```rs
type Balance = <ink::env::DefaultEnvironment as ink::env::Environment>::Balance;
type AccountId = <ink::env::DefaultEnvironment as ink::env::Environment>::AccountId;
type Hash = <ink::env::DefaultEnvironment as ink::env::Environment>::Hash;
​
/// The ERC-20 error types.
#[derive(Debug, PartialEq, Eq, scale::Encode, scale::Decode)]
#[cfg_attr(feature = "std", derive(scale_info::TypeInfo))]
pub enum Error {
    /// Returned if not enough balance to fulfill a request is available.
    InsufficientBalance,
    /// Returned if not enough allowance to fulfill a request is available.
    InsufficientAllowance,
}
​
#[ink::trait_definition]
pub trait ERC20 {
    #[ink(message)]
    fn name(&self) -> String;
​
    #[ink(message)]
    fn symbol(&self) -> String;
​
    #[ink(message)]
    fn decimals(&self) -> u8;
​
    #[ink(message)]
    fn total_supply(&self) -> Balance;
​
    #[ink(message)]
    fn balance_of(&self, owner: AccountId) -> Balance;
​
    #[ink(message)]
    fn allowance(&self, owner: AccountId, spender: AccountId) -> Balance;
​
    #[ink(message)]
    fn transfer(&mut self, to: AccountId, value: Balance) -> Result<(), ()>;
​
    #[ink(message)]
    fn approve(&mut self, spender: AccountId, value: Balance) -> Result<(), ()>;
​
    #[ink(message)]
    fn transfer_from(&mut self, from: AccountId, to: AccountId, value: Balance) -> Result<(), ()>;
}
​
#[ink::trait_definition]
pub trait InkswapERC20: ERC20 {
    #[ink(message)]
    fn domain_separator(&self) -> Hash;
​
    #[ink(message)]
    fn permit_typehash(&self) -> Hash;
​
    #[ink(message)]
    fn nonces(&self, owner: AccountId) -> u128;
​
    #[ink(message)]
    fn permit(
        &mut self,
        owner: AccountId,
        address: AccountId,
        value: Balance,
        deadline: u128,
        v: u8,
        r: Hash,
        s: Hash,
    ) -> Result<()>;
}
​
#[ink::trait_definition]
pub trait InkswapERC20: InkswapERC20 {
    #[ink(message)]
    fn minimum_liquidity(&self) -> u256;
​
    #[ink(message)]
    fn factory(&self) -> AccountId;
​
    #[ink(message)]
    fn token0(&self) -> AccountId;
​
    #[ink(message)]
    fn token1(&self) -> AccountId;
​
    #[ink(message)]
    fn get_reserves(&self) -> (u112, u112, u32);
​
    #[ink(message)]
    fn price0_cumulative_last(&self) -> Balance;
​
    #[ink(message)]
    fn price1_cumulative_last(&self) -> Balance;
​
    #[ink(message)]
    fn k_last(&self) -> u128;
​
    #[ink(message)]
    fn mint(&mut self, to: AccountId) -> Result<Balance, ()>;
​
    #[ink(message)]
    fn burn(&mut self, to: AccountId) -> Result<(Balance, Balance), ()>;
​
    #[ink(message)]
    fn swap(
        &mut self,
        amount0_out: Balance,
        amount1_out: Balance,
        to: AccountId,
        data: [u8],
    ) -> Result<()>;
​
    #[ink(message)]
    fn skim(&mut self, to: AccountId) -> Result<()>;
​
    #[ink(message)]
    fn sync(&mut self) -> Result<()>;
​
    #[ink(message)]
    fn initialize(&mut self, t1: AccountId, t2: AccountId) -> Result<()>;
}
​
#[ink::trait_definition]
pub trait InkswapFactory {
    #[ink(message)]
    fn fee_to(&self) -> AccountId;
​
    #[ink(message)]
    fn fee_to_setter(&self) -> AccountId;
​
    #[ink(message)]
    fn get_pair(&self, token_a: AccountId, token_b: AccountId) -> Result<AccountId, ()>;
​
    #[ink(message)]
    fn all_pairs(&self, num: u128) -> [AccountId];
​
    #[ink(message)]
    fn all_pairs_length(&self) -> u128;
​
    #[ink(message)]
    fn create_pair(&mut self, token_a: AccountId, token_b: AccountId) -> Result<AccountId, ()>;
​
    #[ink(message)]
    fn set_fee_To(&mut self, addr: AccountId) -> Result<(), ()>;
​
    #[ink(message)]
    fn set_fee_to_setter(&mut self, addr: AccountId) -> Result<(), ()>;
}
​
#[ink::trait_definition]
pub trait InkswapRouter {
    #[ink(message)]
    fn factory(&self) -> AccountId;
​
    #[ink(message)]
    fn add_liquidity(
        &mut self,
        token_a: AccountId,
        token_b: AccountId,
        amount_adesired: Balance,
        amount_bdesired: Balance,
        amount_amin: Balance,
        amount_bmin: Balance,
        to: AccountId,
        deadline: u32,
    ) -> Result<(Balance, Balance, Balance), ()>;
​
    #[ink(message)]
    fn remove_liquidity(
        &mut self,
        token_a: AccountId,
        token_b: AccountId,
        liquidity: Balance,
        amount_amin: Balance,
        amount_bmin: Balance,
        to: AccountId,
        deadline: u32,
    ) -> Result<(Balance, Balance), ()>;
​
    #[ink(message)]
    fn remove_liquidity_with_permit(
        &mut self,
        token_a: AccountId,
        token_b: AccountId,
        liquidity: Balance,
        amount_amin: Balance,
        amount_bmin: Balance,
        to: AccountId,
        deadline: u32,
        approve_max: bool,
        v: u8,
        r: Hash,
        s: Hash,
    ) -> Result<(Balance, Balance), ()>;
​
    #[ink(message)]
    fn swap_exact_tokens_for_tokens(
        &mut self,
        amount_in: Balance,
        amount_out_min: Balance,
        path: [AccountId; 2],
        to: AccountId,
        deadline: u32,
    ) -> Result<[Balance], ()>;
​
    #[ink(message)]
    fn swap_tokens_for_exact_tokens(
        &mut self,
        amount_out: Balance,
        amount_in_max: Balance,
        path: [AccountId; 2],
        to: AccountId,
        deadline: u32,
    ) -> Result<[Balance], ()>;
​
    #[ink(message)]
    fn quote(
        &self,
        amount_a: Balance,
        reserve_a: Balance,
        reserve_b: Balance,
    ) -> Result<Balance, ()>;
​
    #[ink(message)]
    fn get_amount_out(
        &self,
        amount_in: Balance,
        reserve_in: Balance,
        reserve_out: Balance,
    ) -> Result<Balance, ()>;
​
    #[ink(message)]
    fn get_amount_in(
        &self,
        amount_out: Balance,
        reserve_in: Balance,
        reserve_out: Balance,
    ) -> Result<Balance, ()>;
​
    #[ink(message)]
    fn get_amounts_out(&self, amount_in: Balance, path: [AccountId; 2]) -> Result<[Balance], ()>;
​
    #[ink(message)]
    fn get_amounts_in(&self, amount_out: Balance, apath: [AccountId; 2]) -> Result<[Balance], ()>;
}
```
- An overview of the technology stack to be used: Rust, !ink
- Documentation of core components, protocols, architecture, etc. : to be deployed
- PoC/MVP or other relevant prior work or research on the topic: we only have a detailed desciption of the workflow of the project, would be happy to provide per request.
- What your project is _not_ or will _not_ provide or implement : not sure, what to say. 
  - This is a place for you to manage expectations and to clarify any limitations that might not be obvious:
Rust monorepository with the source code, and some basic UI for the functionality (can be discussed further)


Things that shouldn’t be part of the application:
- The (future) tokenomics of your project 
- For non-infrastructure projects—deployment and hosting costs, maintenance or audits
- Business-oriented activities (marketing, business planning), events or outreach

## Team :busts_in_silhouette:

### Team members

- Ramil Amerzyanov, Technical lead
- Ilnur Galiev, Rust developer

### Contact

- **Contact Name:** Oleksandra Burmenska
- **Contact Email:** oleksandra@consideritdone.tech 
- **Website:** consideritdone.tech

### Legal Structure

- **Registered Address:** Illinois, Chicago
- **Registered Legal Entity:** Consideritdone LLC

### Team's experience

Please see our portfolio here: https://docsend.com/view/fjrvjtyzgm7wgrkj

### Team Code Repos

https://github.com/ConsiderItDone


Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/ramilexe
- https://github.com/n0cte

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/ramil-amerzyanov/
- https://www.linkedin.com/in/ilnur-galiev-9a587375/


## Development Status :open_book:

- links to your research diary, blog posts, articles, forum discussions or open GitHub issues: see our project portfolio: https://docsend.com/view/fjrvjtyzgm7wgrkj
- references to conversations you might have had related to building this template, : all is kept in the private corporative slack, but would be happy to discuss it further with you. 

## Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. Since these will be part of the agreement, it helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**.

> :exclamation: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Overview

- **Total Estimated Duration:** 4-5 weeks
- **Full-Time Equivalent (FTE):**  1.5 FTE
- **Total Costs:** 20 000

### Milestone 1  — Basic functionality

- **Estimated duration:** 1 month
- **FTE:**  1,5
- **Costs:** 30 000

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Core contract token + tests  | We will create a basic contract token and cover the code with tests |
| 2. | Trade pair token + tests| We will develop a trade pair token and cover the code with tests|
| 3. | Trade pair fabric contract + tests | We will create a trade pair fabric contract and cover the code with tests |
| 4. | Router contract realization + tests | We will develop a router contract and vocer it with tests |
| 5. | E2E tests| Additionally we will provide end to end tests |




## Future Plans

Support the tool and share it with the community.

## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?** Medium / Twitter / Element / Announcement by another team / **personal recommendation** / etc.

Our team had been working on a bunch of Polkadot projets including Nodle - 11th Parachain, and have a lot of experience with WASM VM. 
