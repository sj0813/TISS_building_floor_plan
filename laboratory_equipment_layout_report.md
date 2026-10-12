# 國家運動科學中心大樓新建工程 — 核心實驗室設備配置與模組化測力板地坪機構設計報告

本報告依據**內政部國土管理署**與**啟達聯合建築師事務所**最新審定之建築細部設計圖說（115年9月17日版），以及《1150917-新大樓空間設備調查表-科研版》設備規格，針對 **3 處核心實驗室** 進行詳細的設備平面配置標記、空間機能分區，並特別針對 **1F 虛實整合實驗室之 14~16 cm 運動木地板與 60×60 cm / 60×120 cm 模組化活動測力板（Force Plate / Fake Plate Swappable System）** 提供深入的結構斷面與工程整合設計。

---

## 核心實驗室總覽與配置對照表

| 項次 | 實驗室名稱 | 樓層/編號 | 面積 | 核心定位與機能分區 | 關鍵設備配置標記 | 結構/地坪特殊工法 |
| :--- | :--- | :---: | :---: | :--- | :--- | :--- |
| **1** | **虛實整合實驗室**<br>*(動作模擬、AI動作分析、虛擬運動測試場)* | **1F<br>[117]** | **300 m²** | 1. 動作捕捉捕捉區 (Capture Volume)<br>2. 數位分身虛擬投影區 (Omniverse Wall)<br>3. 受試者準備與肌電區 (EMG Station)<br>4. 運算控制與中央主控台 (Control Desk) | • Vicon Vantage V8 (12鏡頭陣列)<br>• OptiTrack PrimeX 22 (8鏡頭陣列)<br>• AMTI/Kistler 測力板 (60×60 / 60×120)<br>• Delsys Trigno 16ch 無線肌電圖<br>• NVIDIA RTX 6000 Ada GPU 運算機櫃 | **14~16 cm 模組化高架運動木地板**<br>• 60×60 cm 活動木質填補板 (Fake Plate)<br>• 測力板直立剛性置於混凝土平整基底<br>• 2~3 mm 彈性減震隔離縫 |
| **2** | **運動面層實驗分析室**<br>*(運動地板、運動草皮等)* | **2F<br>[209]** | **80 m²** | 1. 面層衝擊與安全測試區 (Impact/Skid Area)<br>2. 材料力學萬能試驗區 (Instron UTM Area)<br>3. 耐候光老化環境實驗區 (Weathering Area)<br>4. 樣品陳列與數據工作站 (Console) | • 衝擊吸收落錘系統 (Triple-A / Berlin)<br>• 擺錘式防滑/摩擦係數儀 (EN 13036-4)<br>• 草皮旋轉阻力測定儀 (EN 15301-1)<br>• 雙柱萬能材料試驗機 (Instron 3400)<br>• Xenon 氙燈耐候機 + QUV 螢光機 | **格子樑 (Waffle Slab) 結構減震區**<br>• 嚴格抑制衝擊落錘垂直諧振<br>• 380V/220V 三相四線重電力<br>• 耐候機專屬 RO 純水給水與重力排水 |
| **3** | **多功能鷹眼技術開發實驗室**<br>*(含挑高鷹眼模擬區)* | **3F<br>[305]** | **315 m²** | 1. 高速軌跡飛行通道 (18m Flight Lane)<br>2. 高速光學鷹眼攝影矩陣 (Truss Array)<br>3. 3D 立體空間標定校正架 (Calibration)<br>4. 研發演算法與判決控制台 (Hawk-Eye Dev) | • 8× Photron / Basler 高速工業攝影機<br>• 1000 Lux 無頻閃 5000K 高演色照明矩陣<br>• 雙 Intel Xeon + RTX GPU 軌跡演算伺服器<br>• 高張力防撞防球護網系統 | **挑高空間設計 + 格子樑結構減震區**<br>• 柱線 3~4 軸大跨距淨高挑高<br>• 消除高樓層微幅晃動，確保立體視覺三角測量之亞毫米級精度 |

---

## 一、1F 【117】虛實整合實驗室 — 設備配置與模組化測力板工程

