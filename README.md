# Supply Chain Management Smart Contract

## Overview

This smart contract is designed to facilitate supply chain management on a blockchain platform. It allows for the tracking and verification of product authenticity throughout the supply chain. This README provides an overview of the contract's features and how to use it.

## Features

- **Product Registration**: Producers can register products in the supply chain by providing a unique product name.

- **Product Transfer**: Producers can transfer products to distributors and retailers, recording each step of the product's journey.

- **Product Verification**: Only the contract owner (e.g., a regulatory authority) can verify the authenticity of products, marking them as verified.

## Smart Contract Functions

### `registerProduct(string _productName)`

- Description: Allows producers to register a new product with a unique product name.
- Parameters:
  - `_productName`: The name of the product.
- Usage: Producers call this function to add their products to the supply chain.

### `transferProduct(uint256 _productId, address _to)`

- Description: Allows producers to transfer unverified products to distributors or retailers.
- Parameters:
  - `_productId`: The unique identifier of the product.
  - `_to`: The address of the recipient (distributor or retailer).
- Usage: Producers use this function to move products along the supply chain.

### `verifyProduct(uint256 _productId)`

- Description: Allows the contract owner to verify the authenticity of a product.
- Parameters:
  - `_productId`: The unique identifier of the product.
- Usage: Only the contract owner can call this function to mark a product as verified.

## Usage

1. **Deploy the Smart Contract**: Deploy this smart contract on a compatible blockchain platform like Ethereum.

2. **Product Registration**: Producers should register their products using the `registerProduct` function, providing a unique product name.

3. **Product Transfer**: Producers can transfer products to distributors and retailers using the `transferProduct` function. Ensure that the product is unverified before transferring.

4. **Product Verification**: Only the contract owner (e.g., a regulatory authority) can verify the authenticity of products using the `verifyProduct` function.

## Example Workflow

1. Producer A registers a product with the name "Product X."

2. Producer A transfers "Product X" to Distributor B.

3. Distributor B transfers "Product X" to Retailer C.

4. The regulatory authority verifies the authenticity of "Product X" by calling `verifyProduct`.

## Note

- This is a simplified example of a supply chain management smart contract and may require additional features and security measures for production use.

- Always ensure that the contract is deployed on a secure and suitable blockchain platform.

- Compliance with relevant regulations and integration with real-world supply chain data sources (e.g., QR code scanning, IoT devices) may be necessary for a complete supply chain management solution.
