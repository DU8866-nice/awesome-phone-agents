# Catalog

Generated from data/tools.yaml. Fields: repo | stars | last push | os | flags (pc = needs a computer, local = can use a local model, byok = needs own model key or account, root = needs root or jailbreak, cn = Chinese-friendly) | description (zh / en)

## 装在安卓手机上的 AI 智能体 / Agent apps for Android phones

- https://github.com/ccch1mneyyy/dsh-Go | stars=26073 | pushed=2026-11-18 | os=android | flags=cn
  - DeepSeek Harness 的手机应用：内置 Linux 环境，在手机本机运行，也能一键切到电脑上的 DSH 接着用；可以看屏幕替你点，三档确认，敏感操作默认交还给你。
  - A phone app for DeepSeek Harness with a built-in Linux environment: run it on the phone or switch to the DSH on your computer; it can read the screen and tap for you, with three confirmation levels and sensitive steps handed back by default.
  - caveat: The iOS version is still in development with no public build
- https://github.com/AAswordman/Operit | stars=9679 | pushed=2026-11-12 | os=android | flags=local,cn
  - 开源的安卓 AI Agent 平台：操作手机界面、内置浏览器和 Ubuntu 终端、长期记忆、MCP 和 Skill 扩展，可接云端模型，也能用 MNN 或 llama.cpp 跑本地模型。
  - An open-source agent platform for Android: it operates the phone UI, has a built-in browser and Ubuntu terminal, long-term memory, MCP and skills, and works with cloud models or local MNN and llama.cpp models.
  - caveat: Operates the UI through Accessibility, Shizuku or root; more access unlocks more
- https://github.com/wangzan101/Mika | stars=8974 | pushed=2026-11-17 | os=android | flags=byok
  - 说一句话，它在后台的隐藏屏幕上替你操作 App 和网页直到办完，你可以照常用手机；比如总结群聊、比价加购物车（停在结账前）。
  - Say what you need and it works your apps and the web on a hidden background screen until it's done, while you keep using your phone; it can sum up a group chat or add a pick to your cart and stop before checkout.
  - caveat: There is no Mika server; use your own model key or sign in with ChatGPT, xAI or OpenRouter. Operating apps needs Android 12+
- https://github.com/kuafuai/andee | stars=6152 | pushed=2026-11-17 | os=android,mac | flags=cn
  - 住在手机或 Mac 上、像人一样用任何 App 的 AI：不用接口、不用 root、不用插电脑，支持任意模型，带长期记忆。
  - An AI that lives on your phone or Mac and uses any app the way you do: no integrations, no root, no cable, any model, with long-term memory.
  - caveat: The README's one-click install goes through a paid third-party build service; you can also download a release and set up your own model
- https://github.com/nano-muse/nanoMuse | stars=3559 | pushed=2026-11-13 | os=android,ios | flags=-
  - 开源的个人 Agent，手机、电脑和网页共用一个有名字和形象的助手，替你做事而不只是回答；手机 App、桌面端和中转服务都在仓库里，可以自己部署。
  - An open-source personal agent with one name and look across phone, desktop and web that does things rather than just answering; the phone app, desktop app and relay are all in the repo and can be self-hosted.
  - caveat: The community relay has a free allowance, then you use your own key; the iPhone app is on TestFlight
- https://github.com/DSH-APP/DSHA | stars=3521 | pushed=2026-11-14 | os=android | flags=cn
  - 在手机上跑完整 DeepSeek Harness 的安卓启动器，内置 Ubuntu 环境，免 Root、免 Termux，装完即用。
  - An Android launcher that runs the full DeepSeek Harness on your phone with a built-in Ubuntu environment; no root or Termux, ready after install.
  - caveat: Needs Android 11+ and arm64
- https://github.com/Mangi-11/Eta | stars=2967 | pushed=2026-11-17 | os=android | flags=byok,cn
  - 第三方系统级 AI 助手：设为默认数字助理后长按电源键唤起，跨 App 操作，并能读写日历、闹钟、便签等系统功能，对 ColorOS 和 HyperOS 做了深度适配。
  - A third-party system-level assistant: set it as the default digital assistant and long-press power to call it; it works across apps and handles calendar, alarms and notes, with deep integration for ColorOS and HyperOS.
  - caveat: Android 13+ on ARM64; core features need no root, while root and LSPosed unlock deeper access
