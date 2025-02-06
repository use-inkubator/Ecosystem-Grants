# Lotto

- **Team Name:** Lucky Team
- **Payment Address:** 14ogWEsaFHYk1rDcRMLVApekUd3np4e1ker81tBF6odd39Q9

## Project Overview :page_facing_up:
### Overview

We would like to build some games with ink! smart contracts and phat contracts.  
Now that we have released the offchain rollup request-response for ink! smart contracts and three decentralized oracles (price feed, vrf, graph api oracle), we would like to build some games on Astar Network to have fun on the community and promote dApps built with ink!.  
This project will focus on building three games:
 - Game 1 : The user has to guess the random number (between 1 and 30 by example) given by the VRF. The user has a unique try. If the user finds the correct number, he will be rewarded.
 - Game 2 is an evolution of the first one. The user has several tries to find the mystery number and the smart contract will give a clue (plus or minus) to find it. Again, the user is rewarded if he finds it.
 - Game 3 will be a kind of Lotto. The user chooses 4 or 5 numbers and if he has all the correct numbers, he wins the jackpot.

### Project Details

In each game, the user will interact with one or more ink! smart contracts and these smart contracts will communicate with phat contract(s) to get the random number via a vrf and perform off-chain computing.

#### Game 1

1) The user chooses a random number between two values. The ink! smart contract on Astar Network saves this number and emits an event
2) A SubQuery or SubSquid indexer will listen this event and run (query) the phat contract on Phala Network.
3) The phat contract on Phala Network calls the smart contract on Astar Network and provides the random number via a vrf
4) The smart contract on Astar Network checks if the user won. If the user wons, he will be able to claim his rewards.

In the UI:
- the user will choose a number between two values
- the communication between the different contracts will be displayed and the user will see the status of their request.
- the user will be able to claim the rewards if he/she won
- the user will be able to see all past games (and filter on their own games)

We will use the treasury of the Lucky's Team to fund the rewards for this game (between 30$ and 50$ in SDN or ASTR tokens).
The first round will be open to all users.
The next rounds will be limited to the addresses that stake on the Lucky dApp.

#### Game 2

This game is an evolution of the first one.
The user has several tries to find the mystery number and the smart contract will give a clue (plus or minus) to find it.
Again, the user is rewarded if they find it.
We will use the treasury of the Lucky's Team to fund the rewards for this game.
The first round will be open to all users.
The next rounds will be limited to the addresses that stake on the Lucky dApp.


#### Game 3

Game 3 will be a kind of Lotto.
The user chooses 4 or 5 numbers between 1 and 49. These numbers can be changed later.
The user will need a NFT to play to the lottery. This NFT will be used as a ticket and will be burned when the numbers are chosen.
Another NFT will be minted with the chosen numbers. If the RMRK NFT is implemented for ink!, we could use a single nft and update it. 

Each X eras the raffle will start and a vrf (phat contract) will provide the winning numbers.
A first phat contract will send the winning numbers to the smart contract deployed on Astar.
A second phat contract will send the addresses of all winners.

An ink! smart contract will manage the jackpots.
If all numbers have been found:
- the vault of the current jackpot is closed and a new one is open,
- the winner(s) will be able to claim the current jackpot.

We will use a share of the dApp Staking revenues to feed the jackpots.
The jackpots will grow each era (to become more and more attractive).
A share of dApp Staking revenues will feed the current jackpot and also the next one to be renewable and make it attractive every time.

The NFT to play to the lottery will be free (claimable or airdropped) to all the addresses that stakes on the Lucky dApp.
The team will never sell any NFT to play to the lottery.

We will try to onboard other projects listed on the dApp staking. Their stakers will have access to the lottery if the project contributes to the jackpot.

#### Common to all games

For both game, we will provide:
- the ink! smart contracts
- the phala offchain rollups (ink! phat contracts)
- a UI for testing and playing with the games.
- the subquery or subsquid indexers used in the UI side
- the subquery or subsquid indexers used to automate the phat contract calls
- the documentation to deploy and use the smart contracts

The smart contracts will be deployed on Shibuya and Shiden and Astar. The phat contracts will be deployed on Phala Testnet and Khala and Phala.

## Team :busts_in_silhouette:

### Team members