### 1.1 實驗室設備平面配置圖 (Equipment Layout Plan)
![1F 虛實整合實驗室設備平面配置圖](C:/Users/00054/.gemini/antigravity/brain/2da235a0-35f9-41c6-96ab-010e9b49e912/lab_1f_equipment_layout.png)

### 1.2 14~16 cm 運動木地板與 60×60 cm / 60×120 cm 模組化測力板地坪機構詳圖
![模組化測力板與14~16cm木地板互換機構工程斷面圖](C:/Users/00054/.gemini/antigravity/brain/2da235a0-35f9-41c6-96ab-010e9b49e912/force_plate_modular_floor_section.png)

### 1.3 測力板與活動木假板 (Fake Plate) 模組化置換機制詳解

> [!IMPORTANT]
> **生物力學測力板之安裝核心原則**：測力板本體**絕對不可直接鎖固於彈性木地板的面層或龍骨上**，否則運動員跳躍奔跑時木地板產生的彈性波與振動諧波將傳導至三軸向測力傳感器，造成垂直力 \(F_z\) 與水平剪力 \(F_x, F_y\) 產生嚴重假影（Artifacts）。

1. **結構基底與高程匹配**：
   - **平整混凝土基底 (Level Concrete Floor)**：結構體打底時以自流平水泥（Self-leveling Mortar）精確找平，水平公差控制在 $\pm 1\,\text{mm}$ 以內。
   - **木地板高度 (Finished Floor Height, FFH)**：整體運動彈性木地板系統總厚度設計為 **140 ~ 160 mm**（含 22mm 楓木面層、24mm 雙層耐水夾板基層、80~100mm 雙向實木龍骨及 14mm 彈性避震墊彈性腳座）。
   - **測力板高度匹配 (Force Plate Assembly)**：
     - 標準三維測力板（如 AMTI OR6-7 或 Kistler 9287C）本體厚度約為 50 mm。
     - 底座配置厚度 90 ~ 110 mm 之**重型鋼製精密調平基座（Heavy-duty Steel Leveling Baseplate / Mounting Pedestal）**，搭配微調螺栓與水平儀，使測力板頂面與木地板表面維持於同一絕對水平基準線（齊平公差 $\le 0.5\,\text{mm}$）。
2. **60 × 60 cm 棋盤式活動模組化設計**：
   - 步態與跑跳測試走道區域（長約 12 公尺、寬約 2.4 公尺）全面規劃為 **$60\,\text{cm} \times 60\,\text{cm}$ 矩陣式可拆卸木質填補板（Fake Dummy Plates）**。
   - **狀態 A：一般運動地板狀態（裝設活動假板）**
     - 當該區塊無測力板時，放入特製 60×60 cm 假板，其表面木紋與周邊地板一致，底層以副龍骨框架穩固支承，運動員跑步踏過無任何異音與落差。
   - **狀態 B：測力板量測狀態（取出假板，置入測力板）**
     - 取下 60×60 cm 假板後，直接將 60×60 cm 測力板單元安放在平整混凝土基座上。
     - **60 × 120 cm 組合模式**：若需進行衝刺步態、跨步或起跳等大步幅測試，可連續拆除兩塊相鄰之 60×60 cm 假板，置入單塊 60×120 cm 雙步測力板（或將兩塊 60×60 cm 測力板無縫並聯）。
3. **2 ~ 3 mm 物理隔振縫 (Acoustic & Vibration Isolation Gap)**：
   - 測力板四周金屬邊緣與木地板邊界之間，預留 **2 ~ 3 mm 氣隙**，外覆抗老化矽膠防塵唇封（Flexible Silicone Lip Seal）。
   - 確保木地板受壓下陷變形時，不與測力板發生任何剛性接觸或擠壓摩擦。
4. **地下纜線管道槽 (Cable Trench)**：
   - 混凝土基底預埋 $100\,\text{mm} \times 50\,\text{mm}$ 鍍鋅走線槽，訊號線（Amphenol / BNC）由測力板底部穿出走線，直通側邊控制台 DAQ 擷取箱，完全隱蔽且防止被踩踏破損。

