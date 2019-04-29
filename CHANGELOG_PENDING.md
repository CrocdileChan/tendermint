## v0.31.5

**

### BREAKING CHANGES:

* CLI/RPC/Config

* Apps

* Go API

* Blockchain Protocol

* P2P Protocol

### FEATURES:

### IMPROVEMENTS:
- [rpc] [\#3534](https://github.com/tendermint/tendermint/pull/3534) Add support for batched requests/responses in JSON RPC
- [cli] [\#3160](https://github.com/tendermint/tendermint/issues/3160) Add `-config=<path-to-config>` option to `testnet` cmd (@gregdhill)
- [cs/replay] \#3460 check appHash for each block
- [rpc] \#3362 `/dial_seeds` & `/dial_peers` return errors if addresses are incorrect (except when IP lookup fails)
- [node] \#3362 returns an error if `persistent_peers` list is invalid (except when IP lookup fails)

### BUG FIXES:
- [state] [\#3537](https://github.com/tendermint/tendermint/pull/3537#issuecomment-482711833) LoadValidators: do not return an empty validator set
- [p2p] \#3532 limit the number of attempts to connect to a peer in seed mode
  to 16 (as a result, the node will stop retrying after a 35 hours time window)
- [consensus] \#2723, \#3451 and \#3317 Fix non-deterministic tests
- [p2p] \#3362 make persistent prop independent of conn direction
  * `Switch#DialPeersAsync` now only takes a list of peers
  * `Switch#DialPeerWithAddress` now only takes an address
