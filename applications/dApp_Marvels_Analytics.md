# Ink! dApp Marvels analytics

  

*   **Team Name:** [Tokenguard.io](http://Tokenguard.io) (Block Solutions Sp z o.o.)
*   **Payment Address:** 15LN4SgUiVgavRwC9aKeh2H82gEStwYCsXoy3dzEyzo8qoAt

  

## Project Overview 📄

  

### Overview

  

Ink! ecosystem is quickly growing thanks to a huge number of marvelous dApp builders that choose Ink! over Solidity because of its security, transparency and easability of use. Each new dApp brings in new users into the ecosystem, creating demand for the underlying native L1 coin which eventually translates into the ecosystem growth.

  

dApp builders currently lack an out-of-the-box solution that would allow them to discover dApp Marvels. What are these? Marvels are data-driven insights concerning the growth of each respective dApp. Whether it's a discovery of power users segment, correlation between two important metrics or understanding which marketing campaign works best - we call them Marvels as they're precious to each dApp owner 💎

  

Tokenguard team would therefore like to propose creation of:

  

#### **Ink! dApp Marvels analytics**

  

We propose creation of a standalone tool that will allow dApp creators & analytical tools index data coming from their smart contracts, aggregate them in a predefined human-readable format and and serve them in plot-ready format directly to your frontend. Such tool is going to run a number of steps to make the Marvel 💎 discovery easy and fun for dApp creators.

  

1. After smart contract deployment, dApp creator runs the Ink! dApp Marvels analytics by uploading contracts' ABIs.
2. The ABIs are decoded and translated into SubSquid powered data processor with smart contract decoder.
3. Using the API interface dApp creator specifies potential dApp Marvels that should be tracked - this can be an event with its respective arguments (or any mixture of both). Marvels can include actions invoked in more than 1 smart contract.
4. Aggregated database of Marvels is created and automatically populated in case any of these events happen on-chain.
5. dApp creator can query the database using API or display the data in a human-readable format using JSONs that can be then plotted on the frontend of your app.

  

The solution can be used as a standalone tool or parsed by data analytics tools available in the space such as Grafana, Tokenguard, Databox and others. Thanks to the API, dApp creators will be able to display their dApp data actively on websites to increase transparency for users.

  

### Substrate Ecosystem Impact

  

In order to facilitate growth, Substrate parachains need a vast and thriving environment of developers creating dApps and smart contracts. Each smart contract generates thousands of transactions that store important technical and business insights. Each new growing dApp, with its own marketing & growth strategy, **brings in new active users to the ecosystem**. These insights are currently hard to discover and the ecosystem needs infrastructure tools that would make it easy for developers and management teams to uncover them, similarly as it is done in EVM environment with tools like Tenderly or Dune Analytics.

  

### Ink! Ecosystem Impact

  

Most of the Ink! teams that we spoke with **are wasting hundreds of hours and thousands of $** to build their own data displaying solutions and maintain them which effectively defocuses them from building and developing user-centric features. Most of these solutions are hard to maintain and manage, increasing the technological debt of each project.

  

Benefits of the proposed solution:

  

*   Allowing Ink! dApp builders to focus on **developing their products**
*   **Time and money savings** on data tracking and visualisation \[Building in-house data-analytics = ~$30k - $70k\]
*   Higher security of dApps as the tool can be used for tracking **security metrics**
*   **dApp transparency** to ecosystem managers and Substrate community
*   Smaller maintenance cost and technological debt
*   **Faster growth of Ink! dApps**

  

### Project Details

  

An overview of the technology stack to be used

*   SubSquid, TypeScript, SQL

PoC/MVP or other relevant prior work or research on the topic

*   [app.tokenguard.io](http://app.tokenguard.io)

Do you need an audit for the contacts? **NO**

CATEGORY: Infrastructure

  

**Visualisation of the dApp Marvel set up @ Tokenguard interface**
<img src="https://imagizer.imageshack.com/img922/3403/DVC6iI.png" width="800" border="0">

**Visualisation of the dApp Marvel set up @ Tokenguard interface**
<img src="https://imagizer.imageshack.com/img924/6769/p0JhTc.png" width="800" border="0">

## Team :busts\_in\_silhouette:

  

### Team members

  

*   Kamil Gorski - CEO ([https://www.linkedin.com/in/gorskikamil/](https://www.linkedin.com/in/gorskikamil/))
*   Jakub Rojek - CTO / Backend developer ([https://www.linkedin.com/in/jakub-rojek-dev/](https://www.linkedin.com/in/jakub-rojek-dev/))
*   Damian Rolek - CDO / Data Analyst ([https://www.linkedin.com/in/damianrolek/](https://www.linkedin.com/in/damianrolek/))
*   Matt Saczewski - Business Development Manager ([https://www.linkedin.com/in/msaczewski/](https://www.linkedin.com/in/msaczewski/))
*   Jacob Piorecki - UI/UX Designer ([https://www.linkedin.com/in/jacobpiorecki/](https://www.linkedin.com/in/jacobpiorecki/))
*   Piotr Józefowicz - Backend Developer ([https://www.linkedin.com/in/piotr-jozefowicz-529669220/](https://www.linkedin.com/in/piotr-jozefowicz-529669220/))
*   Adam Król - Backend Developer ([https://www.linkedin.com/in/adam-kr%C3%B3l-7b3a831b6/](https://www.linkedin.com/in/adam-kr%C3%B3l-7b3a831b6/))
*   Krystian Trepczyński - Frontend Developer ([https://www.linkedin.com/in/krystiantrepczynski/](https://www.linkedin.com/in/krystiantrepczynski/))
*   Jan Kwiatkowski - Blockchain Developer ([https://www.linkedin.com/in/jan-kwiatkowski-web3/](https://www.linkedin.com/in/jan-kwiatkowski-web3/))

  

### Contact

  

*   **Contact Name:** Matt Saczewski
*   **Contact Email:** [matt@tokenguard.io](mailto:matt@tokenguard.io)
*   **Telegram:** @mattsac

  

### Legal Structure

  

*   **Registered Address:** Foksal 3/5 St., 00-366 Warsaw, Poland
*   **Registered Legal Entity:** Block Solutions Sp z o.o.

  

### Team's experience

  

Tokenguard's clients include Swiss Sygnum Bank, [Bitcoin.com](http://Bitcoin.com), Astar and many others recognizable brands. Each of cofounders has tremendous web3 experience - Damian was co-creating DeFi analytics platform Kasuria. Jacob was working at OpenLoyalty, helping web3 projects engage their users and Kamil created web3 security analytics solutions, conducting more than 30+ audits.

  

### Team Code Repos

  

*   [https://github.com/tokenguardio](https://github.com/tokenguardio)

  

## Development Status :open\_book:

  

Tokenguard is currently developing the following features:

  

*   Publicly accessible core analytics for Substrate communities, available at [https://app.tokenguard.io](https://app.tokenguard.io)
*   Ecosystem Analytics for [Astar](https://astar.network/)
*   Ecosystem Analytics for [Aleph Zero](https://alephzero.org/)
*   dApp analytics for [AZero ID](https://azero.id/), [ArthSwap](https://app.arthswap.org), [Panjea](https://panjea.io/), [Interlock](https://www.interlock.network/) and others
*   Partnership with [SubSquid](https://www.subsquid.io/)

  

## Development Roadmap :nut\_and\_bolt:

  

### Overview

  

*   **Total Estimated Duration:** 4 months
*   **Full-Time Equivalent (FTE):** 3 FTE
*   **Total Costs:** 94,600 USD

  

### Milestone 1

*   **Estimated duration:** 1 month
*   **FTE:** 2
*   **Costs:** 18,400 USD

| <br>Number<br> | Deliverable | Specification |
| ---| ---| --- |
| <br>**0a.**<br> | License | MIT |
| <br>**0b.**<br> | Documentation | We will provide inline documentation. |
| <br>**0c.**<br> | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. We will describe how to run these tests. |
| <br>**0d.**<br> | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| <br>1.<br> | dApp Marvels storage | Database:<br>1. Developing a service of automated SQL database creation based on dApp Marvels defined by user<br>2. Connecting the database to SubSquid smart contract decoder:<br>a). collecting raw data separately as smart contract events with their respective arguments<br>b). aggregating the data based on defined dApp marvels<br>3. Implementing automated schema changes to the database based on real-time user changes and newly defined Marvels<br><br>Data processing and handling:<br>1. Prepare a data pipeline that allows accessing the data with low delay<br>a). automated data aggregation pipeline<br>b). processing events coming from numerous smart contracts based on user's dApp Marvel definition<br> |

  

### Milestone 2

*   **Estimated duration:** 2 months
*   **FTE:** 2
*   **Costs:** 50,800 USD

| <br>Number<br> | Deliverable | Specification |
| ---| ---| --- |
| <br>**0a.**<br> | License | MIT |
| <br>**0b.**<br> | Documentation | We will provide inline documentation. |
| <br>**0c.**<br> | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. We will describe how to run these tests. |
| <br>**0d.**<br> | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| <br>2.<br> | dApp Marvels definition | Translating smart contract events into dApp Marvels:<br>1. Create a database that will collect ABIs of dApp's smart contracts and automatically process them using Ink! SubSquid decoder<br>2. Create a template to connect events from multiple smart contracts and set up required arguments & filters using logic rules<br>3. Design universal data model for transforming smart contract calls and methods with their respective arguments into previously user-specified dApp Marvels that need to be tracked & discovered<br>a). defining the database altering schema based on user changes of dApp Marvels<br> |

  

### Milestone 3

*   **Estimated duration:** 1 month
*   **FTE:** 2
*   **Costs:** 25,400 USD

| <br>Number<br> | Deliverable | Specification |
| ---| ---| --- |
| <br>**0a.**<br> | License | MIT |
| <br>**0b.**<br> | Documentation | We will provide both inline documentation of the code and a basic tutorial that explains how a user can specify, collect & display dApp marvels. |
| <br>**0c.**<br> | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| <br>**0d.**<br> | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| <br>0e.<br> | Manual & article | We will publish a tutorial that explains deliverables and how to use them. In the tutorial we will extensively explain the following scope:<br>1. How does dApp Marvel Analytics work?<br>2. Setting up dApp Marvel Analytics<br>a). ABI generation & uploading<br>b). Defining dApp Marvels, including numerous smart contracts<br>c). Tracking dApp Marvels<br>d). Modifying dApp Marvels<br>3. Marvel visualisation & notifications<br>a). How to connect dApp Marvel Analytics to data visualisation tools<br>b). Setting up API notifications<br> |
| <br>3.<br> | REST API interface & Marvel display | Creation of interactive REST API interface:<br>1. Creating a REST API service that will allow users to:<br>a). set up new trackable marvels<br>b). collect information about existing marvels<br>c). modify existing marvels<br>2. Connecting the API to the database for:<br>a). automated schema altering<br>b). events notifications<br>c). data processing<br>3. Adding a JSON outputting service to the database to allow displaying the data in a format readable to analytics tools such as Grafana, Tokenguard and others.<br> |

  

  

  

##