- https://github.com/omnimind-ai/OmniBot | stars=2148 | pushed=2026-11-18 | os=android | flags=cn
  - 端侧 AI 助手：把聊天、Agent 工具、本地工作区和系统集成放进一个应用，无需 root 即可按授权管理日程、联系人、提醒和文件。
  - An on-device AI assistant that puts chat, agent tools, a local workspace and system integration in one app; with your permission and no root it manages calendar, contacts, reminders and files.
  - caveat: The iOS and macOS version is a separate project, ViaVera
- https://github.com/JMAN730/opendroid | stars=1295 | pushed=2026-11-10 | os=android | flags=local
  - 能自己拆解计划、逐步执行并核对结果的安卓 Agent，用截图交给视觉模型理解屏幕，支持导入本地模型。
  - An Android agent that plans multi-step tasks, executes and verifies each step, reads the screen through screenshots for vision models and supports importing local models.
- https://github.com/wangzhishou/OneBox | stars=1194 | pushed=2026-11-17 | os=android | flags=cn
  - 万宝盒：免费的安卓 AI 智能体和工具箱，说一句话就由内置 Agent 调用 90 多个应用内工具，处理图片、PDF、记账和文件。
  - OneBox, a free Android agent and toolbox: one sentence and the built-in agent drives 90+ in-app tools for images, PDFs, bookkeeping and files.
  - caveat: The agent stays inside OneBox's own sandbox; it doesn't read contacts or SMS or operate other apps
- https://github.com/ModalityDance/PalmClaw | stars=1182 | pushed=2026-10-21 | os=android | flags=byok,cn
  - 直接跑在安卓手机上的 Agent 框架：会话、记忆、Skill 和工具都在手机上，执行操作前检查权限并请你确认，支持定时任务和 MCP。
  - An agent framework that runs natively on Android: sessions, memory, skills and tools live on the phone, device actions are checked against permissions and your confirmation, with scheduled tasks and MCP.
- https://github.com/agents-io/PokeClaw | stars=1162 | pushed=2026-06-02 | os=android | flags=local
  - 在手机上用 Gemma 4 本地模型操作手机的开源 App，本地模式不需要账号和 API Key；难的任务可以切换到云端模型。
  - An open-source app that operates the phone with Gemma 4 running on the device; local mode needs no account or API key, and harder tasks can switch to a cloud model.
  - caveat: Android 9+; on CPU-only phones the model takes about 45 seconds to warm up
- https://github.com/HKUDS/PhoneGo | stars=1012 | pushed=2026-11-17 | os=android | flags=-
  - 港大 HKUDS 团队的手机 Agent：把常用页面的操作预先编成地图，执行时直接调用命令、不用每步都问模型，又快又稳；只有没见过的页面才交给视觉模型。
  - A phone agent from the HKUDS team that compiles common screens into a map ahead of time, so most steps are fast, repeatable commands; only unseen screens go to the vision model.
- https://github.com/jackwener/DSH-Android | stars=997 | pushed=2026-11-06 | os=android | flags=byok,cn
  - 不要 root、不用电脑，一个 APK 在安卓手机上跑 DeepSeek Harness：用微信发消息、总结群聊、整理文件、改系统设置；配好 Shizuku 或 ADB 后可在虚拟屏上操作，不占你的屏幕。
  - One APK runs DeepSeek Harness on Android with no root or computer: send messages, sum up group chats, tidy files and change settings; with Shizuku or ADB it works on a virtual display and leaves your screen alone.
  - caveat: Sign in to DeepSeek or add an API key, or use another provider; arm64, Android 10+
- https://github.com/iamr0s/Ruto-GLM | stars=735 | pushed=2026-01-11 | os=android | flags=cn
  - 基于 Open-AutoGLM 的手机端自动化框架：借助 Shizuku 在虚拟屏幕上后台执行任务，主屏照常使用，还能多开应用。
  - A phone-side automation framework built on Open-AutoGLM: with Shizuku it runs tasks on a virtual display in the background, leaving your main screen free, and can run app instances side by side.
  - caveat: Needs Shizuku
