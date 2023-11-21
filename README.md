# PermitTokenCollector

**PermitTokenCollector is a Solidity smart contract that facilitates the transfer of ERC-20 tokens with permit functionality from multiple user addresses to a designated collector address**

## Overview

The contract interacts with an ERC-20 token that supports the permit function, allowing users to sign a permit allowing a specific amount of tokens to be spent by the collector address.

## Usage

1. Deploy the `PermitTokenCollector` contract to the Ethereum blockchain.
2. Set the `collector` address and initialize the `token` interface with the target ERC-20 token's contract address.
3. Users approve the contract to spend their tokens by calling the `permitTransfer` function, providing arrays of user addresses, permit parameters (v, r, s), and corresponding token amounts.
4. The contract uses the permit to transfer the specified token amounts from each user's address to the collector's address.

## Example Deployment

```solidity
// Deploy PermitTokenCollector
PermitTokenCollector collector = new PermitTokenCollector();
collector.setCollectorAddress(YOUR_ADDRESS);
collector.setTokenInterface(0x912CE59144191C1204E64559FE8253a0e49E6548);
#
