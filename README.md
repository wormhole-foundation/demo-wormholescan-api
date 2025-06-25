# WormholeScan API Demo

This project demonstrates how to fetch and analyze data from the [WormholeScan API](https://wormholescan.io/#/developers/api-doc). It showcases querying NTT token configurations and tracking cross-chain transfer operations using the WormholeScan API endpoints.


## Project Structure

The project is organized as follows:

```plaintext
demo-wormholescan-api/
├── src/
│   ├── helpers/
│   │   ├── api-client.ts       # API client for WormholeScan endpoints (mainnet & testnet)
│   │   ├── types.ts            # TypeScript interfaces for API responses
│   │   └── utils.ts            # Utility functions for platform mapping and status detection
│   └── scripts/
│       ├── fetch-ntt-tokens.ts # Script to fetch and display NTT token configurations
│       └── fetch-operations.ts # Script to fetch and track cross-chain transfer operations
├── package.json                # Project dependencies and scripts
└── tsconfig.json               # TypeScript configuration
```

## Prerequisites

Ensure you have the following installed:

- [Node.js and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) installed on your machine

## Setup and Usage

Follow these steps to clone the repository and start querying the WormholeScan API.

**1. Clone the Repository**

```bash
git clone https://github.com/wormhole-foundation/demo-wormholescan-api.git
cd demo-wormholescan-api
```

**2. Install Dependencies**

```bash
npm install
```

## Available Scripts

### Fetch NTT Tokens

Query and display Native Token Transfer (NTT) token configurations from the mainnet WormholeScan API:

```bash
npm run ntt-tokens
```

This script:
- Fetches NTT token list from the mainnet API
- Displays token details including manager addresses, versions, and transceiver information

### Fetch Operations

Track cross-chain transfer operations and their status from the testnet WormholeScan API:

```bash
npm run operations
```

This script:
- Fetches operation data for a specific emitter address
- Shows transfer status progression: `In Progress` → `Emitted` → `Completed`
- Displays transaction hashes, chain routing, and completion status

## Configuration

You can customize the following within the scripts:

- **NTT Tokens**: Modify `TOKENS_TO_PROCESS` in `fetch-ntt-tokens.ts` to change the number of tokens displayed
- **Operations**: Update `EMITTER_ADDRESS` in `fetch-operations.ts` to track a different address
- **API Endpoints**: The scripts use both mainnet and testnet endpoints automatically