- https://github.com/WSK-build/DSHBox | stars=710 | pushed=2026-11-16 | os=android | flags=cn
  - DeepSeek Harness 的移动端：在手机或平板本地运行，也能远程连接，自带终端、文件管理器、浏览器自动化和手机操控，免 Root、免 Termux。
  - A mobile app for DeepSeek Harness that runs it locally on a phone or tablet or connects remotely, with a terminal, file manager, browser automation and phone control; no root or Termux.
- https://github.com/newo-ether/Agora | stars=620 | pushed=2026-11-17 | os=android | flags=byok
  - 自带 API Key 的安卓大模型客户端，支持多服务商、Agent 工作流和远程设备控制。
  - A bring-your-own-key LLM client for Android with multiple providers, agent workflows and remote device control.
  - caveat: The author warns a third party repackaged it under another name; download from the official repo
- https://github.com/niki914/zafiro | stars=377 | pushed=2026-11-17 | os=android | flags=byok
  - 看懂屏幕、跨 App 操作的安卓 Agent，支持 Skill、MCP、记忆和 Termux，带安全防护和会话管理。
  - An Android agent that understands the screen and works across apps, with skills, MCP, memory, Termux, a safety guard and session management.
  - caveat: Uses Accessibility for native apps and Shizuku for others, no root needed

## iPhone 上的 AI 智能体 / Agent apps for iPhone

- https://github.com/Turbo1123/roubao | stars=2419 | pushed=2026-11-09 | os=ios | flags=pc,cn
  - 肉包 2.0：让 AI 直接操作 iPhone，看屏幕、点按、输入、跨应用完成任务；配置好之后在 iPhone 上独立运行，不需要越狱和额外硬件。
  - Roubao 2.0 lets AI operate your iPhone directly: read the screen, tap, type and finish tasks across apps; once set up it runs on the iPhone alone, with no jailbreak or extra hardware.
  - caveat: First setup needs a Mac and cable to build and sign, and the signing needs upkeep; developer preview
- https://github.com/kellyvv/PhoneClaw | stars=1292 | pushed=2026-08-06 | os=ios | flags=local
  - 把手机变成本地 AI Agent：在 iPhone 上跑 Gemma 4 和 MiniCPM-V，调用日历、提醒事项、通讯录、剪贴板等原生能力干活。
  - Turns your phone into a local agent runtime: runs Gemma 4 and MiniCPM-V on the iPhone and gets work done through Calendar, Reminders, Contacts, Clipboard and other native skills.
  - caveat: Available on TestFlight; needs iOS 17+
- https://github.com/rounak/PhoneAgent | stars=808 | pushed=2026-08-15 | os=ios,android | flags=byok
  - 实验性项目：iPhone 上的应用内 Agent，可跨 iPhone App 办事；也提供桥接，让 Codex 等电脑上的 Agent 控制 iPhone 或安卓手机。
  - An experiment with an in-app iPhone agent that works across iPhone apps, plus a bridge that lets Codex and other computer agents control an iPhone or Android phone.
  - caveat: The in-app agent uses the OpenAI API with your own key

## 用电脑上的 Claude Code、Codex 操作手机 / Let Claude Code or Codex drive your phone

- https://github.com/mobile-next/mobile-mcp | stars=10664 | pushed=2026-11-17 | os=android,ios | flags=pc,cn
  - 手机 MCP 服务器：让 AI 助手操作 iOS、安卓的真机、模拟器和仿真器，用无障碍结构或截图坐标点击。
  - A phone MCP server that lets AI agents drive real iOS and Android devices, simulators and emulators through accessibility snapshots or screenshot taps.
- https://github.com/zhongerxin/iPhone-use | stars=5028 | pushed=2026-10-22 | os=ios | flags=pc,cn
  - 让 Codex、WorkBuddy 等通过 USB 操作真实 iPhone：打开 App、读取页面、点击滚动输入，并在侧边栏显示手机实时画面。
  - Lets Codex, WorkBuddy and others operate a real iPhone over USB: open apps, read pages, tap, scroll and type, with a live screen in the sidebar.
  - caveat: Needs a Mac and WebDriverAgent signed onto the phone; sends anonymous usage stats by default, set IPHONE_USE_ANALYTICS=0 to turn off