### 1.4 其他核心設備配置說明
- **光學動捕相機桁架 (Camera Truss)**：沿挑高空間上方吊掛矩形桁架，懸掛 12 台 Vicon Vantage V8 與 8 台 OptiTrack PrimeX 22，鏡頭角度呈 360° 環狀交錯聚焦點於中央測力板捕捉區（$8\,\text{m} \times 5\,\text{m} \times 3\,\text{m}$ 標定體積）。
- **Omniverse 數位分身沉浸式投影牆**：設置於東側牆面（寬 8.0 m、高 3.5 m），搭配超短焦高流明工程投影機與被動 3D 偏光系統，由 RTX 6000 Ada GPU 即時驅動運動員虛擬骨架與互動場景。
- **中央控制台與受試者準備區**：配置於西側入口處，包含 Delsys Trigno 16 通道無線肌電充電底座、貼片準備床、MotionMonitor 即時運算雙螢幕主控台。

---

## 二、2F 【209】運動面層實驗分析室 — 設備配置與機能分區

### 2.1 實驗室設備平面配置圖 (Equipment Layout Plan)
![2F 運動面層實驗分析室設備平面配置圖](C:/Users/00054/.gemini/antigravity/brain/2da235a0-35f9-41c6-96ab-010e9b49e912/lab_2f_equipment_layout.png)

### 2.2 四大實驗機能分區配置
1. **衝擊吸收與安全防滑試驗區 (西北側)**：
   - **衝擊吸收落錘系統 (Triple-A / Berlin Athlete Tester)**：佔地 $1.8\,\text{m} \times 1.2\,\text{m}$，配備標準落錘、力感測器、變形量規及 PT100 溫控單元，依據 EN 14808 / ASTM F2569 標準量測面層衝擊吸收率（Force Reduction）與垂直變形（Vertical Deformation）。
   - **擺錘式防滑/摩擦係數儀 (British Pendulum Skid Tester)**：依 EN 13036-4 測試運動木地板、PU、壓克力與合成面層之抗滑值（BPN/PTV）。
   - **旋轉阻力測試裝置 (EN 15301-1)**：測試足球人工草皮與跑道之釘鞋旋轉扭矩阻力。
2. **材料萬能拉伸與壓縮試驗區 (西南側)**：
   - **雙柱萬能材料試驗機 (Instron 3400 等級)**：佔地 $1.2\,\text{m} \times 0.9\,\text{m}$，具備 10kN ~ 50kN 荷重元，搭配多功能夾具，執行人工草皮草絲拔出力（Tuft withdrawal force）、草皮底布撕裂強度、跑道彈性層拉伸強度及伸長率測試（EN 12230）。
3. **耐候老化與環境試驗區 (東北側)**：
   - **Xenon 氙燈耐候試驗箱 (Atlas Xenotest 440)**：佔地 $1.5\,\text{m} \times 1.2\,\text{m}$，模擬全光譜日光輻射、高溫烘烤與降雨噴淋老化。
   - **QUV 螢光紫外加速老化試驗機**：佔地 $1.4\,\text{m} \times 0.8\,\text{m}$，模擬紫外線 UV-A/UV-B 破壞。
   - **分光色差儀 (Konica Minolta CM-700d)**：評估樣品老化前後之色差 $\Delta E$ 與光澤度衰減。
   - **機電配套**：本區配置專屬三相四線 380V/220V 獨立迴路無熔絲開關、RO 純水供水龍頭及耐腐蝕重力排水孔。
4. **樣品前處理與數據控制中心 (東南側)**：
   - 恆溫恆濕樣品養護置物架（放置測試標準樣品塊 $50\times 50\,\text{cm}$）。
   - 工業級數據採集分析終端機，連接各測試儀器 LAN/RS232 匯流排。

> [!NOTE]
> **結構減震重要性**：本室樓版採**格子樑（Waffle Slab）**施工，有效截斷 Triple-A 落錘連續自由落體敲擊（落錘重 20kg）所產生的低頻振動，避免干擾隔壁 208 綜合討論室與樓下空間。

---

## 三、3F 【305】多功能鷹眼技術開發實驗室 — 設備配置與挑高模擬

### 3.1 實驗室設備平面配置圖 (Equipment Layout Plan)
![3F 多功能鷹眼技術開發實驗室設備平面配置圖](C:/Users/00054/.gemini/antigravity/brain/2da235a0-35f9-41c6-96ab-010e9b49e912/lab_3f_equipment_layout.png)

