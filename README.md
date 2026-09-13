# 高等生產管理（Advanced Production Management）知識領域整理

> 用途：工業工程碩專班「製造管理與決策」課程的知識地圖
> 整理日期：2026-09-13（v2：併入課堂講師舉例的 17 個領域）
> 資料來源：清華大學 OCW 生產計畫與管制、元智大學高等生產管制、台科大工管系研究領域、台大 OCW 作業管理、POMS 期刊 Departments 分類、ASCM/APICS CPIM Body of Knowledge、Hopp & Spearman《Factory Physics》、2025–2026 智慧製造與 RL 排程回顧性論文

---

> **互動心智圖：** https://larry6705.github.io/production-management-mindmap/

## 0. 這門學科在問什麼

高等生產管理處理的是同一個核心問題：
**在需求不確定、產能有限、資源有成本的前提下，決定「生產什麼、生產多少、什麼時候生產、用哪些資源生產」。**

三個交織的軸線：

| 軸線 | 內容 |
|---|---|
| **決策層級** | 策略（數年）→ 戰術（數月）→ 作業（數日／即時） |
| **系統物理** | 產出率、在製品、週期時間、變異之間不可違背的關係 |
| **決策方法** | 從確定性最佳化到隨機／強健最佳化、模擬、啟發式、機器學習 |

大學部的「生產與作業管理」教的是**流程與工具**；研究所層級的「高等生產管理」加上兩件事：**數學模式化**與**不確定性下的決策**。

### 0.1 一條主軸看懂全貌

**設計面（一次性、決定體質）→ 規劃面（週期性、決定節奏）→ 執行面（日常、決定績效）→ 改善面（持續、決定進化）**

| 面向 | 對應章節 | 決策特性 |
|---|---|---|
| 設計面 | 產品設計、製程設計、設施規劃、工廠佈置 | 投資大、不可逆、決定後續成本上限 |
| 規劃面 | 預測、產能、總合計畫、MPS/MRP、採購、庫存 | 滾動循環、以數量與時間為變數 |
| 執行面 | 排程、現場管制、品質管制、設備維護、顧客服務 | 即時、資訊驅動、變異吸收 |
| 改善面 | 精實、TPM、六標準差、ESG/綠色、智慧製造/AI | 長期累積、跨部門 |

### 0.2 課堂講師舉例領域 × 本文章節對照

| 講師舉例領域 | 對應章節 |
|---|---|
| 生產策略 | §1 |
| 產品設計 | §2 |
| 製程設計 | §3 |
| 設施規劃 | §4.1 |
| 工廠佈置 | §4.2 |
| 生產計畫 | §5 預測、§6 產能與總合計畫、§7 MPS/MRP |
| 採購管理 | §8 |
| 庫存管理 | §9 |
| 排程管理 | §10 |
| 精實生產 | §12（理論基礎見 §11） |
| 品質管理 | §13 |
| TPM | §14 |
| ESG | §16 |
| 綠色生產 | §16 |
| 智慧製造 | §19 |
| AI 與生產管理 | §19.3（方法面見 §18） |
| 顧客服務 | §17 |

---

# 一、設計面

## 1. 生產策略與生產系統基礎

- 生產系統分類：專案型 / 零工式（Job Shop）/ 批量 / 流線式 / 連續製程
- 接單策略：MTS、ATO、MTO、ETO — 決定了顧客訂單解耦點（CODP）位置
- 競爭優先序（Competitive Priorities）：成本、品質、交期、彈性、（近年加入）韌性與永續
- 製造策略與能力取捨（Trade-off theory）vs. 累積能力（Sand Cone Model）
- 產品—製程矩陣（Hayes–Wheelwright）：產品生命週期階段與製程型態的匹配
- 製造策略的內容與流程：訂單資格條件（Qualifier）vs. 訂單贏得條件（Order Winner）
- 全球製造網路佈局：廠別角色定位、產能分工、區域化 vs. 集中化
- 生產管理演進史：科學管理 → MRP → MRP II / ERP → JIT/TPS → TOC → 精實六標準差 → 智慧製造

---

## 2. 產品設計與開發

