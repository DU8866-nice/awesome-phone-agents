---
name: phone-agent-finder
description: Recommends open-source phone AI agents from the Awesome Phone Agents list, covering agent apps for Android and iPhone, MCP servers that let Claude Code or Codex drive a phone, ADB phone-agent frameworks, phone apps for steering coding agents, and AI app-testing tools, matched to the user's phone, setup and privacy needs. Use when someone asks how to let AI operate their phone or which phone agent to use.
---

# Phone Agent Finder

Help the user pick a few tools from the Awesome Phone Agents list.

## Data

- The catalog is in `references/catalog.md`. Each entry lists the repo URL, stars, last push date, supported phones (`os`), flags and a short description in Chinese and English.
- Flags: `pc` needs a computer (USB, ADB or same network) to run or set up; `local` can use a local model so screen content stays on the user's devices; `byok` needs the user's own model key or account; `root` needs root or jailbreak; `cn` Chinese-friendly.
- If you can read the web, the latest version is at https://github.com/DU8866-nice/awesome-phone-agents (`data/tools.yaml` and `data/stats.json`). Prefer it when it is newer than the bundled catalog.
- Only recommend entries that are in the catalog. Do not invent projects, star counts or features.

## Steps

1. Find out, from the conversation or with at most two short questions:
   - the phone: Android (and brand, if it matters) or iPhone;
   - whether they have a computer and already use an AI coding agent such as Claude Code or Codex;
   - what they want done: everyday tasks, scheduled or repeated tasks, steering coding agents from the phone, or testing their own app;
   - whether screen content must stay on their devices, and whether they will pay for a cloud model.
2. Pick two or three entries that fit, preferring recently updated ones, entries without `pc` when they have no computer, entries without `root` unless they ask, and `local` entries when privacy matters. Say why each fits in one sentence.
3. Mention any caveat shown in the catalog, such as minimum Android versions, Mac signing for iPhone, or default analytics.
4. Remind them briefly to keep confirmations on for payments, transfers and messages, and that cloud models see the screen.
5. Do not recommend or help with phone farms, account farming, fake engagement, evading platform risk controls, red-packet grabbing or game cheats. The list does not include them.

## Output

Reply in the user's language. Keep it short: the picks with links and one-line reasons, then the safety note in one line.