### 3.2 挑高空間利用與設備佈局特點
1. **18 公尺高速球類軌跡飛行通道 (Flight Lane)**：
   - 沿長軸方向設立 $18.0\,\text{m} \times 4.5\,\text{m}$ 之高速運動測試道，由西側自動發球機（排球、羽球、網球、棒球等高速投球裝置）朝東側落點標靶區射出。
   - 通道周邊與末端配置重型吸音高張力防撞防球護網（Safety Netting），維護周邊人員與精密儀器安全。
2. **8 台高速工業攝影機高空環形矩陣 (Camera Truss Array)**：
   - 挑高區上方架設倒 U 型高剛性鋼結構桁架，掛載 8 台 Photron FASTCAM / Basler 高速攝影機（解析度 $\ge 1080\text{p} @ 500\sim 1000\,\text{fps}$）。
   - 攝影機呈立體多角度俯拍與側拍交會，確保飛行物體全程至少被 4 台以上鏡頭同時補捉，消除視線遮蔽死角。
3. **無頻閃 1000 Lux 專業級照明系統**：
   - 桁架全面佈設高演色性（CRI $\ge 90$）、色溫 5000K、無頻閃（Flicker-Free, 漣波率 $< 1\%$）之大功率 LED 面板燈矩陣。
   - 徹底杜絕高速快門（$1/2000\,\text{sec}$ 以上）拍攝時出現的明暗條紋與色彩滾動假影。
4. **3D 空間立體校正標定架 (Calibration Frame)**：
   - 挑高核心區設置特製可拆裝精密 3D 空間網格標定立方架（$2.0\,\text{m} \times 2.0\,\text{m} \times 2.0\,\text{m}$，帶高反射立體標靶點），作為多鏡頭外參標定（Extrinsic Calibration）之絕對坐標基準。
5. **雙 Xeon / RTX GPU 鷹眼演算與裁判判決控制台**：
   - 設置於東南側防護區，配備 2 台機架式邊緣運算工作站（雙 Intel Xeon CPU + 多張 NVIDIA RTX GPU），運行高速圖像邊緣提取、立體視覺交會重建、空氣動力學軌跡回歸與即時界內/界外（In/Out）落點毫米級判定演算法。

---

## 四、機電設施需求彙整表 (MEP Requirements Matrix)

| 實驗室 | 專屬電力需求 | 網路與訊號匯流排 | 空調/給排水/氣體 | 結構與載重需求 |
| :--- | :--- | :--- | :--- | :--- |
| **1F [117]<br>虛實整合** | • 單相 220V 30A (GPU運算機櫃)<br>• 單相 110V 獨立接地專線 (動捕/肌電)<br>• 系統總用電量預估: 18 kVA | • Cat.6A 萬兆乙太網 (10GbE LAN)<br>• BNC / TTL 外部時脈硬體同調觸發線路<br>• 地下埋入式鍍鋅線槽 (100×50mm) | • 恆溫恆濕空調 ($22\pm 2^\circ\text{C}$, $50\pm 5\%$ RH)<br>• 防靜電防塵環氧樹脂基底 | • 活載重 $\ge 500\,\text{kg/m}^2$<br>• 平整自流平混凝土基底 ($\pm 1\,\text{mm}$)<br>• 14~16cm 模組化木地板基座 |
| **2F [209]<br>運動面層** | • 三相四線 380V/220V 50A (耐候機/UTM)<br>• 單相 220V 20A (落錘測試儀)<br>• 系統總用電量預估: 35 kVA | • Gigabit LAN (儀器數據串接)<br>• RS232 / USB 工業匯流排 | • 耐候機專屬 RO 純水進水管 ($\frac{1}{2}"$)<br>• 重力排水明溝/排水管路 ($\phi 2"$, 耐酸鹼)<br>• 耐候試驗排熱風道 (外排排風管) | • **格子樑 (Waffle Slab) 垂直減震**<br>• 衝擊落錘基座加強載重 ($\ge 600\,\text{kg/m}^2$) |
| **3F [305]<br>多功能鷹眼** | • 單相 220V 40A (雙GPU伺服器)<br>• 單相 110V 30A (高空LED矩陣照明)<br>• 系統總用電量預估: 22 kVA | • 高頻帶寬專用光纖通道 (10G SFP+)<br>• PTP (IEEE 1588) 奈秒級時間戳同步 | • 獨立變頻空調 ($23\pm 2^\circ\text{C}$)<br>• 懸吊桁架氣動減震吊點 | • **挑高淨高空間設計**<br>• **格子樑結構減震** (消除高速相機微震) |