- 新產品開發流程：Stage-Gate 制度、概念設計 → 系統設計 → 細部設計 → 試產 → 量產
- 併行工程（Concurrent Engineering）：設計與製造同步，取代序列式移交
- **品質機能展開（QFD）**：顧客聲音（VOC）→ 工程特性 → 零件 → 製程 → 管制的品質屋展開
- 設計取向方法（DFX 家族）
  - DFM 可製造性設計、DFA 易組裝設計、DFQ、DFS 可服務性、DfE 環境導向設計
  - 目標：把成本與品質問題在設計階段解決（設計階段鎖定約 70–80% 的產品成本）
- 模組化設計與產品平台策略：共用件、零件標準化、產品族架構
- 物料清單（BOM）的設計意涵：多階 BOM、模組化 BOM、計畫性 BOM（Planning BOM）
- 價值工程 / 價值分析（VE/VA）、目標成本制（Target Costing）
- 大量客製化的設計前提：延遲策略（Postponement）與解耦點設計
- 生命週期觀點：可修復性、可拆解性、再製造設計（見 §16）
- 設計變更管理（ECN/ECO）對生產與庫存的衝擊

---

## 3. 製程設計與工作研究

- 製程選擇：製程型態決策與產品—製程矩陣的一致性
- 自動化程度決策：手動 / 半自動 / 全自動 / 彈性製造系統（FMS）的經濟權衡
- 製程能力與技術評估：設備選擇、投資報酬、實質選擇權觀點
- 製程分析工具：流程圖、製程圖（Process Chart）、人機程序圖、多動作程序圖
- **工作研究（Work Study）**
  - 方法研究：動作經濟原則、ECRS 改善原則、標準作業建立
  - 時間研究：碼錶測時、評比與寬放、預定動作時間標準（MTM/MOST）、工作抽查
  - 標準工時的用途：產能計算、排程、成本估算、績效衡量、獎工制度
- **生產線平衡（Line Balancing）**：工作站分派、平衡效率、循環時間與節拍時間
- 群組技術（GT）與零件分類編碼；細胞式製造的製程前提
- 換模與批量的製程設計意涵（連結 §12 SMED）
- 製程失效預防：PFMEA、管制計畫（Control Plan）、製程確效（IQ/OQ/PQ）
- 新興製程議題：積層製造（AM）對製程設計與供應鏈的改寫、人機協作單元

---

## 4. 設施規劃與工廠佈置

### 4.1 設施規劃（Facility Planning）
- 設施選址：因素評分法、重心法、運輸模式、選址—配置整合模式
- 選址考量：市場鄰近性、供應鏈成本、勞動力、關稅與貿易政策、風險分散
- 產能與廠房規模決策、擴廠時機與階段性投資
- 設施需求推估：面積需求、公用設施、動線、擴充預留

### 4.2 工廠佈置（Plant Layout）
- 佈置型態
  - 固定位置式（Fixed-Position）
  - 製程別／功能別（Process Layout）
  - 產品別／生產線式（Product Layout）
  - 細胞式（Cellular）與群組佈置
- **系統化佈置規劃（SLP, Muther）**：P-Q-R-S-T 分析 → 關係圖 → 空間關係圖 → 方案評估
- 分析工具：從至表（From-To Chart）、關係矩陣、流量—距離成本模式
- 數學模式：二次分派問題（QAP）、CRAFT / ALDEP / CORELAP 等啟發式演算法
- **物料搬運系統（MHS）**：搬運設備選擇、AGV/AMR 路徑與車隊規模、輸送帶配置
- 倉儲佈置與儲位指派：ABC 儲位、揀貨路徑最佳化、自動倉（AS/RS）
- 佈置評估：物流成本、彈性、可擴充性、安全與人因、目視化管理
- 精實佈置觀點：U 型線、單件流、縮短搬運距離、減少在製品暫存空間

---

# 二、規劃面

## 5. 需求預測（Forecasting）

- 定性法：德爾菲法、市場調查、專家判斷
- 時間序列：移動平均、指數平滑（單重／Holt 雙重／Holt-Winters 三重）、分解法、ARIMA
- 因果模式：迴歸分析、計量經濟模式
- 預測誤差衡量：MAD、MSE、MAPE、追蹤信號（Tracking Signal）
- 進階議題：間歇性需求（Croston 法）、新產品預測、機器學習預測（LSTM、梯度提升）、預測與庫存決策的整合（Predict-then-Optimize vs. End-to-End）
- **關鍵觀念：所有預測都是錯的；生產管理真正管理的是預測誤差。**

