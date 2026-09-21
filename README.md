# Peer Point Montreal Agent Hackathon

Build and deploy one of five Cloudflare Agent challenges. Each card starts as a working, limited application. Choose a card, deploy it to your temporary lab account, then give the generated Git repository URL to Peer Point OS or clone it into your own IDE.

## Start

1. Choose one card below.
2. Select its **Deploy to Cloudflare** button.
3. Authorize GitHub and select only your temporary lab account.
4. Wait for the starter deployment to finish.
5. Copy the generated Git repository URL.
6. Give the URL to Peer Point OS, or clone it locally.
7. Build, verify, push, and let Workers Builds redeploy automatically.

| Card          | Build                                         | Main primitives                                 | Repository                | Deploy                | Status                           |
| ------------- | --------------------------------------------- | ----------------------------------------------- | ------------------------- | --------------------- | -------------------------------- |
| Threat Hunter | Investigate a seeded authentication attack    | Agents, Workers AI, AI Gateway, Durable Objects | `[CARD_1_REPOSITORY_URL]` | `[CARD_1_DEPLOY_URL]` | Ready                            |
| Code Review   | Repair a failing repository in isolation      | Agents, Sandbox, Containers                     | `[CARD_2_REPOSITORY_URL]` | `[CARD_2_DEPLOY_URL]` | Ready with preview fallback      |
| Inbox Agent   | Clarify an email and gate sending on approval | Agents, durable Actions, Email                  | `[CARD_3_REPOSITORY_URL]` | `[CARD_3_DEPLOY_URL]` | Ready with simulator fallback    |
| Cross-System  | Join CRM, ERP, Jira, and config evidence      | Agents, MCP Portal, Access                      | `[CARD_4_REPOSITORY_URL]` | `[CARD_4_DEPLOY_URL]` | Ready with direct MCP fallback   |
| Watcher       | Detect one material page change without noise | Browser Run, R2, scheduled tasks                | `[CARD_5_REPOSITORY_URL]` | `[CARD_5_DEPLOY_URL]` | Ready with manual-check fallback |

## Peer Point OS prompt

```text
Clone this repository in an isolated Container MCP environment. Read the complete README before editing. Run npm ci and npm run verify to establish a baseline. Implement a working version of the challenge while preserving its Cloudflare primitives and safety constraints. You may choose a different architecture from the suggested path. Run focused tests and npm run verify, inspect the diff, then push through the GitHub gatekeeper. Do not claim success until verification passes. After the push, inspect Workers Builds and give me the deployed URL and demo checklist.
```

## Own IDE

```bash
npm ci
npm run verify
npm run dev
```

After implementing your card:

```bash
npm run verify
npm run deploy
```

## Rules

- Deploy only to the assigned temporary lab account.
- Never commit tokens, capabilities, or private keys.
- Do not hardcode the expected answer.
- Preserve each card's validation, bounds, and approval controls.
- A different implementation is welcome if the required behavior and Cloudflare primitives remain demonstrable.

## Links

- Peer Point OS: `[PEER_POINT_OS_URL]`
- Slides: `[EVENT_SLIDES_URL]`
- Support: `[EVENT_SUPPORT_URL]`
