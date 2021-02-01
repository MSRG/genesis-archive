# experimental-genesis archive

This repo can be used to produce a genesis.blob file needed to join the "0L experimental-network" (chain id `1`).

For reference purposes the binary can be found under /genesis/genesis.blob, along with the waypoint string.

Producing the genesis files requires 0L to be at v4.2.2. The tools required are `libra-genesis-tool` and `stdlib`, which will both found at the git tag v4.2.2. Note: ignore the rust cargo toml number versions which will differ.

### Verify a genesis file
If you are joining as a fullnode or validator node, you may confirm your local key_store.json file contains the correct waypoint in the genesis.blob with:

```
	cargo run -p libra-genesis-tool --release -- verify \
	--validator-backend 'backend=disk;path=$HOME/.0L/key_store.json;namespace=<account>' \
	--genesis-path $HOME/.0L/genesis.blob
```

### Auditing genesis
A hybrid release `v4.2.4-genesis-archive` exists for the purpose of auditing genesis. This uses v4.2.4 tools but includes the v4.2.2 standard library `stdlib`. Note: using a different standard library other than that at v4.2.2 will yield an incorrect waypoint, and you will not be able to sync to the experimental network.

