---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundImage: url('https://marp.app/assets/hero-background.jpg')
---

**Crypto World Summit**

## Hunting the Bear:

# Yield Farming for Fun and Profit

**John Nguyen**
_Ninja Software CTO_
_Unqualified Bear Hunter_
_I just like the tech_

---

# Who am I?

![bg left:30%](./john_corporate.jpeg)

- John Nguyen
- Mining engineer (Piping, Mechanical, Process Controls, Industrial Networks)
- 15 years programming experience
- Ninja Software CTO

---

# Who am I in crypto?

![bg left:30%](./ghana.png)

- 9 years in crypto (2013)
- Ghana deployment
  - Bought BTC for $100
  - Tried to trade my watch for 5BTC
  - Bartered goods
  - Algorithmic trading bots on Mt Gox

---

![bg 80%](./watch.jpg)

---

# Who am I in crypto (cont.)?

![bg left:30%](./john_char.jpg)

- Cypherpunk phase
  - Crypto-steel and cold storage
  - Went into hibernation after the blocksize wars
- Blockchain forensic toolkit
- Build blockchain software
- Invest in DeFi projects

---

# Today's talk

- Yield farming via liquidity provisioning
- We'll be using Uniswap V3, the most cutting edge AMM
- Covering:
  - Position discovery
  - Range types
  - Position maintenance
- This is an _intermediate_ talk
  - Understand metamask, key management, gas fees, self-custody

---

# What is the blockchain?

- Decentralised triple entry ledger
  - Each blockchain contains multiple blocks
    - Each block contains cryptographically verified transactions
      - Transaction can be a simple value transfer or a complex smart contract invocation

Blockchain security is backed by consensus mechanisms (Proof of Work, Proof of Stake), driven by an incentivised miner or staking network.

---

# What are smart contracts?

- Functions that are deployed to the blockchain that interact with other contracts or wallet addresses
- Programs that execute logic and deal with the transfer of value

---

# What is DeFi?

- Decentralised finance
- A new space in the world of blockchains and cryptocurrency, only a few years old
- Trustless financial tools
- Lend, borrow, trade, insure
- Discover huge yields

## No middlemen, no vetting, no blockers

---

# What is Yield Farming?

- The art and science of combining the money legos of DeFi to maximise yield
- Lending tokens, borrowing tokens, derivative tokens, tokenised _everything_
- We can use these tokens and interoperate with different DeFi protocols in weird and wonderful ways

---

# What is an AMM?

- Automated Market Maker
- Two main parties:
  - Traders swaps between pairs
  - Liquidity providers can provide liquidity, receive fees and token rewards
- One of the blocks (money legos) for yield farming
- A few examples: Bancor, Balancer, Sushi, Uniswap V2/V3

---

# What is an AMM (cont.)?

![bg left:70% 90%](./xyk.png)

---

# What is Uniswap V3?

![bg left:30% 90%](./uni.svg)

- One of the most popular AMMs
- New version of Uniswap
- Highly capital efficient
- Liquidity providers create positions with a min and max value
- Can function as limit orders, avoiding slippage

---

# What is a position?

![bg left:20% 90%](./position.svg)

- A limit order that executes over a price range
- You provide liquidity on a pair (e.g. ETH/USDC) for other users to swap against

---

# What is a position (cont.)?

![bg left:20% 90%](./position.svg)

- While the market price is within your range:
  - Fees are generated (0.3%)
  - Your liquidity slowly shifts from one to the other
- While the market price is outside your range:
  - No fees are generated
  - Your liquidity is one-sided (100% ETH or 100% USDC)

---

# How do I choose a position?

- Step 1: Select pair (OHM/ETH)
- Step 2: Select position type (Over, Under, In-Range)
- Step 3: Select position range
- Step 4: Deploy your position
- Step 5: Maintain the position

---

# Step 1: Select Pair on dune

---

![bg 90%](./dune.png)

---

# Step 1 (cont.): Select Pair on dune

![bg 90%](./dune_table.png)

---

# Step 2: Select position type (Over, Under, In-Range)

![bg 90%](./over_range.png)
![bg 90%](./under_range.png)
![bg 90%](./in_range.png)

---

## Position Type: Over

![bg left:40% 90%](./over_range.png)

Good for bear market.

- Capture increases in price

---

# Position Type: Under

![bg left:40% 90%](./under_range.png)

Good for bull market.

- Capture dips in price

---

# Position Type: Within Range

![bg left:40% 90%](./in_range.png)

Good for sideways market.

- Capture fees from volatility
- Automatic rebalancing
  - "Sell" on the way up
  - "Buy" on the way down

---

# Step 3: Select position range (min and max price)

- This depends on price volatility.
- High volatility requires larger ranges
  - Greater exposure to price increases
  - Reduced fees
- Low volatility requires smallerranges
  - Greater exposure to price increases
  - Increased fees

---

![bg 90%](./flipside.png)

---

# Step 3 (cont.): Select position range

Play with the values in Flipside crypto to optimise your risk/reward.

## Position summary:

- Range: 2.2OHM to 4.2OHM
- Volatility: 100% of 5 day price captured
- Fees: 29USD fees generated per day for 2000USD investment

---

# Step 4: Deploy your position

Now it is time to deploy to Uniswap V3!

Make sure you have enough ETH in your wallet to pay the gas fees.

You may need to purchase one or the other token in the pair to be able to fund the position.

---

![bg 100%](./deploy_position.png)

---

# Step 5: Maintain the position

- Claim fees and compound
- Exit and redeploy after crossing over
- Exit and redeploy to chase the price

![bg left:50% 90%](./view_position.png)

---

# Risk 1 - Impermanent Loss

Price moves from one side of a position to the other, it is the equivalent of executing a limit order
Impermanent loss is only realized if you exit your position

- It will always be on the “wrong side”
  - If OHM goes to the moon, you will have 100% ETH
  - If ETH goes to the moon, you will have 100% OHM

Mitigation 1: Long both tokens so you’ll be happy either way
Mitigation 2: “Chase” price by closing and opening new positions

---

# Risk 2 - Volatile Market

- DeFi tokens are extremely volatile
- Reported APY is always changing
- Market can move the wrong way, requiring repositioning
- Gas fees will eat at your profits until roll-ups are more common

---

# Risk Mitigation

- Go through the 4 pillars of a good DeFi project
  - Community
  - Leadership
  - Security
  - Open source
- Come and see me if you want to learn more about due diligence for any DeFi projects

---

# What next?

We've barely scratched the surface of yield farming!

- Hunt for airdrops (UNI)
- Save gas with rollups (Optimism)
- Bond and stake LP tokens for additional rewards (Gysr)
- Leverage with Compound Finance and IndexCoop (ETH2X-FLI)
- Invest in indexed tokens (DPI, BED)
- Increase yield with recursive borrowing (Compound)

---

# What next (cont.)?

- Single sided staking (OHM)
- Buy some NFTs (OpenSea)
- Look into fixed income protocols (Pendle)
- Buy insurance (Nexus)
- Program your own smart contracts (Solidity)!

---

# Contact me

Happy to chat over a coffee about anything to do with crypto, NFTs, software engineering and app development.

- Email: john@ninjasoftware.com.au
- Twitter: @nii236

_Come get a limited edition NFT!_
