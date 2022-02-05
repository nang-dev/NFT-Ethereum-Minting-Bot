# NFT Ethereum Minting Script ⚡️

## Programmically mints NFT during drop directly from the smart contract faster and with higher priority than any human can.

# Problem ⚡️

NFT's are hype at the moment, and each NFT project has a minting phase and a trading phase. Minting is when the NFT's are created on the blockchain for the first time. 

During popular projects, minting price will be low (Ex. 0.08 eth), and can be immediately traded for a high price (Ex. 2 eth). There is a limited amount of spots to mint, and a lot of people trying to mint the NFT. As a result, gas prices spike, and the NFT's can sell out in seconds. 

The normal procedure to mint and NFT is to go on their website and click mint during the public sale. Due to demand, the website is almost always crashing or unloadable.

The next step up is to mint through Etherscan, but this needs Metamask sign in and gas prices have to be set on the spot manually.

# Solution ⚡️

Simple script that talks to the underlying smart contract directly (using RPC call via web3 API). 

Two variables are important, speed and gas price. 

WILL WRITE LATER

# Setup

1. Install node and repo's dependencies

2. Fill in .env with your wallet's public address, private address, and infura url.

3. Edit contractAddr and abi (found in smart contract's Etherscan).

4. Edit contract specific variables: valueSingle, gasPrice, count.

5. Edit smart contract RPC call (line 40) to match the smart contract's minting function (found in smart contract's Etherscan)

# How to run ⚡️

After setup, run:

`node mint.js`

To run on multiple (two) wallets add MY_PUBLIC_ADDR2 and MY_PRIVATE_ADDR2 to env and run (UNDER CONSTRUCTION):
`node mint.js & ; node mint2.js`

During the time of public sale release.

# Next steps ⚡️

Hopefully automate this process more. The challenge is that the function to mint varies from contract to contract. For this reason, contract-specific variables are in the main js function. Once I figure out how to programically set the method call (sniff on Etherscan?), I'll move them out to a separate variable file for readability.

# Does it work? ⚡️

So far, I've tested it once and it was successful on the drop of White Rabbits by GATE: https://etherscan.io/tx/0x2bd04f1948ad747a9e021edf82a3412a4f2fa1a743e8a441b1e411340a25d488