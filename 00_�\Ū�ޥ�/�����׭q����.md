# 00_閱讀技巧 · 版本修訂紀錄 (Changelog)

> 本文件記錄「00_閱讀技巧」自建立以來的每一次版本修訂時間與具體功能變更。
> **最新修訂紀錄永遠保留於最上方**。每次後續修訂網頁時，均同步增補本記事本。

---

### [2026-09-09 19:16] · v1.4：閱讀技巧母子網頁架構重構（母網頁導航中心 ＋ 3 個獨立策略子網頁資料夾）
* **重構為「母網頁導航中心 ＋ 3 個獨立策略子資料夾」階層式體系**：
  - 母網頁 `00_閱讀技巧/00_閱讀技巧.html`：扮演策略總覽導航中心，具備：
    - 策略總覽 Hero 導航橫幅。
    - 3 大策略垂直/響應式專屬卡片（策略 01、02、03），快速直通子頁面。
    - 三大閱讀策略綜合對比矩陣表（適用大考題型、核心視覺信號詞、解題秒殺思維）。
    - 近 10 年技高統測閱讀篇章與三大策略對照分布表（無人機、咖啡豆、泡麵、腳踏車、海洋噪音、都市農業）。
    - 隨視口懸浮查詞 HUD（2,524 字詞庫）與桌機/手機排版雙向切換支援。
  - 子資料夾 01 `01_時間標記與時態演進/`：
    - `01_時間標記與時態演進.html`（獨立即開即用，含心法、示範課文第 1 段、隨堂測驗、4 篇統測真題無人機/咖啡豆/泡麵/腳踏車）。
    - `_redirects`（支援 Cloudflare Pages 根路由）。
    - `使用說明.md`（完整功能與部署導引）。
  - 子資料夾 02 `02_主題句與漢堡段落結構/`：
    - `02_主題句與漢堡段落結構.html`（獨立即開即用，含心法、獨創漢堡模型連動圖、示範課文第 2 段、隨堂測驗、2 篇統測真題海洋噪音/都市農業）。
    - `_redirects`。
    - `使用說明.md`。
  - 子資料夾 03 `03_邏輯轉折詞與語意關係/`：
    - `03_邏輯轉折詞與語意關係.html`（獨立即開即用，含心法、四大邏輯信號詞矩陣、示範課文第 4 段、隨堂測驗、113 統測真題海洋噪音層遞邏輯）。
    - `_redirects`。
    - `使用說明.md`。
* **零特定校名、純個人教學研發資產規範**：
  - 全數網頁、註解、文檔 100% 遵守隱私規範，無任何特定學校校名。
* **嚴格通過「防回歸自主檢核」三重防禦與無頭瀏覽器驗證**：
  - 通過 `verify_interactive_pages.py` 全項契約檢核（HTML 標籤、事件綁定、TTS 速度選單浮點容錯、隨視口 HUD 辭庫、Edge Chromium Headless DOM 載入 100% PASS）。

---

### [2026-09-09 15:40] · v1.3：100% 原始雜誌課文一字不差還原 ＋ 嚴格落實「僅關鍵詞上背景色，句子完全零底色」
* **100% 還原《A+ 雜誌》9 月號 Unit 1 原版課文**：
  - 完整採用雜誌第 10～11 頁之原始散文段落，嚴禁任何自定義改寫或潤飾：
    - **第 1 段**：*A techou is a small notebook for recording daily life. It dates back to the 1810s in the UK. At that time, merchants carried small notebooks to record goods in stores. Around the 1880s, people in Japan began to use techou for daily notes. It soon became popular across Japan and later around the world!*
    - **第 2 段**：*A techou is helpful in many ways. By listing things to do, people can make good use of time. Habits like sleep hours or exercise also become easy to track. What’s more, it helps people set plans and reach goals step by step. In fact, a techou welcomes all kinds of notes!*
    - **第 3 段**：*To make your own techou, start by choosing a page style. Monthly or weekly pages are good choices for planning time. For a flexible style, you can pick blank or grid pages. Today, techou books usually come with both, so you can plan and write freely.*
    - **第 4 段**：*A techou is not just for writing—it’s also a place to show creativity. For example, different pen colors help organize things to do by importance. You can decorate your techou with stickers, stamps, or washi tape. You can also put photos or movie tickets inside to remember special moments. With all these ideas, why not start making your own techou today?*
