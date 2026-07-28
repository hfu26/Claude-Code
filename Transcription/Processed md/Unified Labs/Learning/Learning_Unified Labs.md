# Learning Summary: Unified Labs (Morpho Curator, Asia)
# 学习笔记：Unified Labs（亚洲 Morpho Curator）

**Date / 日期:** 2026-07-28
**Sources / 来源:** Meeting_Clean_Unified_Labs_Catchup.md

## Core Concepts / 核心概念

- **Morpho Curator / 策展人**: An entity whitelisted by Morpho to create and manage lending vaults/markets — deciding which assets get listed, setting LTV and risk parameters, and sourcing both liquidity and borrow demand. / 获 Morpho 白名单授权、可创建并管理借贷金库的主体：决定资产上架、设定 LTV 与风险参数，并同时负责资金端与借款端的获客。
- **Vault-as-a-Service / 金库即服务**: Embedding a curator's Morpho vault into third-party platforms (Perp DEXs, card issuers, content apps) as their native yield backend. / 将 curator 的 Morpho 金库嵌入第三方平台（Perp DEX、发卡商、资讯 App）作为其原生收益底层。
- **Self-looping a tokenized strategy / 策略代币化自循环**: Tokenize your own quant strategy, list it as Morpho collateral, then borrow against it yourself to lever up and capture the full strategy-vs-borrow spread. / 将自营量化策略代币化上架为抵押品，自己作为最大 borrower 加杠杆，吃下策略收益与借款成本之间的全部利差。
- **Native RWA issuance / RWA 原生发行**: The end-state where the on-chain token IS the fund/note itself — no SPV, no wrapper (e.g. HSBC's native note, UK native fund). / RWA 终局形态：token 即基金/票据本身，无 SPV、无 wrapper（如汇丰原生票据、英国原生基金）。
- **Regulatory arbitrage via fixed-rate mode / 固收模式监管套利**: Issuing strategy exposure as a fixed-rate product (adjusted weekly) to avoid triggering asset-management licensing, vs. profit-sharing structures which require licenses. / 以每周可调的固定利率产品形式发行策略敞口，规避资管牌照要求；分红型结构则需牌照。

## Mental Models & Mechanisms / 思维模型与机制

### 1. The whitelist is the moat, not the strategy / 壁垒是白名单，不是策略
- **What / 是什么:** Morpho granted Unified Labs Asia's first (and first non-institutional) curator whitelist, then closed the door to non-institutions.
- **How / 如何运作:** Won via 4 months of non-standardized trust-building: joint recommendations from Asian institutions (华夏基金 etc.), an RWA-lending thesis matching Morpho's roadmap, detailed architecture DD. Principle approval in ~2 months; then bootstrap: Morpho subsidized ~2pts on each side (deposit 5–6%, borrow 7–8%) with Fosun-fund money and ~$20M+ community liquidity to prove demand.
- **Why it matters / 为什么重要:** Without the whitelist "没人跟你聊" — it converts a 3-person team into the counterparty of Fosun, Yunfeng, Futu, Credit Saison. Scarce licenses/permissions can matter more than product in permissioned DeFi. Even quant funds that discover Morpho (e.g. HK's "ForceCap") cannot onboard without a curator.

### 2. "Free but exclusive" channel roll-up / "免费但独家"的渠道卷收
- **What:** Integrate yield backends into every reachable Asian platform at zero fee and zero revenue share, in exchange for exclusivity.
- **How:** SoSoValue (100k DAU, own chain/exchange, overseas users) signed exclusive; pipeline includes Perp DEXs, exchanges, white-label U-card issuers (Interlace: 12k enterprises), content platforms. Payments integration (pay directly from Morpho positions) also run at zero margin.
- **Why:** The exit thesis is acquisition: in ~1+ year post-Clarity-Act, large corporates will buy proven teams, and what's being sold is the exclusive channel network + relationships, not current cash flow. Free integration is customer-acquisition cost for an M&A outcome; it also strengthens joint bargaining with Morpho (who reciprocates with lawyers/engineers — channel value-add).

### 3. Be your own biggest borrower / 自己做最大的 borrower
- **What:** Instead of selling quant-strategy capacity, tokenize it and lever it on your own vault.
- **How:** Strategy runs ~20–30% (HKUST quant circle team, IDG-linked, 1–2 months live money). Borrow at ~9% against the tokenized strategy → capture ~11pts spread on levered AUM. External strategies only accepted if they bring their own capital, in isolated pools with negotiated splits (e.g. "you made 4pts before, you make 8pts with me, I take 4").
- **Why:** Externally sold strategy capacity earns fees; self-looping earns the whole spread. It also sidesteps the cold-start problem of track record — team wealth + close-circle money (千万级) is enough, since the profit engine is leverage, not external AUM. Risk: a strategy blowup damages the curator brand (cf. Gauntlet's rumored ~$1B incident).

### 4. TradFi funding rails beat crypto LPs / 传统资金通道优于 crypto LP
- **What:** Source on-chain liquidity from traditional-finance distribution instead of crypto-native LPs.
- **How:** Fosun issues notes sold in its wealth app to traditional investors; proceeds flow on-chain ($10–20M expected August, post-audit). Next: HKD-stablecoin carry — issue HKD notes at ~2–3% (HKD base rate ~1.7%), swap to USDC for higher stablecoin yield; USD peg ≈ minimal FX risk. Yunfeng similarly fronts traditional gold merchants (~$100M claimed demand), abstracting wallets entirely.
- **Why:** TradFi money is cheaper, stickier, and vastly larger; the platforms with full license stacks (Fosun: brokerage, OTC, tokenization, on-chain wealth mgmt) can move when pure-crypto players can't. "打通传统的钱"是这条赛道的真正规模来源。

### 5. Pragmatic unblock: the oracle adapter / 务实解卡点：预言机换算 adapter
- **What:** Yunfeng's gold-lending launch stalled for months on oracle choice.
- **How:** Pyth = outage history; Chainlink = $k+/month fees Yunfeng refused. Solution: Chainlink's gold feed has a free tier priced per ounce; Unified built a free oz→gram conversion adapter matching Yunfeng's gram-denominated gold token. LTV copied from XAUT ("一模一样，都是黄金，没必要自己想"); liquidation outsourced to Amber Group (~7% penalty); AI-built monitoring of borrower health + feed liveness.
- **Why:** In B2B DeFi the binding constraints are often mundane (oracle fees, legal memos — cf. OCBC blocking its own PR), and the curator's real job is removing them cheaply. Copying battle-tested parameters (XAUT) instead of inventing risk frameworks is rational for commodity collateral.

### 6. Tokenization platforms are a transitional state / 代币化平台是过渡态
- **What:** Founder's thesis: standalone tokenization platforms (Asseto, DigiFT) are 伪需求 (false demand).
- **How:** Big distribution owners (Fosun, Futu — which has a dedicated on-chain product team) tokenize in-house; the end-state is native issuance where token = fund (UK native fund product; HSBC's ~HK$8B native note). Strategy-issuance platforms (Midas — German entity, compliance/KYC/redemption; Accountable — fixed-rate no-license mode + transparency/credit reporting; Pareto) are near-commodities differentiated only by showcases (Fasanara mF-ONE, Hyperithm arb strategy).
- **Why:** Positioning matters: value accrues to (a) distribution owners and (b) permissioned chokepoints (curators), not to middleware wrappers that both sides can disintermediate once native legal frameworks land.

### 7. Ship ahead of regulation / 跑在监管前面
- **What:** "跟着监管走必死" — launch first via license-free structures, retrofit compliance later.
- **How:** Use Accountable's fixed-rate mode (no asset-management license; weekly rate adjustment approximates strategy pass-through); take stablecoins in/out. Acquire licenses once revenue justifies it; treat later compliance as "交保护费".
- **Why:** In a land-grab phase, the scarce asset is proven cases and channels, not licenses; incumbents (banks) are structurally slow (OCBC legal memo), which is exactly the window for small teams.

## Key Insights / 关键洞察

1. **EN:** Permissioned-DeFi gatekeeping (Morpho's closed curator list) has recreated a licensing dynamic: access itself is the business. **CN:** 许可型 DeFi 的准入闸门（Morpho 关闭 curator 名单）重现了"牌照经济"：准入本身就是生意。
2. **EN:** The curator business in Asia is a distribution business wearing a risk-management costume — every revenue line (VaaS, strategy, consulting) monetizes channels and trust, not models. **CN:** 亚洲 curator 业务本质是披着风控外衣的分销生意——三条收入线（VaaS、策略、咨询）变现的都是渠道与信任，而非模型。
3. **EN:** Subsidy wars between lending protocols (Aave undercutting after their whitelist win) can wipe out a curator's TVL overnight; whitelist durability matters more than TVL snapshots when evaluating such companies. **CN:** 借贷协议间的补贴战（Aave 砸利率）可一夜抹平 curator 的 TVL；评估此类公司时，白名单的持久性比 TVL 快照更重要。
4. **EN:** The self-looping model concentrates both upside and tail risk in the curator — 20–30% strategy returns levered at 9% cost is attractive until a blowup destroys the very trust the whitelist encodes (Gauntlet cautionary tale). **CN:** 自循环模式把收益与尾部风险同时集中在 curator 身上——策略 20–30%、借款成本 9% 的杠杆很诱人，但一次爆仓即摧毁白名单所承载的信任（Gauntlet 为前车之鉴）。
5. **EN:** HKD's low funding cost (~1.7% base) plus the USD peg creates a structurally cheap, low-FX-risk carry into USD stablecoin yields — a rail only full-stack licensed groups like Fosun can open. **CN:** 港元低融资成本（基准约 1.7%）叠加联系汇率，构成进入美元稳定币收益的低汇率风险套利通道——只有复星这类全牌照集团能打开。
6. **EN:** For IOSG: the asset being underwritten here is the founder's BD velocity and the whitelist scarcity, with August's three landings (Fosun notes, Yunfeng XAU, SoSoValue) as the near-term verification events. **CN:** 对 IOSG 而言：本案真正在承销的是创始人的 BD 速度与白名单稀缺性，八月三项落地（复星票据、云锋 XAU、SoSoValue）是近期验证节点。

## Open Questions / 未解决问题

1. How durable is the Morpho whitelist exclusivity — could Morpho re-open to institutions and dilute the moat? / Morpho 白名单的排他性能维持多久？若向机构重新开放，壁垒是否被稀释？
2. Can a 3–4 person team actually service exclusive integrations across all of Asia without execution collapse? / 三四个人的团队能否支撑全亚洲的独家集成而不失控？
3. Strategy track record is only 1–2 months of live money — what is real capacity and drawdown behavior? / 策略实盘仅一两个月，真实容量与回撤表现如何？
4. Legal characterization of the "fixed-rate no-license" structure across HK/SG/JP — how long does the regulatory-arbitrage window stay open? / "固收无牌照"结构在港/新/日的法律定性如何，套利窗口能开多久？
5. Verification needed: HSBC native note (~HK$8B), UK native fund product, Gauntlet incident, Yunfeng's claimed $100M gold-borrow demand. / 需核实：汇丰原生票据（约 80 亿港元）、英国原生基金、Gauntlet 踩雷传闻、云锋所称一亿美金黄金借贷需求。
6. Exit dependency: if the acquisition wave post-Clarity-Act doesn't materialize in ~1 year, does the zero-fee exclusive model have a standalone path to profitability? / 若 Clarity Act 后的并购潮一年内未至，零费独家模式是否有独立盈利路径？

## Glossary / 术语表

| Term | Definition / 定义 |
|---|---|
| Curator | Morpho 金库策展人：设定资产、LTV、风控参数并运营金库的白名单主体 |
| LTV | Loan-to-Value，抵押率：借款额与抵押品价值之比 |
| Looping | 循环贷：抵押→借出→再买入抵押品→再抵押，放大敞口与收益 |
| Vault-as-a-Service | 金库即服务：把收益金库嵌入第三方平台作为其理财底层 |
| XAU / XAUT | 云锋金融的黄金代币 / Tether Gold（黄金锚定代币，风控参数参照对象） |
| SPV | Special Purpose Vehicle，特殊目的载体：传统 RWA 发行中的隔离主体 |
| Native issuance | 原生发行：token 本身即基金/票据，无 wrapper 与 SPV |
| Oracle / 预言机 | 链上价格喂送服务（Chainlink、Pyth），清算依赖其报价 |
| Liquidation penalty | 清算罚金：清算时对借款人收取的折价（本案约 7%） |
| Carry trade | 套息交易：低成本货币融资投向高收益资产（港元→USDC 收益） |
| Clarity Act | 美国数字资产市场结构法案，被视为机构大规模入场的监管开关 |
| AUM | Assets Under Management，管理资产规模 |
| Isolated pool | 隔离池：风险相互隔离的独立借贷市场 |
| Showcase | 标杆案例：证明平台/策略可行性的首个落地产品 |
