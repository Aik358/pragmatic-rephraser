# 语用印坊 · Pragmatic Rephraser

**HW1 · Prompt-Based NLP Mini Project** — one Chinese sentence in, five pragmatic expressions out.

输入**一个中文句子**，系统先识别它的言语行为（请求 / 批评 / 拒绝 / 抱怨 / 建议 / 陈述），再把**同一个意图**改写成五种语用版本：

| # | 语气 | 策略 (Brown & Levinson 1987) |
|---|------|------------------------------|
| 01 | 直接 Neutral Direct | bald on-record |
| 02 | 礼貌 Polite | positive politeness（常规缓和） |
| 03 | 非常礼貌 Very Polite | negative politeness（敬称、致歉、缓和语） |
| 04 | 委婉暗示 Indirect Hint | off-record（意在言外） |
| 05 | 亲昵随意 Casual | in-group markers（附加语气） |

## 在线使用

**https://aik358.github.io/pragmatic-rephraser/**

无需安装、无需登录。默认使用**离线规则引擎**；也可以在「配置 AI」中填入自己的 OpenAI 兼容 API Key（DeepSeek / 智谱 / Kimi / OpenAI / 豆包）启用大模型改写。密钥默认只在当前页面会话中使用，不会上传到本站（本站没有服务器）。

## 交互设计

纸墨美学的**活字印刷台**隐喻：一句话经过排字、压印、揭纸的仪式，展开为五张"语气印谱"；每个版本新增的语用手段以颜料色标出；选择一句后，按「原句 + 言语行为」的散列盖下一枚**确定性印记**——同一句话总能得到同一枚章。

- `#q=<句子>` — 打开即自动改写并展示结果（分享 / 评阅用）
- `#settings` — 直接打开 AI 配置
- `D` — 开/关语用批注　`R` — 清空
- 支持 `prefers-reduced-motion` 与「动效 开/关」手动切换

## 隐私说明

- 页面为纯静态单文件（`index.html`），零依赖、无追踪、无后端；
- 仅当用户主动点击 AI 生成或「测试连接」时，输入句与自己配置的密钥才会发送到**用户自行配置的服务商地址**；
- 不勾选「记住密钥」时，密钥只保存在当前页面会话中，刷新即消失。

## 运行

直接双击 `index.html` 即可离线使用全部功能（AI 调用需通过 `http(s)://` 打开页面，浏览器会拦截 `file://` 的跨域请求）。

---
*Course assignment for an NLP course (PolyU). Linguistic framework: Brown & Levinson (1987). Design language inspired by [未定之场](https://github.com/OBdangshang07/AI_project/tree/main/Esthetics/Deepseek0820).*
