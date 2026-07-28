# Meeting Summary: Unified Labs Catchup
# 会议纪要：Unified Labs 线下 Catchup

**Date / 日期:** 2026-07-28 (approximate / 约)
**Type / 类型:** 1:1 founder catchup (first offline meeting) / 创始人一对一线下首次见面
**Speakers / 参会人:** speaker_0 (IOSG / Frank), speaker_1 (Unified Labs founder / 创始人)
**Company / 公司:** Unified Labs — first non-institutional Morpho curator in Asia / 亚洲第一家（非机构）Morpho curator

---

## 1. Morpho Curator Whitelist: The Core Moat / Morpho 白名单：核心壁垒

**EN:** Unified Labs spent ~4 months securing Morpho's curator whitelist — the first in Asia and the first non-institutional grantee. Morpho has since indicated it will no longer whitelist non-institutional curators, making the license a scarce, defensible asset. The application was non-standardized: they won trust via joint recommendations from Asian institutions (China AMC and others), an RWA-lending thesis aligned with Morpho's strategy, and detailed DD on architecture and looping design. Principle approval took ~2 months; the hardest part was bootstrapping — initial TVL came from a Fosun-linked USD fund (with Morpho subsidizing ~2pts on both deposit and borrow sides, reaching 5–6% deposit / 7–8% borrow) and ~$20M+ of liquidity from a community leader's DeFi following. TVL briefly approached $100M-scale before Aave's rate-cutting compressed it back down ("打回原形"), but the whitelist itself remains the BD unlock: "没有白名单，没人跟你聊."

**CN:** Unified Labs 花了约四个月拿到 Morpho curator 白名单——亚洲第一家、也是第一家非机构获批方。Morpho 此后表示不再向非机构开放白名单，使该资格成为稀缺壁垒。申请无标准流程：靠亚洲多家机构（华夏基金等）联合推荐、契合 Morpho 战略的 RWA 借贷方案、以及详尽的架构与循环机制设计打动对方，约两个月拿到原则性批准。最难的是冷启动：初始 TVL 来自复星系美元基金（Morpho 存借两侧各补贴约 2 个点，做到存款 5–6%、借款 7–8%），流动性来自社区 KOL 带来的两千多万美金。TVL 一度接近上亿规模，后因 Aave 砸利率大幅回撤，但白名单本身就是 BD 的敲门砖。

## 2. Business Model: Three Lines / 业务模式：三条线

**EN:** (1) **Vault-as-a-Service via exclusive distribution**: instead of raising from LPs, they integrate Morpho vaults into asset-rich platforms — Perp DEXs, exchanges, white-label U-card issuers serving 10k+ enterprises, and content platforms embedding wealth modules. They charge nothing and take no revenue share, but demand Asia exclusivity, aiming to lock up the entire Asian channel network (SoSoValue, ~100k DAU, is already exclusive). (2) **Tokenized quant strategy**: run with an HKUST-linked quant team (IDG-affiliated), currently doing ~20–30% returns with 1–2 months of live money. Plan: tokenize the strategy, list it on Morpho as collateral, and self-borrow as the largest borrower to capture the full ~11pt spread (20% strategy return vs ~9% borrow cost) rather than selling the strategy externally. (3) **RWA leverage strategies**: package looped RWA positions for 15–20% fees, targeting institution-grade assets (e.g. credit-card receivables from a Credit Saison-linked Japanese trust player). Also exploring C-end margin finance. Future revenue mix: strategy P&L (the largest), plus consulting fees for traditional institutions wanting Morpho showcases (e.g. a major Asian medical fund backed by Middle East capital).

