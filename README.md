# 🪙 SUI Distributor • Batch Sender via CSV

A modern web interface for sending **SUI tokens in batches** using a simple CSV file.  
Built with pure **HTML, CSS, and JavaScript**, it allows anyone to upload a CSV with wallet addresses and amounts, validate the data, and send multiple transactions on-chain using **Sui-compatible wallets** such as **Suiet**, **Slush**, or **Sui Wallet**.

---

## 🚀 Features

- 🧾 **CSV Upload** — drag & drop or select a `.csv` file with columns `address,value`
- ✅ **Validation** — automatic validation of wallet addresses and numeric values
- 📊 **Preview Table** — editable preview with validation highlights
- 🧮 **Automatic Totals** — displays the number of rows, valid entries, and total SUI amount
- 💾 **Export JSON** — copy or download your validated batch in JSON format
- 🔗 **Wallet Connection** — supports Sui wallets via the [Wallet Standard API](https://docs.sui.io/standards/wallet-standard)
- ⚙️ **Network Selection** — Devnet, Testnet, and Mainnet supported
- ⛽ **Gas Budget Control** — set custom gas budget for your transactions
- 🧱 **Move Module Integration** — interacts directly with your deployed Move contract

---
🧩 How It Works

Upload a .csv file with format:

address,value
0x123...,1.5
0xabc...,0.25


The app validates each address and value.

Click Connect Wallet to authorize your Suiet/Slush/Sui Wallet.

Review and correct invalid rows.

Click Send Batch to execute your on-chain Move module function:

<PACKAGE_ID>::batch_distribute::distribute


The console log shows full transaction details.

💡 Notes

Works best with the latest versions of Suiet, Slush, or Sui Wallet extensions.

Ensure your wallet is set to the same network (Devnet/Testnet/Mainnet) selected in the app.

If the wallet doesn’t connect, reload the page and verify that your extension grants “site access.”

🧠 Tech Stack

Frontend: HTML5, CSS3, JavaScript (ES Modules)

Blockchain: Move language (Sui framework)

Wallet Integration: Wallet Standard API

Network SDK: @mysten/sui v1.42.0

🧪 Testing

The UI includes built-in validation tests.
Click “Run Tests” to execute browser-based checks for:

Address validation (isSuiAddress)

CSV parsing logic

Input data consistency

📜 License

MIT License © 2025  Johnathan Soares
Free to use and modify — please credit the original project if you fork or reuse it.

🧰 Credits

Developed by Johnathan Soares
Built for the SUI Bootcamp community — empowering developers to automate token distribution using on-chain Move modules.