---

## 6. 產能規劃與總合生產計畫（Aggregate Planning / S&OP）

- 長期產能決策：產能擴充時機與規模、領先／落後策略、規模經濟與學習曲線
- 總合生產計畫（APP）策略：追逐策略、平準策略、混合策略
- 求解手法：試誤表格法、運輸模式、線性規劃 / 混合整數規劃
- 產能相關決策變數：加班、外包、雇用／解雇、季節性庫存、欠撥
- **銷售與作業規劃（S&OP）**：跨部門需求與供給的共識流程，現代版稱 IBP（整合性商業規劃）
- 粗略產能規劃（RCCP）與資源需求規劃（RRP）

---

## 7. 主生產排程與物料規劃（MPS → MRP → MRP II → ERP → APS）

### 7.1 主生產排程（MPS）
- 由總合計畫展開到具體品項與時段
- 可承諾量（ATP）、時間柵欄（Time Fence）、需求時間柵欄與規劃時間柵欄
- MPS 與訂單允諾（Order Promising）的關係（連結 §17）

### 7.2 物料需求規劃（MRP）
- 三大輸入：MPS、物料清單（BOM）、庫存記錄檔
- 邏輯：毛需求 → 淨需求 → 批量化 → 時間反推（Lead Time Offsetting）→ 逐階展開
- 批量法則：L4L、EOQ、POQ、Silver-Meal、Wagner-Whitin（動態規劃最佳解）
- 系統緊張（System Nervousness）、安全前置時間 vs. 安全存量、低階碼
- MRP 的先天假設缺陷：**固定前置時間、無限產能** → 研究所課程最常拿來討論的破口

### 7.3 能力需求規劃（CRP）與閉環 MRP
- 負荷剖面（Load Profile）、負荷調整與投料控制

### 7.4 MRP II / ERP / MES / APS
- MRP II：把財務、行銷、人力納入同一套計畫循環
- ERP：跨模組交易整合；MES：製造執行層資料回饋
- **APS（先進規劃排程）**：有限產能、同時考慮物料與產能、最佳化引擎驅動
- DDMRP（需求驅動 MRP）：以策略性緩衝點取代純預測推式邏輯

---

## 8. 採購與供應管理（Purchasing & Sourcing）

- 採購在生產管理中的定位：物料成本常占製造業總成本 50–70%，槓桿最大
- **自製或外購決策（Make-or-Buy）**：成本分析、核心能力、產能彈性、技術外流風險
- 策略性採購（Strategic Sourcing）流程：支出分析 → 市場分析 → 尋源策略 → 議價 → 合約 → 績效管理
- **採購組合矩陣（Kraljic Matrix）**：槓桿型 / 策略型 / 瓶頸型 / 一般型物料的差異化策略
- 供應商管理
  - 供應商評選：QCDSM 構面、AHP / TOPSIS / DEA 多準則評估（見 §18）
  - 供應商開發、輔導與稽核；供應商績效計分卡
  - 單一源 vs. 雙源 / 多源策略；供應商早期參與（ESI）
- 採購作業模式：集中 vs. 分散採購、框架合約、電子採購（e-Procurement）、線上競標
- 議價與談判、總持有成本（TCO）而非單價思維
- 前置時間管理：採購前置時間的變異是安全存量的主要驅動因子
- 委外加工（外包工序）管理：工序委外的排程、品質與帳務控管
- 採購風險：斷料、漲價、匯率、地緣政治；長約與避險
- 永續採購：供應商 ESG 稽核、衝突礦產、碳足跡要求（連結 §16）

---

## 9. 存貨管理（Inventory Management）

- 存貨的功能分類：週期存貨、安全存貨、在途存貨、預期存貨、批量存貨
- 確定性模式：EOQ、EPQ（生產批量）、數量折扣模式、Backorder 模式
- 隨機性模式：
  - 連續盤點（Q, R）模式、定期盤點（P, T）模式、（s, S）政策
  - 服務水準：週期服務水準（CSL）vs. 訂單滿足率（Fill Rate）
  - 報童模式（Newsvendor）— 單期決策的原型，也是收益管理的基礎
