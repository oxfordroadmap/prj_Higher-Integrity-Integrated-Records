

* [en] Project: Governance of Academic Research Integrity ─ Records and Audits
* [zh-t] 專案：學術倫理治理 ─ 記錄審計
# [專案名稱/案件編號]：學術倫理治理 ─ 記錄審計
* ***Case ID:** 2026-RCM-001
* 中文: 
	* **研究者/記錄者/陳情人**: [您的名字或代號]
	* **目標機構**: [機構全名]
	* **目標計畫/單位**: [相關系所或計畫名稱]
	* **主管機關**: [如：教育部高教司]
* English: 
	* **Researcher/Auditor/?:** [您的名字或代號]
	* **Target Institution:** [機構全名]
	* **Target Program:** [相關系所或計畫名稱]
	* **Supervisory Authority**: [如：中華民國教育部 (Ministry of Education, Taiwan) ]

---
## 元文檔說明

> 這份標準化的 `README.template.md` 將「學術倫理治理」中的「記錄審計」邏輯抽象化設計為通用框架。任何研究者、碩博學生或科研人員若遭遇學術倫理、科研倫理（RCM, Research Lifecycle Management）或行政程序問題，皆可直接 Fork 本項目填入自己的個案數據，以數位科技維護自身學術誠信與權益。
---

## 1. 專案說明 Project Description

本專案為「學術倫理治理」行政程序之行動研究（Action Research）的基礎「記錄審計」，有以下特點。

1. **生命週期管理**：本專案採用**科研生命週期管理**（Research Lifecycle Management, RCM）的角度，系統化檢視學術生命週期中的數據軌跡，以支持學術倫理、學術誠信與行政風險控制等治理目的。 
2. **行政程序數字轉型**：本專案整合應用 **GitHub 版本控制平台**、**Markdown 文檔體系**（含文本間相對路徑鏈結與數據可視化）以及**數位證據防護技術**，協助記錄者精確追蹤行政往來軌跡。
3. **數據溯源及數據治理**：透過此架構，本專案利用數據溯源（Data Provenance）技術，確保關於學術倫理、科研倫理或行政程序的損害既遂、救濟程序及機關回覆，皆能轉化為中立、可稽核且具備結構化特性的數據，進而優化高教環境的數據治理（Data Governance）。
4. **公開及個人記錄**：本專案可採 **[公開 Public / 機構 Internal / 個人 Private]** 紀錄方式（請依設定自行標記）。
5. **數位手段及事實對齊**：使用者可透過 GitHub Repository 的權限設置，靈活切換公開範圍，並利用 `Fork`、`Pull Request` 等分布式版本控制工具，接受利害關係人或調查單位提出記錄更新與事實對齊之要求。

## 2. 檔案結構 Directory Structure

本儲存庫之檔案結構係依據行政審計與數據溯源標準規劃，以確保紀錄之完整性與可稽核性：

```text
/
├── README.md                    # 本說明文件
├── /Stakeholders/               # 利害關係/職位角色矩陣與責任定義
│   ├── Stakeholders.md            # 參與本案之組織職位說明
│   └── _Roles_Mapping.md          # 依據教育部規章之權責對應
├── /Logs/                       # 行政往來與反應日誌 (Timeline)
│   ├── YYYY-MM-DD.md              # 每日/每次事件之行政紀錄
│   └── _Governance_Log.md         # 行政程序時序總表 (含甘特圖)
├── /Evidence/                   # 證據庫 (Metadata & Audit)
│   ├── README.md                  # 存取權限說明
│   └── _Evidence_Index.csv        # 證據索引表 (包含 SHA-256 Hash)
├── /Analysis/                   # 治理程序分析
│   └── Admin_Proc_Audit.md        # 程序符合性分析
└── /Proposals/                  # 建議事項
    └── Settlement_Framework.md    # 和解與調查建議框架
```

## 3. 記錄及使用方式 (Usage Guide)

本專案採用「版本控制」進行行政存證。使用者遭遇事件時，應即時將公文、信件或通訊紀錄轉為數位檔案，存入 `/Evidence/` 並計算 Hash 值；隨後於 `/Logs/` 建立以日期為檔名之 Markdown 紀錄，並透過相對路徑與 `/Stakeholders/` 之職位互連。若行政狀態變更，須同步更新本頁儀表板，並透過 `git commit` 固定時間戳記。

### 利害關係/職位角色 Stakeholders

本專案拒絕流於個人恩怨之爭辯，核心聚焦於「職位權責」。本模組（詳見 [./Stakeholders/Stakeholders.md](./Stakeholders/Stakeholders.md)）將以下要素進行矩陣整合與交叉定位：

