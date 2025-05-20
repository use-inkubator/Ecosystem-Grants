# Step-Debugger for Ink! v6

- **Team name:** Ink Step-Debugger team
- **Payment address:** 5GHdT44FcYDALAkcqmKW1HkVzAcni8gkrpLy6T4kdMn17izE

---

## Project overview :page_facing_up:

### Overview

- **Tagline**: An IDE-integrated step-debugger for Ink! v6 smart contracts using the Debug Adapter Protocol (DAP)
- **Brief description**: We propose a developer tool that enables step-by-step debugging of Ink! v6 smart contracts directly inside VS Code, using a custom Debug Adapter built for PolkaVM and pallet-revive. This allows developers to set breakpoints, step through execution, and inspect state—without running a node.
- **Relation to Ink! ecosystem**: The tool will be the first step-debugger for Ink! v6 using the new tracing APIs from pallet-revive and PolkaVM. This brings the debugging experience closer to that of Solidity and other modern smart contract ecosystems.
- **Chosen project category: Tools**
- **Importance**: Step-debugging is a crucial part of modern developer workflows. This project fills a gap in the Ink! toolchain by introducing interactive, IDE-native debugging, drastically improving productivity.
- **Why our team is interested**: Our team understands the big pains for the developers of debugging through logs and tracing. The new tracing APIs in Ink! v6 give us the opportunity to fix this once and for all with a structured, polished tool.

---

### Ink! ecosystem impact

This **step-debugger** will benefit the Ink! ecosystem by offering:

- **Modern tooling**: Brings Ink! debugging up to par with EVM-like tools like Hardhat and Remix.
- **Lowering the learning curve**: Makes smart contract behavior visible and understandable, especially for newer developers.
- **Developer velocity**: Reduces iteration time and frustration by enabling real-time debugging instead of post-mortem log analysis.
- **Toolchain completeness**: Supports the Ink! 6 migration and broader Polkadot ecosystem readiness.

---

### Project details

1. **Core functionality & data flow**
    1. **Data models / API specs**:
        - Uses the **tracing APIs** of `pallet-revive` and **PolkaVM debug symbols** to observe execution and pause at breakpoints.
        - Executes contracts in an **off-chain sandbox** (DRink! or similar) without requiring a full node.
        - Implements the **Debug Adapter Protocol (DAP)** to connect with VS Code or other IDEs.
    2. **Architecture overview**:
        - **VS Code Extension**: Minimal shell for launching debug sessions via launch.json.
        - **Rust-based Debug Adapter**: Bridges VS Code and the PolkaVM sandbox, managing execution and state.
        - **Ink! execution backend**: Uses DRink! or a similar runtime with PolkaVM interpreter mode.
2. **Technology stack**:
    - **DAP**: Debug Adapter Protocol (JSON over stdio)
    - **Rust**: For the adapter and runtime integration
    - **VS Code**: For UI
    - **PolkaVM + pallet-revive**: Target execution engine
    - **Ink! v6**: Target contract language
3. **Documentation & prior research**:
    - Extensive review of PolkaVM, DRink!, and DAP.
    - Planning done with Ink! v6 in mind—focused on the future stack.
4. **Non-goals / limitations**:
    - Does not target to support Ink! v5 or `pallet-contracts`
    - Does not include a unified GUI
    - Does not support expression evaluation or conditional breakpoints in MVP
5. **Audit needed?** No
6. **Category**: Infrastructure (Tools)
7. **Business model**: Open-source debugging tool with no monetization planned. The primary goal is community adoption.
8. **Growth strategy and future plans**: Future versions may include advanced features like expression evaluation, conditional breakpoints, multi-contract debugging, custom GUI, and community-driven improvements.

> Exclusions:
>
> - We do not support old Ink! versions or Substrate Wasm contracts. This is strictly for Ink! v6 and pallet-revive.

---

## Team :busts_in_silhouette:

### Team members

- Illia Abrosimov – Team leader / project lead
- Yaroslav Kulpin – PolkaVM / runtime integration
- Ivan Savin – Debug adapter and frontend tooling

### Contact