- GuiGou is application architect in Web 2 and works more and more in web3.   
As a technical ambassador for Astar and ambassador for Phala, he promotes the ink! smart contracts via some tutorials (https://polkaverse.com/11143) and replies about the technical questions on ink! smart contracts via Astar's discord.
- Arno is a software engineer, web developer and ambassador for Polkadot, Phala, Acala and Talisman Sentinel


### Team's experience

We developed the Lucky dApp, built on top of dApp Staking in Astar Network.  
If the user stakes on the Lucky dApp, he will still receive the rewards from the dApp Staking, and furthermore, he will have a chance to win extra rewards. It’s a no-loss lottery!  
The dApp is built with several ink! smart contracts, a subquery indexer, and off-chain workers (scheduled jobs).  
We are replacing the scheduled jobs with phat contracts to improve decentralization and demonstrate the interoperability between ink! smart contracts (Shiden/Astar) and ink! phat contracts (Khala/Phala).

The dApp is already live on Shiden and Astar. 
- Website:  https://lucky.substrate.fi/
- Documentation: https://polkaverse.com/11201/introducing-the-d-app-lucky-37998  
- GitHub: https://github.com/LuckyDapp 

We built decentralized and trustless oracles for ink! smart contracts: [decentralized_oracles.md](decentralized_oracles.md) 
- Website:  https://lucky.substrate.fi/ 
- GitHub: https://github.com/decentralized-oracles 


### Team Code Repos

GitHub accounts of team members:
- https://github.com/GuiGou12358
- https://github.com/arnobase


## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 6.5 months
- **Full-Time Equivalent (FTE):**  1 FTE
- **Total Costs:** 65,000 USD

### Milestone 1  — Game 1

- **Estimated duration:** 1.5 month
- **FTE:**  1 FTE 
- **Costs:** 15,000 USD

|  Number | Deliverable                    | Specification                                                                                                                                                   |
|--------:|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                        | Apache 2.0                                                                                                                                                      |
| **0b.** | Documentation                  | We will provide documentation that explains how to use and test these smart contracts                                                                           |
| **0c.** | Testing and Testing Guide      | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
|      1. | Phat contracts                 | We will deliver the phala offchain rollup                                                                                                                       |
|      2. | Ink! smart contracts           | We will deliver the ink! smart contracts                                                                                                                        |
|      3. | UI                             | We will deliver the UI to test and play with the delivered smarts contracts                                                                                     |
|      4. | SubQuery and SubSquid indexers | We will deliver the indexers used in the UI side and also to automate the whole process                                                                         |


### Milestone 2  — Game 2

- **Estimated duration:** 1.5 month
- **FTE:**  1 FTE
- **Costs:** 15,000 USD

|  Number | Deliverable                    | Specification                                                                                                                                                   |
|--------:|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                        | Apache 2.0                                                                                                                                                      |
| **0b.** | Documentation                  | We will provide documentation that explains how to use and test these smart contracts                                                                           |
| **0c.** | Testing and Testing Guide      | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
|      1. | Phat contracts                 | We will deliver the phala offchain rollup                                                                                                                       |
|      2. | Ink! smart contracts           | We will deliver the ink! smart contracts                                                                                                                        |
|      3. | UI                             | We will deliver the UI to test and play with the delivered smarts contracts                                                                                     |
|      4. | SubQuery and SubSquid indexers | We will deliver the indexers used in the UI side and also to automate the whole process                                                                         |


### Milestone 3  — Ink! Smart contract and Phat Contract used for the game 3

- **Estimated duration:** 1 month
- **FTE:**  1 FTE
- **Costs:** 10,000 USD

|  Number | Deliverable                    | Specification                                                                                                                                                   |
|--------:|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                        | Apache 2.0                                                                                                                                                      |
| **0b.** | Documentation                  | We will provide documentation that explains how to use and test these smart contracts                                                                           |
| **0c.** | Testing and Testing Guide      | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
|      1. | Phat contracts                 | We will deliver the phala offchain rollup                                                                                                                       |
|      2. | Ink! smart contracts           | We will deliver the ink! smart contracts                                                                                                                        |



### Milestone 4  — Indexers and UI used for the game 3

- **Estimated duration:** 1.5 month
- **FTE:**  1 FTE
- **Costs:** 15,000 USD

|  Number | Deliverable                    | Specification                                                                                                                                                   |
|--------:|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                        | Apache 2.0                                                                                                                                                      |
| **0b.** | Documentation                  | We will provide documentation that explains how to use and test                                                                                                 |
| **0c.** | Testing and Testing Guide      | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
|      1. | UI                             | We will deliver the UI to test and play with the delivered smarts contracts                                                                                     |
|      2. | SubQuery and SubSquid indexers | We will deliver the indexers used in the UI side and also to automate the whole process                                                                         |


### Milestone 4  — NFT used in the game 2

- **Estimated duration:** 1 month
- **FTE:**  1 FTE
- **Costs:** 10,000 USD

|  Number | Deliverable                    | Specification                                                                                                                                                   |
|--------:|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                        | Apache 2.0                                                                                                                                                      |
| **0b.** | Documentation                  | We will provide documentation that explains how to use and test                                                                                                 |
| **0c.** | Testing and Testing Guide      | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
|      1. | UI                             | We will deliver the UI to test and play with the delivered smarts contracts                                                                                     |
|      2. | SubQuery and SubSquid indexers | We will deliver the indexers used in the UI side and also to automate the whole process                                                                         |


## Future Plans



## Additional Information :heavy_plus_sign:

**How did you hear about the Bounty Program?**   
We had a recommendation from the Phala Team and we already applied to the previous cohort.

