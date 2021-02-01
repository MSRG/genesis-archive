# experimental-genesis archive

This repo can be used to produce a genesis.blob file needed to join the "0L experimental-network" (chain id `1`).

For reference purposes the binary can be found under /genesis/genesis.blob, along with the waypoint string.

Producing the genesis files requires 0L to be at v4.2.2. Importantly the versions of `libra-genesis-tool` and `stdlib` will both be at the git tag v4.2.2 (ignore the rust cargo toml number versions which will differ).