- https://github.com/DIYgod/pinky | stars=2378 | pushed=2026-11-18 | os=android,ios | flags=pc,cn
  - 让 Claude Code、Codex、Cursor 等任何 MCP Agent 操作真实的 iPhone 或安卓手机：你在电脑上看着它干活，有风险的步骤由你批准，随时可以接管，事后能回放。
  - Lets Claude Code, Codex, Cursor or any MCP agent use a real iPhone or Android phone: you watch on your computer, approve risky steps, take over any time and replay afterwards.
  - caveat: Desktop app for macOS, Windows and Linux; asks before payments by default
- https://github.com/danielealbano/android-remote-control-mcp | stars=846 | pushed=2026-11-13 | os=android | flags=-
  - 装在安卓手机上的 MCP 服务器：Claude 等 AI 远程连上后即可读界面、点按、输入和滑动；可选隐私模式，先把邮箱、卡号等个人信息遮掉再发给模型。
  - An Android app that runs an MCP server on the phone, so Claude and other models can connect remotely to read the UI, tap, type and swipe; an optional privacy mode hides emails, card numbers and other personal data before it reaches the model.
- https://github.com/witchan/ios-mcp | stars=695 | pushed=2026-09-27 | os=ios | flags=root,cn
  - 运行在越狱 iPhone 上的 MCP 服务器：触控手势、硬件按键、文字输入、截图、App 管理和无障碍元素操作。
  - An MCP server for jailbroken iPhones: touch gestures, hardware buttons, text input, screenshots, app management and accessibility elements.
- https://github.com/lxe/phoneuse | stars=684 | pushed=2026-11-15 | os=ios | flags=pc
  - 在电脑上看到并操作未改装的 iPhone：AirPlay 镜像画面进来，蓝牙键鼠发出去，Claude Code、Codex 在你允许后可以点按和输入，不用越狱和数据线。
  - See and operate an unmodified iPhone from your computer: AirPlay mirroring in, Bluetooth mouse and keyboard out, so Claude Code and Codex can tap and type with your permission; no jailbreak or cable.
  - caveat: Alpha; builds for Linux and macOS 15+, Windows from source
- https://github.com/OpenMinis/iCTRL | stars=621 | pushed=2026-11-12 | os=ios | flags=pc
  - 基于 XCUITest 的 iOS 自动化服务，给 AI 用的接口更友好，可让 Agent 操作 iPhone 和 iPad。
  - An AI-friendly iOS automation service built on XCUITest that lets agents operate an iPhone or iPad.
  - caveat: The author says it is for testing and research only; the pairing key means full control of the phone

## 手机 Agent 框架：电脑通过 ADB 控制手机 / Phone agent frameworks: a computer drives the phone over ADB

- https://github.com/zai-org/Open-AutoGLM | stars=26620 | pushed=2026-03-06 | os=android | flags=pc,cn
  - 智谱开源的手机 Agent 模型和框架：说一句“打开小红书搜美食”，它看屏幕、规划并自动完成；内置敏感操作确认，登录和验证码可以人工接管，也支持 WiFi 远程调试。
  - Zhipu's open phone agent model and framework: say "search for food on Xiaohongshu" and it reads the screen, plans and finishes the job, with confirmation for sensitive steps, hand-over for logins and CAPTCHAs, and remote ADB over Wi-Fi.
  - caveat: Host the model yourself or use a third-party model service
- https://github.com/google/artemis | stars=17646 | pushed=2026-10-01 | os=android | flags=pc
  - Google 开源：把自然语言指令变成可靠的安卓自动化，能跨 App 完成测试流程和日常任务，可通过 MCP 交给 Claude Code 等使用。
  - From Google: turns natural-language instructions into reliable Android automation across apps, for test flows and everyday tasks, and exposes MCP for Claude Code and other agents.
