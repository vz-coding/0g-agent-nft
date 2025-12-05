# Steps to deploy

## Setup
```bash
pnpm install
```

`npm install` will fail at figuring out the `@types/chai` dependencies.

## Config .env

Config your `.env` file from the [.env.example](./.env.example)

Fill the `*_PRIVATE_KEY` with your own private keys (Can be same for the demo purpose).

## Deploy

Run

```bash
npx hardhat compile
```

to compile the contracts first.


Then run

```bash
npx hardhat deploy --network zgTestnet
```

to deploy.

You will see the similar output as below.

```bash
🚀 Deploying TEEVerifier with account: 0x6d21AE116C1150016D3C14cc0d53B1a5324Db7D8
📝 Deploying TEEVerifier with Beacon Proxy...
📋 Using trusted measurements:
  MRTD: 0x0000000000000000000000000000000000000000000000000000000000000000
  RTMR0: 0x0000000000000000000000000000000000000000000000000000000000000000
  RTMR1: 0x0000000000000000000000000000000000000000000000000000000000000000
  RTMR2: 0x0000000000000000000000000000000000000000000000000000000000000000
  RTMR3: 0x0000000000000000000000000000000000000000000000000000000000000000
deploying "TEEVerifierImpl" (tx: 0x0007da684424651a61ca7e24e5b4bc5cfa3c1dfdff18f4b7e2e48684df82fab3)...: deployed at 0x7507e21C88DFE9288326F4B6C9708F202369dCf6 with 591667 gas
deploying "TEEVerifierBeacon" (tx: 0xebdf432468f9bb9acb2349ec15bd910edc9447959e0824932dc6d1b52032fed2)...: deployed at 0xA8926a2d098Bcf436b5543aBD023D0fd859A0414 with 252039 gas
deploying "TEEVerifier" (tx: 0xe61a5e6ebdbeec70658d8c13d589369155eee8813557ea9af28349664652c8d7)...: deployed at 0x097Be94b8Ef5FC8a3a707dfd8D5D53a32a06A784 with 229860 gas
✅ TEEVerifier deployed at: 0x097Be94b8Ef5FC8a3a707dfd8D5D53a32a06A784
🔍 Deployment verification:
  Verified: true
  TEE Address: 0x168752bb1d04b4c93F3ED0a6e8F84534b16F2014
🚀 Deploying Verifier with account: 0x6d21AE116C1150016D3C14cc0d53B1a5324Db7D8
📝 Deploying Verifier with Beacon Proxy...
📋 Using TEEVerifier as ATTESTATION_CONTRACT: 0x097Be94b8Ef5FC8a3a707dfd8D5D53a32a06A784
📋 Attestation config:
  Oracle Type: 0
  Contract Address: 0x097Be94b8Ef5FC8a3a707dfd8D5D53a32a06A784
deploying "VerifierImpl" (tx: 0x00afb1c2f6c0e245a0dd9e35a238c8cbc02b238db47512d3e0670d994b49d5b5)...: deployed at 0x0ab9ab46a064dcCba6Ba9949281a7ab87AEe879A with 1976720 gas
deploying "VerifierBeacon" (tx: 0x3fdf54763408c38b17588d10b88f4c7165ff68d6b577f4ebae8522d2b04bd068)...: deployed at 0xdf4fd41BacfB22A84ba7505ec38916A31F4ec750 with 252039 gas
deploying "Verifier" (tx: 0x5083e8601b6ab0de34ea3385381735f4ea9fd434a4d7e5a01c736d0cefc0a828)...: deployed at 0x367F270a3bC0e611219391deaDE5dDFE924Adb1B with 364550 gas
✅ Verifier deployed at: 0x367F270a3bC0e611219391deaDE5dDFE924Adb1B
🚀 Deploying AgentNFT with account: 0x6d21AE116C1150016D3C14cc0d53B1a5324Db7D8
📋 Using Verifier at: 0x367F270a3bC0e611219391deaDE5dDFE924Adb1B
📝 Deploying AgentNFT with Beacon Proxy...
deploying "AgentNFTImpl" (tx: 0x746d950e7458b5d1645718bd9fe7e208f38a5a46880444b4e70c042d471c525b)...: deployed at 0x4c6733Df2B07B879888efE31dEEd1337224F1E82 with 3594043 gas
deploying "AgentNFTBeacon" (tx: 0xcfc8d6e80c0df2a29edc28a0bdba0953e9548265a5595e8bb0dbf5b3d2e2282f)...: deployed at 0x2e750eE832B7926C71ab61E72Ce585a6E6F959a3 with 252039 gas
deploying "AgentNFT" (tx: 0x16803c970ea8f9ade9bcdd8b9b2830156ffdacd2917f969580d0f0d265785b78)...: deployed at 0x73950D6f0C04d37a52a7bD057B1f480c2B425913 with 500978 gas
✅ AgentNFT deployed at: 0x73950D6f0C04d37a52a7bD057B1f480c2B425913
🚀 Deploying AgentMarket with account: 0x6d21AE116C1150016D3C14cc0d53B1a5324Db7D8
📋 Using AgentNFT at: 0x73950D6f0C04d37a52a7bD057B1f480c2B425913
📝 Deploying AgentMarket with Beacon Proxy...
deploying "AgentMarketImpl" (tx: 0xbc1599234e629a2ff0edc6837d8ad49fd7b31610157c5a463f82ed577ba54d8b)...: deployed at 0x81B57ca3723d5F738282DdFEAbA3613d13076f25 with 2745356 gas
deploying "AgentMarketBeacon" (tx: 0x3f2d8db34c7eff1890bacd3eb2f1824b06422a64e055fb8d0266304073c92b3e)...: deployed at 0xc0235ee7c12D7287B84F40cb61a64F8c091E66d3 with 252039 gas
deploying "AgentMarket" (tx: 0x81f1db0e7ee54d602fc9e1a06fcaac150ff1918121ae824ff619b641aede7640)...: deployed at 0xe601438c21D2e637935E32E9E10DbD7C4C6CBF7B with 385902 gas
✅ AgentMarket deployed at: 0xe601438c21D2e637935E32E9E10DbD7C4C6CBF7B
```

The full deployment includes a lot of things, like `Verifier`, `AgentNFT`, `AgentMarket` etc.

You can check the contracts on the 0g Chainscan, the [AgentNFT](https://chainscan-galileo.0g.ai/address/0x73950d6f0c04d37a52a7bd057b1f480c2b425913) as an example.