* **嚴格落實「僅關鍵字上視覺線索背景色，句子完全零背景色」**：
  - 所有句子樣式強制套用 `background: transparent !important;`，徹底根除整行色塊造成的視覺混亂與壓迫感。
  - 線索開啟時，相關句**僅以乾淨俐落的虛線底線**標示結構。
  - **全篇僅有核心關鍵字**（如 `the 1810s`、`carried`、`the 1880s`、`helpful in many ways`、`also`、`What's more`、`not just... also`、`For example`）套用柔黃高亮底色（`background: #fef08a; border-bottom: 2px solid #ca8a04;`），版面極致純淨清晰。
* **詞庫與隨視口查詞 HUD 擴充至 2,524 字**：
  - 同步納入課文內 `washi tape`、`grid`、`goods`、`merchants`、`creativity`、`flexibility` 等原版詞彙，點詞查詞 100% 覆蓋。

---

### [2026-09-09 15:30] · v1.2：閱讀策略教學系統深度重構（垂直堆疊選單、線索預設關閉盲測、策略心法先行、空中美語雜誌授權聲明、底線+關鍵字背景色、漢堡段落模型圖、獨立頁面零干擾）
* **垂直堆疊策略研習選單（Vertical Stacked Menu Cards）**：
  - 徹底移除橫向溢出滑動條，將 4 大模組（技巧01、技巧02、技巧03、統測真題）改為行動端最友善的垂直卡片排列，一覽無遺絕不漏看。
* **考點視覺線索預設關閉（Default Clues OFF for Blind Testing）**：
  - 進入頁面預設為紙本大考盲測模式（`cluesVisible = false`），學生點擊「💡 考點視覺線索：關閉中」才主動喚醒彩色引導。
* **策略心法深度剖析先行（Theory-First Pedagogy）**：
  - 篇章前完整配置【策略核心概念】、【⚡ 統測秒殺判讀口訣】與【🔑 高頻關鍵信號詞庫】（點擊發音與查詞），先扎根心法再進入 Techou 實戰。
* **空中美語雜誌版權與教學使用聲明**：
  - 篇章上方正式標註：本示範篇章節選改編自《A+ English 空中美語》2026年9月號，版權屬於空中美語雜誌社；本文僅作為個人教學研究與學生學習之用，無商業營利用途。
* **極簡清爽視覺標記（Underline-Only Sentences & Highlight Signals）**：
  - 徹底告別整句色塊造成的擁擠感，相關句一律採用「乾淨虛線底線」；僅核心關鍵字（如 `In the 1810s`, `also`, `What's more`）享有「柔黃底色 ＋ 深黃底線」高亮。
* **技巧02互動式「漢堡段落架構圖」(Interactive Hamburger Paragraph Model)**：
  - 獨創互動漢堡圖（🍔 頂層麵包：主題句 ➔ 🥬 夾心餡料：支持細節 ➔ 🍞 底層麵包：結論句），點擊各層可即時連動並平滑捲動至文章對應句子。
* **各技巧獨立專頁視圖（Isolated Skill Views）**：
  - 技巧01、02、03 與統測真題各自具備獨立頁面，完全隔離非相關線索，徹底消除跨策略之色彩與標記干擾。
* **統測真題與隨堂測驗全套比照**：
  - 113 最新年份真題、追加真題及隨堂題庫全面遵循上述乾淨線索、預設關閉、點詞查詞 HUD 與真人語音規範。

---

### [2026-09-09 15:00] · v1.1：統測佐證真題專區全面升級（最新年份優先 113➔108、真題篇章考點視覺顯色、點句彈出解構視窗、點詞即顯 HUD、動態追加真題功能）
* **最新年份優先排序（Reverse-Chronological Provenance）**：
  - TVE 佐證篇章全面重整為以「最新大考優先」排序：
    1. **113 統測 Q26~30《海洋噪音對鯨豚生態的威脅》**（技巧 #02 主題句結構 ＋ 技巧 #03 First / In addition / What's more / Therefore 轉折層遞）
    2. **113 統測 Q31~35《無人機配送技術的發展演進》**（技巧 #01 In the 2010s / In 2016 / Today 歷史時間軸演進）
    3. **112 統測 Q31~35《都市農業的興起與三大益處》**（技巧 #02 主題句 ➔ First / also / What's more 支持細節 ➔ Clearly 結論句）
    4. **111 統測 Q26~30《咖啡豆的起源與跨世紀傳播》**（技巧 #01 9th century / 15th century / 17th century 跨世紀歷史時間軸）
    5. **110 統測 Q31~35《泡麵的誕生與全球食品革命》**（技巧 #01 late 1950s / In 1958 / Later in 1971 歷史發明演進）
    6. **108 統測 Q26~30《腳踏車的誕生與踏板演進》**（技巧 #01 In the 1810s / Later in the 1860s 年代發展）
