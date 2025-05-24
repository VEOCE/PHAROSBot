# PHAROS TESTNET
## Features ✨

- **Automated Swaps**: Performs random swaps between WPHRS and USDC tokens
- **PHRS Transfers**: Sends small amounts of PHRS to random addresses
- **Faucet Claims**: Automatically claims testnet tokens from the faucet
- **Daily Check-ins**: Completes daily check-in tasks for potential rewards
- **Proxy Support**: Rotates proxies for each operation (if provided)
- **Multi-wallet Support**: Processes multiple wallets sequentially

## Prerequisites 📋

- Node.js (v18 or higher)
- npm or yarn
- Pharos Testnet wallet with private keys
- (Optional) Proxy list in `proxies.txt`

## Installation ⚙️

1. Clone the repository:
   ```bash
   git clone https://github.com/VEOCE/PHAROSBot.git
   cd Pharos-Auto-Bot
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `nano .env` file in the root directory with your private keys:
   ```
   PRIVATE_KEY_1=your_first_private_key_here
   PRIVATE_KEY_2=your_second_private_key_here
   ```

4. (Optional) Add proxies to `proxies.txt` (one per line):
   ```
   http://user:pass@ip:port
   socks5://user:pass@ip:port
   ```

## Usage 🚀

Run the bot:
```bash
node index.js
```

The bot will:
1. Display a banner with project info
2. Load proxies (if available)
3. Process each wallet sequentially:
   - Claim faucet (if available)
   - Perform daily check-in
   - Execute 10 PHRS transfers
   - Execute 10 token swaps
4. Repeat every 30 minutes

## Important Notes ⚠️

1. This bot is for TESTNET use only
2. Never use mainnet private keys
3. The bot runs indefinitely until stopped (Ctrl+C)
4. All transactions use 0 gas price (testnet feature)
5. The bot includes random delays between operations
