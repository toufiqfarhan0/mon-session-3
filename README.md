# ToufiqNFT (Monad Deployment)

This repository contains an ERC721 NFT Smart Contract deployed on the **Monad Testnet**. It leverages OpenZeppelin's standard libraries for security and robustness, implementing **Access Control** to manage permissions effectively.

## 🚀 Features

- **ERC721 Standard**: Fully compliant Non-Fungible Token implementation.
- **URI Storage**: Supports individual token URIs for metadata (IPFS/Pinata).
- **Role-Based Access Control (RBAC)**:
  - `DEFAULT_ADMIN_ROLE`: Can manage other roles.
  - `MINTER_ROLE`: Restricted permission to mint new NFTs.
- **Secure**: Built using vetted OpenZeppelin contracts.

## 🛠 Contract Details

- **Contract Name**: ToufiqNFT
- **Symbol**: TOU
- **Solidity Version**: ^0.8.20

| Role | Permissions |
| :--- | :--- |
| **Admin** | Manage roles, grant/revoke permissions |
| **Minter** | Call `safeMint` to create new NFTs |

## 📦 Deployment Info

- **Network**: Monad Testnet
- **Contract Address**: `0x914c227426360e0556fF4cc818A517bbD8C6AB66`
- **Block Explorer**: [Monad Explorer](https://testnet.monadvision.com/token/0x914c227426360e0556fF4cc818A517bbD8C6AB66)

## 📖 Usage

### Minting an NFT

Only helpful addresses with the `MINTER_ROLE` can mint.

1. Call `safeMint`:
   - `to`: Address receiving the NFT.
   - `tokenId`: Unique ID for the NFT (e.g., `1`).
   - `uri`: Metadata URI (e.g., `https://orange-fascinating-bison-71.mypinata.cloud/ipfs/bafkreifoh2umfzs5pvnjecccs2hdpfi72fx2d4g74a7inobmkpfjumv6ru`).

### Granting Roles

The Admin can grant the Minter role to new addresses:
- Call `grantRole(MINTER_ROLE, newMinterAddress)`.

## 🧰 Tech Stack

- **Solidity**: Smart Contract Language
- **OpenZeppelin**: Secure Contract Library
- **Remix IDE**: Development & Deployment Environment
- **Monad**: High-performance L1 Blockchain

## 📜 License

This project is licensed under the MIT License.
