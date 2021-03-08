## Binance sortable chain
Binance sortable chain is a bsc-geth fork allowing for bundled sorting of validated transactions.

### Using binance sortable chain for your validator?
pm me on telegram [@code0x2](https://t.me/code0x2) if you want profit maximalizing tx's sent to you

### Whats new in sortable chain bsc-geth?
- BSC-Geth's tx pool now has a seperate memory slot for storing `sealingBundles` (commit [b9993614eafadfcdd983bcd99adedc9bddb922b1](https://github.com/Code0x2/binance-sortable-chain/commit/b9993614eafadfcdd983bcd99adedc9bddb922b1))

- BSC-Geth's block sealing for mining/validating will seal blocks in the following order: 1st, check for any internal sealingBundles that are before the deadline for them and add. 2nd, check for local transactions and add. 3rd, add remaining transacions until block is full/no more transactions (commit [91c48d32691a972521dc0c4cb754bffb61e52db9](https://github.com/Code0x2/binance-sortable-chain/commit/91c48d32691a972521dc0c4cb754bffb61e52db9))

- BSC-Geth has a new JSON-RPC endpoint, called `eth_sendBundle`. This queues a new set of signed transactions and assigns a deadline to them, for next block sealing (commit [fa7e7e93f7482c17f143872ad9793af2805963df](https://github.com/Code0x2/binance-sortable-chain/commit/fa7e7e93f7482c17f143872ad9793af2805963df))