- 多階存貨（Multi-echelon）與 Clark-Scarf 結構
- ABC / VED 分類、庫存週轉率、循環盤點制度
- 實務制度：VMI、寄售庫存、風險共擔（Risk Pooling）與平方根法則
- 呆滯料（E&O）管理與存貨評價

---

# 三、執行面

## 10. 作業排程與現場管制（Scheduling & Production Activity Control）

### 10.1 排程理論
- 問題分類法 α|β|γ（機器環境 | 限制條件 | 目標函數）
- 機器環境：單機、平行機、流程型工廠（Flow Shop）、零工式工廠（Job Shop）、彈性／開放工廠
- 目標函數：Makespan、總完工時間、延遲工件數、加權延遲、TWT
- 經典結果：SPT 最小化平均流程時間、EDD 最小化最大延遲、Johnson 法則（2 機 Flow Shop）、Moore 法則
- 複雜度：多數 Job Shop 問題為 NP-hard → 依賴啟發式與 metaheuristic
- 實務擴充：整備時間相依（Sequence-dependent Setup）、批次排程、人員與模具等次要資源限制

### 10.2 現場派工與管制
- 派工法則（Dispatching Rules）：FCFS、SPT、EDD、CR、ATC、SLACK
- 投料控制（Input/Output Control）、瓶頸管理、批量分割（Lot Splitting）
- 生產活動管制（PAC）：工單開立、進度追蹤、異常回饋、工時與料帳回報
- 甘特圖、看板、電子派工看板、即時重排程（Rescheduling）與排程穩定性

---

## 11. 生產系統理論：Factory Physics 與變異管理

- 基本參數：產出率（TH）、在製品（WIP）、週期時間（CT）、利用率（u）
- **Little's Law：WIP = TH × CT** — 整個領域最重要的恆等式
- 最佳情況／最差情況／實務情況效能界線，關鍵在製品（Critical WIP）
- 變異的來源與量化：SCV、製程時間變異、流動變異、當機與換模的影響
- 排隊理論：M/M/1、M/G/1、G/G/1 近似（Kingman 公式），利用率趨近 1 時週期時間爆炸
- 變異緩衝法則（Variability Buffering Law）：變異必然由**存貨、產能、時間**三者之一吸收
- 推式 vs. 拉式：MRP（推）、Kanban、CONWIP、POLCA 的比較
- **限制理論（TOC）**：五大聚焦步驟、DBR（鼓—緩衝—繩）、緩衝管理、有效產出會計

---

# 四、改善面

## 12. 精實生產與持續改善

- 豐田生產系統（TPS）兩大支柱：及時化（JIT）與自働化（Jidoka）
- 七大浪費、價值流圖（VSM）、節拍時間（Takt Time）
- 拉式與看板系統設計：看板數量計算、超市（Supermarket）、水蜘蛛
- 平準化（Heijunka）、單件流、快速換模（SMED）、防呆（Poka-yoke）
- 5S、標準作業、現地現物、改善（Kaizen）與 PDCA、方針管理（Hoshin Kanri）
- 精實六標準差（Lean Six Sigma）：消除浪費 + 降低變異的整合
- 精實在非重複性環境（高混低量、MTO）的適用性爭論
- 精實與 Factory Physics 的理論對話：看板本質上是 WIP 上限控制

---

## 13. 品質管理（Quality Management）

- 品質觀念演進：檢驗 → 統計品管（SQC）→ 品質保證（QA）→ 全面品質管理（TQM）
- 品質大師論點：Deming 十四要點與 PDCA、Juran 三部曲、Crosby 零缺點、田口品質損失函數
- **統計製程管制（SPC）**
  - 計量值管制圖（X̄-R、X̄-S、I-MR）、計數值管制圖（p、np、c、u）
  - 管制界限 vs. 規格界限、八大判異準則、管制圖的第一／第二型誤差
  - 製程能力分析：Cp、Cpk、Pp、Ppk、製程績效與六標準差水準
