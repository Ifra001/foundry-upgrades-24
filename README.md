# Upgradable Smart Contract: Box

This project demonstrates an upgradable smart contract using the UUPS (Universal Upgradeable Proxy Standard) pattern. The contract includes two versions:

- **BoxV1**: Implements basic functionality to retrieve a stored value.
- **BoxV2**: Extends functionality to allow updating the stored value.

## Features

- **Upgradeable Architecture**: Utilizes the UUPS proxy pattern for efficient and flexible upgrades.
- **Versioning**: Each version includes a `version()` function to identify the current implementation version.
- **Access Control**: Uses OpenZeppelin's `OwnableUpgradeable` to restrict sensitive operations to the contract owner.

## Upgrade Process

1. Deploy the `BoxV2` implementation contract.
2. Use the proxy contract's `upgradeTo(address newImplementation)` function to upgrade to `BoxV2`.

## Dependencies

This project uses the following OpenZeppelin libraries:

- `@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol`
- `@openzeppelin/contracts-upgradeable/proxy/utils/Initializable.sol`
- `@openzeppelin/contracts-upgradeable/access/OwnableUpgradeable.sol`