---

## 五、圖面輸出檔案索引

所有高解析度圖檔（300 DPI）均已同步輸出至本專案之 `exported_floor_maps/` 目錄：
1. **1F 虛實整合實驗室設備平面圖**：[`exported_floor_maps/lab_1f_equipment_layout.png`](file:///c:/Users/00054/我的雲端硬碟%20(goodman10@gmail.com)/1-Biomechanics%20Lab%20PC-%20TISS/(新建築物%20)Future_building%20Space%20Organization/exported_floor_maps/lab_1f_equipment_layout.png)
2. **模組化測力板與14~16cm木地板互換機構斷面圖**：[`exported_floor_maps/force_plate_modular_floor_section.png`](file:///c:/Users/00054/我的雲端硬碟%20(goodman10@gmail.com)/1-Biomechanics%20Lab%20PC-%20TISS/(新建築物%20)Future_building%20Space%20Organization/exported_floor_maps/force_plate_modular_floor_section.png)
3. **2F 運動面層實驗分析室設備平面圖**：[`exported_floor_maps/lab_2f_equipment_layout.png`](file:///c:/Users/00054/我的雲端硬碟%20(goodman10@gmail.com)/1-Biomechanics%20Lab%20PC-%20TISS/(新建築物%20)Future_building%20Space%20Organization/exported_floor_maps/lab_2f_equipment_layout.png)
4. **3F 多功能鷹眼技術開發實驗室設備平面圖**：[`exported_floor_maps/lab_3f_equipment_layout.png`](file:///c:/Users/00054/我的雲端硬碟%20(goodman10@gmail.com)/1-Biomechanics%20Lab%20PC-%20TISS/(新建築物%20)Future_building%20Space%20Organization/exported_floor_maps/lab_3f_equipment_layout.png)
5. **原始建築細部設計圖說局部裁切圖 (CAD 原圖)**：
   - 1F 虛實整合實驗室 CAD 圖：[`exported_floor_maps/cad_1f_lab_plan.png`](file:///c:/Users/00054/我的雲端硬碟%20(goodman10@gmail.com)/1-Biomechanics%20Lab%20PC-%20TISS/(新建築物%20)Future_building%20Space%20Organization/exported_floor_maps/cad_1f_lab_plan.png)
   - 2F 運動面層實驗分析室 CAD 圖：[`exported_floor_maps/cad_2f_lab_plan.png`](file:///c:/Users/00054/我的雲端硬碟%20(goodman10@gmail.com)/1-Biomechanics%20Lab%20PC-%20TISS/(新建築物%20)Future_building%20Space%20Organization/exported_floor_maps/cad_2f_lab_plan.png)
   - 3F 多功能鷹眼技術開發實驗室 CAD 圖：[`exported_floor_maps/cad_3f_lab_plan.png`](file:///c:/Users/00054/我的雲端硬碟%20(goodman10@gmail.com)/1-Biomechanics%20Lab%20PC-%20TISS/(新建築物%20)Future_building%20Space%20Organization/exported_floor_maps/cad_3f_lab_plan.png)
6. **核心實驗室智慧空間與設備互動平台 (HTML 互動儀表板)**：
   - Artifact 側邊欄：[`laboratory_interactive_dashboard.html`](file:///C:/Users/00054/.gemini/antigravity/brain/2da235a0-35f9-41c6-96ab-010e9b49e912/laboratory_interactive_dashboard.html)
   - 本地工作目錄：[`laboratory_interactive_dashboard.html`](file:///c:/Users/00054/我的雲端硬碟%20(goodman10@gmail.com)/1-Biomechanics%20Lab%20PC-%20TISS/(新建築物%20)Future_building%20Space%20Organization/laboratory_interactive_dashboard.html)

