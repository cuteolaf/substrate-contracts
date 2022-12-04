# Posts
> Smart contract by ink!

## What does it do?
- Create a post
- Add reactions to a post (Like / Dislike)

## How to compile
Run `cargo contract build --release`

## How to deploy

### Deploy with CLI tools
1. Upload the WASM code to the node(with pallet-contracts)
```bash
cargo contract upload --url ws://localhost:9944 -suri <Secret Key URI> ./target/ink/posts.wasm
```
2. Instantiate the uploaded smart contract
```bash
cargo contract instantiate --url ws://localhost:9944 --suri <Secret Key URI> ./target/ink/posts.wasm
```

### Deploy with the ContractS UI
1. Run the blockchain node

```bash
./target/release/node-template --dev --tmp
```

2. Open the [Contracts UI](https://weightv1--contracts-ui.netlify.app/) and verify that it is connected to the local node.

3. Click **Add New Contract**.

4. Click **Upload New Contract Code**.

5. Select the `posts.contract` file, then click **Next**.

6. Click **Upload and Instantiate**.

7. Explore and interact with the smart contract using the Contracts UI.