- **行政程序法要件**：依據《行政程序法》及《[教育部處理人民陳情案件作業規定](https://edu.law.moe.gov.tw/LawContent.aspx?id=FL051320)》，界定「行政違失之舉發」與「行政權益之維護」之法定義務。
- **科研生命週期 (RCM) 行為角色義務**：界定研究數據生成、論文署名、博士學位申請等節點之行為人義務。
- **權責矩陣定義**：將上述兩者結合，明晰特定職位（如研發處長、博班主任、學倫案件承辦人）在特定時間點應作為而不作為之行政責任。

### 行政往來與反應日誌 Admin Audit Log 

下表紀錄本案之關鍵行政事件，完整時序、行政週期延遲與甘特圖數據可視化，請參見 [./Logs/Governance_Log.md](./Logs/Governance_Log.md) 。

| **日期** Date | 描述 **Event Description** | 關係人 **Stakeholders**   | 狀態 **Status** |
| ----------- | ------------------------ | ---------------------- | ------------- |
| 2026-03-XX  | 初次提出科研產權爭議               | Program Director       | Pending       |
| 2026-05-XX  | 送達最後期限通知                 | R&D Office Coordinator | Expired       |
| 2026-05-21  | 國際學術審查受理通知               | IAFOR Administration   | Accepted      |

提示：當目標機構發生行政逾期、沈默或程序拒絕時，應於此表即時更新對應狀態（如 `Expired` 或 `Effective obstruction`）。

### 證據庫元數據 (Evidence Metadata & Access Control)

所有存於 `/Evidence/` 下之檔案均已完成數位指紋登記，以供主管機關（教育部）進行實質事實核對。完整清單請參見 [./Evidence/Evidence_Index.tsv](./Evidence/Evidence_Index.tsv)。

- **存取權限** (Access Control): 鑑於原始檔案包含個人敏感資料，為兼顧公共利益與隱私保護，原始物證不對外公開，僅限相關法定行政調查單位（如教育部高教司、校內學術倫理委員會）進行實質稽核時依法調取。
- **真實性驗證** (Verification): 所有檔案均附帶 `SHA-256` 雜湊值。任何第三方調閱檔案時，可透過 Hash 比對確保檔案自存證那一刻起未經任何後續竄改或變造。

### 公開聲明 (Open Statement)

> **中文聲明**：本專案所載內容均為公開事實與行政往來紀錄之匯整。本人以研究者身份，針對「科研誠信」與「行政程序法」之執行情形進行客觀紀錄。相關資料將持續同步彙整並呈報至教育部高教司，作為學術行政程序合法性與妥適性之查核參考。本專案旨在維護高教公共利益與科研倫理，過程嚴格保護個人隱私，拒絕任何非關職權之私怨揭露。

> **English Statement**: This repository serves as an administrative audit log for action research purposes. No personal names are disclosed within the documentation; only official roles, institutional capacities, and organizational units are identified to ensure procedural clarity, legal compliance, and institutional accountability. All data provenance records are maintained under strict cryptographic validation to assist regulatory reviews.

### 技術與戰術提示 (Technical & Strategic Notes)

1. **GitHub Markdown 互連**：本儲存庫全面採用相對路徑（Relative Paths）。您可以直接將文件中的鏈結（如 `[行政紀錄](./Logs/_Governance_Log.md)`）替換為實際的路徑，實現網狀互連（Backlinks），在導航時自動對齊脈絡。  
2. **中性語言防禦**：本文件庫在數據記錄與事實陳述中，**嚴格避開**「惡意」、「故意」、「欺騙」、「無恥」等主觀情緒或道德評判詞彙；僅使用「紀錄」、「受理」、「期限」、「權責」、「行政沈默」、「不作為」等中性行政與法律術語，確保在行政訴訟與救濟程序中具備無懈可擊的專業度。
3. **時間向度與週期衝突**：本項目在數據呈現上採用數據可視化，重點突顯「科研週期（如研討會投稿截止、論文發表）與行政週期（如公文展延、行政拖延）」之間的緊張關係。透過拉出時間差，能向主管機關清晰證明「機構之行政怠惰如何具體導致科研產權在國際上發生既遂損害」。
4. **可擴張性與 AI 數據治理**：本文件庫採用高度結構化的 Markdown 與 CSV 形式，不僅支持「同據各表（同一套數據，多方解讀）」，更在引進「AI 智能助手」或自動化審計工具時，能完美優化數據溯源（Data Provenance），讓 AI 能夠快速讀取、生成圖譜並判讀體制性失能（Data Governance）。
5. **證據鏈架構與行動賽局**：傳統框架多採 `Evidence-Claims（證據-主張）` 的平面結構，易流於口水戰。本專案升級為基於日誌的 **`Evidence-Analysis-Proposals（證據-分析-提案）` 縱深架構**，並輔以**多方利害關係人分析（Multi-stakeholder Analysis）**。此架構直面當前高等教育中，投機者利用「行政程序與制度盲點」打擊「學術誠信」的實踐問題。透過本工具，研究者得以將「**學術品牌、國際信譽、法律攻防、及行動賽局**」整合為一體，建立不可逆的制度問責鏈。


# 行動研究註記 Action Research Note

這份模板已經將「學術誠信」「學術倫理」及「學術績效」博弈思維的相關的概念（行政賽局、損害既遂、AI 數據治理、中性語言）完全文字化與數位化。
