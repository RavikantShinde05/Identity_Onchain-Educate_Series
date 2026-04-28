# Exploring Verify & Access with Concordium ID:

This chapter provides a deep dive into Concordium's Verify & Access feature, a framework for privacy-preserving, auditable, and compliant identity verification using Zero-Knowledge Proofs (ZKPs). The session is led by Dragos Danciulescu and Doris Benda.

## Key Concepts :

## The Problem with Traditional Identity: The session begins by outlining the significant liabilities and costs associated with traditional identity verification, including the risks of storing Personal Identifiable Information (PII), the high cost of data breaches, and the increasing burden of regulatory compliance (e.g., GDPR, MiCA). For users, it leads to over-sharing of sensitive data and repetitive onboarding processes.
## Concordium's Solution - Verify & Access: The core of the solution is the use of ZKPs, which allow a user to prove a statement is true (e.g., "I am over 18") without revealing the underlying data (their date of birth). This eliminates the need for merchants to store sensitive PII, mitigating risk and preserving user privacy.
## Three-Party Verification Model:
- User: Proves attributes from their Concordium Wallet using a ZK proof.
- Merchant: Verifies the proof without ever seeing or storing the user's raw personal data.
organisasi* Concordium Blockchain: Serves as a digital notary. An immutable, tamper-proof audit anchor is created on-chain to record that a verification took place, without any PII.
## The Full Audit Chain: A three-record system ensures a complete and secure audit trail.
- VRA (Verification Request Anchor): An on-chain transaction that initiates the process, creating a timestamped record to prevent replay attacks.
- VAR (Verification Audit Record): A private, off-chain record stored by the merchant in their database, containing metadata for their internal compliance logs.
- VAA (Verification Audit Anchor): A final on-chain transaction that closes the audit trail, confirming the verification was successfully resolved.
## Verification Methods: Two primary methods are available:
- Against an ID: Simple identity gating for age, nationality, etc., where no payment is involved. This works with the lightweight Concordium ID App.
- Against an Account: Used when a flow involves both identity verification and an on-chain payment or transaction. This requires a full wallet with an on-chain account. 