- https://github.com/droidrun/mobilerun | stars=10061 | pushed=2026-11-17 | os=android,ios | flags=pc,local
  - 用自然语言自动操作安卓和 iOS 设备的开源框架，也用于 App 测试，支持 OpenAI、Anthropic、Gemini、DeepSeek、Ollama 等模型。
  - An open-source framework for operating Android and iOS devices with natural language, also used for app testing, with OpenAI, Anthropic, Gemini, DeepSeek, Ollama and other models.
  - caveat: A paid cloud service exists but isn't needed to run locally
- https://github.com/X-PLUG/MobileAgent | stars=9386 | pushed=2026-11-03 | os=android | flags=pc,cn
  - 阿里通义实验室的 Mobile-Agent 系列：手机 GUI Agent 框架和 GUI-Owl 模型，可在线体验，也可本地部署。
  - The Mobile-Agent family from Alibaba's Tongyi Lab: a phone GUI agent framework and the GUI-Owl models, with online demos or local deployment.
- https://github.com/TencentQQGYLab/AppAgent | stars=6922 | pushed=2025-03-19 | os=android | flags=pc
  - 腾讯的多模态手机 Agent：先自己探索或看人演示来学会一个新 App，再像人一样点按和滑动。
  - Tencent's multimodal phone agent that learns a new app by exploring on its own or watching a human demo, then taps and swipes like a person.
- https://github.com/minitap-ai/mobile-use | stars=3403 | pushed=2026-11-15 | os=android,ios | flags=pc,byok
  - 用自然语言控制安卓或 iOS 设备的开源 Agent，从发消息到在复杂 App 里导航都能做，可选 OpenAI、Google、xAI、OpenRouter 等模型。
  - An open-source agent that controls Android or iOS devices in plain language, from sending messages to navigating complex apps, with OpenAI, Google, xAI, OpenRouter and other models.
- https://github.com/IPADS-SAI/MobiAgent | stars=1936 | pushed=2026-07-17 | os=android | flags=cn
  - IPADS 团队的可定制手机 Agent 系统：MobiMind 模型、AgentRR 加速框架和 MobiFlow 评测，附安卓 App。
  - A customizable mobile agent system from the IPADS team with the MobiMind models, the AgentRR acceleration framework, the MobiFlow benchmark and an Android app.
- https://github.com/ComputerUseAgent/AutoCua | stars=1296 | pushed=2026-11-17 | os=android,ios | flags=pc
  - 一组 AI Agent，替你操作 Mac、Windows、Linux、手机和浏览器。
  - A team of AI agents that works your Mac, Windows, Linux, phone and browser.
- https://github.com/suyiiyii/AutoGLM-GUI | stars=1134 | pushed=2026-11-17 | os=android | flags=pc,cn
  - AutoGLM 的图形界面：网页上连接手机、下达任务，支持定时执行、Docker 部署、对话历史和多设备管理。
  - A graphical interface for AutoGLM: connect phones and give tasks in the browser, with scheduled runs, Docker deployment, history and multiple devices.

## 在手机上指挥电脑里的 Claude Code、Codex / Steer Claude Code and Codex from your phone

- https://github.com/pingdotgg/t3code | stars=64166 | pushed=2026-11-18 | os=android,ios | flags=-
  - 编程 Agent 的开源控制台：Agent 在你的电脑上跑，用你自己的订阅，在桌前开个线程，出门后在手机上批准下一步；支持 Claude Code、Codex、Cursor 等。
  - An open-source control plane for coding agents: they run on your machine with your own subscriptions, so you start a thread at your desk and approve the next step from your phone; works with Claude Code, Codex, Cursor and more.
- https://github.com/getpaseo/paseo | stars=24274 | pushed=2026-11-18 | os=android,ios | flags=-
  - Claude Code、Codex、Copilot、OpenCode 的统一界面：Agent 在你的机器上并行运行，手机、桌面、网页都能推进，支持语音下任务，没有遥测。
  - One interface for Claude Code, Codex, Copilot and OpenCode: agents run in parallel on your machine, you move work forward from phone, desktop or web, with voice mode and no telemetry.
- https://github.com/siteboon/claudecodeui | stars=14668 | pushed=2026-11-16 | os=web | flags=-
  - Claude Code、Cursor CLI 和 Codex 的桌面和手机网页界面，可本地或远程使用，用 npx 一条命令自己部署。
  - A desktop and mobile web UI for Claude Code, Cursor CLI and Codex, usable locally or remotely and self-hosted with one npx command.
