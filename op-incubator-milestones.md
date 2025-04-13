## Super DCA Development Phases & Timeline (Weeks 3–12)

### Phase 1: Local Cross-Chain Infrastructure with SuperSim  
**Timeline:** Weeks 3–4  
**Milestone:** Week 4 – MVP Demo (SuperSim-Only)

**Objectives:**  
- Build and validate core cross-chain DCA infrastructure using `SuperSim` (a Foundry Anvil-based cross-chain simulator).
- Create a local dual-chain environment to simulate real-world L2 bridging.

**Deliverables:**
- Super DCA Token (ERC-7802) deployed to both OPChainA (ChainID 901) and OPChainB (ChainID 902) via **Create2** for identical addresses.
- Super DCA Uniswap V4 Gauge deployed with the DCA token address using **Create2**.
- Bridging logic enabling token flow from origin to destination within SuperSim.

**Technical Tasks:**
- Configure SuperSim with OPChainA & OPChainB.
- Write CREATE2-based deterministic deployment scripts.
- Deploy DCA token and Gauge contracts on both chains.
- Validate mint/burn bridging and gauge sync logic.

**Dependencies:**
- Foundry + SuperSim
- CREATE2 deployment scripts
- OPStack forked configs

---

### Phase 2: Frontend Development & Fee Hook Logic  
**Timeline:** Weeks 5–8  
**Milestone:** Week 8 – 80% Backend & Frontend Complete

**Objectives:**  
- Expand UI functionality for interacting with DCA Pools.
- Implement dynamic fee logic in Uniswap v4 `beforeSwap` hook.

**Deliverables:**
- Frontend v1 UI: view pools, initiate streams, bridge tokens, monitor activity.
- Gauge Hook logic: DCA Pool-originated swaps pay 0 fee, others pay BASE_FEE.
- Hook integration with backend and frontend logic.

**Technical Tasks:**
- Connect frontend to SuperSim RPCs for OPChainA & OPChainB.
- Write and test `beforeSwap` fee logic based on caller identity.
- Validate DCA fee exemption vs. BASE_FEE for others.

**Dependencies:**
- Frontend framework (React/Next.js)
- Hook contract logic and tests
- Updated DCA Pool contract if needed

---

### Phase 3: Testnet Deployment & Final Integration  
**Timeline:** Weeks 9–12  
**Milestone:** Week 12 – Final Demo Day

**Objectives:**  
- Move from local simulation to public testnets (Base, Optimism, Superchain Testnet).
- Prepare for public-facing demo with all Super DCA features.

**Deliverables:**
- Deployment scripts for testnets using `CREATE2`.
- Fully functional cross-chain demo: stream → bridge → swap → distribute.
- Frontend v2 connected to live RPCs.
- Gauge voting and liquidity incentives live.

**Technical Tasks:**
- Deploy contracts on selected testnets.
- Bridge mock/testnet tokens and validate swaps.
- Final QA across chains.

**Dependencies:**
- Public RPC endpoints
- Superfluid testnet
- Gelato setup
- Testnet token faucets

---

### Summary Table

| Phase | Weeks | Milestone | Deliverables | Dependencies |
|-------|-------|-----------|--------------|--------------|
| Phase 1 | 3–4 | Week 4: MVP Demo | Local dual-chain infra, cross-chain token + gauge | Foundry, SuperSim, CREATE2 |
| Phase 2 | 5–8 | Week 8: 80% Complete | Frontend v1 + dynamic fee logic | Frontend dev, Hook logic, SuperSim |
| Phase 3 | 9–12 | Week 12: Final Demo | Testnet deployment + full UI | RPCs, Gelato, Superfluid, scripts |

