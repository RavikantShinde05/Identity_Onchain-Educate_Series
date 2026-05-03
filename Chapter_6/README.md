## X402 on Concordium:
Hosted by Giles Mallinson, with presentations by Dragos Danciulescu (Concordium) and Denys Doronin (CTO, Boosty Labs).

This workshop explores the integration of the x402 payment protocol with the Concordium blockchain, demonstrating how to build agentic and identity-gated payment flows.

## Part 1:
### The Missing Payment Layer & The History of HTTP 402
Dragos Danciulescu began by explaining the concept of a "missing payment layer" on the web. He delved into the history of the HTTP 402 "Payment Required" status code, which was reserved in 1997 but never implemented due to the dot-com bubble burst that ended early digital cash systems. The web instead defaulted to application-layer payments like credit cards and PayPal, which are not native to the HTTP protocol and are uneconomical for micropayments.

## Part 2:
What is x402 & How Does It Work?
x402 is an open, chain-agnostic payment protocol built on HTTP, originally developed by Coinbase and now governed by the Linux Foundation. Its core features include:

No Native Token or Account Required: Relies solely on HTTP headers and stablecoin settlement.
Simplified Flow: The process involves a client requesting a resource, a server responding with a 402 error and payment details, the client making the payment and resending the request with a payment signature, and a facilitator verifying and settling the transaction.

The Core Problem x402 Solves
x402 standardizes web payments at the protocol level, making it easy for machines and AI agents to programmatically pay for services without complex setups like subscriptions or API keys.

## Part 3:
The Concordium + x402 Integration
While x402 handles pricing and settlement, it does not handle identity. This is where Concordium's unique features create a powerful synergy:

### Identity-Gated Payments:
Concordium’s protocol-level identity layer allows for verification (e.g., age-gating, jurisdiction checks) using Zero-Knowledge (ZK) proofs, ensuring compliance without revealing sensitive personal data.
Sponsored Transactions (Protocol 10): The facilitator can sponsor gas fees (CCD), creating a frictionless user experience where users only need to hold stablecoins to make payments.

## Part 4: x402 in Practice: A Demo by Boosty Labs
Denys Doronin, CTO of Boosty Labs, presented a live demo showcasing the architecture and a real payment flow. The demo illustrated an age-gated payment scenario where a user:

Requests access to a resource.
Generates a ZK proof to verify they are over 18 without revealing their actual age.
Signs a payment transaction.
The facilitator verifies both the identity proof and the payment in a single cycle.
Upon successful settlement, the user gains access to the resource.
The demo covered both a user-facing UI flow and a programmatic script for machine-to-machine (M2M) communication, highlighting the protocol's flexibility for both human and agent-based systems.