- 量測系統分析（MSA）：Gage R&R、偏倚、線性、穩定性
- 驗收抽樣：AQL、OC 曲線、MIL-STD-105E / ISO 2859、抽樣風險
- **六標準差 DMAIC**：定義 → 量測 → 分析 → 改善 → 管制；DMADV / DFSS
- 品質改善工具：QC 七大手法、新 QC 七大手法、8D、根本原因分析（5 Why、魚骨圖）
- 失效模式分析：DFMEA / PFMEA、風險優先數（RPN）與新版 AP 評級
- 品質成本（COQ）：預防、鑑定、內部失敗、外部失敗成本的權衡
- 品質管理系統與標準：ISO 9001、IATF 16949、APQP / PPAP / MSA / SPC 五大核心工具
- 品質與生產的介面：不良品對有效產能的侵蝕、重工對排程的干擾、供應商來料品質

---

## 14. 設備管理與全面生產保養（TPM）

- 維護策略光譜：事後維護（BM）→ 預防維護（PM）→ 預知維護（PdM）→ 可靠度中心維護（RCM）
- **TPM 八大支柱**：自主保養、計畫保養、個別改善、品質保養、初期管理、教育訓練、事務管理、安全衛生環境
- 自主保養七步驟；設備初期清掃與源頭對策
- **OEE（設備綜合效率）= 時間稼動率 × 性能稼動率 × 良品率**
  - 設備六大損失：故障、換模調整、空轉小停止、速度低下、不良重工、初期良率
  - OEE 的誤用：對非瓶頸設備追求高 OEE 會製造過量生產（連結 §11 TOC）
- 可靠度工程：MTBF、MTTR、可用度（Availability）、浴缸曲線、串並聯系統可靠度
- 備品（Spare Parts）庫存管理：慢速移動件的存量決策
- 保養排程與生產排程的衝突協調：計畫停機的機會成本
- 預測性維護的資料基礎：振動、溫度、電流訊號 → ML 異常偵測與剩餘壽命預測（連結 §19）

---

# 五、外部與整合面

## 15. 供應鏈與物流網路

- 供應鏈結構與 SCOR 模型：Plan / Source / Make / Deliver / Return
- 配銷需求規劃（DRP）、多階配銷網路設計、越庫作業（Cross-docking）
- 運輸模式選擇與路徑規劃（VRP）、第三方物流（3PL）
- **長鞭效應（Bullwhip Effect）**：成因（需求訊號處理、批量訂購、價格波動、短缺賽局）與對策（資訊共享、CPFR、每日低價、配額分配）
- 供應鏈協調契約：批發價、回購、收益共享、數量彈性
- 供應鏈韌性與風險管理：中斷風險、備援產能、安全庫存策略、近岸／友岸外包
- 供應鏈數位化：控制塔（Control Tower）、端到端可視化、區塊鏈履歷

---

## 16. ESG、綠色生產與循環經濟

### 16.1 ESG 與永續治理
- ESG 三構面在製造業的落點：環境（E）排放與資源、社會（S）勞動與供應鏈人權、治理（G）合規與揭露
- 揭露框架與法規：GRI、SASB、TCFD、IFRS S1/S2、台灣永續報告書規範
- 碳盤查與範疇：Scope 1 / 2 / 3（ISO 14064-1）、產品碳足跡（ISO 14067）
- 國際貿易衝擊：歐盟 CBAM 碳邊境調整、客戶端減碳要求下沉至供應鏈
- 供應鏈 ESG 稽核與永續採購（連結 §8）

### 16.2 綠色生產與循環經濟
- 清潔生產（Cleaner Production）與污染源頭減量
- 能源管理：ISO 50001、能源基線、設備能耗監測、尖峰負載管理
- 資源效率：材料利用率、廢料與回料管理、水資源循環、廢棄物減量
- **生命週期評估（LCA）**：從搖籃到墳墓／搖籃，環境衝擊量化
- 環境導向設計（DfE）、可回收性與可拆解性設計（連結 §2）
- 循環經濟 3R/9R：再使用、再製造（Remanufacturing）、再生利用；逆物流網路設計
- 綠色績效指標：單位產值碳排、能源密集度、廢棄物回收率
- 永續與傳統績效的權衡與綜效：減廢常同時是降本（與精實的交集）

