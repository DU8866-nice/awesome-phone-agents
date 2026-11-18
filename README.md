<!-- 本文件由 scripts/build_readme.py 生成，请勿直接修改。要改内容请编辑 data/tools.yaml 后重新生成。 -->

# Awesome Phone Agents · 手机 AI 智能体大全

[![Stars](https://img.shields.io/github/stars/DU8866-nice/awesome-phone-agents?style=flat-square)](https://github.com/DU8866-nice/awesome-phone-agents) [![Last commit](https://img.shields.io/github/last-commit/DU8866-nice/awesome-phone-agents?style=flat-square)](https://github.com/DU8866-nice/awesome-phone-agents/commits) [![License: CC0-1.0](https://img.shields.io/badge/license-CC0--1.0-lightgrey?style=flat-square)](LICENSE) [![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](CONTRIBUTING.md)

**简体中文** | [English](README.en.md)

> 让 AI 替你操作手机的开源工具精选：手机上直接装的 AI 智能体、用 Claude Code 和 Codex 遥控手机、ADB 手机 Agent 框架，以及在手机上指挥电脑里的编程助手。每个工具标明支持 Android 还是 iPhone、要不要电脑、要不要 root、能不能用本地模型，星标每周自动刷新。

“AI 手机”正在从厂商发布会走到每个人手里：说一句“帮我把群聊总结一下”“比个价，加到购物车”，AI 就会自己打开 App、看屏幕、点按、输入，把事情办完。过去几个月，开源社区冒出了一大批这样的工具：有直接装在安卓手机上的 App，有让电脑上的 Claude Code、Codex 接管手机的 MCP 服务器，也有智谱 Open-AutoGLM、阿里 Mobile-Agent 这样的开源框架和模型。

这份清单面向想动手用的人，而不是论文清单：按你的设备和用法整理这些工具，标明支持安卓还是 iPhone、要不要电脑、要不要 root、能不能用本地模型。

收录 61 个项目 · 数据更新于 2026-11-18

## 目录

- [按你的情况挑](#pick)
- [用之前先知道](#rules)
- [装在安卓手机上的 AI 智能体](#cat-android)（18）
- [iPhone 上的 AI 智能体](#cat-iphone)（3）
- [用电脑上的 Claude Code、Codex 操作手机](#cat-remote)（7）
- [手机 Agent 框架：电脑通过 ADB 控制手机](#cat-frameworks)（9）
- [在手机上指挥电脑里的 Claude Code、Codex](#cat-coding)（10）
- [给开发者：用 AI 测试自己的 App](#cat-testing)（7）
- [模型与评测（开发者）](#cat-models)（5）
- [基础工具](#cat-basics)（2）
- [常见问题](#faq)
- [让 AI 助手帮你挑](#finder)
- [相关合集](#related)
- [参与贡献](#contributing)

<a id="pick"></a>
## 按你的情况挑

| 你的情况 | 推荐先试 |
|---|---|
| 安卓手机，不想碰电脑 | [Mika](https://github.com/wangzan101/Mika)、[Operit](https://github.com/AAswordman/Operit)、[DSH-Android](https://github.com/jackwener/DSH-Android)、[PokeClaw](https://github.com/agents-io/PokeClaw)（本地模型） |
| 安卓手机，想让 AI 在后台干活、不占屏幕 | [Mika](https://github.com/wangzan101/Mika)、[DSH-Android](https://github.com/jackwener/DSH-Android)、[Ruto](https://github.com/iamr0s/Ruto-GLM)（虚拟屏） |
| iPhone | [Pinky](https://github.com/DIYgod/pinky)（配合电脑）、[肉包](https://github.com/Turbo1123/roubao)（需 Mac 签名一次）、[PhoneClaw](https://github.com/kellyvv/PhoneClaw)（本地模型） |
| 已经在用 Claude Code 或 Codex | [Pinky](https://github.com/DIYgod/pinky)、[mobile-mcp](https://github.com/mobile-next/mobile-mcp)、[iPhone Use](https://github.com/zhongerxin/iPhone-use) |
| 想定时、批量跑重复任务 | [Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM)、[AutoGLM-GUI](https://github.com/suyiiyii/AutoGLM-GUI)、[Mobilerun](https://github.com/droidrun/mobilerun) |
| 出门也想盯着电脑上的编程助手 | [T3 Code](https://github.com/pingdotgg/t3code)、[Paseo](https://github.com/getpaseo/paseo)、[CC Pocket](https://github.com/K9i-0/ccpocket) |
| 开发者，想让 AI 测试自己的 App | [Midscene](https://github.com/web-infra-dev/midscene)、[agent-device](https://github.com/callstack/agent-device)、[Argent](https://github.com/software-mansion/argent) |

<a id="rules"></a>
## 用之前先知道

> [!IMPORTANT]
> - **屏幕内容会发给模型。** 这类工具靠截图或界面结构“看”手机，聊天记录、验证码、余额都可能出现在画面里。用云端模型时，这些内容会发给模型服务商；标 🔒 的工具可以用本地模型，内容不出设备。
> - **付款、转账和删除要自己确认。** 优先选默认在付款、发消息前询问你的工具，并保持这些确认开着。别让 AI 无人看管地碰钱包、银行和不能撤销的操作。
> - **权限给多少，它就能做多少。** 无障碍服务、Shizuku、ADB 和 root 都意味着手机的大部分控制权。只从官方仓库下载，只授权你信任的工具，用完关掉远程访问。
> - **注意平台规则。** 很多 App 的条款禁止自动化操作，频繁自动点按可能触发风控、导致账号受限。用在自己的日常事务上，别拿来刷量。
> - **iPhone 的限制。** iOS 不允许普通 App 操作其他 App，所以 iPhone 方案大多需要电脑配合，或者用 Mac 签名安装，签名到期要维护。

本清单不收录群控、养号、刷量和多账号营销工具，不收录绕过风控或反检测的“隐身”云手机，也不收录抢红包、游戏外挂类工具。

**图例**：💻 需要电脑（USB、ADB 或同一网络）· 🔒 可用本地模型，屏幕内容不上传 · 🔑 需要自备模型 API Key 或账号 · 🔓 需要 root 或越狱 · 🀄 中文友好 · 🆕 近 60 天新建 · 💤 超过一年未更新 · 📦 已归档

> [!NOTE]
> 标记和支持的系统依据各项目 README 的说明，只在 README 写明时才标，没标不代表不支持。收录指核对过仓库说明，不等于逐个在真机上实测过。

<a id="cat-android"></a>
## 装在安卓手机上的 AI 智能体

装一个 APK 就能用，不需要电脑。多数通过无障碍服务读屏和点按，有的支持 Shizuku 或虚拟屏，让 AI 在后台操作、不占用你的屏幕。

- **[dsh-Go](https://github.com/ccch1mneyyy/dsh-Go)** · ★ 26.1k · 🀄 🆕<br>DeepSeek Harness 的手机应用：内置 Linux 环境，在手机本机运行，也能一键切到电脑上的 DSH 接着用；可以看屏幕替你点，三档确认，敏感操作默认交还给你。<br><sub>Android · 更新于 2026-11 · AGPL-3.0</sub><br><sub>💡 iOS 版仍在开发中，暂无公开安装包</sub>
- **[Operit](https://github.com/AAswordman/Operit)** · ★ 9.7k · 🔒 🀄<br>开源的安卓 AI Agent 平台：操作手机界面、内置浏览器和 Ubuntu 终端、长期记忆、MCP 和 Skill 扩展，可接云端模型，也能用 MNN 或 llama.cpp 跑本地模型。<br><sub>Android · 更新于 2026-11 · LGPL-3.0</sub><br><sub>💡 通过无障碍、Shizuku 或 Root 操作界面，权限越高能做的越多</sub>
- **[Mika](https://github.com/wangzan101/Mika)** · ★ 9.0k · 🔑 🆕<br>说一句话，它在后台的隐藏屏幕上替你操作 App 和网页直到办完，你可以照常用手机；比如总结群聊、比价加购物车（停在结账前）。<br><sub>Android · 更新于 2026-11 · Apache-2.0</sub><br><sub>💡 没有 Mika 服务器，用自己的模型 Key 或登录 ChatGPT、xAI、OpenRouter 账号；操作 App 需要 Android 12 及以上</sub>
- **[andee](https://github.com/kuafuai/andee)** · ★ 6.2k · 🀄<br>住在手机或 Mac 上、像人一样用任何 App 的 AI：不用接口、不用 root、不用插电脑，支持任意模型，带长期记忆。<br><sub>Android / macOS · 更新于 2026-11</sub><br><sub>💡 README 推荐的一键安装走第三方付费打包服务；也可以直接下载 Release，自己配置模型</sub>
- **[nanoMuse](https://github.com/nano-muse/nanoMuse)** · ★ 3.6k · 🆕<br>开源的个人 Agent，手机、电脑和网页共用一个有名字和形象的助手，替你做事而不只是回答；手机 App、桌面端和中转服务都在仓库里，可以自己部署。<br><sub>Android / iPhone · 更新于 2026-11 · GPL-3.0</sub><br><sub>💡 社区中转服务有免费额度，用完后换自己的 Key；iPhone 版通过 TestFlight 安装</sub>
- **[DSHA](https://github.com/DSH-APP/DSHA)** · ★ 3.5k · 🀄<br>在手机上跑完整 DeepSeek Harness 的安卓启动器，内置 Ubuntu 环境，免 Root、免 Termux，装完即用。<br><sub>Android · 更新于 2026-11 · MIT</sub><br><sub>💡 需要 Android 11 及以上、arm64</sub>
- **[Eta](https://github.com/Mangi-11/Eta)** · ★ 3.0k · 🔑 🀄<br>第三方系统级 AI 助手：设为默认数字助理后长按电源键唤起，跨 App 操作，并能读写日历、闹钟、便签等系统功能，对 ColorOS 和 HyperOS 做了深度适配。<br><sub>Android · 更新于 2026-11 · GPL-3.0</sub><br><sub>💡 Android 13 及以上 ARM64，基础功能无需 Root；Root 和 LSPosed 可开放更深的能力</sub>
- **[OmniBot](https://github.com/omnimind-ai/OmniBot)** · ★ 2.1k · 🀄<br>端侧 AI 助手：把聊天、Agent 工具、本地工作区和系统集成放进一个应用，无需 root 即可按授权管理日程、联系人、提醒和文件。<br><sub>Android · 更新于 2026-11</sub><br><sub>💡 iOS 和 macOS 版是另一个项目 ViaVera</sub>
- **[opendroid](https://github.com/JMAN730/opendroid)** · ★ 1.3k · 🔒<br>能自己拆解计划、逐步执行并核对结果的安卓 Agent，用截图交给视觉模型理解屏幕，支持导入本地模型。<br><sub>Android · 更新于 2026-11</sub>
- **[OneBox](https://github.com/wangzhishou/OneBox)** · ★ 1.2k · 🀄<br>万宝盒：免费的安卓 AI 智能体和工具箱，说一句话就由内置 Agent 调用 90 多个应用内工具，处理图片、PDF、记账和文件。<br><sub>Android · 更新于 2026-11 · Apache-2.0</sub><br><sub>💡 Agent 只在万宝盒自身的沙箱里操作，不读通讯录、短信，也不操作其他 App</sub>
- **[PalmClaw](https://github.com/ModalityDance/PalmClaw)** · ★ 1.2k · 🔑 🀄<br>直接跑在安卓手机上的 Agent 框架：会话、记忆、Skill 和工具都在手机上，执行操作前检查权限并请你确认，支持定时任务和 MCP。<br><sub>Android · 更新于 2026-10 · AGPL-3.0</sub>
- **[PokeClaw](https://github.com/agents-io/PokeClaw)** · ★ 1.2k · 🔒<br>在手机上用 Gemma 4 本地模型操作手机的开源 App，本地模式不需要账号和 API Key；难的任务可以切换到云端模型。<br><sub>Android · 更新于 2026-06 · Apache-2.0</sub><br><sub>💡 Android 9 及以上；只有 CPU 的手机首次加载模型约需 45 秒</sub>
- **[PhoneGo](https://github.com/HKUDS/PhoneGo)** · ★ 1.0k<br>港大 HKUDS 团队的手机 Agent：把常用页面的操作预先编成地图，执行时直接调用命令、不用每步都问模型，又快又稳；只有没见过的页面才交给视觉模型。<br><sub>Android · 更新于 2026-11 · MIT</sub>
- **[DSH-Android](https://github.com/jackwener/DSH-Android)** · ★ 997 · 🔑 🀄 🆕<br>不要 root、不用电脑，一个 APK 在安卓手机上跑 DeepSeek Harness：用微信发消息、总结群聊、整理文件、改系统设置；配好 Shizuku 或 ADB 后可在虚拟屏上操作，不占你的屏幕。<br><sub>Android · 更新于 2026-11 · Apache-2.0</sub><br><sub>💡 登录 DeepSeek 账号或填 API Key，也可换其他服务商；需要 arm64、Android 10 及以上</sub>
- **[Ruto-GLM](https://github.com/iamr0s/Ruto-GLM)** · ★ 735 · 🀄<br>基于 Open-AutoGLM 的手机端自动化框架：借助 Shizuku 在虚拟屏幕上后台执行任务，主屏照常使用，还能多开应用。<br><sub>Android · 更新于 2026-01</sub><br><sub>💡 需要 Shizuku</sub>
- **[DSHBox](https://github.com/WSK-build/DSHBox)** · ★ 710 · 🀄<br>DeepSeek Harness 的移动端：在手机或平板本地运行，也能远程连接，自带终端、文件管理器、浏览器自动化和手机操控，免 Root、免 Termux。<br><sub>Android · 更新于 2026-11 · GPL-3.0</sub>
- **[Agora](https://github.com/newo-ether/Agora)** · ★ 620 · 🔑<br>自带 API Key 的安卓大模型客户端，支持多服务商、Agent 工作流和远程设备控制。<br><sub>Android · 更新于 2026-11 · GPL-3.0</sub><br><sub>💡 作者提醒：有第三方用它的代码改名打包分发，请从官方仓库下载</sub>
- **[zafiro](https://github.com/niki914/zafiro)** · ★ 377 · 🔑<br>看懂屏幕、跨 App 操作的安卓 Agent，支持 Skill、MCP、记忆和 Termux，带安全防护和会话管理。<br><sub>Android · 更新于 2026-11 · MIT</sub><br><sub>💡 原生 App 用无障碍服务操作，其他 App 可用 Shizuku，无需 Root</sub>

<a id="cat-iphone"></a>
## iPhone 上的 AI 智能体

iOS 不允许普通 App 操作其他 App，所以 iPhone 上能直接替你点屏幕的方案很少，大多需要先用 Mac 签名安装。想用电脑上的 AI 操作 iPhone，看下一节。

- **[roubao](https://github.com/Turbo1123/roubao)** · ★ 2.4k · 💻 🀄<br>肉包 2.0：让 AI 直接操作 iPhone，看屏幕、点按、输入、跨应用完成任务；配置好之后在 iPhone 上独立运行，不需要越狱和额外硬件。<br><sub>iPhone · 更新于 2026-11 · MIT</sub><br><sub>💡 首次配置需要 Mac 和数据线编译签名，签名到期后要重新维护；目前是开发者预览版</sub>
- **[PhoneClaw](https://github.com/kellyvv/PhoneClaw)** · ★ 1.3k · 🔒<br>把手机变成本地 AI Agent：在 iPhone 上跑 Gemma 4 和 MiniCPM-V，调用日历、提醒事项、通讯录、剪贴板等原生能力干活。<br><sub>iPhone · 更新于 2026-08 · Apache-2.0</sub><br><sub>💡 可通过 TestFlight 安装，需要 iOS 17 及以上</sub>
- **[PhoneAgent](https://github.com/rounak/PhoneAgent)** · ★ 808 · 🔑<br>实验性项目：iPhone 上的应用内 Agent，可跨 iPhone App 办事；也提供桥接，让 Codex 等电脑上的 Agent 控制 iPhone 或安卓手机。<br><sub>iPhone / Android · 更新于 2026-08 · MIT</sub><br><sub>💡 应用内 Agent 使用 OpenAI 接口，需要自己的 Key</sub>

<a id="cat-remote"></a>
## 用电脑上的 Claude Code、Codex 操作手机

手机连上电脑后，通过 MCP 交给你已经在用的 AI 助手操作，适合整理资料、跑重复流程或让 AI 帮你测试自己的 App。

- **[mobile-mcp](https://github.com/mobile-next/mobile-mcp)** · ★ 10.7k · 💻 🀄<br>手机 MCP 服务器：让 AI 助手操作 iOS、安卓的真机、模拟器和仿真器，用无障碍结构或截图坐标点击。<br><sub>Android / iPhone · 更新于 2026-11 · Apache-2.0</sub>
- **[iPhone-use](https://github.com/zhongerxin/iPhone-use)** · ★ 5.0k · 💻 🀄 🆕<br>让 Codex、WorkBuddy 等通过 USB 操作真实 iPhone：打开 App、读取页面、点击滚动输入，并在侧边栏显示手机实时画面。<br><sub>iPhone · 更新于 2026-10 · MIT</sub><br><sub>💡 需要 Mac 并先在手机上签名安装 WebDriverAgent；默认发送匿名使用统计，设 IPHONE_USE_ANALYTICS=0 可关闭</sub>
- **[pinky](https://github.com/DIYgod/pinky)** · ★ 2.4k · 💻 🀄 🆕<br>让 Claude Code、Codex、Cursor 等任何 MCP Agent 操作真实的 iPhone 或安卓手机：你在电脑上看着它干活，有风险的步骤由你批准，随时可以接管，事后能回放。<br><sub>Android / iPhone · 更新于 2026-11 · Apache-2.0</sub><br><sub>💡 电脑端支持 macOS、Windows、Linux；默认在付款前询问你</sub>
- **[android-remote-control-mcp](https://github.com/danielealbano/android-remote-control-mcp)** · ★ 846<br>装在安卓手机上的 MCP 服务器：Claude 等 AI 远程连上后即可读界面、点按、输入和滑动；可选隐私模式，先把邮箱、卡号等个人信息遮掉再发给模型。<br><sub>Android · 更新于 2026-11</sub>
- **[ios-mcp](https://github.com/witchan/ios-mcp)** · ★ 695 · 🔓 🀄<br>运行在越狱 iPhone 上的 MCP 服务器：触控手势、硬件按键、文字输入、截图、App 管理和无障碍元素操作。<br><sub>iPhone · 更新于 2026-09 · MIT</sub>
- **[phoneuse](https://github.com/lxe/phoneuse)** · ★ 684 · 💻 🆕<br>在电脑上看到并操作未改装的 iPhone：AirPlay 镜像画面进来，蓝牙键鼠发出去，Claude Code、Codex 在你允许后可以点按和输入，不用越狱和数据线。<br><sub>iPhone · 更新于 2026-11 · MIT</sub><br><sub>💡 alpha 版；Linux 和 macOS 15 以上有安装包，Windows 需从源码构建</sub>
- **[iCTRL](https://github.com/OpenMinis/iCTRL)** · ★ 621 · 💻<br>基于 XCUITest 的 iOS 自动化服务，给 AI 用的接口更友好，可让 Agent 操作 iPhone 和 iPad。<br><sub>iPhone · 更新于 2026-11 · Apache-2.0</sub><br><sub>💡 作者声明仅用于自动化测试和研究，配对密钥等于整台手机的控制权</sub>

<a id="cat-frameworks"></a>
## 手机 Agent 框架：电脑通过 ADB 控制手机

在电脑上运行，用 ADB 或 WebDriverAgent 连接手机，由视觉模型看屏幕、规划并执行操作。要会一点命令行，可以长时间、定时地跑任务。

- **[Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM)** · ★ 26.6k · 💻 🀄<br>智谱开源的手机 Agent 模型和框架：说一句“打开小红书搜美食”，它看屏幕、规划并自动完成；内置敏感操作确认，登录和验证码可以人工接管，也支持 WiFi 远程调试。<br><sub>Android · 更新于 2026-03 · Apache-2.0</sub><br><sub>💡 模型可以自己部署，也可以用第三方模型服务</sub>
- **[artemis](https://github.com/google/artemis)** · ★ 17.6k · 💻<br>Google 开源：把自然语言指令变成可靠的安卓自动化，能跨 App 完成测试流程和日常任务，可通过 MCP 交给 Claude Code 等使用。<br><sub>Android · 更新于 2026-10 · Apache-2.0</sub>
- **[mobilerun](https://github.com/droidrun/mobilerun)** · ★ 10.1k · 💻 🔒<br>用自然语言自动操作安卓和 iOS 设备的开源框架，也用于 App 测试，支持 OpenAI、Anthropic、Gemini、DeepSeek、Ollama 等模型。<br><sub>Android / iPhone · 更新于 2026-11 · MIT</sub><br><sub>💡 另有付费云服务，本地运行不需要</sub>
- **[MobileAgent](https://github.com/X-PLUG/MobileAgent)** · ★ 9.4k · 💻 🀄<br>阿里通义实验室的 Mobile-Agent 系列：手机 GUI Agent 框架和 GUI-Owl 模型，可在线体验，也可本地部署。<br><sub>Android · 更新于 2026-11 · MIT</sub>
- **[AppAgent](https://github.com/TencentQQGYLab/AppAgent)** · ★ 6.9k · 💻 💤<br>腾讯的多模态手机 Agent：先自己探索或看人演示来学会一个新 App，再像人一样点按和滑动。<br><sub>Android · 更新于 2025-03 · MIT</sub>
- **[mobile-use](https://github.com/minitap-ai/mobile-use)** · ★ 3.4k · 💻 🔑<br>用自然语言控制安卓或 iOS 设备的开源 Agent，从发消息到在复杂 App 里导航都能做，可选 OpenAI、Google、xAI、OpenRouter 等模型。<br><sub>Android / iPhone · 更新于 2026-11 · Apache-2.0</sub>
- **[MobiAgent](https://github.com/IPADS-SAI/MobiAgent)** · ★ 1.9k · 🀄<br>IPADS 团队的可定制手机 Agent 系统：MobiMind 模型、AgentRR 加速框架和 MobiFlow 评测，附安卓 App。<br><sub>Android · 更新于 2026-07 · Apache-2.0</sub>
- **[AutoCua](https://github.com/ComputerUseAgent/AutoCua)** · ★ 1.3k · 💻 🆕<br>一组 AI Agent，替你操作 Mac、Windows、Linux、手机和浏览器。<br><sub>Android / iPhone · 更新于 2026-11 · MIT</sub>
- **[AutoGLM-GUI](https://github.com/suyiiyii/AutoGLM-GUI)** · ★ 1.1k · 💻 🀄<br>AutoGLM 的图形界面：网页上连接手机、下达任务，支持定时执行、Docker 部署、对话历史和多设备管理。<br><sub>Android · 更新于 2026-11 · Apache-2.0</sub>

<a id="cat-coding"></a>
## 在手机上指挥电脑里的 Claude Code、Codex

编程助手在你的电脑上跑，手机负责看进度、批准下一步和发新任务，离开工位也不耽误。

- **[t3code](https://github.com/pingdotgg/t3code)** · ★ 64.2k<br>编程 Agent 的开源控制台：Agent 在你的电脑上跑，用你自己的订阅，在桌前开个线程，出门后在手机上批准下一步；支持 Claude Code、Codex、Cursor 等。<br><sub>Android / iPhone · 更新于 2026-11 · MIT</sub>
- **[paseo](https://github.com/getpaseo/paseo)** · ★ 24.3k<br>Claude Code、Codex、Copilot、OpenCode 的统一界面：Agent 在你的机器上并行运行，手机、桌面、网页都能推进，支持语音下任务，没有遥测。<br><sub>Android / iPhone · 更新于 2026-11</sub>
- **[claudecodeui](https://github.com/siteboon/claudecodeui)** · ★ 14.7k<br>Claude Code、Cursor CLI 和 Codex 的桌面和手机网页界面，可本地或远程使用，用 npx 一条命令自己部署。<br><sub>Web · 更新于 2026-11 · AGPL-3.0</sub>
- **[coucou](https://github.com/Louis-CFM/coucou)** · ★ 7.3k · 🆕<br>住在 Mac 刘海里的小伙伴，帮你盯着编程 Agent 的会话；离开电脑后跟到 iPhone 或安卓手机上，锁屏、灵动岛和小组件都能批准权限。<br><sub>iPhone / Android · 更新于 2026-11 · MIT</sub>
- **[nexting](https://github.com/Nexting-ai/nexting)** · ★ 2.4k<br>远程遥控你自己的 AI Agent：从手机连接 Mac 或 Windows 上的 Claude Code、Codex、Grok 和 Cursor，查看会话、发送任务。<br><sub>iPhone · 更新于 2026-11 · MIT</sub>
- **[happier](https://github.com/happier-dev/happier)** · ★ 2.2k · 🀄<br>多设备控制中心：在手机、桌面和浏览器上编排 Claude Code、Codex 等编程代理，开源、可自托管、端到端加密。<br><sub>Android / iPhone · 更新于 2026-11 · MIT</sub>
- **[collie](https://github.com/AltanS/collie)** · ★ 1.7k<br>开源的手机网页应用：显示终端里的 Claude Code、Codex、OpenCode，并让你远程回复，部署在你自己的电脑上，配合 Herdr 使用。<br><sub>Web · 更新于 2026-11 · MIT</sub>
- **[ccpocket](https://github.com/K9i-0/ccpocket)** · ★ 1.1k · 🀄<br>把编程代理装进口袋：用聊天的方式在手机上操作 Codex 和 Claude，发指令、批准下一步、看结果，换到平板或 Mac 也能接着做。<br><sub>Android / iPhone · 更新于 2026-11 · MIT</sub>
- **[Mobile-Harness](https://github.com/techjarves/Mobile-Harness)** · ★ 952<br>安卓上的 AI 开发工作台：在手机上和编程 Agent 对话、改项目、跑真正的 Linux 命令并预览网页。<br><sub>Android · 更新于 2026-11 · MIT</sub>
- **[codex-relay](https://github.com/gronxb/codex-relay)** · ★ 746<br>Codex CLI 的手机搭档：在工作区跑本地中转，通过你自己的网络配对，在手机上跟进或引导 Codex 会话，代码和状态都留在电脑上。<br><sub>iPhone · 更新于 2026-11 · Apache-2.0</sub>

<a id="cat-testing"></a>
## 给开发者：用 AI 测试自己的 App

- **[docker-android](https://github.com/budtmo/docker-android)** · ★ 16.2k<br>把安卓模拟器装进 Docker，浏览器里就能看，带录屏和 MCP 服务器，适合给 Agent 准备测试手机。<br><sub>Android · 更新于 2026-11</sub>
- **[midscene](https://github.com/web-infra-dev/midscene)** · ★ 15.6k · 🀄<br>Midscene：AI 视觉测试框架，用自然语言写 E2E 测试，支持网页、安卓、iOS 和鸿蒙。<br><sub>Android / iPhone / HarmonyOS · 更新于 2026-11 · MIT</sub>
- **[agent-device](https://github.com/callstack/agent-device)** · ★ 5.4k<br>给编程 Agent 用的设备层：通过命令行、MCP 或 Node.js API 控制 iOS、安卓、鸿蒙的模拟器和真机，让 Agent 在运行中的 App 里验证自己的改动。<br><sub>Android / iPhone / HarmonyOS · 更新于 2026-11 · MIT</sub>
- **[argent](https://github.com/software-mansion/argent)** · ★ 3.2k · 🀄<br>让 AI 助手操控 iOS 模拟器、安卓模拟器和真机，点按、分析性能、复现问题。<br><sub>Android / iPhone · 更新于 2026-11 · Apache-2.0</sub>
- **[ios-simulator-mcp](https://github.com/joshuayoes/ios-simulator-mcp)** · ★ 2.2k<br>操作 iOS 模拟器的 MCP 服务器：获取信息、控制界面交互、检查元素。<br><sub>iPhone · 更新于 2026-11 · MIT</sub>
- **[sim-use](https://github.com/lycorp-jp/sim-use)** · ★ 1.6k<br>LINE 雅虎开源：把屏幕变成省 token 的文字大纲，让 AI 按别名点按 iOS 模拟器和安卓设备上的元素。<br><sub>Android / iPhone · 更新于 2026-11 · Apache-2.0</sub>
- **[arbigent](https://github.com/takahirom/arbigent)** · ★ 658<br>AI Agent 测试框架，有图形界面也有代码接口，把复杂场景拆成小步骤，支持安卓、iOS 和网页。<br><sub>Android / iPhone / Web · 更新于 2026-10 · Apache-2.0</sub>

<a id="cat-models"></a>
## 模型与评测（开发者）

上面这些工具背后的手机 GUI 模型，以及评估手机 Agent 的环境。

- **[MAI-UI](https://github.com/Tongyi-MAI/MAI-UI)** · ★ 2.4k · 🀄<br>通义的 GUI Agent 基座模型，统一手机、电脑、浏览器场景，用 100 多台真机、150 多个 App 训练和评测。<br><sub>更新于 2026-08</sub>
- **[AgentCPM-GUI](https://github.com/OpenBMB/AgentCPM-GUI)** · ★ 1.4k · 🀄<br>清华 THUNLP 等开源的端侧 GUI Agent 模型，能操作中文和英文 App。<br><sub>更新于 2026-01 · Apache-2.0</sub>
- **[CogAgent](https://github.com/zai-org/CogAgent)** · ★ 1.2k · 🀄<br>智谱开源的端到端视觉语言 GUI Agent 模型。<br><sub>更新于 2026-10 · Apache-2.0</sub>
- **[UI-Venus](https://github.com/inclusionAI/UI-Venus)** · ★ 1.1k<br>inclusionAI 的通用 GUI Agent 模型，覆盖手机 App、网页和桌面系统。<br><sub>更新于 2026-10</sub>
- **[android_world](https://github.com/google-research/android_world)** · ★ 1.0k<br>Google 的安卓 Agent 评测环境和基准。<br><sub>更新于 2026-11 · Apache-2.0</sub>

<a id="cat-basics"></a>
## 基础工具

- **[scrcpy](https://github.com/Genymobile/scrcpy)** · ★ 155.1k · 💻<br>在电脑上显示并控制安卓手机，很多手机 Agent 都靠它看屏幕和操作。<br><sub>Android · 更新于 2026-11 · Apache-2.0</sub>
- **[skyadb](https://github.com/sky22333/skyadb)** · ★ 776 · 🀄<br>装在安卓手机上的 ADB 助手，用无线调试或 OTG 管理其他手机、平板、电视和盒子，可接 OpenAI 兼容模型让 AI 操作设备。<br><sub>Android · 更新于 2026-11 · GPL-3.0</sub>

<a id="faq"></a>
## 常见问题

**和豆包手机、厂商自带的 AI 助手有什么区别？**
厂商助手有系统级权限，体验更顺，但只在特定手机上有、模型也不能换。这里的开源工具在大多数安卓手机上都能装，模型可以自己选，代码可以检查，代价是要自己配置，稳定性因 App 而异。

**需要 root 吗？**
大多数不需要。安卓 App 一般用无障碍服务；想在后台虚拟屏上操作，通常需要 Shizuku 或开启无线调试。只有少数工具需要 root，iPhone 上的越狱方案已单独标 🔓。

**要花钱吗？**
工具都是开源的。用云端模型要付模型费用；PokeClaw、PhoneClaw 这类能在手机上跑本地模型的工具可以不花钱，但对手机配置有要求，速度也更慢。

**最适合拿来做什么？**
读得多、点得多、但不需要判断的事最合适：总结群聊和帖子、查资料、比价、填表、整理文件、测试自己的 App。涉及钱和隐私的操作，建议只让它准备好，最后一步由你来点。

**星标数多久更新一次？**
每周一由 GitHub Actions 自动刷新并重新排序，链接每周检查一次。

<a id="finder"></a>
## 让 AI 助手帮你挑

这份清单也是一个 skill。把仓库里的 [`skills/phone-agent-finder`](skills/phone-agent-finder) 文件夹装进你的 AI 助手（或运行 `npx skills add DU8866-nice/awesome-phone-agents`），然后问它：

> 我用小米手机，不想 root，也不想连电脑，想让 AI 每天帮我总结几个群的聊天，用哪个？

它会按你的手机系统、是否有电脑、隐私要求和用途，从清单里挑两三个并说明理由，同时提醒付款和隐私方面要注意的地方。

<a id="related"></a>
## 相关合集

| 项目 | 说明 | ⭐ | 最近更新 |
|---|---|---:|---|
| [Awesome-GUI-Agent](https://github.com/showlab/Awesome-GUI-Agent) | 多模态 GUI Agent 的论文和资源。 | 1.2k | 2025-08 |
| [GUI-Agents-Paper-List](https://github.com/OSU-NLP-Group/GUI-Agents-Paper-List) | GUI Agent 论文清单。 | 932 | 2026-11 |
| [Awesome-LLM-Powered-Phone-GUI-Agents](https://github.com/PhoneLLM/Awesome-LLM-Powered-Phone-GUI-Agents) | 大模型手机 GUI Agent 的论文综述和清单。 | 186 | 2026-09 |

<a id="contributing"></a>
## 参与贡献

欢迎推荐项目或纠错：[提交 Issue](https://github.com/DU8866-nice/awesome-phone-agents/issues/new/choose)，或者修改 [`data/tools.yaml`](data/tools.yaml) 后提 PR，详见[贡献指南](CONTRIBUTING.md)。README 由脚本生成，请不要直接改它。

## Star 趋势

[![Star History Chart](https://api.star-history.com/svg?repos=DU8866-nice/awesome-phone-agents&type=Date)](https://star-history.com/#DU8866-nice/awesome-phone-agents&Date)
