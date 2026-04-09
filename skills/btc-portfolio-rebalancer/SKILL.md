---
name: btc-portfolio-rebalancer
description: >
  Automatically rebalances Stacks/Bitcoin portfolios between Bitflow LPs and
  HODLMM pools based on yield delta.
metadata:
  openclaw:
    author: "axiawang"
    emoji: "⚖️"
    category: "Yield"
    tags: "defi,bitcoin,rebalance,btc-yield"
    requires: "BITFLOW_API_KEY,STX_PRIVATE_KEY"
    user-invocable: "false"
    entry: "btc-portfolio-rebalancer/btc-portfolio-rebalancer.ts"
---

# BTC Portfolio Rebalancer

Autonomous liquidity management for optimal Bitcoin-native yield.

## What it does
Monitors yield spreads across HODLMM pools and standard Bitflow LPs. It automatically moves user liquidity to the highest-performing pool.

## Why agents need it
Continuous yield chasing without manual oversight, staying delta-neutral.

## Commands
- `rebalance-now`: Orchestrates an immediate rebalance check and execution.

## Output contract
Success: `{ "status": "success", "from_pool": "string", "to_pool": "string", "amount_stx": number, "tx_hash": "string" }`
Error: `{ "error": "descriptive message" }`

## Safety notes
Includes a hard-coded 2% slippage cap. Requires transaction signing permission.
