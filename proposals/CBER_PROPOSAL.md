# Super DCA V2: Advancing Decentralized Finance with New Fee Models for TWAMMs  

## Abstract  

Super DCA V2 seeks to answer two critical research questions in decentralized finance (DeFi):  
1. Can liquidity providers (LPs) earn competitive yields through a self-sustaining protocol with sub-0.1% fee structures, eliminating the need for intermediary protocol fees?  
2. Does this ultra-low fee model reduce total costs (including price impact) for traders compared to existing TWAMM implementations charging 0.5% fees?  

To address these questions, the study introduces a mathematical framework for analyzing direct LP fees and transaction costs in Super DCA. The system aims to achieve sustainability through pure market efficiency by implementing dynamic fee adjustments and eliminating intermediary protocol fees. The proposed research will develop and validate these hypotheses using simulations and on-chain pilot data, contributing actionable insights for building truly decentralized market-making systems.  

## Introduction 

### Research Significance  

Automated market makers (AMMs) have revolutionized trading in DeFi by providing permissionless liquidity and trustless execution. Constant Function Automated Market Makers (CFAMM) are the basic AMM structure. In an AMM, LPs can be affected by Loss-Versus-Rebalancing (LVR). In LVR, arbitrage trades adjust the reserves of the pool, leaving LPs with fewer of the tokens that are undervalued. However, the existing TWAMM implementations lack mechanisms for dynamic fee adjustments, relying instead on static fee structures and externalized execution processes. These limitations often misalign stakeholder incentives and restrict protocol scalability. 

Super DCA introduces innovations that address these challenges:  

1. **Self-Sustaining Fee Model:** The protocol achieves sustainability with sub-0.1% fees by eliminating intermediary costs and optimizing for pure market efficiency.  
2. **Direct Value Distribution:** All fees are distributed directly to LPs, removing protocol-level fee extraction and maximizing capital efficiency.  

These mechanisms have the potential to redefine AMM best practices, demonstrating that sustainable DeFi protocols can operate without intermediary fee structures.  

### Contribution  

This research fills a gap in the literature by:  

- Modeling the impact of dynamic fee adjustments on user costs and LP yield performance.  
- Conducting empirical comparisons between Super DCA and traditional TWAMM systems.  
- Validating the hypothesis that dynamic fees improve protocol efficiency and sustainability.  

By addressing these topics, the research contributes to the broader understanding of fee structures and incentive mechanisms in DeFi.

## Team
- **Location:** Philadelphia, PA, USA
### Team Members

