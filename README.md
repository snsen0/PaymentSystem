# Cryptocurrency Payment System

This React Native application utilizes a timer to monitor the session timeout of the user. If the user remains inactive for a specified period, the session expires, and they are redirected to the login page.

User wallet information (address, private key, mnemonic) is stored using react-native-encrypted-storage. If the wallet already exists, the information is retrieved; otherwise, a new wallet is created.

Wallet balances on different blockchain networks (SciChain, Binance, Ethereum) are obtained using the ethers.js library and displayed on the screen.

A QR code scanner (react-native-qrcode-scanner) is employed to scan another user's wallet address. Token and coin transfer transactions are executed based on the information obtained from the scanned QR code. After payment, the success status and transaction details are acquired through the QR code.

JSON-RPC providers are used to connect to different blockchain networks. An Alert window is shown to the user for transaction confirmation. If the user confirms the transaction, the relevant transaction is executed, and the success status is sent to the success URL.

Using the Axios library, an HTTP POST request is sent to the success URL, containing the transaction hash and other essential information.

This code block is used to send a POST request to a success URL with the details of a transaction (token or coin transfer) after it has been successfully completed. The transaction details, such as the transaction hash (transactionHash), used RPC address (transferInfo.rpc), transferred amount (transferInfo.amount), and product ID (transferInfo.id), are included as parameters in this request.


## Installation

```sh
npm i
npm i react-native-get-random-values
npm i @ethersproject/shims
npm i ethers
npm i react-native-qrcode-scanner
npm i react-native-modal
npm i react-native-encrypted-storage
npm i react-native-qrcode-svg
npm i @react-native-community/clipboard
npm i axios
npx react-native start
```

<br />
<br />


![paymentSystem](https://github.com/snsen0/PaymentSystem/assets/148704343/acbbba6a-8d02-4796-bd3e-66d6c2ae83d2)



