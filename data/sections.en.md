<!-- section:intro -->
The "AI phone" is moving from launch events into everyone's hands: say "sum up this group chat" or "compare prices and add it to my cart", and the AI opens the app, reads the screen, taps and types until the job is done. In the past few months the open-source community has produced a wave of these tools: apps you install on an Android phone, MCP servers that hand your phone to Claude Code or Codex, and open frameworks and models such as Zhipu's Open-AutoGLM and Alibaba's Mobile-Agent.

This list is for people who want to use them, not a paper list. It sorts the tools by your device and setup and shows, for each one, Android or iPhone support, whether it needs a computer or root, and whether it can use a local model.

<!-- section:pick -->
## Pick by your setup

| Your situation | Try first |
|---|---|
| Android phone, no computer | [Mika](https://github.com/wangzan101/Mika), [Operit](https://github.com/AAswordman/Operit), [DSH-Android](https://github.com/jackwener/DSH-Android), [PokeClaw](https://github.com/agents-io/PokeClaw) (local model) |
| Android, agent works in the background | [Mika](https://github.com/wangzan101/Mika), [DSH-Android](https://github.com/jackwener/DSH-Android), [Ruto](https://github.com/iamr0s/Ruto-GLM) (virtual display) |
| iPhone | [Pinky](https://github.com/DIYgod/pinky) (with a computer), [Roubao](https://github.com/Turbo1123/roubao) (one-time Mac signing), [PhoneClaw](https://github.com/kellyvv/PhoneClaw) (local model) |
| You already use Claude Code or Codex | [Pinky](https://github.com/DIYgod/pinky), [mobile-mcp](https://github.com/mobile-next/mobile-mcp), [iPhone Use](https://github.com/zhongerxin/iPhone-use) |
| Scheduled or repeated tasks | [Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM), [AutoGLM-GUI](https://github.com/suyiiyii/AutoGLM-GUI), [Mobilerun](https://github.com/droidrun/mobilerun) |
| Keep an eye on coding agents while away | [T3 Code](https://github.com/pingdotgg/t3code), [Paseo](https://github.com/getpaseo/paseo), [CC Pocket](https://github.com/K9i-0/ccpocket) |
| Developer testing your own app | [Midscene](https://github.com/web-infra-dev/midscene), [agent-device](https://github.com/callstack/agent-device), [Argent](https://github.com/software-mansion/argent) |

<!-- section:rules -->
## Good to know

> [!IMPORTANT]
> - **Your screen goes to the model.** These tools "see" the phone through screenshots or the UI tree, so chats, one-time codes and balances may be in view. With a cloud model, that content goes to the model provider; tools marked 🔒 can use a local model so it stays on your devices.
> - **Confirm payments, transfers and deletions yourself.** Prefer tools that ask before paying or sending messages by default, and keep those confirmations on. Don't leave an agent unsupervised around wallets, banking or anything that can't be undone.
> - **Access granted is access used.** Accessibility, Shizuku, ADB and root all hand over most control of the phone. Download only from official repos, grant access only to tools you trust, and turn off remote access when you're done.
> - **Mind the platform rules.** Many apps forbid automation in their terms, and frequent automated taps can trip risk controls and get accounts restricted. Use these for your own chores, not to inflate numbers.
> - **iPhone limits.** iOS doesn't let ordinary apps control other apps, so most iPhone options need a computer, or a Mac to sign and install, with signing that needs upkeep.

This list does not include phone-farm, account-farming, fake-engagement or multi-account marketing tools, "stealth" cloud phones built to evade detection, or red-packet grabbers and game cheats.

<!-- section:faq -->
## FAQ

**How is this different from the AI assistant my phone maker ships?**
Built-in assistants have system-level access and feel smoother, but only on certain phones and with a fixed model. The open-source tools here install on most Android phones, let you pick the model and let you read the code; the trade-off is setup work and reliability that varies by app.

**Do I need root?**
Mostly no. Android apps usually use Accessibility; working on a background virtual display usually needs Shizuku or wireless debugging. Only a few tools need root, and jailbreak-based iPhone tools are marked 🔓.

**Does it cost anything?**
The tools are open source. Cloud models cost whatever the provider charges; tools such as PokeClaw and PhoneClaw can run a local model on the phone for free, but need capable hardware and are slower.

**What is it best at?**
Jobs with lots of reading and tapping but little judgment: summing up chats and posts, looking things up, comparing prices, filling forms, tidying files and testing your own app. For anything involving money or privacy, let it prepare and tap the last step yourself.

**How often are stars updated?**
Every Monday GitHub Actions refreshes the stars and re-sorts the list, and links are checked weekly.

<!-- section:finder -->
## Let your AI agent pick

This list is also a skill. Install the [`skills/phone-agent-finder`](skills/phone-agent-finder) folder in your AI agent (or run `npx skills add DU8866-nice/awesome-phone-agents`) and ask:

> I have a Pixel, don't want to root it or plug it into a computer, and want AI to sum up a few group chats every day. Which tool should I use?

It picks two or three entries for your phone, whether you have a computer, your privacy needs and the task, explains why, and points out what to watch for with payments and privacy.

<!-- section:contributing -->
## Contributing

Suggestions and corrections are welcome: [open an issue](https://github.com/DU8866-nice/awesome-phone-agents/issues/new/choose), or edit [`data/tools.yaml`](data/tools.yaml) and send a PR. See the [contributing guide](CONTRIBUTING.md). The README is generated by a script, so please don't edit it directly.
