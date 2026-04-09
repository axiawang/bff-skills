---
name: agent-reputation-scorer
description: >
  Calculate agent reputation based on historical Bitflow transaction density,
  success rate, and HODLMM engagement.
metadata:
  openclaw:
    author: "axiawang"
    emoji: "🎖️"
    category: "Infrastructure"
    tags: "defi,bitcoin,risk,reputation,analytics"
    requires: "BITFLOW_API_KEY"
    user-invocable: "false"
    entry: "agent-reputation-scorer/agent-reputation-scorer.ts"
---

# Agent Reputation Scorer

Analyze and score Bitcoin-native agents on their DeFi track record.

## What it does
This skill scans the Bitflow transaction history of a given Stacks address to evaluate its reliability. It considers transaction frequency, successful completion rates, and historical liquidity provision (HODLMM) to generate a weighted reputation score (0-100).

## Why agents need it
Autonomous agents need a way to verify the "credit-worthiness" of other agents before engaging in complex DeFi swaps or multi-agent escrow agreements. This skill provides a trust layer for the agentic economy.

## Commands
- `get-reputation <address>`: Returns the reputation scorecard for the specified STX address.

## Output contract
Success: `{ "address": "string", "score": number, "rank": "string", "risk_level": "low|med|high", "proof": "string" }`
Error: `{ "error": "descriptive message" }`

## Safety notes
This skill only performs read-only operations on-chain. It does not require private keys and cannot move funds.