#### Principal Investigator: Michael Ghen
- **Contact Email:** [mike@mikeghen.com](mailto:mike@mikeghen.com)
- **Social Media Profile:** [https://x.com/mikeghen](https://x.com/mikeghen)

#### Research Associate: Raphael Nembhard
- **Contact Email:** [raphael@digitalinnovation.info](mailto:raphael@digitalinnovation.info)
- **Social Media Profile:** [https://x.com/VillageFarmerr](https://x.com/VillageFarmerr)
- **Website:** [https://github.com/DeluxeRaph](https://github.com/DeluxeRaph)

### Legal Structure

- **Registered Address:** 2204 Manning St. Philadelphia, PA 19103
- **Registered Legal Entity:** Michael Ghen, Sole Proprietor

### Team's Experience

**Michael Ghen** is an adjunct professor of computer science at Rowan University. He has been researching the efficiency of blockchain networks since 2019 as part of a post-graduate fellowship at Drexel University, funded by a U.S. Department of Education's GAANN program for Post-Graduate Cyber Security researchers. His research was done under the supervision of Dr. Steven Weber, the Head of the Department of Electrical and Computer Engineering at Drexel. The research involved the modeling and analysis of Bitcoin mining, Ethereum staking, and Oracle networks and systems. 

**Education:**
- BS in Computer Engineering, Penn State University
- MS in Strategic Analytics, Brandeis University
- Cyber Security Post-Graduate Fellowship, Drexel University

**Professional Experience:**
- 10 years experience in data engineering, science, and software development
- 5 years experience building applications for the Ethereum Virtual Machine (EVM)
- Currently, independent contractor for ScopeLift, contributing to projects from organizations such as:
  - ZKSync Association
  - Tally
  - Wormhole 

**Web3 Awards:**
Michael Ghen has been recognized for his contributions to the web3 ecosystem with the following awards:

- **2024:** Finalist, Onchain Summer Buildathon (Unplugged Category) - Base
- **2023:** Best Use of Compound Finance, ETH Online Hackathon - ETH Global, Compound Grants
- **2022:** Finalist, ETHOnline Hackathon - ETH Global
- **2021:** Best Use of Superfluid, Scaling Ethereum Hackathon - ETH Global, Superfluid

**Raphael Nembhard** is a full-stack developer and blockchain specialist with expertise in smart contract development and AI-focused agentic workflows. As Co-Founder and CTO at Okay Bet, he leads technical development of innovative prediction market solutions, focusing on cross-chain market aggregation and trader staking mechanisms.

**Education:**
- Polkadot Blockchain Academy Certification (Rust, Substrate, and Blockchain Architecture)
- Associate Degree in Communication Studies, Community College of Philadelphia

**Professional Experience:**
- Co-Founder and CTO at Okay Bet
- Freelance Software Engineer specializing in smart contract development and AI workflows
- Systems Integrator for Philadelphia-area businesses
- Notable Technical Projects:
  - Dynamic Governance Liquidator (DGL): Governance logic and TWAMM integration
  - Run Money: Web3 saving and fitness app with staking mechanisms
  - Saverville: Financial farming simulation using Chainlink VRF
  - Various AI projects focused on agentic workflows

**Web3 Awards:**
Raphael Nembhard has been recognized for his contributions to the web3 ecosystem with the following awards:
- **2024:** Finalist, Onchain Summer Buildathon (Unplugged Category) - Base

### Team Code Repos

- [GitHub - Super-DCA-Tech/superdca-contracts](https://github.com/Super-DCA-Tech/superdca-contracts)
- [GitHub - Super-DCA-Tech/superdca-liquidity-network](https://github.com/Super-DCA-Tech/superdca-liquidity-network)
- [GitHub - Super-DCA-Tech/super-dca-whitepaper](https://github.com/Super-DCA-Tech/super-dca-whitepaper)

### Team GitHub Profiles

- [mikeghen (Michael Ghen) · GitHub](https://github.com/mikeghen)
- [DeluxeRaph (Raphael Nembhard) · GitHub](https://github.com/DeluxeRaph)

### Existing Support

Super DCA received support for our research from the following organizations as part of Gitcoin Grants Round 20 and 21:

- [Optimism](https://optimism.xyz)
- [Token Engineering Commons](https://tecommons.org/)

You can find Super DCA on Gitcoin's Explorer for a full history of grants and contributions received:

- [Super DCA on Gitcoin Explorer](https://explorer.gitcoin.co/#/projects/0xa37658ed45bb954b5bc89672cfaf820200500a7bfeb0f9e0333a1ec5dfa64292)

## Methodology  

Super DCA's methodology builds upon the [Time-Weighted Average Market Maker (TWAMM) design proposed by Paradigm](https://www.paradigm.xyz/2021/07/twamm) while introducing novel architectural features. The core innovation lies in creating an embedded AMM using a Uniswap liquidity network where all protocol fees accrue to stakeholders through the DCA token.

Our research methodology focuses on three key areas that differentiate Super DCA:

1. **Fee Distribution Architecture:** We analyze how routing swaps through paired DCA token pools (e.g., USDC-DCA and DCA-ETH) enables AMM fees to flow to protocol stakeholders rather than being extracted. This routing feature is designed to reduce Loss-Versus-Rebalancing (LVR), a common issue in traditional AMMs where arbitrage trades exploit stale prices, impacting LP returns. This includes modeling optimal fee parameters and distribution mechanisms. For a comprehensive breakdown of the fee model architecture and its theoretical foundations, please refer to the [Fee Distribution Architecture section of the Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper#embedded-amm-using-a-uniswap-liquidity-network).

![DCA Liquidity Network Architecture](./images/DCALiquidityNetwork.png)
*Figure: Super DCA's liquidity network architecture showing how trades route through paired DCA token pools to enable fee capture by protocol stakeholders*


2. **Simplified Solver Mechanism:** We evaluate our staking-based execution model where competition is purely based on DCA token stake rather than solver sophistication. This removes technical barriers while preventing front-running through the staking requirement. For a detailed explanation of this staking-based execution model and its benefits, see the [Execution Incentive section of the Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper#execution-incentive), which describes how DCA token holders can stake to earn execution rights and undercut Gelato's fees.

3. **Dynamic Fee Optimization:** We study how pool volume affects execution costs and model fee adjustments to target optimal swap frequencies. Our pilot data shows pools can sustainably reduce fees as volume increases while maintaining 4-hour target execution intervals. For empirical evidence of this dynamic fee behavior, see the [Order Pools with Dynamic Fees section of the Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper#order-pools-with-dynamic-fees), which includes data from our initial pilot demonstrating how execution frequency responds to fee adjustments.

The methodology leverages empirical data from our pilot implementation, which demonstrated competitive exchange rates with minimal liquidity requirements. For example, a USDC-ETH pool achieved rates within 1.04% of Chainlink oracle prices using just ~2,000 USDC equivalent of concentrated and full-range liquidity positions.


### Dynamic Fee Modeling  

We employ mathematical modeling to quantify losses incurred by users. Total loss is expressed as:  

```
Total Loss (%) = Protocol Fee (%) + AMM Fee (%) + Execution Fee (%)
```

For a comprehensive breakdown of the fee model architecture and its theoretical foundations, please refer to the [Fee Distribution Architecture section of the Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper#embedded-amm-using-a-uniswap-liquidity-network).

#### Key Equations  

1. **Protocol Fee:**  
   ```
   Protocol Fee (%) = Fixed Percentage of Volume (e.g., 0.5% on existing TWAMMs)
   ```
This represents the standard protocol-level fee charged by existing TWAMM implementations. Super DCA eliminates this fee entirely by leveraging its unique architecture where the AMM fees themselves serve as the protocol incentive mechanism.

2. **AMM Fee:**  
   ```
   AMM Fee (%) = n * f
   ```
Where `f` is the Uniswap pool fee rate (e.g., 0.05% per pool). The factor of 2 represents the mandatory two-pool path through the DCA token (e.g., USDC→DCA→ETH), resulting in a fixed 0.1% total AMM fee. This dual-pool structure eliminates the need for a separate protocol fee, as the AMM fees naturally accrue to liquidity providers who stake the protocol's DCA token, creating a self-sustaining incentive mechanism. For a detailed explanation of this dual-pool architecture and its fee implications, see the [Embedded AMM using a Uniswap Liquidity Network section of the Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper#embedded-amm-using-a-uniswap-liquidity-network).

3. **Execution Fee:**  
   ```
   Execution Fee (%) = Fixed Percentage of Swap Amount (e.g., 1%)
   Execution Trigger = Accumulated Fee >= Gas Cost
   ```

The system targets a 4-hour execution frequency (matching industry standard TWAMMs) through the following fee adjustment mechanism:

   ```
   TARGET_DURATION = 4 hours
   MIN_FEE_PERCENTAGE = 0.01%
   MAX_FEE_PERCENTAGE = 0.1%   
   ADJUSTMENT_FACTOR = 0.95  // 5% reduction each time

   On each successful swap:
       current_duration = time_since_last_swap
       
       if current_duration < TARGET_DURATION:
           // Swap happening too frequently, reduce fee
           new_fee_percentage = max(
               current_fee_percentage * ADJUSTMENT_FACTOR,
               MIN_FEE_PERCENTAGE
           )
       else:
           // Swap happening too infrequently, increase fee
           new_fee_percentage = min(
               current_fee_percentage / ADJUSTMENT_FACTOR,
               MAX_FEE_PERCENTAGE
           )
   ```

When swaps occur more frequently than every 4 hours, the fee percentage is gradually reduced by 5% each time, making it take longer to accumulate enough fees for the next execution. This creates a natural equilibrium where higher volume pools can operate with lower percentage fees while maintaining consistent execution intervals. For empirical evidence of this fee adjustment mechanism and its effects, see the [Order Pools with Dynamic Fees section of the Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper#order-pools-with-dynamic-fees), which includes data showing how execution frequency responds to fee adjustments. Visually represented in the figure below:

![DCA Execution Frequency Adjustment](./images/DCAExecFrequency.png)
*Figure: Shows how the execution fee change from 1% to 0.5% causes the execution frequency to double. The line at 4 hours shows the target execution interval. Above the threshold, the fee percentage is increased and below, it is decreased.*


### Comparative Analysis: Traditional TWAMMs vs Super DCA

Traditional TWAMMs and Super DCA differ fundamentally in their fee structures and execution mechanisms. TWAMMs protocols charge a fixed protocol fee, and sometimes there is a hidden AMM fee also applied to the swap. On some DCA systems the user themselves also has to pay the execution costs, while others abosorb the cost in their fixed fee structure. 

#### Traditional TWAMM Model
```
Total Cost = Protocol Fee (0.5%) + AMM Fee (0-1%)
             = 0.50-1.5% per trade
```
Traditional TWAMMs rely on external solver networks and implement fixed protocol fees that don't adjust based on volume. They maintain separate fee structures for AMM and protocol operations, while also creating higher barriers to entry for executors due to their architecture.

The AMM fee is 0% in cases where the TWAMM protocol abosorbs the fee as part of its own fee structure. AMM fees vary with Uniswap V3 having a 1% upper bound for the fees a pool can charge. The AMM fee may not be transparent to the user and its left up to the protocol to determine how to account for that. In most instances it appears that TWAMMs using Uniswap for liquidity charge their protocol fee on top of the fee that liquidity providers charge through the AMM.

#### Super DCA Model
```
Total Cost = AMM Fee (0.1%) + Dynamic Execution Fee (0.01-0.1%)
           = 0.11-0.2% per trade
```
where the Dynamic Execution Fee is a function `f` of both trading volume and network conditions (i.e., gas price) at time `t`:
```
DynamicExecutionFee(t) = f(volume(t), gas_price(t))
```
In addition to the dynamic execution fee there is also a dynamic execution _frequency_ since the time it will take to accumulate enough volume to trigger an execution is a function of volume and gas price. The execution frequency is determined by calculating how long it will take to accumulate enough fees to cover gas costs. (See the [Architecture section of the Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper#architecture), specifically the Swap Buffer component which acts as a temporary holding area for accumulated fees until they reach the execution threshold.) The function below is the one currently implemented in the Super DCA contract:

```javascript
/// @notice Get the next distribution time based on the 
/// current gas price, gas needed, and token to WETH rate
/// @param gasPrice The current gas price in Wei
/// @param gasNeeded The gas needed to execute the swap
/// @param tokenToWethRate The rate of the token to WETH
/// @return The next distribution time
function getNextDistributionTime(
    uint256 gasPrice, 
    uint256 gasNeeded,
    uint256 tokenToWethRate
) public view returns (uint256) {
    // Calculate volume in tokens per second
    uint256 volume = getVolume(inputToken);
    
    // Calculate required token amount to cover gas costs
    uint256 tokenAmount = gasPrice * gasLimit * tokenToWethRate;
    
    // Calculate time needed to accumulate enough tokens
    uint256 timeToDistribute = (tokenAmount / volume) / (10 ** 9);
    return lastDistributedAt + timeToDistribute;
}
```

This dynamic timing mechanism ensures that executions only occur when economically viable, automatically adjusting to network conditions. For example:

- During high gas prices, executions will naturally space out further to accumulate enough fees
- Higher volume pools will execute more frequently as they accumulate fees faster
- Lower volume pools will execute less frequently

This creates a self-balancing system where execution frequency organically adjusts to maintain economic viability while maximizing execution opportunities within gas constraints. For more details on this see the section on Execution Frequency in the [Order Pools with Dynamic Fees section of the Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper?tab=readme-ov-file#order-pools-with-dynamic-fees).

### Simulation and Benchmarking  

Python-based simulations will test scenarios for LP yields and trader costs. These simulations will benchmark Super DCA's performance against other protocols using metrics like price slippage, transaction cost efficiency, and liquidity utilization. For details on our previous simulation methodologies and results, see the [Small and Fast Swaps section of the Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper#small-and-fast-swaps).


### Existing Pilot On Optimism Network

Super DCA has already deployed a pilot on the Optimism network with a USDC-ETH pool. The pool has been used to collect data onchain to validate the hypotheses and the results have been promising. You can read more about the pilot by reading our updates about it on the Token Engineering Commons forum:

- [Super DCA Benchmarks](https://forum.tecommons.org/t/super-dca-benchmarks/1404)
- [Super DCA GG20 Update](https://forum.tecommons.org/t/super-dca-gg20-update/1397)

The network on Optimism is made up of three liquidity pools:

- DCA-USDC.e
- DCA-ETH
- DCA-OP

This existing pilot has already collected data about the performance of the Super DCA TWAMM compared to other AMMs on Optimism (see: [Super DCA Benchmarks](https://forum.tecommons.org/t/super-dca-benchmarks/1404)). However, it has also identified parts of the protocol that need to be improved. The results are still promising and having the system up and collecting data is very helpful. The figure below shows the results of the pilot benchmarking anaysis.

![DCA Pilot Benchmarking](./images/image.png)
*Figure: Shows the results of the pilot benchmarking analysis.*

### Second Pilot On Base Network
The second pilot will be deployed on the Base network with a USDC-ETH pool and USDC-TOSHI pairs, thus pools for:

- DCA-USDC
- DCA-ETH
- DCA-TOSHI

The USDC-ETH pair will still be used for benchmarks. TOSHI is selected for this pilot to introduce additional volatility and test the robustness of the protocol. Our hypothesis is that the protocol will still be able to better sustain itself when the network has more volatility in it. 

Additionally, the second pilot will include an updated Super DCA system that implements some enhancements and fixes that were identified in the first pilot. Furthermore, the version of the Super DCA contract on Base will be audited by a reputable firm to ensure that it is ready for production.

The second pilot will run for a longer period of time to collect more data and allow for a more comprehensive analysis of the protocol's performance. A Dune Analytics dashboard will be created to provide transparency into the system's performance and facilitate ongoing research validation.

## Budget and Deliverables  

**Total Estimated Duration:** 20 weeks  
**Full-time Equivalent (FTE):** 20-30 days  
**Total Project Costs:** $27,500  

The research and development process for Super DCA V2 is structured into four key milestones:  

1. **Development of Models, Simulations, and Smart Contract Updates**  
2. **Smart Contract Audit and Remediation**  
3. **Pilot Deployment, Data Collection, and Dashboard Creation**  
4. **Analysis, Reporting, and Dissemination**  

Each milestone is carefully designed to ensure rigorous testing, robust auditing, and impactful dissemination of results. Below is a detailed breakdown of each milestone.  

### Milestone 1: Development of Models, Simulations, and Smart Contract Updates  

- **Estimated Duration:** 7 weeks  
- **FTE:** 7-9 days  
- **Costs:** $4,500  

#### Deliverables  

| Number | Deliverable                | Specification                                                                                     |
|--------|----------------------------|---------------------------------------------------------------------------------------------------|
| 1      | Dynamic Fee Models         | Develop mathematical models for dynamic fee structures tailored to trade volume.                 |
| 2      | Simulation Environment     | Build a Python-based simulation to test LP yields and trader costs under various scenarios.      |
| 3      | Stakeholder Incentive Analysis | Model and test mechanisms for sustainable fee distribution to LPs.                  |
| 4      | Smart Contract Updates     | Improve Super DCA protocol contracts to address findings from the first pilot and prepare them for audit.  |

#### Details  

During this phase, theoretical models will be developed to optimize fee structures used. Simulations will assess the relationship between trade volume, gas prices, LP yields, and price impact. Updated smart contracts will integrate findings from our first pilot and ensure a smooth audit process before the second pilot.



### Milestone 2: Smart Contract Audit and Remediation  

- **Estimated Duration:** 4 weeks  
- **FTE:** 4-6 days  
- **Costs:** $14,000
  - Third-party Audit: $10,000
  - Development & Remediation: $4,000

#### Deliverables  

| Number | Deliverable                    | Specification                                                                                     |
|--------|--------------------------------|---------------------------------------------------------------------------------------------------|
| 1      | Smart Contract Audit           | Independent audit of smart contracts to identify vulnerabilities and ensure robustness.          |
| 2      | Remediation and Updates        | Address and resolve audit findings, updating contracts for secure deployment.                    |

#### Details  

This milestone ensures that Super DCA’s smart contracts meet the highest security standards. The audit will be conducted by a reputable third-party firm specializing in blockchain security. Following the audit, the team will implement necessary remediations to address any identified vulnerabilities.  


### Milestone 3: Pilot Deployment, Data Collection, and Dashboard Creation  

- **Estimated Duration:** 15 weeks  
- **FTE:** 5-8 days  
- **Costs:** $5,000  

#### Deliverables  

| Number | Deliverable                  | Specification                                                                                     |
|--------|------------------------------|---------------------------------------------------------------------------------------------------|
| 1      | Super DCA Pools Deployment   | Deploy pools on Optimism for real-world performance evaluation.                                  |
| 2      | On-chain Data Collection     | Gather metrics on swap execution frequency, LP yields, and price impact.                        |
| 3      | Dune Analytics Dashboard     | Build a live dashboard using Dune Analytics to monitor system performance in real-time. ([Sample Dashboard](https://dune.com/superdca/super-dca-pilot-optimism))          |
| 4      | Benchmark Comparison         | Analyze data against Uniswap’s 0.5% fee model to validate hypotheses.                            |

#### Details  

This milestone involves deploying Super DCA pools on Optimism to validate performance in a live environment. Metrics such as LP yields, swap execution frequency, and price impact will be tracked. A Dune Analytics dashboard will be developed to provide real-time monitoring for stakeholders.  

### Milestone 4: Analysis, Reporting, and Dissemination  

- **Estimated Duration:** 4 weeks  
- **FTE:** 4-7 days  
- **Development Costs:** $4,000  

#### Deliverables  

| Number | Deliverable                  | Specification                                                                                     |
|--------|------------------------------|---------------------------------------------------------------------------------------------------|
| 1      | Data Analysis                | Analyze collected data to validate hypotheses about LP yields and price impact.                  |
| 2      | Research Paper Preparation   | Draft a comprehensive white paper outlining methodology, results, and implications.              |
| 3      | Presentation and Dissemination | Present findings at conferences and publish open-access materials to share insights.            |

#### Details  
The final milestone consolidates all findings into a comprehensive research paper, which will undergo peer review. The team will also present results at relevant academic and industry conferences, ensuring broad dissemination of insights. 


## Future Work Toward Fee-less DCA using Hook Design Patterns in Uniswap V4
A major development effort under way at Super DCA is a deeper integration with Uniswap. By taking advantage of Uniswap V4's Hooks architecture, this integration addresses two issues highlighted in the [Super DCA White Paper](https://github.com/Super-DCA-Tech/super-dca-whitepaper) that were previously considered inescapable fees:

1. Network transaction fees
2. Embedded AMM/market maker fees

Through Uniswap's V4 Hooks architecture, these fees can be shifted to other network participants, particularly MEV traders operating in the background. This enables Super DCA to offer a "fee-less" DCA experience by leveraging the network's existing MEV activity to absorb costs that were previously unavoidable.
