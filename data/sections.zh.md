<!-- section:intro -->
“AI 手机”正在从厂商发布会走到每个人手里：说一句“帮我把群聊总结一下”“比个价，加到购物车”，AI 就会自己打开 App、看屏幕、点按、输入，把事情办完。过去几个月，开源社区冒出了一大批这样的工具：有直接装在安卓手机上的 App，有让电脑上的 Claude Code、Codex 接管手机的 MCP 服务器，也有智谱 Open-AutoGLM、阿里 Mobile-Agent 这样的开源框架和模型。

这份清单面向想动手用的人，而不是论文清单：按你的设备和用法整理这些工具，标明支持安卓还是 iPhone、要不要电脑、要不要 root、能不能用本地模型。

<!-- section:pick -->
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

<!-- section:rules -->
## 用之前先知道

> [!IMPORTANT]
> - **屏幕内容会发给模型。** 这类工具靠截图或界面结构“看”手机，聊天记录、验证码、余额都可能出现在画面里。用云端模型时，这些内容会发给模型服务商；标 🔒 的工具可以用本地模型，内容不出设备。
> - **付款、转账和删除要自己确认。** 优先选默认在付款、发消息前询问你的工具，并保持这些确认开着。别让 AI 无人看管地碰钱包、银行和不能撤销的操作。
> - **权限给多少，它就能做多少。** 无障碍服务、Shizuku、ADB 和 root 都意味着手机的大部分控制权。只从官方仓库下载，只授权你信任的工具，用完关掉远程访问。
> - **注意平台规则。** 很多 App 的条款禁止自动化操作，频繁自动点按可能触发风控、导致账号受限。用在自己的日常事务上，别拿来刷量。
> - **iPhone 的限制。** iOS 不允许普通 App 操作其他 App，所以 iPhone 方案大多需要电脑配合，或者用 Mac 签名安装，签名到期要维护。

本清单不收录群控、养号、刷量和多账号营销工具，不收录绕过风控或反检测的“隐身”云手机，也不收录抢红包、游戏外挂类工具。

<!-- section:faq -->
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

<!-- section:finder -->
## 让 AI 助手帮你挑

这份清单也是一个 skill。把仓库里的 [`skills/phone-agent-finder`](skills/phone-agent-finder) 文件夹装进你的 AI 助手（或运行 `npx skills add DU8866-nice/awesome-phone-agents`），然后问它：

> 我用小米手机，不想 root，也不想连电脑，想让 AI 每天帮我总结几个群的聊天，用哪个？

它会按你的手机系统、是否有电脑、隐私要求和用途，从清单里挑两三个并说明理由，同时提醒付款和隐私方面要注意的地方。

<!-- section:contributing -->
## 参与贡献

欢迎推荐项目或纠错：[提交 Issue](https://github.com/DU8866-nice/awesome-phone-agents/issues/new/choose)，或者修改 [`data/tools.yaml`](data/tools.yaml) 后提 PR，详见[贡献指南](CONTRIBUTING.md)。README 由脚本生成，请不要直接改它。
