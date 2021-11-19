Minimalistic SDK to interact with EVM compatible blockchains

# Installation

```
poetry add eth-sdk

pip install sth-sdk
```

# Setup

Get started by running

```
poetry run eth-sdk
```

which will generate an `eth-sdk` folder with a `config.yml` file inside of it. The sample configuration looks like this

```
mainnet:
  contracts:
    dai: '0x6B175474E89094C44Da98b954EedeAC495271d0F'
  etherscan:
    api_key: ICZKZRP33RIZSYZJSJJ1S1ZNU64CY3KDNG
    url: https://api.etherscan.io/api
  rpc: https://mainnet.infura.io/v3/4210ba8eb536423e8ae5d774c5064fa1
```

You can add additional networks, rpcs, etherscan info or contracts to it.


# Usage

The sdk consists of a minimalistic contract sdk.

```
from eth_sdk import eth_sdk

sdk = eth_sdk('mainnet', signer)
```

By initializing the sdk it will look inside your `eth-sdk/config.yml` and initialize all the contracts in it. 

The contracts can then be accessed as followed.

```
sdk.dai.totalSupply()
```

In order for the contracts to be built succesfully they need to be verified in etherscan.