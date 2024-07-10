# DegenToken Smart Contract

This repository contains the `DegenToken` smart contract, an ERC20 token with minting, burning, transferring, and game store functionalities.

## Contract Functions

- **mint**: `function mint(address to, uint256 amount) public onlyOwner`
  - Mints tokens to the specified address. Only the owner can call this.

- **transferTokens**: `function transferTokens(address _receiver, uint amount) external`
  - Transfers tokens from the caller to the specified receiver.

- **checkBalance**: `function checkBalance() external view returns (uint)`
  - Returns the balance of the caller.

- **burnTokens**: `function burnTokens(uint amount) external`
  - Burns the specified amount of tokens from the caller's account.

- **gameStore**: `function gameStore() public pure returns (string memory)`
  - Returns a list of items available in the game store.

- **redeemTokens**: `function redeemTokens(uint choice) external payable`
  - Redeems tokens for items from the store based on the user's choice.

## Deployment on Remix

### Steps

1. **Open Remix IDE**: Go to [Remix IDE](https://remix.ethereum.org/).
2. **Create and Paste Code**: Create a new file named `DegenToken.sol` and paste the contract code.
3. **Compile**: Select the compiler version `0.8.25` and compile the contract.
4. **Deploy**:
   - Use `Injected Web3` environment for MetaMask.
   - Connect MetaMask to Avalanche Fuji Testnet.
   - Deploy the contract and confirm in MetaMask.

### Adding Avalanche Fuji Testnet to MetaMask

- Network Name: Avalanche Fuji C-Chain
- New RPC URL: `https://api.avax-test.network/ext/bc/C/rpc`
- ChainID: `43113`
- Symbol: `AVAX`
- Block Explorer URL: `https://testnet.snowtrace.io`

### Get Test AVAX

- Use a faucet to get test AVAX tokens for your MetaMask wallet.

## Verification on Snowtrace

1. **Find Contract**: Copy the contract address from Remix and search it on [Snowtrace](https://testnet.snowtrace.io/).
2. **Verify and Publish**:
   - Go to the `Code` tab.
   - Click `Verify and Publish`.
   - Select `Solidity (Single file)`, version `0.8.25`, and enable optimization.
   - Paste the contract code and verify.

## Interacting with Verified Contract

Once verified, you can interact with the contract directly on Snowtrace.

---

This README provides a quick guide to deploying, compiling, and verifying the `DegenToken` smart contract using Remix and Snowtrace.