- https://github.com/Louis-CFM/coucou | stars=7307 | pushed=2026-11-13 | os=ios,android | flags=-
  - 住在 Mac 刘海里的小伙伴，帮你盯着编程 Agent 的会话；离开电脑后跟到 iPhone 或安卓手机上，锁屏、灵动岛和小组件都能批准权限。
  - A tiny friend in your Mac's notch that watches your coding agent sessions and follows you to iPhone or Android, with approvals on the Lock Screen, Dynamic Island and widgets.
- https://github.com/Nexting-ai/nexting | stars=2352 | pushed=2026-11-17 | os=ios | flags=-
  - 远程遥控你自己的 AI Agent：从手机连接 Mac 或 Windows 上的 Claude Code、Codex、Grok 和 Cursor，查看会话、发送任务。
  - Remote control for your own agents: connect from your phone to Claude Code, Codex, Grok and Cursor on a Mac or Windows PC to view sessions and send tasks.
- https://github.com/happier-dev/happier | stars=2230 | pushed=2026-11-18 | os=android,ios | flags=cn
  - 多设备控制中心：在手机、桌面和浏览器上编排 Claude Code、Codex 等编程代理，开源、可自托管、端到端加密。
  - A multi-device control center for orchestrating Claude Code, Codex and other coding agents from phone, desktop and browser; open source, self-hostable and end-to-end encrypted.
- https://github.com/AltanS/collie | stars=1669 | pushed=2026-11-17 | os=web | flags=-
  - 开源的手机网页应用：显示终端里的 Claude Code、Codex、OpenCode，并让你远程回复，部署在你自己的电脑上，配合 Herdr 使用。
  - An open-source phone web app that shows your terminal agents, including Claude Code, Codex and OpenCode, and lets you answer them remotely; you host it on your own computer alongside Herdr.
- https://github.com/K9i-0/ccpocket | stars=1105 | pushed=2026-11-18 | os=android,ios | flags=cn
  - 把编程代理装进口袋：用聊天的方式在手机上操作 Codex 和 Claude，发指令、批准下一步、看结果，换到平板或 Mac 也能接着做。
  - Coding agents in your pocket: chat with Codex and Claude from your phone to send instructions, approve steps and see results, then continue on a tablet or Mac.
- https://github.com/techjarves/Mobile-Harness | stars=952 | pushed=2026-11-14 | os=android | flags=-
  - 安卓上的 AI 开发工作台：在手机上和编程 Agent 对话、改项目、跑真正的 Linux 命令并预览网页。
  - An AI development workspace on Android: chat with coding agents, edit projects, run real Linux commands and preview web servers on the phone.
- https://github.com/gronxb/codex-relay | stars=746 | pushed=2026-11-17 | os=ios | flags=-
  - Codex CLI 的手机搭档：在工作区跑本地中转，通过你自己的网络配对，在手机上跟进或引导 Codex 会话，代码和状态都留在电脑上。
  - A phone companion for the Codex CLI: a local relay in your workspace pairs over your own network so you can follow or steer Codex sessions from the phone while code and state stay on your computer.

## 给开发者：用 AI 测试自己的 App / For developers: test your own app with AI

- https://github.com/budtmo/docker-android | stars=16154 | pushed=2026-11-18 | os=android | flags=-
  - 把安卓模拟器装进 Docker，浏览器里就能看，带录屏和 MCP 服务器，适合给 Agent 准备测试手机。
  - Android emulators in Docker with noVNC, video recording and an MCP server, handy for giving agents a test phone.
- https://github.com/web-infra-dev/midscene | stars=15632 | pushed=2026-11-17 | os=android,ios,harmony | flags=cn
  - Midscene：AI 视觉测试框架，用自然语言写 E2E 测试，支持网页、安卓、iOS 和鸿蒙。
  - Midscene, an AI-vision E2E testing framework: write tests in natural language for web, Android, iOS and HarmonyOS.