**CN:** （1）**独家分销的 Vault-as-a-Service**：不直接向 LP 募资，而是把 Morpho vault 集成进有资产的平台——Perp DEX、交易所、服务上万家企业的白牌 U 卡商、嵌入理财板块的资讯平台。免费集成、不分成，但要求亚洲独家，目标是锁定整个亚洲渠道网络（SoSoValue 已独家，日活约 10 万）。（2）**量化策略代币化**：与港科大量化圈团队（IDG 背景）合作，实盘一两个月，年化约 20–30%。计划将策略代币化后上 Morpho 作为抵押品，自己作为最大 borrower 加杠杆，吃下约 11 个点的完整利差（策略 20% vs 借款成本 9%），而非对外卖策略份额。（3）**RWA 杠杆策略**：将 RWA looping 仓位打包，收 15–20% 费用，只挑机构级资产（如日本 Credit Saison 系信托的信用卡账单资产）。另布局 C 端 margin finance。未来收入大头是策略，其次是给传统机构做 Morpho showcase 的咨询费（如中东资金背景的亚洲最大医疗基金代币化项目）。

## 3. Landed / Landing Cases (August) / 落地与将落地案例（八月）

**EN:** Three cases targeted for August: (a) **Fosun** — $10–20M via a novel TradFi funding rail: Fosun issues notes sold through its wealth app to traditional investors, proceeds flow on-chain into Unified's pools. Fosun has the full stack (brokerage, licensed OTC, tokenization, on-chain wealth mgmt), and they're jointly planning an HKD-stablecoin carry trade — issue HKD notes at ~2–3% (HKD rates at ~1.7%), convert to USDC for stablecoin yield, with the USD peg minimizing FX risk. (b) **Yunfeng Financial** — gold token (XAU) lending on Morpho; Yunfeng claims ~$100M borrowing demand from traditional gold businesses, with Yunfeng abstracting away wallets/stablecoins for clients. Unified solved the oracle deadlock (months-long) by building a free adapter converting Chainlink's free gold feed from oz to grams, avoiding both Pyth's outage risk and Chainlink's $k/month fees. LTV parameters copied from XAUT; liquidation via Amber Group at ~7% penalty; Unified runs AI-built monitoring of borrower health and oracle feeds. (c) **SoSoValue** integration. Potential lead investor: Credit Saison (wants a live case first).

**CN:** 八月目标落地三案：（a）**复星**——1000–2000 万美金，创新的传统资金通道：复星发行票据，在复星财富 App 向传统投资人销售，募集资金上链进入 Unified 的池子。复星全牌照全栈（券商、OTC、代币化、链上财富管理），双方还在筹划港元稳定币套利：以约 2–3 个点发港元票据（港元利率仅 1.7%），换 USDC 做稳定币收益，联系汇率下汇率风险极低。（b）**云锋金融**——黄金代币 XAU 上 Morpho 借贷；云锋称传统黄金商有约一亿美金借贷需求，并为客户代持代操作。预言机卡点数月后被解决：利用 Chainlink 免费黄金喂价源，自建盎司转克的换算 adapter，既避开 Pyth 宕机风险又省下 Chainlink 每月数千美金费用。LTV 参数直接对标 XAUT；清算由 Amber Group 执行，罚金约 7 个点；Unified 用 AI 辅助开发的系统监控借款人健康度与预言机喂价。（c）**SoSoValue** 集成。潜在领投方 Credit Saison（要求先见落地 case）。

## 4. Competitive Landscape / 竞争格局

**EN:** Asian Morpho curators: only Unified plus "Bridge" (a 2018 hedge fund doing on-chain quant only, no ecosystem BD) and partially Asseto (whose curator is an arms-length partner used only for listing). Founder's takes: standalone tokenization platforms (Asseto, DigiFT) are "伪需求" — large platforms (Fosun, Futu, which has a dedicated on-chain product team) tokenize in-house; the end-state of RWA is native issuance where the token IS the fund (citing a UK native fund product and HSBC's ~HK$8B native note), making today's wrapper/SPV platforms transitional. Midas differs as a strategy-issuance platform (German entity handling compliance/KYC/redemption) but is slow and controlling (per Hyperithm's experience), and requires an asset-management license. Accountable's fixed-rate mode requires no license — the regulatory-arbitrage route Unified plans to use for fast launch. Curator archetypes: Steakhouse (big clients, consulting fees), Gauntlet (aggressive quant, highest pressure, recent ~$1B blowup rumor), Hyperithm (quant), Sentora (emerging stablecoins — PayPal, Ripple). Unified positions itself as the aggregate of all these models in Asia, doubling down on whichever proves most profitable.

