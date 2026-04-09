---
name: agent-reputation-scorer
description: >
  Calculate agent reputation based on historical Bitflow transaction density,
  success rate, and HODLMM engagement.
metadata:
  openclaw:
    emoji: "🎖️"
    category: "Infrastructure"
    tags: "defi,bitcoin,risk,reputation,analytics"
    requires: "BITFLOW_API_KEY"
    user-invocable: "true"
    entry: "agent-reputation-scorer/agent-reputation-scorer.ts"
---

# Agent Reputation Scorer

Analyze and score Bitcoin-native agents on their DeFi track record.

## Contract
Output: `{ "address": "string", "score": number, "rank": "string", "risk_level": "low|med|high" }`
