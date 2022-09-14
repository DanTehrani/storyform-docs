# Zero-knowledge proofs

### Proving your reputation as a respondent, anonymously

We envision Storyform to become a tool that enables a nascent way of collecting data through surveys, with the power of zero-knowledge proofs, or more precisely, zk-SANRKs. That is, enabling survey respondents to prove their reputation or membership without revealing their identity. An example**: a survey that targets members of a particular DAO, asking for their honest thoughts about working for the DAO.** The respondents can remain anonymous in their answers, while proving that they work for that particular DAO.



### The road to making anonymous surveys practical

To realize anonymous surveys on Storyform, we need to make some leaps in making zk-SNARK practical. Firstly, we aim to becoming compatible with the existing identity infrastructure on Ethereum, which is based on ECDSA. And unfortunately, zk-SNARK schemes that are practical today, don't work with ECDSA well. Therefore, we are actively working on developing the necessary building blocks, such as an idea of doing an ECDSA signature verification in a non-conventional way, which is relatively friendlier to zk-SNARKs. More on this can be found in [this Ethereum Research post](https://ethresear.ch/t/efficient-ecdsa-signature-verification-using-circom/13629).

&#x20;











