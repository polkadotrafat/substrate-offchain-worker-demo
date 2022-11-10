# Substrate Off-chain Worker Demo

Fork of https://github.com/jimmychu0807/substrate-offchain-worker-demo

Two pallets running off chain workers. The first one fetches asset price, the second one fetches mock grid data modeled on DREX mini-grid.

<img src="https://github.com/polkadotrafat/substrate-offchain-worker-demo/blob/main/ocw_grid.png" />

### Run

1. First, complete the [basic Rust setup instructions](./docs/rust-setup.md).

2. To run it, use Rust's native `cargo` command to build and launch the template node:

  ```sh
  cargo run --release -- --dev --tmp
  ```

3. To build it, the `cargo run` command will perform an initial build. Use the following command to
build the node without launching it:

  ```sh
  cargo build --release
  ```

Since this repository is based on Substrate Node Template,
[it's README](https://github.com/substrate-developer-hub/substrate-node-template/blob/v3.0.0%2Bmonthly-2021-10/README.md)
applies to this repository as well.

### About Off-chain Worker

- The core of OCW features are demonstrated in [`pallets-ocw`](./pallets/ocw/src/lib.rs), and
[`pallets-example-offchain-worker`](./pallets/example-offchain-worker/src/lib.rs).

  Note that in order for the offchain worker to run, we have injected *Alice* key in
[`node/service.rs`](node/src/service.rs#L93-L104)

- Goto [**docs/README.md**](docs/README.md) to learn more about off-chain worker (extracted from Substrate
  Recipes, based on Substrate v3).

- Review the code of [**Offchain Worker Example Pallet** within Substrate](https://paritytech.github.io/substrate/latest/src/pallet_example_offchain_worker/lib.rs.html#18-709)
  and its [rustdoc](https://paritytech.github.io/substrate/latest/pallet_example_offchain_worker/).
  This pallet is also [added in this repository](pallets/example-offchain-worker).