---

## 17. 顧客服務與需求端管理

- 顧客服務在生產管理中的角色：生產系統的最終產出是「交付體驗」，不只是產品
- **服務水準定義**
  - 準時交貨率（OTD）、訂單滿足率（Fill Rate）、完美訂單（Perfect Order）
  - 訂單前置時間（Order Lead Time）與交期可靠度（Delivery Reliability）
  - 服務水準協議（SLA）與罰則設計
- **訂單管理流程**：詢價 → 報價 → 訂單允諾（ATP/CTP）→ 排程 → 出貨 → 售後
  - 可承諾量（ATP）vs. 可允諾產能（CTP）
  - 交期報價（Due Date Quotation）：預測交期與排程能力的整合決策
- 需求端管理：訂單接受與拒絕決策、需求塑形（Demand Shaping）、促銷與產能的協調
- 服務作業管理：等候線管理、服務能力與需求匹配、服務品質模式（SERVQUAL）
- 售後服務與備品供應：保固、維修網路、備品存貨（連結 §14）
- 客訴處理與品質回饋迴路：8D 回覆、客訴 → 製程改善的閉環（連結 §13）
- 收益管理（Revenue Management）：有限產能下的訂價與配額決策
- 客製化服務：大量客製化、延遲策略、組態式報價（CPQ）

---

# 六、方法與技術

## 18. 決策方法論工具箱（「決策」這一半的內容）

| 方法族 | 代表工具 | 典型生管應用 |
|---|---|---|
| 數學規劃 | LP、MILP、非線性規劃 | 總合計畫、批量排程、網路設計 |
| 動態規劃 | Wagner-Whitin、Bellman 方程 | 動態批量、設備汰換、存貨政策 |
| 隨機模式 | 馬可夫鏈、排隊論、報童模式 | 產線可靠度、產能與週期時間分析 |
| 不確定性最佳化 | 隨機規劃、強健最佳化、分散式強健最佳化 | 需求不確定下的產能與排程決策 |
| 啟發式 / Metaheuristic | GA、SA、Tabu Search、ACO、NSGA-II | Job Shop 排程、多目標最佳化 |
| 模擬 | 離散事件模擬、蒙地卡羅、Agent-based | 產線瓶頸分析、What-if、政策驗證 |
| 多準則決策 | AHP、ANP、TOPSIS、DEA、VIKOR、灰關聯 | 供應商評選、設備／技術方案評估 |
| 實驗設計 | DOE、因子實驗、反應曲面、田口方法 | 製程參數最佳化、良率提升 |
| 資料驅動 | 機器學習預測、深度強化學習（DRL） | 動態排程、預測性維護、即時決策 |
| 賽局與行為 | 賽局理論、行為作業（Behavioral Ops） | 供應鏈契約、人為決策偏誤（如報童偏誤） |

> 研究所課程的真正分水嶺：不只是會算，而是能**選對模式、說明假設、評估解的穩健性**。

---

## 19. 智慧製造與 AI 於生產管理

### 19.1 架構與系統層級
- 工業 4.0 架構：CPS（虛實整合系統）、IIoT、邊緣／雲端運算、5G
- 系統層級：ERP（企業）→ APS（規劃）→ MES（執行）→ SCADA/PLC（設備）
- 資料基礎建設：產品與製程履歷追溯、資料品質、MES–ERP 資料一致性、統一命名空間

### 19.2 數位分身（Digital Twin）
- 層級：機台 / 生產線 / 廠級 / 供應鏈
- 功能分類：監控（Monitoring）、預測（Prediction）、最佳化（Optimization）、控制（Control）
- 與模擬的差異：即時資料連動與雙向回饋

### 19.3 AI 與生產管理的結合點
- 需求預測與價格預測
- 預測性維護：異常偵測、剩餘使用壽命（RUL）預測
- 品質：AOI 視覺檢測、缺陷分類、製程參數與良率的因果分析
- 排程：深度強化學習（DRL）動態排程、與最佳化引擎的混合式架構
- 供應鏈：風險預警、補貨決策自動化
- 生成式 AI 在製造的應用：知識萃取、SOP 生成、工程對話介面、Agent 化決策輔助
- **導入陷阱**：資料品質不足、模型可解釋性、與既有排程邏輯衝突、人員信任與採用

