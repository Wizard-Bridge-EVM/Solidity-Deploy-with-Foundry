<p align="center">
  <a href="https://wizard-bridge-evm.gitbook.io/docs">
      <picture>
        <img alt="logo" src="https://github.com/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry/blob/main/wizardbridgeevm-logo-white.png" height="200px">
      </picture>
</a>
</p>

<div align="center">
<a href="https://x.com/wizardbridgeevm" ><img src="https://img.shields.io/twitter/follow/wizardbridgeevm.svg?style=social" /></a>
<a href="https://testnet-wizardbridgeevm.web.app" ><img src="https://img.shields.io/badge/Test-Website-green" /></a>
<a href="https://www.facebook.com/people/Wizard-Bridge-EVM/61551776916251" ><img src="https://img.shields.io/badge/Page-Facebook-blue" /></a>

<a href="https://github.com/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry/stargazers"><img src="https://img.shields.io/github/stars/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry" alt="Stars Badge"/></a>
<a href="https://github.com/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry/network/members"><img src="https://img.shields.io/github/forks/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry" alt="Forks Badge"/></a>
<a href="https://github.com/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry/pulls"><img src="https://img.shields.io/github/issues-pr/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry" alt="Pull Requests Badge"/></a>
<a href="https://github.com/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry/issues"><img src="https://img.shields.io/github/issues/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry" alt="Issues Badge"/></a>
<a href="https://github.com/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry/graphs/contributors"><img alt="GitHub contributors" src="https://img.shields.io/github/contributors/Wizard-Bridge-EVM/Solidity-Deploy-with-Foundry?color=2b9348"></a>
</div>

<br>

## Deployments
<b>1.</b> deploy - Utils
```
forge create --rpc-url <YOU_RPC_CHAIN> --private-key <YOU_PRIVATE_KEY> src/Utils:Utils
```
1.2
```
forge verify-contract --verifier blockscout --verifier-url <EXP_URL>/api? <YOU_CONTRACT_ADDRESS> Uilts --chain-id <CHAIN_ID>
```
<b>2.</b> deploy - WizardBridgeEVM
```
Edit (foundry.toml): libraries = ["src/WizardBridgeEVM.sol:Utils:<address>"]
```
2.1
```
forge create --rpc-url <YOU_RPC_CHAIN> --private-key <YOU_PRIVATE_KEY> src/WizardBridgeEVM.sol:WizardBridgeEVM --constructor-args <TRUSTEDSIGNER_ADDRESS> <FEE_IS_WEI>wei
```
2.3
```
forge verify-contract --verifier blockscout --verifier-url <EXP_URL>/api? <YOU_CONTRACT_ADDRESS> WizardBridgeEVM --chain-id <CHAIN_ID>
```

<br>

---

## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
