# Resilient-Apps-with-Polkadot-Cloud
A self-sovereign bridge transforming Web2 OAuth tokens into on-chain Polkadot DIDs with offchain signature checks. Full user control enables instant revocation and seamless identity use across any parachain.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
markdown
# Polkadot Identity Bridge

A **user-controlled system** that turns standard Web2 login tokens (Google, Apple) into **revocable Polkadot DIDs**, verified securely off-chain and anchored on-chain.

No third-party holds your data — **own, revoke, or move your identity anytime.**

---

## Project Summary

This tool lets anyone convert a familiar Web2 login into a **self-sovereign, blockchain-native identity** on Polkadot.

- **Frontend**: Simple React interface with OAuth login  
- **Logic**: Substrate pallet + offchain workers validate JWT signatures  
- **Storage**: Only a hash and status stored on-chain  
- **Result**: A portable `did:polkadot:...` ready for any parachain

**Mission**: Make Web3 identity as easy as Web2 — but truly yours.

---

## How to Run

### 1. Run the Custom Chain

```bash
git clone https://github.com/yourhandle/polkadot-identity-bridge.git
cd polkadot-identity-bridge/chain
cargo build --release
./target/release/polkadot --dev --ws-external
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
Websocket: ws://127.0.0.1:9944
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
** ### 2. Start the Web App **
cd ../app
npm install
npm run dev
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
Visit http://localhost:5173
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
###3. Try It Out

Connect a Polkadot wallet (e.g., via browser extension)
Sign in with Google
Confirm the transaction → Your DID is created
Use it across Polkadot ecosystem apps

Revocation available via CLI or upcoming dashboard.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
Tech Stack
Polkadot SDK, Rust
frame-system, sp-offchain, reqwest
React, Vite, Polkadot.js API, Google OAuth
Offchain JWT validation, Blake2 commitment
