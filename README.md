# Launch your own Initial Coin Offering

This repo contains coursework project from [LearnWeb3](https://learnweb3.io/) completed by [0xsenzel](https://github.com/0xSenzel/) for [LearnWeb3DAO-Sophomore](https://learnweb3.io/courses/c1d7081b-63a9-4c6e-b35c-9fcbbad418b2) lesson.

## Project Info

NFT Collection allows whitelisted address from [Whitelist-Dapp](https://0xsenzel-whitelist-dapp.vercel.app/) to mint our NFT collection. The Dapp will be able to mint 20 different NFT based on the sequence of minter.

## Project Demo

<figure>
<img src="./my-app/public/demo1.PNG" alt="demo1" style="width:100%">
<p align="center">Fig.1 - Home Page When Login By Non-Owner Address Before Starting of Presale</p>
</figure>

<br/>

<figure>
<img src="./my-app/public/demo2.PNG" alt="demo1" style="width:100%">
<p align="center">Fig.2 - Home Page When Login By Owner Address Before Starting of Presale</p>
</figure>

<br/>

<figure>
<img src="./my-app/public/demo3.PNG" alt="demo1" style="width:100%">
<p align="center">Fig.3 - Home Page After Presale Started</p>
</figure>

## Project Setup

### Hardhat

Head to [hardhat-tutorial](./hardhat-tutorial/) folder:

Install dependencies

```
npm install
```

Compile smart contract

```
npx hardhat compile
```

To deploy smart contracts: <br/>
Head to [hardhat.config.js](./hardhat-tutorial/hardhat.config.js) file, change the value of:

- `ALCHEMY_HTTP_URL` with your own Ethereum Network API
- `PRIVATE_KEY` with your Ethereum wallet's private key
- `API_KEY` with your Etherscan's API Key

Then run the following command.

```
npx hardhat run scripts/deploy.js --network goerli
npx hardhat verify --network goerli YOUR_SMARTCONTRACT_ADDRESS "CONSTRUCTOR ARG1"
```

### React & Next Js

Head to [my-app](./my-app/) folder:

```
npm install
```

Replace the variable inside [this folder](./my-app/constants/index.js):

- `NFT_CONTRACT_ABI` with compiled ABI of [NFT-Collection](https://github.com/0xSenzel/nft-collection) contract.
- `NFT_CONTRACT_ADDRESS` with deployed contract of [NFT-Collection](https://github.com/0xSenzel/nft-collection) contract.
- `TOKEN_CONTRACT_ABI` with compiled ABI of this contract
- `TOKEN_CONTRACT_ADDRESS` with deployed contract of this contract

To run the app locally:

```
npm run dev
```
