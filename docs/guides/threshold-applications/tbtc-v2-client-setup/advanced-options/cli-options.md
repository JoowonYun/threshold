---
description: Review available CLI Options below.
---

# CLI Options

{% embed url="https://github.com/keep-network/keep-core/blob/main/docs/resources/client-start-help" %}

```
$ keep-client start --help
Starts the Keep Client in the foreground

Usage:
  keep-client start [flags]

Flags:
      --ethereum.url string                        WS connection URL for Ethereum client.
      --ethereum.keyFile string                    The local filesystem path to Keep operator account keyfile.
      --ethereum.miningCheckInterval duration      The time interval in seconds in which transaction mining status is checked. If the transaction is not mined within this time, the gas price is increased and transaction is resubmitted. (default 1m0s)
      --ethereum.maxGasFeeCap wei                  The maximum gas fee the client is willing to pay for the transaction to be mined. If reached, no resubmission attempts are performed. (default 500 gwei)
      --ethereum.requestPerSecondLimit int         Request per second limit for all types of Ethereum client requests. (default 150)
      --ethereum.concurrencyLimit int              The maximum number of concurrent requests which can be executed against Ethereum client. (default 30)
      --ethereum.balanceAlertThreshold wei         The minimum balance of operator account below which client starts reporting errors in logs. (default 500000000 gwei)
      --network.bootstrap                          Run the client in bootstrap mode.
      --network.peers strings                      Addresses of the network bootstrap nodes.
  -p, --network.port int                           Keep client listening port. (default 3919)
      --network.announcedAddresses strings         Overwrites the default Keep client address announced in the network. Should be used for NAT or when more advanced firewall rules are applied.
      --network.disseminationTime int              Specifies courtesy message dissemination time in seconds for topics the node is not subscribed to. Should be used only on selected bootstrap nodes. (0 = none)
      --storage.dir string                         Location to store the Keep client key shares and other sensitive data.
      --clientInfo.port int                        Client Info HTTP server listening port. (default 9601)
      --clientInfo.networkMetricsTick duration     Client Info network metrics check tick in seconds. (default 1m0s)
      --clientInfo.ethereumMetricsTick duration    Client info Ethereum metrics check tick in seconds. (default 10m0s)
      --tbtc.preParamsPoolSize int                 tECDSA pre-parameters pool size. (default 1000)
      --tbtc.preParamsGenerationTimeout duration   tECDSA pre-parameters generation timeout. (default 2m0s)
      --tbtc.preParamsGenerationDelay duration     tECDSA pre-parameters generation delay. (default 10s)
      --tbtc.preParamsGenerationConcurrency int    tECDSA pre-parameters generation concurrency. (default 1)
      --tbtc.keyGenerationConcurrency int          tECDSA key generation concurrency. (default number of cores)
      --developer.bridgeAddress string             Address of the Bridge smart contract
      --developer.randomBeaconAddress string       Address of the RandomBeacon smart contract
      --developer.tokenStakingAddress string       Address of the TokenStaking smart contract
      --developer.walletRegistryAddress string     Address of the WalletRegistry smart contract

Global Flags:
  -c, --config string   Path to the configuration file. Supported formats: TOML, YAML, JSON.
      --developer       Developer network
      --goerli          Görli network
      --mainnet         Mainnet network

Environment variables:
    KEEP_ETHEREUM_PASSWORD    Password for Keep operator account keyfile decryption.
    LOG_LEVEL                 Space-delimited set of log level directives; set to "help" for help.
```
