# MeshPay

A protocol for enabling Bitcoin transactions in environments without direct Internet access, leveraging Bluetooth Low Energy (BLE) mesh networks with economic incentives.

## How it works

1. **Proof-of-Internet (PoI):** Beacon nodes with internet access periodically broadcast signed messages containing the latest Bitcoin block header and their payment address
2. **Transaction Construction:** Offline users create and sign multiple versions of their Bitcoin transaction, each including a small relay fee output to a different beacon's address
3. **Mesh Propagation:** Transactions are broadcast through the BLE mesh network to all participants, finding their way to beacon nodes
4. **Selective Relay:** Each beacon only forwards the transaction variant that includes payment to their address, creating natural competition and incentive alignment
5. **Bitcoin Settlement:** The Bitcoin network's consensus mechanism handles the conflicting transactions, confirming exactly one variant (no consensus change needed)

## Use cases

- Natural disaster scenarios with limited internet infrastructure
- Remote areas with sparse connectivity
- Censorship-resistant payment broadcasting
- Research into offline cryptocurrency systems

## Academic context

This work builds upon existing research in offline cryptocurrency systems, particularly addressing limitations in Lightning Network approaches like LNMesh that require continuous connectivity for security. The protocol operates at the Bitcoin base layer, avoiding the complexity of payment channel monitoring and watchtower services.
