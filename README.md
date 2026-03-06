📜 Smart Health Lens | AI 健康顧問面板
Smart Health Lens 是一款基於 Google Gemini 2.5 Flash 模型開發的智慧健康分析工具。使用者只需上傳 食物照片 或 健檢報告（如 InBody 或 體重計數據），AI 即可自動辨識影像內容、提取關鍵指標，並即時生成視覺化圖表與個人化健康建議。

✨ 核心功能
雙模態智慧辨識：自動判斷上傳內容為「食物」或「醫療報告」。

關鍵指標提取：

食物：估算卡路里、蛋白質、碳水化合物及脂肪。

報告：提取體重、體脂肪率、肌肉量及內臟脂肪等級。

視覺化數據面板：使用 Chart.js 生成環狀圖（食物比例）或長條圖（身體指標）。

AI 健康評分：根據營養平衡或身體組成數據，給予 0-100 的直觀評分。

行動建議：提供三點具體的個人化健康改善建議。

即時互動介面：支援拖放上傳（Drag & Drop）與平滑的載入動畫。

🛠️ 技術棧
前端: HTML5, CSS3 (Flexbox/Grid), JavaScript (Vanilla JS)

AI 引擎: Google Gemini 2.5 Flash API

圖表庫: Chart.js

圖示: Font Awesome 6.0

API 請求: Fetch API (Base64 影像編碼傳輸)

🚀 快速開始
1. 取得 Gemini API Key
前往 Google AI Studio 申請免費或付費的 API Key。

2. 下載專案
將原始碼儲存為 index.html。

3. 執行程式
由於此專案為純前端設計，你可以直接用瀏覽器打開 index.html，或使用 VS Code 的 Live Server 擴充功能執行。

4. 開始分析
在頁面頂端輸入你的 Gemini API Key。

點擊上傳區域或直接將圖片拖入。

等待 AI 運算（通常在 2-5 秒內），即可看到分析結果。

📋 JSON 數據結構範例
AI 會嚴格回傳以下格式，確保介面解析穩定：

JSON
{
  "type": "Food",
  "label": "雞肉酪梨沙拉",
  "metrics": {
    "calories": 450,
    "protein": 35,
    "carbs": 15,
    "fat": 28
  },
  "health_score": 85,
  "advice": [
    "增加膳食纖維攝取",
    "蛋白質比例優良，適合運動後食用",
    "注意醬料中的隱形鈉含量"
  ]
}
⚠️ 注意事項
隱私權：本工具直接從客戶端瀏覽器發送請求至 Google API，不會在任何第三方伺服器儲存您的圖片或 API Key。

精準度：食物營養估算為 AI 視覺模擬結果，僅供參考，不應作為專業醫療診斷依據。

API 限制：請確保您的 API Key 有效，且該模型在您所在的地區可用。

💡 未來擴充方向
[ ] 支援多圖對比分析。

[ ] 串接 LocalStorage 以記錄歷史健康數據。

[ ] 匯出分析報告為 PDF。

[ ] 支援更多語言的語義分析。
