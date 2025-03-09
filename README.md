# Bitcoin Wallet Generator and Fund Transfer Script

This Python script allows you to generate multiple Bitcoin wallets, check their balances, and transfer funds to a specified destination address. It uses the `bitcoinlib` library for wallet management and interacts with external APIs (`mempool.space` and `Blockchair`) for dynamic fee estimation and balance checking.

## Features
- **Wallet Generation**: Generate new Bitcoin wallets with private keys and addresses.
- **Balance Checking**: Check the BTC balance of generated wallets using the Blockchair API.
- **Dynamic Fee Estimation**: Fetch recommended transaction fees using the Mempool API.
- **Fund Transfer**: Transfer funds from generated wallets to a specified destination address.

## Prerequisites
Before using this script, ensure you have the following:
1. **Python 3.x** installed on your machine.
2. Required Python libraries installed (see `requirements.txt`).
3. A stable internet connection (for interacting with APIs).

## Installation
1. Clone this repository (if applicable):
   ```bash
   git clone https://github.com/moxonx/Bitcoin-Wallet-brute-force.git
   cd bitcoin-wallet-generator
   ```
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Run the script:
   ```bash
   python wallet_transfer.py
   ```
2. Follow the prompts:
   - Enter the number of wallets to generate.
   - Enter the destination wallet address.
3. The script will:
   - Generate the specified number of wallets.
   - Check the balance of each wallet.
   - Transfer funds (if any) to the destination address.

## Example Output
```
2023-10-01 12:00:00 - INFO - Generated new wallet - Address: 1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa, Private Key: L4gB6...
2023-10-01 12:00:05 - INFO - Balance for 1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa: 0.001 BTC
2023-10-01 12:00:10 - INFO - Transaction successful! Sent 0.0009 BTC from 1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa to 3J98t1WpEZ73CNmQviecrnyiWrnqRhWNLy. TXID: abc123...
```

## Important Notes
- **Security**: Never share your private keys or commit them to version control. Use this script in a secure environment.
- **Testnet**: For testing, you can switch to the Bitcoin testnet by modifying the `network` parameter in the `wallet_create_or_open` function.
- **API Limits**: Be aware of API rate limits for `mempool.space` and `Blockchair`. If you encounter issues, consider using premium API keys.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Support
If you find this project helpful, consider giving it a ⭐ on GitHub. For questions or issues, please open an issue in the repository.