**CN:** 亚洲 Morpho curator 格局：除 Unified 外仅有"Bridge"（2018 年成立的对冲基金，只做链上量化，不做生态 BD）和部分意义上的 Asseto（其 curator 是外部合作方，仅用于上架）。创始人观点：独立代币化平台（Asseto、DigiFT）是伪需求——大平台（复星、富途，后者有专门的链上产品部门）都自建代币化；RWA 终局是原生发行，token 即基金本身（举例英国原生基金产品与汇丰约 80 亿港元原生票据），当前的 wrapper/SPV 平台皆为过渡态。Midas 定位不同，是策略发行平台（德国主体解决合规/KYC/赎回），但慢且控制欲强（Hyperithm 的反馈），并要求资管牌照。Accountable 固收模式无需牌照——Unified 计划借此监管套利快速上线。Curator 各流派：Steakhouse（大客户咨询费）、Gauntlet（激进量化、压力最大、近期有十亿级踩雷传闻）、Hyperithm（量化）、Sentora（新兴稳定币增值：PayPal、Ripple）。Unified 定位为亚洲的"全流派集合体"，哪条线跑通就 focus 哪条。

## 5. Team, Background & Exit / 团队、背景与退出路径

**EN:** Team of 3, plus a newly recruited Malaysia-based SEA ecosystem lead (ex-ecosystem lead at a protocol the founder followed; the person who first introduced him to Morpho). Founder background: 2 years on central-bank tokenization pilots (Australia supply-chain finance, Singapore cross-border trade verification; with 曹老板/孟岩), full-cycle startup experience including fundraising; later at a prior firm (花老师) for 4 months; also worked on an OCBC deployment (claimed first CCIP-type system in APAC, PR blocked by OCBC legal pending a legal memo). Cost base is minimal — effectively no runway pressure. Exit thesis: within ~1+ year, once regulation (Clarity Act) normalizes, large corporates will acquire the few proven Asian teams; Unified is building to be acquired for its channel network, partnerships, and strategy brand. Strategy for external quant funds: whitelist is the moat (e.g. HK quant fund "ForceCap" can't onboard without a curator); will only onboard external strategies that bring their own capital, via isolated pools with negotiated revenue share.

**CN:** 团队三人，新招一名马来西亚籍东南亚生态负责人（前某协议生态负责人，正是最早向创始人介绍 Morpho 的人）。创始人背景：两年央行代币化试点（澳大利亚供应链金融、新加坡跨境贸易核验，与曹老板、孟岩共事），有完整从零到一创业与融资经验；后在前东家（花老师处）四个月；参与过 OCBC 项目落地（自称亚太第一个 CCIP 类系统，PR 因 OCBC 法务要求 legal memo 被搁置）。成本极低，几乎无 runway 压力。退出逻辑：约一年多后，监管（Clarity Act）明朗，大公司将并购亚洲少数已跑通的团队；Unified 卖的是渠道网络、合作关系与策略品牌。对外部量化基金：白名单即壁垒（如香港量化基金"ForceCap"无 curator 无法上架）；仅接受自带资金的外部策略，用隔离池并协商收益分成。

---

## Key Decisions / 关键决策

1. **EN:** Pursue Asia-wide exclusive integrations ("free but exclusive") to build a proprietary channel network before competitors arrive. **CN:** 以"免费但独家"模式扫遍亚洲平台集成，抢在竞争者进入前建立专有渠道网络。
2. **EN:** Tokenize the in-house quant strategy and self-loop on Morpho as the largest borrower, rather than selling strategy capacity externally. **CN:** 将自营量化策略代币化并在 Morpho 上自我加杠杆（自己做最大 borrower），而非对外出售策略额度。
3. **EN:** Launch via Accountable's fixed-rate (no-license) mode first; acquire licenses later — "跟着监管走必死". **CN:** 先走 Accountable 固收模式（无需牌照）快速上线，牌照后补——"跟着监管走必死"。
4. **EN:** Focus fundraising on TradFi rails (Fosun notes, HKD stablecoin carry, banks) rather than crypto-native LPs. **CN:** 融资/资金来源重心放在传统金融通道（复星票据、港元稳定币套利、银行），而非 crypto 原生 LP。

## Open Items / 待办与跟进

1. **EN:** Founder to send revenue forecast to Frank. **CN:** 创始人将收入预测发给 Frank。
2. **EN:** Frank to sync internally with colleague (who is out of date on Unified's progress) before discussing a potential IOSG investment ("投个投吧"). **CN:** Frank 需与同事内部对齐（对方不了解 Unified 最新进展），再讨论 IOSG 是否参与投资。
3. **EN:** Verify August landings: Fosun note issuance ($10–20M, post-audit), Yunfeng XAU lending volume, SoSoValue integration. **CN:** 跟踪八月落地：复星票据（审计后 1000–2000 万美金）、云锋 XAU 借贷量、SoSoValue 集成。
4. **EN:** Watch Credit Saison lead-investment condition (requires one live case) and the claimed HSBC native note / UK native fund precedents. **CN:** 跟进 Credit Saison 领投条件（需先有落地 case），并核实汇丰原生票据 / 英国原生基金先例。

---

## Appendix: Scoring Table / 附录：评分表

No formal token scoring was conducted in this meeting (founder catchup, no token investment scoring discussion). Qualitative assessments of projects discussed / 本次会议为创始人 catchup，未进行正式代币评分；以下为讨论到的项目定性评价：

| Project / 项目 | Role in discussion / 角色 | Speaker assessment / 谈话中的评价 |
|---|---|---|
| Morpho | 底层借贷协议 | "当红炸子鸡"；渠道增值支持强（出律师、工程师）；白名单极稀缺，不再开放给非机构 |
| Aave | 竞对协议 | 砸利率打补贴战导致 Unified TVL 回撤；做集成"没什么竞争力" |
| Spark | 竞对协议 | 不适合做集成 |
| Midas | 策略发行平台 | 有 showcase（Fasanara mF-ONE、Hyperithm 策略）但慢、控制多、需资管牌照 |
| Accountable | 发行/透明度平台 | 固收模式无需牌照，可监管套利快速上线；解决透明度与征信 |
| Pareto | 发行平台 | 与 Midas/Accountable 同质化，靠 showcase 区分 |
| Asseto / DigiFT | 代币化平台 | "伪需求"——大平台自建代币化；属过渡态 |
| SoSoValue | 独家分销伙伴 | 日活 10 万，海外（日本/东南亚）用户，已签独家 |
| 复星 Fosun | 资金通道伙伴 | 全牌照全栈、"胆大且懂"；票据融资 + 港元稳定币套利 |
| 云锋金融 Yunfeng | 资产端伙伴 | 黄金 XAU 借贷，口称一亿美金需求；执行慢（2–3 人管多项目），需持续教育推动 |
| 富途 Futu | 潜在合作方 | "很懂"，有专门链上产品部门，合作保密项目中 |
| Gauntlet | 竞对 curator | 最激进、压力最大，近期十亿级踩雷传闻 |
| Steakhouse | 竞对 curator | 大客户 + 咨询费路线 |
| Sentora | 竞对 curator | 新兴稳定币（PayPal、Ripple）增值路线 |
| Hyperithm | 竞对/同行 | 韩国对冲基金，量化路线，Midas 上有大策略 |
| Interlace | 潜在客户 | 新加坡企业发卡商，服务 1.2 万企业，卡内存款生息场景 |
| Amber Group | 清算服务方 | 承接云锋清算，罚金约 7% |
| Chainlink / Pyth | 预言机 | Chainlink 贵但可靠（找到免费黄金喂价源）；Pyth 有宕机前科 |