* **互動式考點重點顯示功能（Interactive Clue Highlights & Popover）**：
  - 統測佐證真題篇章完整支援視覺線索彩色顯色（紫色時間軸、藍色主題句、綠色轉折詞、粉色結論句）。
  - 點擊任一句子自動平滑捲動置中並滑出底端「懸浮線索說明卡」，內含【考點彩色膠囊標籤】、【統測考點深度解構】、【整句繁體中文翻譯】與【🔊 朗讀整句】。
* **隨視口動態查詞 HUD 全篇貫穿（Tap-to-Lookup HUD）**：
  - 統測真題中所有英文單詞皆已封裝支援點擊查詞，點擊即浮現繁體中文詞義、詞性與發音，辭庫擴增至 2,507+ 字。
* **動態追加統測真題控制台（Dynamic Append Console）**：
  - 預設先展示最新 3 篇（113、113、112），並於底部配置「➕ 追加更多統測佐證篇章（從 113 往前回溯）」按鈕，學生可一鍵無限拓展對比 111、110、108 年之相同篇章架構。

---

### [2026-09-09 14:40] · v1.0：全系統首發上線（以 9 月 A+ 雜誌 Techou 為原型 ＋ 三大核心策略 ＋ 10年統測真題佐證 ＋ 模組化擴充選單）
* **建置背景與教學目標**：
  - 協助高職學生掌握高中英閱三大通用策略：【時間線索與時態】、【主題句與段落結構】、【邏輯轉折詞解讀】。
  - 整合多模態視覺線索開關、底端懸浮解構視窗、2,364+ 字隨視口查詞 HUD、真人 TTS 美式朗讀與永遠置底無限適性題庫。
* **主要功能模組與技術架構**：
  1. **示範篇章與連貫段落設計（Continuous Prose）**：
     - 以 9 月號《A+ 雜誌》日式手帳篇章為原型，完整重現 4 大段落，嚴禁碎片化折行。
  2. **三大閱讀技巧視覺線索與底端懸浮視窗（Floating Clue Popover）**：
     - 🟪 **紫色（`clue-timeline`）**：1810s、1880s 過去年代與過去式動詞標記。
     - 🟦 **藍色（`clue-topic`）**：首句主題句 (*A techou is helpful in many ways.*)。
     - 🟧 **暖琥珀（`clue-details`）**：具體支持細節與操作步驟。
     - 🟩 **綠色（`clue-transitions`）**：*also*、*What's more*、*not just... also*、*For example* 關鍵轉折詞。
     - 🟪 **柔粉色（`clue-conclusion`）**：段落末端總結結論句。
     - 點擊任一線索句平滑捲動置中，底端優雅滑出懸浮卡，包含考點彩色膠囊標籤、深度解構、整句中譯與獨立朗讀。
  3. **近 10 年統測閱讀測驗相同架構佐證專區（TVE Exam Provenance）**：
     - **108統測Q26~30《腳踏車演進史》**（佐證時間年代與過去式發明篇章）。
     - **112統測Q31~35《都市農業興起》**（佐證首句主題句 ➔ 支持細節 ➔ 結論句）。
     - **111統測Q16~20《植物性飲食與環境》**（佐證 *not just... also*、*For example* 轉折詞因果判讀）。
  4. **全套標配功能完備支援**：
     - 內建 2,364+ 字完整繁中辭庫，隨視口動態懸浮查詞 HUD 點詞即顯。
     - 4 階字級放大（A / A+ / A++ / A+++）與行動/桌機排版切換。
     - 無限適性追加題庫（三級難度），詳解必附整句中譯與誘答陷阱掃除卡。
     - 模組化閱讀策略選單，便於未來隨時整合技巧 #04、#05... 等新策略。