- **Contact name:** Illia Abrosimov
- **Contact email:** aillia.dev@gmail.com

### Team's experience

Our team has combined expertise in:

- **Ink! / Substrate / PolkaVM** development and sandbox environments.
- **Rust systems programming** and DAP-based tools.
- **VS Code extension tooling**.

### Team code repos

- http://github.com/last-dot/Ink-Step-Debugger

**GitHub accounts**:

- https://github.com/last-dot
- https://github.com/NeonMaliket
- https://github.com/SoV3n04ek

**LinkedIn**:

- https://linkedin.com/in/illia-abrosimov
- https://linkedin.com/in/jaroslav-kulpin-8aa91924b

---

## Development status :open_book:

- **Research**: Studied the PolkaVM execution engine and `pallet-revive` tracing API. Evaluated DRink! sandbox tool for integration.
- **Tooling review**: Analyzed feasibility of DAP, breakpoints via debug symbols, PolkaVM single-step execution.
- **Initial prototyping**: Basic contract execution with sandbox verified.

---

## Development roadmap :nut_and_bolt:

### Overview

- **Total estimated duration:** 3 months
- **Full-time equivalent (FTE):** ~3 FTE
- **Total costs**: 60,000 USD

### Month 1 — Design and Prototype Execution Engine

- **FTE**: 2
- **Costs**: 20,000 USD
- Research DRink!, PolkaVM, and tracing APIs. Set up sandbox execution. Define core architecture of the adapter.

| **Number** | **Deliverable** | **Specification** |
| --- | --- | --- |
| **1.** | License | Publish code under **MIT** license |
| **2.** | Docs | Document architecture, sandbox setup, debugging process |
| **3.** | Adapter prototype | Can launch debug session and execute a contract to completion |
| **4.** | Breakpoint architecture | Implement file:line -> instruction address mapping, planning for future |
| **5.** | Contract run | DRink!-based or custom PolkaVM sandbox for isolated execution |

---

### Month 2 — Implement Breakpoints, Stepping, and State Inspection

- **FTE**: 3
- **Costs**: 30,000 USD
- Implement debug session lifecycle, stepping, call stack tracking, and state inspection logic.

| **Number** | **Deliverable** | **Specification** |
| --- | --- | --- |
| **6.** | Breakpoint hit | Stop execution at breakpoint, notify DAP client |
| **7.** | Step execution | Support step over, into, out with temporary breakpoints or trace tracking |
| **8.** | Call stack | Show function call hierarchy from CallTrace or PolkaVM stack info |
| **9.** | Variable scope | Basic contract storage and function params inspection |
| **10.** | Integration tests | Contracts for test cases: breakpoints, stepping, nested calls |

---

### Month 3 — VS Code Integration, Stability, and Documentation

- **FTE**: 1.5
- **Costs**: 10,000 USD
- Finalize extension packaging, cross-platform polish, and write usage guide.

| **Number** | **Deliverable** | **Specification** |
| --- | --- | --- |
| **11.** | VS Code extension | Publish a usable debugger integrated with DAP client in VS Code |
| **12.** | Debug session UX | Launch.json templates, smooth F5 experience, readable variables |
| **13.** | Variable pretty-printers | Format common types like Balance, AccountId nicely |
| **14.** | Usage guide | Step-by-step doc with screenshots and limitations |
| **15.** | Final demo | Showcase contract with working debugger, recorded or live |

---

## Future Plans

Once MVP is complete, future phases may include:

1. **Advanced variable inspection**: DWARF parsing to show local vars
2. **Expression evaluation & watch**: REPL and dynamic watches
3. **Conditional breakpoints**: Pause when variables match conditions
4. **Custom GUI**: Interactive visualization of state, execution flow
5. **Replay on-chain transactions**: Load historical traces and replay
6. **Multi-contract debugging**: Cross-contract call tracking and stepping
7. **Attach to node (future)**: RPC-based tracing from actual chain
8. **Broad editor support**: JetBrains, Emacs, etc. via DAP
9. **Community feedback loop**: Feature voting and community engagement

---

## Additional information :heavy_plus_sign:

**How did you hear about the Bounty Program?**

Recommendation from a colleague.
