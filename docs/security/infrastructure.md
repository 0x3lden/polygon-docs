### Polygon Bridge Security

Polygon develops and maintains bridges to transfer assets to-and-from the Ethereum blockchain for both the Polygon PoS network and Polygon zkEVM scaling solution. These bridges implement a lock-and-mint architecture which results in assets being controlled (locked) by the bridge smart contract implementations. As the aggregate value of locked assets on Polygon bridges is significant, we apply a corresponding focus on bridge security. Much of the security efforts documented here are rigorously applied to bridge security, including risk management, secure software development practices, auditing, vulnerability management, CI/CI and bug bounties. We leverate dedicated on-chain bridge monitoring.

### Bridge Monitoring

The bridge on-chain infrastructure is monitored for real-time events as a way to augment the application security efforts associated with product development (i.e. threat modeling, code auditing, library and supply-chain risk and bug bounties). The real time monitoring includes both on-chain machine learning models to detect unknown threats in real time as well as empirical rule-based algorithms to capture known adversarial or error scenarios. 

The monitoring infrastructure was developed both in-house and by vendors as needed to augment our capabilities in specific analysis areas. Any adverse bridge events detected by our models and tools are evaluated, triaged and, if necessary, escalated to the proper team for further analysis. The monitoring process is integrated with our enterprise incident response process for seamless integration with internal processes.

### Multisig Security

Specific requirements are followed by any Polygon Labs employee that is a signer on a corporate multisig contract. Multisig contacts are corporately owned  and control treasury assets or smart contract deployments. They consist of Safes (previously Gnosis Safes) and other smart contract multisig implementations. Hardware wallets are hardware-based cold storage such as Trezor or Ledger devices that store private keys and enable signing multisig transactions offline. Signer multisig requirement include:

- **Hardware Wallet:** Polygon requires Cold storage from an accepted vendor dedicated for company official use only and secured by a PIN
- **Hot Wallets:** Hot wallets are not allowed for use on Polygon multisigs
- **Corporate Workstation:** Signing must be performed from a company system  managed by  our enterprise mobile device management (MDM) platform  complete with anti-virus (AV) and endpoint detection and device (EDR).
- **Clean Key:** All signers are required to create a clean key that has never been exposed to a hot wallet
- **Mnemonic Storage:** Polygon mandates safe storage of mnemonic passphrases and provides guidance to its employees
- **Secure Communication:** All multisig signing events are coordinated using Polygon’s accepted communication protocols for multisigs.

**All corporate multisigs are monitored 24/7 by the Polygon security team.**

