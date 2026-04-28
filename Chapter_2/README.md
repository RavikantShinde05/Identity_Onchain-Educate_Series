# DEEP DIVE INTO IDENTITY:

Part 1: The Concordium Approach to Identity (with Dragos Danciulescu)
The first half of the session introduces the fundamental challenges of identity on public blockchains and presents Concordium's unique solution.

The Problem: Public blockchains face a trade-off between fully anonymous chains (like Monero, Zcash), which lack accountability, and pseudonymous chains (like Bitcoin, Ethereum), which offer insufficient privacy for serious business adoption.
Concordium's Solution: A system that provides privacy by default and accountability when legally required. Every account is linked to a verified real-world identity, but this link is encrypted and can only be broken through a multi-jurisdictional legal process.
Separation of Powers: The system's security relies on the strict separation of duties among four key participants, ensuring no single party can link an identity to an account on their own:
Identity Provider (IDP): Verifies real-world identity but has no knowledge of on-chain accounts.
Privacy Guardians (PGs): Hold cryptographic key shares for decryption but have no access to personal data.
The Authority: A legal entity (e.g., law enforcement) that coordinates the disclosure process with a court order.
Concordium: Provides the protocol and infrastructure but holds no personally identifiable information (PII).
Part 2: The Science Behind the Identity Layer (with Daniel Tschudi)
The second half delves into the cryptographic principles that make Concordium's identity system possible, focusing on Self-Sovereign Identity (SSI) and Zero-Knowledge Proofs (ZKPs).

Self-Sovereign Identity (SSI): An identity model where the user (Holder) is in full control. An Issuer provides a credential (e.g., an ID), and the Holder can present this to a Verifier (e.g., a business) to prove claims without over-sharing information.
Verifiable Presentations & Zero-Knowledge Proofs: Instead of showing the full credential, users generate a Verifiable Presentation using a ZKP. This allows them to prove specific statements (e.g., "I am over 18") without revealing the underlying data (e.g., their exact birthdate).
Key ZKP Properties:
Completeness: An honest user can always prove a true statement.
Soundness: A dishonest user cannot prove a false statement.
Zero-knowledge: The verifier learns nothing beyond the truth of the statement itself.
Proof Types Used by Concordium:
Sigma Protocols: Used for revealing specific attributes (e.g., family name).
Bulletproofs: Used for more complex proofs like Range Proofs (e.g., "I am between 18 and 65"), Set-Membership (e.g., "I am from Country A or B"), and Set-Non-Membership (e.g., "I am not from a sanctioned country").
