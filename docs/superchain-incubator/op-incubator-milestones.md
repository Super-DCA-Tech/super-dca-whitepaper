## Super DCA Development Phases & Timeline (Weeks 3–12)

### Phase 1: Local Cross-Chain Infrastructure with SuperSim  
**Timeline:** Weeks 3–4  
**Milestone:** Week 4 – MVP Demo

**Objectives:**  
- Build and validate Cross-chain DCA infrastructure using `SuperSim`.
- Create a local Cross-chain environment to simulate real-world L2 bridging.

**Deliverables:**
- Setup Super DCA Network in `Supersim`
    - Super DCA Token deployed to both OPChainA (ChainID 901) and OPChainB (ChainID 902) via **Create2** for identical addresses.
    - Deploy Uniswap v4 infrastructure
- Intra-chain swap logic enabling SuperDCA token to be used as a base token in token swaps.
    - Swap path ex. (x -> DCA -> y)

**Technical Tasks:**
- Write SuperSim deployment scripts.
- Write CREATE2-based deterministic deployment scripts.
- Deploy DCA token and Gauge contracts on both chains.
- Validate base token swaps.

**Dependencies:**
- Foundry + SuperSim
- CREATE2 deployment scripts

---

### Phase 2: Frontend Development & Fee Hook Logic  
**Timeline:** Weeks 5–8  
**Milestone:** Week 8 – Backend & Frontend

**Objectives:**  
- Expand UI functionality for interacting with DCA Pools.
- Implement dynamic fee logic in Uniswap v4 `beforeSwap` hook.
- Add links to "Add Liquidity" to USDC-DCA and ETH-DCA pools on app.uniswap.org

**Deliverables:**
- Frontend v1 UI: view pools, initiate streams, bridge tokens, monitor activity.
- Gauge Hook logic: Implemented functions to set the mint rate and update the manager roles

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
- Move from local simulation to testnet.
- Prepare for public-facing demo with all Super DCA features.

**Deliverables:**
- Deployment scripts for testnets using `CREATE2`.
- Fully functional cross-chain demo: stream → bridge → swap → distribute.
- Frontend v2 connected to live RPCs.

**Technical Tasks:**
- Deploy contracts on selected testnet.
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
| Phase 1 | 3–4 | Week 4: MVP Demo | SuperSim local infra, cross-chain token & gauge deployment, swap logic | Foundry, SuperSim, CREATE2 |
| Phase 2 | 5–8 | Week 8: Backend & Frontend | Frontend v1, dynamic fee hook, liquidity links | Frontend dev, Hook logic, SuperSim |
| Phase 3 | 9–12 | Week 12: Final Demo | Testnet deploy, cross-chain demo, frontend v2 | RPCs, Superfluid, Gelato, deployment scripts |