### 19.4 導入與變革
- 投資報酬評估與試點選題、成熟度評估（如 SIRI）
- 人機協作與工作設計、技能轉型
- 資安（OT Security）與系統韌性

---

## 20. 績效衡量與整合議題

- 績效指標體系：成本、品質、交期（OTD）、彈性、生產力、OEE、週期時間、庫存週轉
- 平衡計分卡、SCOR 模型、KPI 之間的取捨與衝突（局部最佳 vs. 系統最佳）
- 成本會計介面：標準成本、作業基礎成本制（ABC）、有效產出會計（TA）
- 大量客製化（Mass Customization）、延遲策略（Postponement）、模組化設計
- 韌性（Resilience）與敏捷性（Agility）作為新的競爭優先序
- 製造業服務化（Servitization）：從賣產品到賣結果

---

## 附錄 A：核心經典與教材

| 類別 | 書目 |
|---|---|
| 中文主教材 | 林則孟《生產計畫與管理》，華泰 |
| 系統理論 | Hopp & Spearman, *Factory Physics* |
| 排程理論 | Pinedo, *Scheduling: Theory, Algorithms, and Systems* |
| 存貨與供應鏈 | Silver, Pyke & Thomas, *Inventory and Production Management* |
| 供應鏈 | Chopra & Meindl, *Supply Chain Management* |
| 設施規劃 | Tompkins et al., *Facilities Planning*；Muther, *Systematic Layout Planning* |
| 產品開發 | Ulrich & Eppinger, *Product Design and Development* |
| 工作研究 | Niebel & Freivalds, *Methods, Standards, and Work Design* |
| 品質管理 | Montgomery, *Introduction to Statistical Quality Control* |
| TPM | Nakajima《TPM 入門》 |
| 作業管理通論 | Stevenson / Heizer & Render, *Operations Management* |
| TOC | Goldratt《目標》(The Goal) |
| 精實 | Womack & Jones《精實革命》、今井正明《現場改善》 |
| 專業認證 | ASCM/APICS CPIM Body of Knowledge（8 模組） |

## 附錄 B：主要期刊

Management Science、Operations Research、Production and Operations Management (POM)、Journal of Operations Management (JOM)、International Journal of Production Research (IJPR)、International Journal of Production Economics (IJPE)、Journal of Intelligent Manufacturing、Computers & Industrial Engineering、Journal of Cleaner Production（永續方向）

## 附錄 C：ASCM/APICS CPIM 八大模組（實務界的知識骨架）

1. 供應鏈與策略
2. 銷售與作業規劃（S&OP）
3. 需求管理
4. 供給管理
5. 細部排程
6. 存貨管理
7. 配銷
8. 品質、技術與持續改善

---

## 參考來源

- 國立清華大學 OCW「生產計畫與管制」課程大綱 — https://ocw.nthu.edu.tw/ocw/index.php?page=course&cid=136
- 元智大學工業工程與管理學系 產業電子化與生產管理實驗室「高等生產管制」 — http://e-enterprise.iem.yzu.edu.tw/
- 國立臺灣科技大學工業管理系研究領域說明 — https://www.techadmi.edu.tw/depinfo.php?seq=108
- 國立臺灣大學 OCW「作業管理」 — https://ocw.aca.ntu.edu.tw/ntu-ocw/ocw/cou/101S205
- POMS Journal Departments（研究領域分類） — https://www.poms.org/journal/review_board
- ASCM APICS CPIM 認證知識體系 — https://www.ascm.org/cpim-certification/
- Factory Physics (Hopp & Spearman) 章節架構 — https://www.waveland.com/browse.php?t=587
- Reinforcement learning in dynamic job shop scheduling: a comprehensive review — https://link.springer.com/article/10.1007/s10845-025-02585-6
- Digital twin driven factory and production planning (FPP) — https://www.tandfonline.com/doi/full/10.1080/21693277.2025.2507954
- AI-Driven Digital Twins for Manufacturing: A Review Across Hierarchical Manufacturing System Levels — https://www.mdpi.com/1424-8220/26/1/124