- https://github.com/callstack/agent-device | stars=5431 | pushed=2026-11-18 | os=android,ios,harmony | flags=-
  - 给编程 Agent 用的设备层：通过命令行、MCP 或 Node.js API 控制 iOS、安卓、鸿蒙的模拟器和真机，让 Agent 在运行中的 App 里验证自己的改动。
  - A device layer for coding agents: a CLI, MCP server and Node.js API to control iOS, Android and HarmonyOS simulators and devices, so agents can verify their changes in the running app.
- https://github.com/software-mansion/argent | stars=3206 | pushed=2026-11-17 | os=android,ios | flags=cn
  - 让 AI 助手操控 iOS 模拟器、安卓模拟器和真机，点按、分析性能、复现问题。
  - Lets AI agents control iOS simulators, Android emulators and devices to tap, profile performance and reproduce bugs.
- https://github.com/joshuayoes/ios-simulator-mcp | stars=2231 | pushed=2026-11-10 | os=ios | flags=-
  - 操作 iOS 模拟器的 MCP 服务器：获取信息、控制界面交互、检查元素。
  - An MCP server for iOS simulators: get info, drive UI interactions and inspect elements.
- https://github.com/lycorp-jp/sim-use | stars=1551 | pushed=2026-11-14 | os=android,ios | flags=-
  - LINE 雅虎开源：把屏幕变成省 token 的文字大纲，让 AI 按别名点按 iOS 模拟器和安卓设备上的元素。
  - From LY Corporation: turns the screen into a token-efficient outline so agents can tap elements by alias on iOS Simulator and Android.
- https://github.com/takahirom/arbigent | stars=658 | pushed=2026-10-02 | os=android,ios,web | flags=-
  - AI Agent 测试框架，有图形界面也有代码接口，把复杂场景拆成小步骤，支持安卓、iOS 和网页。
  - An AI agent testing framework with both a UI and a code interface that breaks complex scenarios into steps, for Android, iOS and web.

## 模型与评测（开发者） / Models and benchmarks (for developers)

- https://github.com/Tongyi-MAI/MAI-UI | stars=2430 | pushed=2026-08-19 | os=- | flags=cn
  - 通义的 GUI Agent 基座模型，统一手机、电脑、浏览器场景，用 100 多台真机、150 多个 App 训练和评测。
  - Tongyi's foundation GUI agent model covering phone, computer and browser, trained and evaluated on 100+ real phones and 150+ apps.
- https://github.com/OpenBMB/AgentCPM-GUI | stars=1430 | pushed=2026-01-11 | os=- | flags=cn
  - 清华 THUNLP 等开源的端侧 GUI Agent 模型，能操作中文和英文 App。
  - An open on-device GUI agent model from THUNLP and partners that operates Chinese and English apps.
- https://github.com/zai-org/CogAgent | stars=1202 | pushed=2026-10-12 | os=- | flags=cn
  - 智谱开源的端到端视觉语言 GUI Agent 模型。
  - Zhipu's open end-to-end vision-language GUI agent model.
- https://github.com/inclusionAI/UI-Venus | stars=1082 | pushed=2026-10-28 | os=- | flags=-
  - inclusionAI 的通用 GUI Agent 模型，覆盖手机 App、网页和桌面系统。
  - A general GUI agent model from inclusionAI for mobile apps, the web and desktop operating systems.
- https://github.com/google-research/android_world | stars=1015 | pushed=2026-11-10 | os=- | flags=-
  - Google 的安卓 Agent 评测环境和基准。
  - Google's environment and benchmark for autonomous Android agents.

## 基础工具 / Building blocks

- https://github.com/Genymobile/scrcpy | stars=155090 | pushed=2026-11-17 | os=android | flags=pc
  - 在电脑上显示并控制安卓手机，很多手机 Agent 都靠它看屏幕和操作。
  - Display and control your Android device from a computer; many phone agents rely on it to see and act.
- https://github.com/sky22333/skyadb | stars=776 | pushed=2026-11-17 | os=android | flags=cn
  - 装在安卓手机上的 ADB 助手，用无线调试或 OTG 管理其他手机、平板、电视和盒子，可接 OpenAI 兼容模型让 AI 操作设备。
  - An ADB helper that runs on an Android phone and manages other phones, tablets, TVs and boxes over wireless debugging or OTG, with an OpenAI-compatible model to let AI operate them.
