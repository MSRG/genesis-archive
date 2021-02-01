# experimental-genesis archive

This repo can be used to produce a genesis.blob file, needed to join the "experimental-network" (chain_id == 1).

For reference purposes the binary can be found under /genesis/genesis.blob, along with the waypoint string.

Producing the genesis files requires the 0L v4.2.0. Importantly the versions of `libra-genesis-tool` and `stdlib` will both be at the git tag v4.2.0 (ignore the rust cargo toml number versions which will differ).

