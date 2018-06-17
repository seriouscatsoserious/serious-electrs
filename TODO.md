# Electrum

* Poll mempool after transaction broadcast
* Support TLS (via https://docs.rs/rustls/)
* Snapshot DB after successful indexing - and run queries on the latest snapshot
* Update height to -1 for txns with any [unconfirmed input](https://electrumx.readthedocs.io/en/latest/protocol-basics.html#status)

# Bitcoind

* Stream blocks (instead batching RPCs)
* Use nTx from [getblockheader RPC](https://github.com/bitcoin/bitcoin/pull/13451) for better batching
* Handle bitcoind connection failures - instead of crashing
* Add getrawtransactions() API (for RPC batching)

# Performance

* Experiment with [sled](https://github.com/spacejam/sled) DB

# Rust

* Use Bytes instead of Vec[u8] when possible
* Return errors instead of panics
* Use generators instead of vectors