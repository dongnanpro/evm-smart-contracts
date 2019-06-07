# evm-smart-contracts
Open source repository of EVM Smart Contracts.

## Folder Structure
Due to the folder size limitations of 1000 contracts per folder, pagination folders were created with the `./contracts` folder. These paginated folders appear as:
  * 1
  * 2
  * 3

## Example

```
{
  "address": "0x02557a5e05defeffd4cae6d83ea3d173b272c904",
  "chain": "ETH",
  "chainID": 1,
  "commonName": "Compound: Oracle",
  "contractName": "PriceOracle",
  "compilerVersion": "v0.4.24+commit.e67f0147",
  "optimization": true,
  "runs": "200",
  "evmVersion": "default",
  "sourceCode": "pragma solidity ^0.4.24;\ncontract ErrorReporter {\n\n    /**\n      * @dev `error` corresponds to enum Error; `info` corresponds to enum FailureInfo, and `detail` is an arbitrary\n      * contract-specific code that enables us to report opaque error codes from upgradeable contracts.\n      **/\n    event Failure(uint error, uint info, uint detail);\n\n    enum Error {\n        NO_ERROR,\n        OPAQUE_ERROR, // To be used when reporting errors from upgradeable contracts; the opaque code should be given as `detail` in the `Failure` event\n        UNAUTHORIZED,\n        INTEGER_OVERFLOW,\n        INTEGER_UNDERFLOW,\n        DIVISION_BY_ZERO,\n        BAD_INPUT,\n        TOKEN_INSUFFICIENT_ALLOWANCE,\n        TOKEN_INSUFFICIENT_BALANCE,\n        TOKEN_TRANSFER_FAILED,\n        MARKET_NOT_SUPPORTED,\n        SUPPLY_RATE_CALCULATION_FAILED,\n        _TO_SET_PRICE\n    }\n\n    enum OracleFailureInfo {\n        ACCEPT_ANCHOR_ADMIN_PENDING_ANCHOR_ADMIN_CHECK,\n        SET_PAUSED_OWNER_CHECK,\n        SET_PENDING_ANCHOR_ADMIN_OWNER_CHECK,\n        SET_PENDING_ANCHOR_PERMISSION_CHECK,\n        SET_PRICE_CALCULATE_SWING,\n        SET_PRICE_CAP_TO_MAX,\n        SET_PRICE_MAX_SWING_CHECK,\n        SET_PRICE_NO_ANCHOR_PRICE_OR_INITIAL_PRICE_ZERO,\n        SET_PRICE_PERMISSION_CHECK,\n        SET_PRICE_ZERO_PRICE,\n        SET_PRICES_PARAM_VALIDATION,\n        SET_PRICE_IS_READER_ASSET\n    }\n\n    /**\n      * @dev `msgSender` is msg.sender; `error` corresponds to enum OracleError; `info` corresponds to enum \n}",
  "bytecode": "608060405234801561001057600080fd5b5060405160a0806200161e833981016040818152825160208085015183860151606087015160809097015160038054600160a060020a0319908116331790915560058054600160a060020a038089169190931617905593870190955267016345785d8a000095869052600695909555919491939290841615806100a5575081600160a060020a031684600160a060020a031614155b15156100ad57fe5b600160a060020a0384161561010157600160a060020a03831615156100ce57fe5b600160a060020a0384811660009081526001602052604090208054600160a060020a031916918516919091179055610112565b600160a060020a0383161561011257fe5b600160a060020a0382161561016657600160a060020a038116151561013357fe5b600160a060020a0382811660009081526001602052604090208054600160a060020a031916918316919091179055610177565b600160a060020a0381161561017757fe5b5050505050611492806200018c6000396000f30060806040526004361061010",
  "constructorArguments": "0000000000000000000000003c6809319201b978d821190ba03fa19a3523bd9600000000000000000000000089d24a6b4ccb1b6faa2625fe562bdd9a23260359000000000000000000000000729d19f657bd0614b4985cf1d82531c67569197b000000000000000000000000a0b86991c6218b36c1d19d4a2e9eb0ce3606eb48000000000000000000000000729d19f657bd0614b4985cf1d82531c67569197b"
}
```
